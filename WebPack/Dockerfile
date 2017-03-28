FROM microsoft/aspnetcore:1.1
RUN curl -sL https://deb.nodesource.com/setup_6.x | bash -
RUN apt-get install -y build-essential nodejs
ARG source
WORKDIR /app
ENV ASPNETCORE_URLS http://*:5000
EXPOSE 5000 5001
COPY ${source:-obj/Docker/publish} .
ENTRYPOINT ["dotnet", "WebPack.dll"]
