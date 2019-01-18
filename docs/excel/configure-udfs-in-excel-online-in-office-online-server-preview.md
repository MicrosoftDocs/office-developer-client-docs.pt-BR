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
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a><span data-ttu-id="5cd1b-103">Configurar UDFs no Excel Online no Office Online Server</span><span class="sxs-lookup"><span data-stu-id="5cd1b-103">Configure UDFs in Excel Online in Office Online Server</span></span>

<span data-ttu-id="5cd1b-104">Use as funções definidas pelo usuário (UDFs) no Excel Online no Office Online Server chamar funções personalizadas.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-104">Use user-defined functions (UDFs) in Excel Online in Office Online Server to call custom functions.</span></span> 
  
<span data-ttu-id="5cd1b-105">Funções definidas pelo usuário (UDFs) no Excel Online permitem que você chamar funções personalizadas escritas em código gerenciado usando fórmulas nas células.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-105">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells.</span></span> <span data-ttu-id="5cd1b-106">Você pode usar UDFs para:</span><span class="sxs-lookup"><span data-stu-id="5cd1b-106">You can use UDFs to:</span></span>
  
- <span data-ttu-id="5cd1b-107">Chamar funções matemáticas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="5cd1b-108">Obter dados de fontes de dados personalizadas para planilhas.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="5cd1b-109">Chame serviços da web.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-109">Call web services.</span></span>
    
<span data-ttu-id="5cd1b-110">Você pode instalar binários UDF em um dos dois locais:</span><span class="sxs-lookup"><span data-stu-id="5cd1b-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="5cd1b-111">Um diretório local.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-111">A local directory.</span></span> <span data-ttu-id="5cd1b-112">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5cd1b-112">For example:</span></span> 
    
    <span data-ttu-id="5cd1b-113">C:\UDFs\MySampleUdf.dll</span><span class="sxs-lookup"><span data-stu-id="5cd1b-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="5cd1b-114">Cache de assembly global.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-114">The global assembly cache.</span></span> <span data-ttu-id="5cd1b-115">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5cd1b-115">For example:</span></span> 
    
    <span data-ttu-id="5cd1b-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="5cd1b-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="5cd1b-117">Referência ao local quando você criar uma definição de **New-OfficeWebAppsExcelUserDefinedFunction** no servidor do Office Online.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5cd1b-118">Servidor do Office Online não oferece suporte a UDFs localizados em compartilhamentos de rede.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-118">Office Online Server does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server"></a><span data-ttu-id="5cd1b-119">Habilitar UDFs em servidor do Office Online</span><span class="sxs-lookup"><span data-stu-id="5cd1b-119">Enable UDFs on Office Online Server</span></span> 

<span data-ttu-id="5cd1b-120">Quando um administrador cria um novo farm de servidor do Office Web Apps usando o cmdlet [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell, assemblies UDF são desabilitados por padrão.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-120">When an adminstrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="5cd1b-121">O valor padrão do sinalizador **ExcelUdfsAllowed** é false.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="5cd1b-122">Para habilitar UDFs, execute o seguinte comando do Windows PowerShell no Office Online Server, depois que o farm do Office Web Apps Server foi criado.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a><span data-ttu-id="5cd1b-123">Criar definições de UDF no servidor on-line do Office</span><span class="sxs-lookup"><span data-stu-id="5cd1b-123">Create UDF definitions on Office Online Server</span></span>

<span data-ttu-id="5cd1b-124">Após habilitar UDFs, você precisa criar uma definição para binário que contém os UDFs.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="5cd1b-125">Para criar uma definição para seu UDF binários no servidor do Office Online, use o cmdlet **New-OfficeWebAppsExcelUserDefinedFunction** .</span><span class="sxs-lookup"><span data-stu-id="5cd1b-125">To create a definition for your UDF binary on the Office Online Server, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="5cd1b-126">Esse cmdlet inclui os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="5cd1b-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="5cd1b-127">**Assembly**</span><span class="sxs-lookup"><span data-stu-id="5cd1b-127">**Assembly**</span></span>
    
- <span data-ttu-id="5cd1b-128">**AssemblyLocation**</span><span class="sxs-lookup"><span data-stu-id="5cd1b-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="5cd1b-129">**Habilitar** (definido como False por padrão)</span><span class="sxs-lookup"><span data-stu-id="5cd1b-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="5cd1b-130">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5cd1b-130">**Description**</span></span>
    
<span data-ttu-id="5cd1b-131">Os exemplos a seguir mostram como criar as definições de UDF.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="5cd1b-132">Depois de criar a nova referência UDF, execute o **iisreset** no servidor para pegue a referência imediatamente.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a><span data-ttu-id="5cd1b-133">Comandos adicionais do Office Online Server UDF Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5cd1b-133">Additional Office Online Server UDF Windows PowerShell commands</span></span>

<span data-ttu-id="5cd1b-134">Use os seguintes cmdlets do Windows PowerShell para trabalhar com UDFs:</span><span class="sxs-lookup"><span data-stu-id="5cd1b-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="5cd1b-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (sem parâmetros obrigatórios) - retorna uma lista de definições de UDF que são configuradas no servidor do Office Online.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server.</span></span> 
    
- <span data-ttu-id="5cd1b-136">**Set-OfficeWebAppsExcelUserDefinedFunction** (Parâmetro de identidade necessário) - define propriedades em definições de UDF existentes.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="5cd1b-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Parâmetro de identidade necessário) - remove as definições de UDF existentes.</span><span class="sxs-lookup"><span data-stu-id="5cd1b-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="5cd1b-138">Amostra UDF</span><span class="sxs-lookup"><span data-stu-id="5cd1b-138">UDF sample</span></span>

<span data-ttu-id="5cd1b-139">Os arquivos a seguir fornecem uma pasta de trabalho de exemplo que usa um UDF e UDF binário:</span><span class="sxs-lookup"><span data-stu-id="5cd1b-139">The following files provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="5cd1b-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): uma pasta de trabalho de exemplo que usa um UDF</span><span class="sxs-lookup"><span data-stu-id="5cd1b-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): a sample workbook that uses a UDF</span></span>  
- <span data-ttu-id="5cd1b-141">[EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): o binário UDF</span><span class="sxs-lookup"><span data-stu-id="5cd1b-141">[EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): the UDF binary</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="5cd1b-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cd1b-142">See also</span></span>

- [<span data-ttu-id="5cd1b-143">Configurar definições administrativas Excel Online</span><span class="sxs-lookup"><span data-stu-id="5cd1b-143">Configure Excel Online administrative settings</span></span>](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [<span data-ttu-id="5cd1b-144">Servidor do Office Online</span><span class="sxs-lookup"><span data-stu-id="5cd1b-144">Office Online Server</span></span>](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

