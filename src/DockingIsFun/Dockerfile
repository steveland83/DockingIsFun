FROM microsoft/aspnetcore-build:1.0-1.1
ARG source
WORKDIR /app
EXPOSE 80
RUN ["dotnet", "restore DockingIsFun"]
RUN ["dotnet", "build DockingIsFun"]
COPY ${source:-obj/Docker/publish} .
ENTRYPOINT ["dotnet", "DockingIsFun.dll"]
