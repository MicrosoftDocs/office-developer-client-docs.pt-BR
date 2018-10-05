---
title: Configurar UDFs no Excel Online no Office Online Server Preview
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Use as funções definidas pelo usuário (UDFs) no Excel Online no Office Online Server Preview para chamar funções personalizadas.
ms.openlocfilehash: 2b76b7351a0882762165e37b55c8fbe78f657c34
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384819"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server-preview"></a>Configurar UDFs no Excel Online no Office Online Server Preview

[Este tópico é uma documentação de pré-lançamento e está sujeita a alterações em versões futuras.] Use as funções definidas pelo usuário (UDFs) no Excel Online no Office Online Server Preview para chamar funções personalizadas. 
  
Funções definidas pelo usuário (UDFs) no Excel Online permitem que você chamar funções personalizadas escritas em código gerenciado usando fórmulas nas células. Você pode usar UDFs para:
  
- Call custom mathematical functions.
    
- Get data from custom data sources into worksheets.
    
- Chame serviços da web.
    
Você pode instalar binários UDF em um dos dois locais:
  
- Um diretório local. Por exemplo: 
    
    C:\UDFs\MySampleUdf.dll
    
- Cache de assembly global. Por exemplo: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Referência ao local quando você criar uma definição de **New-OfficeWebAppsExcelUserDefinedFunction** no Office Online Server Preview. 
  
> [!NOTE]
> Visualização do Office Online Server não dá suporte a UDFs localizados em compartilhamentos de rede. 
  
## <a name="enable-udfs-on-office-online-server-preview"></a>Habilitar UDFs no Office Online Server Preview

Quando um administrador cria um novo farm de servidor do Office Web Apps usando o cmdlet [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell, assemblies UDF são desabilitados por padrão. O valor padrão do sinalizador **ExcelUdfsAllowed** é false. 
  
Para habilitar UDFs, execute o seguinte comando do Windows PowerShell no Office Online Preview de servidor, depois que o farm do Office Web Apps Server foi criado.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server-preview"></a>Criar definições de UDF no Office Online Server Preview

Após habilitar UDFs, você precisa criar uma definição para binário que contém os UDFs. Para criar uma definição para seu UDF binários no Office Online Server Preview, use o cmdlet **New-OfficeWebAppsExcelUserDefinedFunction** . Esse cmdlet inclui os seguintes parâmetros: 
  
- **Assembly**
    
- **AssemblyLocation**
    
- **Habilitar** (definido como False por padrão) 
    
- **Descrição**
    
Os exemplos a seguir mostram como criar as definições de UDF.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Depois de criar a nova referência UDF, execute o **iisreset** no servidor para pegue a referência imediatamente. 
  
## <a name="additional-office-online-server-preview-udf-windows-powershell-commands"></a>Comandos do Windows PowerShell do Office Online Server Preview UDF adicionais

Use os seguintes cmdlets do Windows PowerShell para trabalhar com UDFs:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (sem parâmetros obrigatórios) - retorna uma lista de definições de UDF que são configuradas no Office Online Server Preview. 
    
- **Set-OfficeWebAppsExcelUserDefinedFunction** (Parâmetro de identidade necessário) - define propriedades em definições de UDF existentes. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (Parâmetro de identidade necessário) - remove as definições de UDF existentes. 
    
## <a name="udf-sample"></a>Amostra UDF

Os arquivos a seguir fornecem uma pasta de trabalho de exemplo que usa um UDF e UDF binário:
  
- [BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx) – uma pasta de trabalho de exemplo que usa um UDF  
- [EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll) – o binário UDF 
    
## <a name="see-also"></a>Confira também

- [Configurar definições administrativas Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Servidor do Office Online](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

