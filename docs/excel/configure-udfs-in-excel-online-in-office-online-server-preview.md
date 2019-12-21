---
title: Configurar UDFs no Excel online no servidor do Office Online
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Use funções definidas pelo usuário (UDFs) no Excel online no servidor do Office Online para chamar funções personalizadas.
ms.openlocfilehash: c9ace9a678a57a0d97e2fee65ee62bf9497f4451
ms.sourcegitcommit: 55205b4ec1376713d31e75d195e031798fb2c6ad
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/20/2019
ms.locfileid: "40825762"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Configurar UDFs no Excel online no servidor do Office Online

Use funções definidas pelo usuário (UDFs) no Excel online no servidor do Office Online para chamar funções personalizadas. 
  
As funções definidas pelo usuário (UDFs) no Excel online permitem chamar funções personalizadas escritas em código gerenciado usando fórmulas em células. Você pode usar UDFs para:
  
- Chamar funções matemáticas personalizadas.
    
- Obter dados de fontes de dados personalizadas para planilhas.
    
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
    
- **Set-OfficeWebAppsExcelUserDefinedFunction** (parâmetro Identity obrigatório): define as propriedades nas definições de UDF existentes. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (parâmetro Identity obrigatório)-Remove definições UDF existentes. 
    
## <a name="udf-sample"></a>Exemplo de UDF

O arquivo de exemplo a seguir fornece um exemplo de pasta de trabalho que usa um UDF e o binário UDF:
  
- [BooleanDataType. xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): um exemplo de pasta de trabalho que usa um UDF  
    
## <a name="see-also"></a>Confira também

- [Configurar definições administrativas do Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

