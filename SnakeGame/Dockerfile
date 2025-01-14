FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR SnakeGame

EXPOSE 80
EXPOSE 5000

COPY ./*.csproj ./
RUN dotnet restore

COPY . .
RUN dotnet publish -c Release -o out


FROM mcr.microsoft.com/dotnet/sdk:8.0
WORKDIR /SnakeGame
COPY --from=build /SnakeGame/out .
ENTRYPOINT ["dotnet","SnakeGame.dll"]