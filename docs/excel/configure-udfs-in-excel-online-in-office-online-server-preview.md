---
title: Configurar UDFs no Excel Online no Servidor do Office Online
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Use UDFs (funções definidas pelo usuário) no Excel Online no Servidor do Office Online para chamar funções personalizadas.
ms.openlocfilehash: e1b005079c03ae3028ba6bf9ee1156c6ae2eae80
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2020
ms.locfileid: "43102930"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Configurar UDFs no Excel Online no Servidor do Office Online

Use UDFs (funções definidas pelo usuário) no Excel Online no Servidor do Office Online para chamar funções personalizadas. 
  
As UDFs (funções definidas pelo usuário) no Excel Online permitem que você chame funções personalizadas escritas em código gerenciado usando fórmulas em células. Você pode usar UDFs para:
  
- Chamar funções matemáticas personalizadas.
    
- Obter dados de fontes de dados personalizadas para planilhas.
    
- Chamar serviços Web.
    
Você pode instalar binários UDF em um dos dois locais:
  
- Um diretório local. Por exemplo: 
    
    C:\UDFs\MySampleUdf.dll
    
- O cache de assembly global. Por exemplo: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Fazer referência ao local ao criar uma **definição New-OfficeWebAppsExcelUserDefinedFunction** no Servidor do Office Online. 
  
> [!NOTE]
> O Servidor do Office Online não dá suporte a UDFs localizadas em compartilhamentos de rede. 
  
## <a name="enable-udfs-on-office-online-server"></a>Habilitar UDFs no Servidor do Office Online 

Quando um administrador cria um novo farm do Servidor do Office Web Apps usando o cmdlet [New-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) do Windows PowerShell, os assemblies UDF são desabilitados por padrão. O valor padrão do **sinalizador ExcelUdfsAllowed** é false. 
  
Para habilitar UDFs, execute o seguinte comando do Windows PowerShell no Servidor do Office Online, depois que o farm do Servidor do Office Web Apps tiver sido criado.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Criar definições UDF no Servidor do Office Online

Depois de habilitar UDFs, você precisa criar uma definição para o binário que contém as UDFs. Para criar uma definição para o binário UDF no Servidor do Office Online, use o cmdlet **New-OfficeWebAppsExcelUserDefinedFunction.** Este cmdlet inclui os seguintes parâmetros: 
  
- **Assembly**
    
- **AssemblyLocation**
    
- **Habilitar** (definido como False por padrão) 
    
- **Descrição**
    
Os exemplos a seguir mostram como criar as definições de UDF.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Depois de criar a nova referência de UDF, execute **o iisreset** no servidor para escolher a referência imediatamente. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Comandos adicionais do Servidor do Office Online UDF do Windows PowerShell

Use os seguintes cmdlets do Windows PowerShell para trabalhar com UDFs:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (sem parâmetros necessários) - Retorna uma lista de definições UDF configuradas no Servidor do Office Online. 
    
- **Set- OfficeWebAppsExcelUserDefinedFunction** (parâmetro de identidade obrigatório) – define propriedades em definições UDF existentes. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (parâmetro de identidade necessário) - Remove definições UDF existentes. 
    
## <a name="udf-sample"></a>Exemplo de UDF

O arquivo de exemplo a seguir fornece uma pasta de trabalho de exemplo que usa um binário UDF e UDF:
  
- [BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): uma amostra de uma workbook que usa uma UDF  
    
## <a name="see-also"></a>Confira também

- [Configurar definições administrativas do Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Servidor do Office Online](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

