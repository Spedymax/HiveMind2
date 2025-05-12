FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /app
COPY . .
RUN dotnet restore ./Dev0psProject/Dev0psProject.CommunicationControl.API.csproj
RUN dotnet publish ./Dev0psProjedt/DevOpsProject.CommunicationControl.API.csproj -c Release -o / app/out

FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS runtime
WORKDIR / app

COPY --from=build /app/out ./
ENV ASPNETCORE_URLS-http://+:8080
ENV ASPNETCORE_ENVIRONMENT=Development

EXPOSE 8880
ENTRYPOINT
["dotnet", "DevOpsProject.CommunicationControl.API.dll"]