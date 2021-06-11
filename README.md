# OpenApi-Generator-Path-Repro
Replicate OpenApi generator issue with space in path

___

## Commands to replicate:

```
mkdir "src with-space"
cd '.\src with-space\'
dotnet new classlib
dotnet openapi add url https://petstore.swagger.io/v2/swagger.json
dotnet build
```

## Output:

> GenerateNSwagCSharp:
    dotnet --roll-forward-on-no-candidate-fx 2 C:\Users\JvR\.nuget\packages\nswag.msbuild\13.0.5\build\../tools/NetCore21//dotnet-nswag.dll openapi2csclient /className:swaggerClient /namespace:src_with_space /input:C:\SourceCode\OpenApi-Generator-Path-Repro\src with-space\swagger.json /output:obj\swaggerClient.cs
  NSwag command line tool for .NET Core NetCore21, toolchain v13.0.5.0 (NJsonSchema v10.0.22.0 (Newtonsoft.Json v11.0.0.0))
  Visit http://NSwag.org for more information.
  NSwag bin directory: C:\Users\JvR\.nuget\packages\nswag.msbuild\13.0.5\tools\NetCore21
  System.Reflection.TargetInvocationException: Exception has been thrown by the target of an invocation. ---> System.IO.FileNotFoundException: Could not find file 'C:\SourceCode\OpenApi-Generator-Path-Repro\src'.