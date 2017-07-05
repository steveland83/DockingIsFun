FROM microsoft/aspnetcore:1.1
ARG source
WORKDIR /app
EXPOSE 80
RUN ["dotnet", "restore dockingisfun"]
RUN ["dotnet", "build dockerisfun"]
COPY ${source:-obj/Docker/publish} .
ENTRYPOINT ["dotnet", "DockingIsFun.dll"]
