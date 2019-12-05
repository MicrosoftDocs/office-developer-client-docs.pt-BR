---
title: Configurar UDFs no Excel online no servidor do Office Online
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Use funções definidas pelo usuário (UDFs) no Excel online no servidor do Office Online para chamar funções personalizadas.
ms.openlocfilehash: 6e16ea753090b2fefca4ae15330f1a27d53da777
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819354"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a><span data-ttu-id="8b7d2-103">Configurar UDFs no Excel online no servidor do Office Online</span><span class="sxs-lookup"><span data-stu-id="8b7d2-103">Configure UDFs in Excel Online in Office Online Server</span></span>

<span data-ttu-id="8b7d2-104">Use funções definidas pelo usuário (UDFs) no Excel online no servidor do Office Online para chamar funções personalizadas.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-104">Use user-defined functions (UDFs) in Excel Online in Office Online Server to call custom functions.</span></span> 
  
<span data-ttu-id="8b7d2-105">As funções definidas pelo usuário (UDFs) no Excel online permitem chamar funções personalizadas escritas em código gerenciado usando fórmulas em células.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-105">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells.</span></span> <span data-ttu-id="8b7d2-106">Você pode usar UDFs para:</span><span class="sxs-lookup"><span data-stu-id="8b7d2-106">You can use UDFs to:</span></span>
  
- <span data-ttu-id="8b7d2-107">Chamar funções matemáticas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="8b7d2-108">Obter dados de fontes de dados personalizadas para planilhas.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="8b7d2-109">Chamar serviços Web.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-109">Call web services.</span></span>
    
<span data-ttu-id="8b7d2-110">Você pode instalar binários UDF em um dos dois locais:</span><span class="sxs-lookup"><span data-stu-id="8b7d2-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="8b7d2-111">Um diretório local.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-111">A local directory.</span></span> <span data-ttu-id="8b7d2-112">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8b7d2-112">For example:</span></span> 
    
    <span data-ttu-id="8b7d2-113">C:\UDFs\MySampleUdf.dll</span><span class="sxs-lookup"><span data-stu-id="8b7d2-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="8b7d2-114">O cache de assembly global.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-114">The global assembly cache.</span></span> <span data-ttu-id="8b7d2-115">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8b7d2-115">For example:</span></span> 
    
    <span data-ttu-id="8b7d2-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="8b7d2-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="8b7d2-117">Faça referência ao local ao criar uma definição de **New-OfficeWebAppsExcelUserDefinedFunction** no servidor do Office Online.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8b7d2-118">O servidor do Office Online não dá suporte a UDFs localizados em compartilhamentos de rede.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-118">Office Online Server does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server"></a><span data-ttu-id="8b7d2-119">Habilitar UDFs no servidor do Office Online</span><span class="sxs-lookup"><span data-stu-id="8b7d2-119">Enable UDFs on Office Online Server</span></span> 

<span data-ttu-id="8b7d2-120">Quando um administrador cria um novo farm do servidor do Office Web Apps usando o cmdlet [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) do Windows PowerShell, os assemblies UDF estão desabilitados por padrão.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-120">When an adminstrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="8b7d2-121">O valor padrão do sinalizador **ExcelUdfsAllowed** é false.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="8b7d2-122">Para habilitar UDFs, execute o seguinte comando do Windows PowerShell no servidor do Office Online, após a criação do farm do servidor do Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a><span data-ttu-id="8b7d2-123">Criar definições de UDF no servidor do Office Online</span><span class="sxs-lookup"><span data-stu-id="8b7d2-123">Create UDF definitions on Office Online Server</span></span>

<span data-ttu-id="8b7d2-124">Depois de habilitar UDFs, você precisará criar uma definição para o binário que contém os UDFs.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="8b7d2-125">Para criar uma definição para seu binário UDF no servidor do Office Online, use o cmdlet **New-OfficeWebAppsExcelUserDefinedFunction** .</span><span class="sxs-lookup"><span data-stu-id="8b7d2-125">To create a definition for your UDF binary on the Office Online Server, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="8b7d2-126">Este cmdlet inclui os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8b7d2-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="8b7d2-127">**Defletor**</span><span class="sxs-lookup"><span data-stu-id="8b7d2-127">**Assembly**</span></span>
    
- <span data-ttu-id="8b7d2-128">**AssemblyLocation**</span><span class="sxs-lookup"><span data-stu-id="8b7d2-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="8b7d2-129">**Habilitar** (definido como false por padrão)</span><span class="sxs-lookup"><span data-stu-id="8b7d2-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="8b7d2-130">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8b7d2-130">**Description**</span></span>
    
<span data-ttu-id="8b7d2-131">Os exemplos a seguir mostram como criar as definições de UDF.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="8b7d2-132">Após criar a nova referência de UDF, execute **iisreset** no servidor para selecionar a referência imediatamente.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a><span data-ttu-id="8b7d2-133">Comandos do Windows PowerShell adicionais do servidor do Office Online</span><span class="sxs-lookup"><span data-stu-id="8b7d2-133">Additional Office Online Server UDF Windows PowerShell commands</span></span>

<span data-ttu-id="8b7d2-134">Use os seguintes cmdlets do Windows PowerShell para trabalhar com UDFs:</span><span class="sxs-lookup"><span data-stu-id="8b7d2-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="8b7d2-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (nenhum parâmetro obrigatório)-retorna uma lista de definições UDF configuradas no servidor do Office Online.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server.</span></span> 
    
- <span data-ttu-id="8b7d2-136">**Set-OfficeWebAppsExcelUserDefinedFunction** (parâmetro Identity obrigatório): define as propriedades nas definições de UDF existentes.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="8b7d2-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (parâmetro Identity obrigatório)-Remove definições UDF existentes.</span><span class="sxs-lookup"><span data-stu-id="8b7d2-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="8b7d2-138">Exemplo de UDF</span><span class="sxs-lookup"><span data-stu-id="8b7d2-138">UDF sample</span></span>

<span data-ttu-id="8b7d2-139">O arquivo de exemplo a seguir fornece um exemplo de pasta de trabalho que usa um UDF e o binário UDF:</span><span class="sxs-lookup"><span data-stu-id="8b7d2-139">The following sample file provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="8b7d2-140">[BooleanDataType. xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): um exemplo de pasta de trabalho que usa um UDF</span><span class="sxs-lookup"><span data-stu-id="8b7d2-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): a sample workbook that uses a UDF</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="8b7d2-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b7d2-141">See also</span></span>

- [<span data-ttu-id="8b7d2-142">Configurar definições administrativas do Excel Online</span><span class="sxs-lookup"><span data-stu-id="8b7d2-142">Configure Excel Online administrative settings</span></span>](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [<span data-ttu-id="8b7d2-143">Office Online Server</span><span class="sxs-lookup"><span data-stu-id="8b7d2-143">Office Online Server</span></span>](https://docs.microsoft.com/officeonlineserver/office-online-serverr)
    

