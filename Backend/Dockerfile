FROM mcr.microsoft.com/dotnet/aspnet:6.0-alpine
RUN apk update && apk upgrade
RUN apk add --no-cache netcat-openbsd
RUN apk add --no-cache icu-libs
RUN apk add --no-cache tzdata
RUN apk add --no-cache curl

ENV ASPNETCORE_URLS http://*:8000
EXPOSE 8000
WORKDIR /app
COPY ./publish /app

ENTRYPOINT ["dotnet", "crypto-random.dll"]
