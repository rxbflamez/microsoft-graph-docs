---
title: "Install a Microsoft Graph SDK"
description: "Provides instructions for installing the .NET, Go, Java, JavaScript, PHP, PowerShell, and Python Microsoft Graph SDKs."
ms.localizationpriority: medium
author: MichaelMainer
---

# Install a Microsoft Graph SDK

Microsoft Graph SDKs are available to be included in your projects via GitHub and popular platform package managers. This article describes how you can install a Microsoft Graph SDK into your project.

SDKs are available in the following languages:

- [.NET](#install-the-microsoft-graph-net-sdk)
- [Go (preview)](#install-the-microsoft-graph-go-sdk-preview)
- [Java](#install-the-microsoft-graph-java-sdk)
- [JavaScript](#install-the-microsoft-graph-javascript-sdk)
- [PHP](#install-the-microsoft-graph-php-sdk)
- [PowerShell](#install-the-microsoft-graph-powershell-sdk)
- [Python (preview)](#install-the-microsoft-graph-python-sdk-preview)

## Install the Microsoft Graph .NET SDK

The Microsoft Graph .NET SDK is included in the following NuGet packages:

- [Microsoft.Graph](https://github.com/microsoftgraph/msgraph-sdk-dotnet): Contains the models and request builders for accessing the `v1.0` endpoint with the fluent API. Microsoft.Graph has a dependency on Microsoft.Graph.Core.
- [Microsoft.Graph.Beta](https://github.com/microsoftgraph/msgraph-beta-sdk-dotnet): Contains the models and request builders for accessing the `beta` endpoint with the fluent API. Microsoft.Graph.Beta has a dependency on Microsoft.Graph.Core.
- [Microsoft.Graph.Core](https://github.com/microsoftgraph/msgraph-sdk-dotnet): The core library for making calls to Microsoft Graph.

To install the Microsoft.Graph packages into your project, you can use either the [Package Manager UI in Visual Studio or the Package Manager Console](/nuget/quickstart/install-and-use-a-package-in-visual-studio). The following Package Manager Console commands install the Microsoft.Graph and Microsoft.Graph.Core libraries. Microsoft.Graph.Core is installed as a dependency of Microsoft.Graph.

```PowerShell
Install-Package Microsoft.Graph
```

## Install the Microsoft Graph Go SDK (preview)

[!INCLUDE [go-sdk-preview](../../includes/go-sdk-preview.md)]

The Microsoft Graph Go SDK is included in the following packages:

- [Microsoft Graph SDK for Go](https://github.com/microsoftgraph/msgraph-sdk-go): Contains the models and request builders for accessing the `v1.0` endpoint with the fluent API.
- [Microsoft Graph Beta SDK for Go](https://github.com/microsoftgraph/msgraph-beta-sdk-go): Contains the models and request builders for accessing the `beta` endpoint with the fluent API.
- [Microsoft Graph Core SDK for Go](https://github.com/microsoftgraph/msgraph-sdk-go-core): The core library for making calls to Microsoft Graph.

```Shell
go get github.com/microsoftgraph/msgraph-sdk-go
go get github.com/Azure/azure-sdk-for-go/sdk/azidentity
go get github.com/microsoft/kiota-authentication-azure-go
```

## Install the Microsoft Graph Java SDK

The Microsoft Graph Java SDK is included in the following packages:

- [microsoft-graph](https://github.com/microsoftgraph/msgraph-sdk-java): Contains the models and request builders for accessing the `v1.0` endpoint with the fluent API.
- [microsoft-graph-beta](https://github.com/microsoftgraph/msgraph-beta-sdk-java): Contains the models and request builders for accessing the `beta` endpoint with the fluent API.
- [microsoft-graph-core](https://github.com/microsoftgraph/msgraph-sdk-java-core): The core library for making calls to Microsoft Graph.
- [microsoft-graph-auth](https://github.com/microsoftgraph/msgraph-sdk-java-auth): Provides an authentication scenario-based wrapper of Microsoft Authentication Library (MSAL) for use with the Microsoft Graph SDK.

To install the Microsoft Graph Java SDK, do one of the following:

- Use Gradle to install the Microsoft Graph Java SDK. Add the repository and a compile dependency for microsoft-graph to your project's build.gradle:
    
  ```Gradle
    repository {
        mavenCentral()
    }
    
    dependency {
        // Include the sdk as a dependency
        implementation 'com.microsoft.graph:microsoft-graph:5.+'
        // Include Azure identity for authentication
        implementation 'com.azure:azure-identity:1.+'
    }
  ```

- Use Maven to install the Microsoft Graph Java SDK. Add the dependency in the `dependencies` element in pom.xml:
    
  ```xml
    <dependency>
        <groupId>com.microsoft.graph</groupId>
        <artifactId>microsoft-graph</artifactId>
        <version>[5.0,)</version>
    </dependency>
    <dependency>
        <groupId>com.azure</groupId>
        <artifactId>azure-identity</artifactId>
        <version>[1.3,)</version>
    </dependency>
  ```

## Install the Microsoft Graph JavaScript SDK

The Microsoft Graph JavaScript SDK is included in the following packages:

- @microsoft/microsoft-graph-client ([npm](https://www.npmjs.com/package/@microsoft/microsoft-graph-client)): The core library for making calls to Microsoft Graph.
- @microsoft/microsoft-graph-types ([npm](https://www.npmjs.com/package/@microsoft/microsoft-graph-types)): The TypeScript types for the Microsoft Graph entities.

Use [npm](https://www.npmjs.com) to install the Microsoft Graph JavaScript SDK:

```Shell
npm install @microsoft/microsoft-graph-client --save
npm install @microsoft/microsoft-graph-types --save-dev
```

## Install the Microsoft Graph PHP SDK

The [Microsoft Graph PHP SDK](https://github.com/microsoftgraph/msgraph-sdk-php) is available from [packagist.org](https://packagist.org/packages/microsoft/microsoft-graph) and can be installed in the following ways:

- Use composer to install the Microsoft Graph PHP SDK manually:

    ```Shell
    composer require microsoft/microsoft-graph
    ```

- Use composer.json to install the Microsoft Graph PHP SDK:

    ```json
    {
        "require": {
            "microsoft/microsoft-graph": "^1.8"
        }
    }
    ```

## Install the Microsoft Graph PowerShell SDK

All the modules are published on [PowerShell Gallery](https://www.powershellgallery.com/packages/Microsoft.Graph). To install:

``` powershell
Install-Module Microsoft.Graph
```

If you're upgrading from the preview modules, run `Install-Module` with `AllowClobber` and `Force` parameters to avoid command name conflicts:

``` powershell
 Install-Module Microsoft.Graph -AllowClobber -Force
```

## Install the Microsoft Graph Python SDK (preview)

[!INCLUDE [python-sdk-preview](../../includes/python-sdk-preview.md)]

The [Microsoft Graph Core Python Client Library (preview)](https://github.com/microsoftgraph/msgraph-sdk-python-core) is available on [PyPI](https://pypi.org/).

```Shell
python -m pip install msgraph-core
python -m pip install azure-identity
```

## See also

- For more details about the features and capabilities of the SDK, see the SDK [design requirements documentation](https://github.com/microsoftgraph/msgraph-sdk-design). 
- For a list of samples for Microsoft Graph, see the [Microsoft Graph resources page](https://developer.microsoft.com/en-us/graph/gallery/?filterBy=Samples).
- For step-by-step training for creating a Microsoft Graph app, see the [Microsoft Graph tutorials](/graph/tutorials).