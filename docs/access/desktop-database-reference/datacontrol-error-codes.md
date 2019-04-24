---
title: Códigos de erro do DataControl
TOCTitle: DataControl error codes
ms:assetid: d81446e2-aae6-b460-08a3-eae9920dc767
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250089(v=office.15)
ms:contentKeyID: 48548027
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 387f37e180d346c09cf3dadbf66f665cb83dbd0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294540"
---
# <a name="datacontrol-error-codes"></a><span data-ttu-id="0b591-102">Códigos de erro do DataControl</span><span class="sxs-lookup"><span data-stu-id="0b591-102">DataControl error codes</span></span>


<span data-ttu-id="0b591-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b591-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0b591-p101">A tabela abaixo lista os códigos de erro do objeto [RDS.DataControl](datacontrol-object-rds.md), mostrando a conversão decimal positiva dos dois bytes inferiores, a conversão decimal negativa do código de erro completo e os valores hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="0b591-p101">The following table lists the [RDS.DataControl](datacontrol-object-rds.md) object error codes. The positive decimal translation of the low two bytes, the negative decimal translation of the full error code, and the hexadecimal values are shown.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b591-106">Códigos de erro do RDS.DataControl</span><span class="sxs-lookup"><span data-stu-id="0b591-106">RDS.DataControl error codes</span></span></p></th>
<th><p><span data-ttu-id="0b591-107">Número</span><span class="sxs-lookup"><span data-stu-id="0b591-107">Number</span></span></p></th>
<th><p><span data-ttu-id="0b591-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b591-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b591-109"><strong>IDS_AsyncPending</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-109"><strong>IDS_AsyncPending</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-110">4107</span><span class="sxs-lookup"><span data-stu-id="0b591-110">4107</span></span><br />
<span data-ttu-id="0b591-111">-2146824175</span><span class="sxs-lookup"><span data-stu-id="0b591-111">-2146824175</span></span><br />
<span data-ttu-id="0b591-112">0x800A1011</span><span class="sxs-lookup"><span data-stu-id="0b591-112">0x800A1011</span></span></p></td>
<td><p><span data-ttu-id="0b591-113">A operação não pode ser executada enquanto houver uma operação assíncrona pendente.</span><span class="sxs-lookup"><span data-stu-id="0b591-113">Operation cannot be performed while async operation is pending.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b591-114"><strong>IDS_BadInlineTablegram</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-114"><strong>IDS_BadInlineTablegram</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-115">4105</span><span class="sxs-lookup"><span data-stu-id="0b591-115">4105</span></span><br />
<span data-ttu-id="0b591-116">-2146824183</span><span class="sxs-lookup"><span data-stu-id="0b591-116">-2146824183</span></span><br />
<span data-ttu-id="0b591-117">0x800A1009</span><span class="sxs-lookup"><span data-stu-id="0b591-117">0x800A1009</span></span></p></td>
<td><p><span data-ttu-id="0b591-118">Tablegram embutido inválido.</span><span class="sxs-lookup"><span data-stu-id="0b591-118">Bad inline tablegram.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b591-119"><strong>IDS_CantConnect</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-119"><strong>IDS_CantConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-120">4099</span><span class="sxs-lookup"><span data-stu-id="0b591-120">4099</span></span><br />
<span data-ttu-id="0b591-121">-2146824189</span><span class="sxs-lookup"><span data-stu-id="0b591-121">-2146824189</span></span><br />
<span data-ttu-id="0b591-122">0x800A1003</span><span class="sxs-lookup"><span data-stu-id="0b591-122">0x800A1003</span></span></p></td>
<td><p><span data-ttu-id="0b591-123">Não foi possível conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="0b591-123">Cannot connect to server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b591-124"><strong>IDS_CantCreateObject</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-124"><strong>IDS_CantCreateObject</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-125">4100</span><span class="sxs-lookup"><span data-stu-id="0b591-125">4100</span></span><br />
<span data-ttu-id="0b591-126">-2146824188</span><span class="sxs-lookup"><span data-stu-id="0b591-126">-2146824188</span></span><br />
<span data-ttu-id="0b591-127">0x800A1004</span><span class="sxs-lookup"><span data-stu-id="0b591-127">0x800A1004</span></span></p></td>
<td><p><span data-ttu-id="0b591-128">Não foi possível criar o objeto comercial.</span><span class="sxs-lookup"><span data-stu-id="0b591-128">Business object cannot be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b591-129"><strong>IDS_CantFindDataspace</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-129"><strong>IDS_CantFindDataspace</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-130">4102</span><span class="sxs-lookup"><span data-stu-id="0b591-130">4102</span></span><br />
<span data-ttu-id="0b591-131">-2146824186</span><span class="sxs-lookup"><span data-stu-id="0b591-131">-2146824186</span></span><br />
<span data-ttu-id="0b591-132">0x800A1006</span><span class="sxs-lookup"><span data-stu-id="0b591-132">0x800A1006</span></span></p></td>
<td><p><span data-ttu-id="0b591-133">A propriedade Dataspace não é válida.</span><span class="sxs-lookup"><span data-stu-id="0b591-133">Dataspace property is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b591-134"><strong>IDS_CantInvokeMethod</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-134"><strong>IDS_CantInvokeMethod</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-135">4101</span><span class="sxs-lookup"><span data-stu-id="0b591-135">4101</span></span><br />
<span data-ttu-id="0b591-136">-2146824187</span><span class="sxs-lookup"><span data-stu-id="0b591-136">-2146824187</span></span><br />
<span data-ttu-id="0b591-137">0x800A1005</span><span class="sxs-lookup"><span data-stu-id="0b591-137">0x800A1005</span></span></p></td>
<td><p><span data-ttu-id="0b591-138">Não foi possível invocar o método no objeto comercial.</span><span class="sxs-lookup"><span data-stu-id="0b591-138">Method cannot be invoked on business object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b591-139"><strong>IDS_CrossDomainWarning</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-139"><strong>IDS_CrossDomainWarning</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-140">4112</span><span class="sxs-lookup"><span data-stu-id="0b591-140">4112</span></span><br />
<span data-ttu-id="0b591-141">-2146824170</span><span class="sxs-lookup"><span data-stu-id="0b591-141">-2146824170</span></span><br />
<span data-ttu-id="0b591-142">0x800A1016</span><span class="sxs-lookup"><span data-stu-id="0b591-142">0x800A1016</span></span></p></td>
<td><p><span data-ttu-id="0b591-143">Esta página acessa dados em outro domínio.</span><span class="sxs-lookup"><span data-stu-id="0b591-143">This page accesses data on another domain.</span></span> <span data-ttu-id="0b591-144">Você quer permitir isso?</span><span class="sxs-lookup"><span data-stu-id="0b591-144">Do you want to allow this?</span></span> <span data-ttu-id="0b591-145">Para evitar essa mensagem no Internet Explorer, você pode adicionar um site seguro à zona de sites confiáveis na guia <strong>segurança</strong> da caixa de diálogo <strong>Opções da Internet</strong> .</span><span class="sxs-lookup"><span data-stu-id="0b591-145">To avoid this message in Internet Explorer, you can add a secure website to your Trusted Sites zone on the <strong>Security</strong> tab of the <strong>Internet Options</strong> dialog box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b591-146"><strong>IDS_InvalidADCClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-146"><strong>IDS_InvalidADCClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-147">4106</span><span class="sxs-lookup"><span data-stu-id="0b591-147">4106</span></span><br />
<span data-ttu-id="0b591-148">-2146824176</span><span class="sxs-lookup"><span data-stu-id="0b591-148">-2146824176</span></span><br />
<span data-ttu-id="0b591-149">0x800A1010</span><span class="sxs-lookup"><span data-stu-id="0b591-149">0x800A1010</span></span></p></td>
<td><p><span data-ttu-id="0b591-150">Versão de cliente RDS inVálida — o cliente é mais recente do que o servidor.</span><span class="sxs-lookup"><span data-stu-id="0b591-150">Invalid RDS Client Version — Client is newer than server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b591-151"><strong>IDS_INVALIDARG</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-151"><strong>IDS_INVALIDARG</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-152">5376</span><span class="sxs-lookup"><span data-stu-id="0b591-152">5376</span></span><br />
<span data-ttu-id="0b591-153">-2147019520</span><span class="sxs-lookup"><span data-stu-id="0b591-153">-2147019520</span></span><br />
<span data-ttu-id="0b591-154">0x80071500</span><span class="sxs-lookup"><span data-stu-id="0b591-154">0x80071500</span></span></p></td>
<td><p><span data-ttu-id="0b591-155">Um ou mais argumentos são inválidos.</span><span class="sxs-lookup"><span data-stu-id="0b591-155">One or more arguments are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b591-156"><strong>IDS_InvalidBindings</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-156"><strong>IDS_InvalidBindings</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-157">4097</span><span class="sxs-lookup"><span data-stu-id="0b591-157">4097</span></span><br />
<span data-ttu-id="0b591-158">-2146824191</span><span class="sxs-lookup"><span data-stu-id="0b591-158">-2146824191</span></span><br />
<span data-ttu-id="0b591-159">0x800A1001</span><span class="sxs-lookup"><span data-stu-id="0b591-159">0x800A1001</span></span></p></td>
<td><p><span data-ttu-id="0b591-160">Erro na propriedade Bindings.</span><span class="sxs-lookup"><span data-stu-id="0b591-160">Error in bindings property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b591-161"><strong>IDS_InvalidParam</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-161"><strong>IDS_InvalidParam</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-162">4110</span><span class="sxs-lookup"><span data-stu-id="0b591-162">4110</span></span><br />
<span data-ttu-id="0b591-163">-2146824172</span><span class="sxs-lookup"><span data-stu-id="0b591-163">-2146824172</span></span><br />
<span data-ttu-id="0b591-164">0x800A1014</span><span class="sxs-lookup"><span data-stu-id="0b591-164">0x800A1014</span></span></p></td>
<td><p><span data-ttu-id="0b591-165">Um ou mais argumentos são inválidos.</span><span class="sxs-lookup"><span data-stu-id="0b591-165">One or more arguments are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b591-166"><strong>IDS_NOINTERFACE</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-166"><strong>IDS_NOINTERFACE</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-167">5377</span><span class="sxs-lookup"><span data-stu-id="0b591-167">5377</span></span><br />
<span data-ttu-id="0b591-168">-2147019519</span><span class="sxs-lookup"><span data-stu-id="0b591-168">-2147019519</span></span><br />
<span data-ttu-id="0b591-169">0x80071501</span><span class="sxs-lookup"><span data-stu-id="0b591-169">0x80071501</span></span></p></td>
<td><p><span data-ttu-id="0b591-170">Não há suporte para essa interface.</span><span class="sxs-lookup"><span data-stu-id="0b591-170">No such interface is supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b591-171"><strong>IDS_NotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-171"><strong>IDS_NotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-172">4111</span><span class="sxs-lookup"><span data-stu-id="0b591-172">4111</span></span><br />
<span data-ttu-id="0b591-173">-2146824171</span><span class="sxs-lookup"><span data-stu-id="0b591-173">-2146824171</span></span><br />
<span data-ttu-id="0b591-174">0x800A1015</span><span class="sxs-lookup"><span data-stu-id="0b591-174">0x800A1015</span></span></p></td>
<td><p><span data-ttu-id="0b591-175">A solicitação não pode ser executada enquanto o manipulador de eventos estiver processando.</span><span class="sxs-lookup"><span data-stu-id="0b591-175">Request cannot be executed while the event handler is still processing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b591-176"><strong>IDS_ObjectNotSafe</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-176"><strong>IDS_ObjectNotSafe</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-177">4103</span><span class="sxs-lookup"><span data-stu-id="0b591-177">4103</span></span><br />
<span data-ttu-id="0b591-178">-2146824185</span><span class="sxs-lookup"><span data-stu-id="0b591-178">-2146824185</span></span><br />
<span data-ttu-id="0b591-179">0x800A1007</span><span class="sxs-lookup"><span data-stu-id="0b591-179">0x800A1007</span></span></p></td>
<td><p><span data-ttu-id="0b591-180">As configurações de segurança deste computador proíbem a criação do objeto comercial.</span><span class="sxs-lookup"><span data-stu-id="0b591-180">Safety settings on this computer prohibit creation of business object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b591-181"><strong>IDS_RecordsetNotOpen</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-181"><strong>IDS_RecordsetNotOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-182">4109</span><span class="sxs-lookup"><span data-stu-id="0b591-182">4109</span></span><br />
<span data-ttu-id="0b591-183">-2146824173</span><span class="sxs-lookup"><span data-stu-id="0b591-183">-2146824173</span></span><br />
<span data-ttu-id="0b591-184">0x800A1013</span><span class="sxs-lookup"><span data-stu-id="0b591-184">0x800A1013</span></span></p></td>
<td><p><span data-ttu-id="0b591-185"><strong>Recordset</strong> não está aberto.</span><span class="sxs-lookup"><span data-stu-id="0b591-185"><strong>Recordset</strong> is not open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b591-186"><strong>IDS_ResetInvalidField</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-186"><strong>IDS_ResetInvalidField</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-187">4108</span><span class="sxs-lookup"><span data-stu-id="0b591-187">4108</span></span><br />
<span data-ttu-id="0b591-188">-2146824174</span><span class="sxs-lookup"><span data-stu-id="0b591-188">-2146824174</span></span><br />
<span data-ttu-id="0b591-189">0x800A1012</span><span class="sxs-lookup"><span data-stu-id="0b591-189">0x800A1012</span></span></p></td>
<td><p><span data-ttu-id="0b591-190">A coluna especificada em <strong>SortColumn</strong> ou <strong>FilterColumn</strong> não existe.</span><span class="sxs-lookup"><span data-stu-id="0b591-190">Column specified in <strong>SortColumn</strong> or <strong>FilterColumn</strong> does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b591-191"><strong>IDS_RowsetNotUpdateable</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-191"><strong>IDS_RowsetNotUpdateable</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-192">4104</span><span class="sxs-lookup"><span data-stu-id="0b591-192">4104</span></span><br />
<span data-ttu-id="0b591-193">-2146824184</span><span class="sxs-lookup"><span data-stu-id="0b591-193">-2146824184</span></span><br />
<span data-ttu-id="0b591-194">0x800A1008</span><span class="sxs-lookup"><span data-stu-id="0b591-194">0x800A1008</span></span></p></td>
<td><p><span data-ttu-id="0b591-195">O conjunto de linhas não pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="0b591-195">Rowset not updateable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b591-196"><strong>IDS_UnexpectedError</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-196"><strong>IDS_UnexpectedError</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-197">4351</span><span class="sxs-lookup"><span data-stu-id="0b591-197">4351</span></span><br />
<span data-ttu-id="0b591-198">-2146823937</span><span class="sxs-lookup"><span data-stu-id="0b591-198">-2146823937</span></span><br />
<span data-ttu-id="0b591-199">0x800A10FF</span><span class="sxs-lookup"><span data-stu-id="0b591-199">0x800A10FF</span></span></p></td>
<td><p><span data-ttu-id="0b591-200">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="0b591-200">Unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b591-201"><strong>IDS_UpdatesFailed</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-201"><strong>IDS_UpdatesFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-202">4098</span><span class="sxs-lookup"><span data-stu-id="0b591-202">4098</span></span><br />
<span data-ttu-id="0b591-203">-2146824190</span><span class="sxs-lookup"><span data-stu-id="0b591-203">-2146824190</span></span><br />
<span data-ttu-id="0b591-204">0x800A1002</span><span class="sxs-lookup"><span data-stu-id="0b591-204">0x800A1002</span></span></p></td>
<td><p><span data-ttu-id="0b591-205">Não foi possível atualizar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0b591-205">Unable to update database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b591-206"><strong>IDS_URLMONNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="0b591-206"><strong>IDS_URLMONNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="0b591-207">4119</span><span class="sxs-lookup"><span data-stu-id="0b591-207">4119</span></span><br />
<span data-ttu-id="0b591-208">-2146824169</span><span class="sxs-lookup"><span data-stu-id="0b591-208">-2146824169</span></span><br />
<span data-ttu-id="0b591-209">0x800A1017</span><span class="sxs-lookup"><span data-stu-id="0b591-209">0x800A1017</span></span></p></td>
<td><p><span data-ttu-id="0b591-210">A propriedade <strong>URL</strong> do DataControl requer o arquivo do sistema Urlmon.dll, que não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="0b591-210">DataControl <strong>URL</strong> property requires the system file Urlmon.dll, which cannot be found.</span></span></p></td>
</tr>
</tbody>
</table>

