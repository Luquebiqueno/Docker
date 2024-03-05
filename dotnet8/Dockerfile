
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build-env
WORKDIR /App
RUN apt-get update && dotnet restore

FROM mcr.microsoft.com/dotnet/aspnet:8.0
WORKDIR /var/www
COPY --from=build-env /var/www .
ENTRYPOINT ["dotnet", "DotNet.Docker.dll"]