#Depending on the operating system of the host machines(s) that will build or run the containers, the image specified in the FROM statement may need to be changed.
#For more information, please see http://aka.ms/containercompat 

FROM mcr.microsoft.com/dotnet/core/aspnet:2.2-nanoserver-1809 AS base
WORKDIR /app
EXPOSE 80

FROM mcr.microsoft.com/dotnet/core/sdk:2.2-nanoserver-1809 AS build
WORKDIR /src
COPY ["ProductMicroservice/ProductMicroservice.csproj", "ProductMicroservice/"]
RUN dotnet restore "ProductMicroservice/ProductMicroservice.csproj"
COPY . .
WORKDIR "/src/ProductMicroservice"
RUN dotnet build "ProductMicroservice.csproj" -c Release -o /app

FROM build AS publish
RUN dotnet publish "ProductMicroservice.csproj" -c Release -o /app

FROM base AS final
WORKDIR /app
COPY --from=publish /app .
ENTRYPOINT ["dotnet", "ProductMicroservice.dll"]
