---
title: Configurar UDFs no Excel Online no Office Online Server
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Use as funções definidas pelo usuário (UDFs) no Excel Online no Office Online Server chamar funções personalizadas.
ms.openlocfilehash: dbba60a62a1a4783b47c3f1fe40a118dd8ed0d6d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722785"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Configurar UDFs no Excel Online no Office Online Server

Use as funções definidas pelo usuário (UDFs) no Excel Online no Office Online Server chamar funções personalizadas. 
  
Funções definidas pelo usuário (UDFs) no Excel Online permitem que você chamar funções personalizadas escritas em código gerenciado usando fórmulas nas células. Você pode usar UDFs para:
  
- Chamar funções matemáticas personalizadas.
    
- Obter dados de fontes de dados personalizadas para planilhas.
    
- Chame serviços da web.
    
Você pode instalar binários UDF em um dos dois locais:
  
- Um diretório local. Por exemplo: 
    
    C:\UDFs\MySampleUdf.dll
    
- Cache de assembly global. Por exemplo: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Referência ao local quando você criar uma definição de **New-OfficeWebAppsExcelUserDefinedFunction** no servidor do Office Online. 
  
> [!NOTE]
> Servidor do Office Online não oferece suporte a UDFs localizados em compartilhamentos de rede. 
  
## <a name="enable-udfs-on-office-online-server"></a>Habilitar UDFs em servidor do Office Online 

Quando um administrador cria um novo farm de servidor do Office Web Apps usando o cmdlet [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell, assemblies UDF são desabilitados por padrão. O valor padrão do sinalizador **ExcelUdfsAllowed** é false. 
  
Para habilitar UDFs, execute o seguinte comando do Windows PowerShell no Office Online Server, depois que o farm do Office Web Apps Server foi criado.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Criar definições de UDF no servidor on-line do Office

Após habilitar UDFs, você precisa criar uma definição para binário que contém os UDFs. Para criar uma definição para seu UDF binários no servidor do Office Online, use o cmdlet **New-OfficeWebAppsExcelUserDefinedFunction** . Esse cmdlet inclui os seguintes parâmetros: 
  
- **Assembly**
    
- **AssemblyLocation**
    
- **Habilitar** (definido como False por padrão) 
    
- **Descrição**
    
Os exemplos a seguir mostram como criar as definições de UDF.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Depois de criar a nova referência UDF, execute o **iisreset** no servidor para pegue a referência imediatamente. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Comandos adicionais do Office Online Server UDF Windows PowerShell

Use os seguintes cmdlets do Windows PowerShell para trabalhar com UDFs:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (sem parâmetros obrigatórios) - retorna uma lista de definições de UDF que são configuradas no servidor do Office Online. 
    
- **Set-OfficeWebAppsExcelUserDefinedFunction** (Parâmetro de identidade necessário) - define propriedades em definições de UDF existentes. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (Parâmetro de identidade necessário) - remove as definições de UDF existentes. 
    
## <a name="udf-sample"></a>Amostra UDF

Os arquivos a seguir fornecem uma pasta de trabalho de exemplo que usa um UDF e UDF binário:
  
- [BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): uma pasta de trabalho de exemplo que usa um UDF  
- [EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): o binário UDF 
    
## <a name="see-also"></a>Confira também

- [Configurar definições administrativas Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Servidor do Office Online](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

