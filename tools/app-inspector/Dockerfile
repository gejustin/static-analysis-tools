FROM mcr.microsoft.com/dotnet/sdk:6.0

RUN dotnet tool install --global Microsoft.CST.ApplicationInspector.CLI

ENV PATH="/root/.dotnet/tools:$PATH"

ENTRYPOINT [ "appinspector" ]
