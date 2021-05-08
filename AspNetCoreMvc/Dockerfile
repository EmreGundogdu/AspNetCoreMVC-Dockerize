 FROM mcr.microsoft.com/dotnet/sdk:3.1
WORKDIR /app
COPY . .
RUN dotnet restore 
RUN dotnet publish AspNetCoreMvc.csproj -c Release -o out
FROM mcr.microsoft.com/dotnet/aspnet
WORKDIR out
ENV ASPNETCORE_URLS="http://*:4500"
ENTRYPOINT ["dotnet","AspNetCoreMvc.dll"]