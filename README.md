# JSON-to-ENV-dotnet

[![gh-page](https://github.com/ajami1331/JSON-to-ENV-dotnet/actions/workflows/gh-pages.yml/badge.svg)](https://github.com/ajami1331/JSON-to-ENV-dotnet/actions/workflows/gh-pages.yml)

Try it out: https://ajami1331.github.io/JSON-to-ENV-dotnet/

Will flatten with ASP.NET json seperator `:`

Example:

```
{
  "Logging": {
    "LogLevel": {
      "Default": "Debug",
      "System": "Information",
      "Microsoft": "Information"
    }
  },
  "Serilog": {
    "Using": [  "Serilog.Sinks.Seq", "Serilog.Sinks.Console" ],
    "WriteTo": [
      { "Name": "Console" },
      {
        "Name": "Seq",
        "Args": { "serverUrl": "http://localhost:5341/" }
      }
    ]
  }
}
```

```
Logging__LogLevel__Default=Debug
Logging__LogLevel__System=Information
Logging__LogLevel__Microsoft=Information
Serilog__Using__0=Serilog.Sinks.Seq
Serilog__Using__1=Serilog.Sinks.Console
Serilog__WriteTo__0__Name=Console
Serilog__WriteTo__1__Name=Seq
Serilog__WriteTo__1__Args__serverUrl=http://localhost:5341/

```
