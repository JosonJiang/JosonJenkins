#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

#FROM microsoft/aspnetcore:2.0-stretch AS base
#WORKDIR /app
#EXPOSE 80
#
#FROM microsoft/aspnetcore-build:2.0-stretch AS build
#WORKDIR /src
#
#COPY ["JosonJenkins/JosonJenkins.csproj", "JosonJenkins/"]
#RUN dotnet restore "JosonJenkins/JosonJenkins.csproj"
#COPY . .
#WORKDIR "/src/JosonJenkins"
#RUN dotnet build "JosonJenkins.csproj" -c Release -o /app/build
#
#FROM build AS publish
#RUN dotnet publish "JosonJenkins.csproj" -c Release -o /app/publish
#
#FROM base AS final
#WORKDIR /app
#COPY --from=publish /app/publish .

FROM mcr.microsoft.com/dotnet/core/sdk:2.2-stretch
WORKDIR /Joson
EXPOSE 80
EXPOSE 443

COPY . .

ENTRYPOINT ["dotnet", "JosonJenkins.dll"]