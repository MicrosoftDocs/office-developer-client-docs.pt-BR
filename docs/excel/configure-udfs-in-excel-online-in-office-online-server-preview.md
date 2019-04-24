---
title: Configurar UDFs no Excel online no servidor do Office Online
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Use funções definidas pelo usuário (UDFs) no Excel online no servidor do Office Online para chamar funções personalizadas.
ms.openlocfilehash: dbba60a62a1a4783b47c3f1fe40a118dd8ed0d6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311057"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Configurar UDFs no Excel online no servidor do Office Online

Use funções definidas pelo usuário (UDFs) no Excel online no servidor do Office Online para chamar funções personalizadas. 
  
As funções definidas pelo usuário (UDFs) no Excel online permitem chamar funções personalizadas escritas em código gerenciado usando fórmulas em células. Você pode usar UDFs para:
  
- Call custom mathematical functions.
    
- Get data from custom data sources into worksheets.
    
- Chamar serviços Web.
    
Você pode instalar binários UDF em um dos dois locais:
  
- Um diretório local. Por exemplo: 
    
    C:\UDFs\MySampleUdf.dll
    
- O cache de assembly global. Por exemplo: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Faça referência ao local ao criar uma definição de **New-OfficeWebAppsExcelUserDefinedFunction** no servidor do Office Online. 
  
> [!NOTE]
> O servidor do Office Online não dá suporte a UDFs localizados em compartilhamentos de rede. 
  
## <a name="enable-udfs-on-office-online-server"></a>Habilitar UDFs no servidor do Office Online 

Quando um administrador cria um novo farm do servidor do Office Web Apps usando o cmdlet [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) do Windows PowerShell, os assemblies UDF estão desabilitados por padrão. O valor padrão do sinalizador **ExcelUdfsAllowed** é false. 
  
Para habilitar UDFs, execute o seguinte comando do Windows PowerShell no servidor do Office Online, após a criação do farm do servidor do Office Web Apps.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Criar definições de UDF no servidor do Office Online

Depois de habilitar UDFs, você precisará criar uma definição para o binário que contém os UDFs. Para criar uma definição para seu binário UDF no servidor do Office Online, use o cmdlet **New-OfficeWebAppsExcelUserDefinedFunction** . Este cmdlet inclui os seguintes parâmetros: 
  
- **Defletor**
    
- **AssemblyLocation**
    
- **Habilitar** (definido como false por padrão) 
    
- **Descrição**
    
Os exemplos a seguir mostram como criar as definições de UDF.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Após criar a nova referência de UDF, execute **iisreset** no servidor para selecionar a referência imediatamente. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Comandos do Windows PowerShell adicionais do servidor do Office Online

Use os seguintes cmdlets do Windows PowerShell para trabalhar com UDFs:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (nenhum parâmetro obrigatório)-retorna uma lista de definições UDF configuradas no servidor do Office Online. 
    
- **Set-OfficeWebAppsExcelUserDefinedFunction** (Parâmetro Identity obrigatório): define as propriedades nas definições de UDF existentes. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (Parâmetro Identity obrigatório)-Remove definições UDF existentes. 
    
## <a name="udf-sample"></a>Exemplo de UDF

Os arquivos a seguir fornecem uma pasta de trabalho de exemplo que usa um UDF e o binário UDF:
  
- [BooleanDataType. xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): um exemplo de pasta de trabalho que usa um UDF  
- [EcsUdfsCommonSet. dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): o binário UDF 
    
## <a name="see-also"></a>Confira também

- [Configurar definições administrativas do Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

