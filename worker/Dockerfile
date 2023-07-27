# syntax=docker/dockerfile:1

FROM mcr.microsoft.com/dotnet/sdk:7.0 as build

LABEL image.name="Dotnet Worker"
LABEL image.version="1.0"
LABEL image.description="A Dotnet worker, which contains and handles all the votes"
LABEL image.author="mmaziec"


WORKDIR /worker
COPY *.csproj .
RUN dotnet restore
COPY . .
RUN dotnet publish -c Release -o /app

FROM mcr.microsoft.com/dotnet/runtime:7.0
WORKDIR /app
COPY --from=build /app .
EXPOSE 80
ENTRYPOINT ["dotnet", "Worker.dll"]