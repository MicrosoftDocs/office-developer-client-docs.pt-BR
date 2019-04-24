---
title: ErrorValueEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: ErrorValueEnum
ms:assetid: 2af99f32-6004-1225-367c-45d693f447b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249058(v=office.15)
ms:contentKeyID: 48543921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2d4207f157d361f3b8aba2ff80f46d06b2f328e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293319"
---
# <a name="errorvalueenum"></a><span data-ttu-id="bf2ec-102">ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="bf2ec-102">ErrorValueEnum</span></span>

<span data-ttu-id="bf2ec-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf2ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bf2ec-104">Especifica o tipo de erro de tempo de execução do ADO.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-104">Specifies the type of ADO run-time error.</span></span>

<span data-ttu-id="bf2ec-105">Três formatos de número de erro são listados:</span><span class="sxs-lookup"><span data-stu-id="bf2ec-105">Three forms of the error number are listed:</span></span>

- <span data-ttu-id="bf2ec-p101">Decimal positivo  os dois bytes baixos de um número completo em formato decimal. Esse número é exibido na caixa de diálogo de erros padrão do Visual Basic. Por exemplo, Erro de tempo de execução '3707'.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-p101">Positive decimal — the low two bytes of the full number in decimal format. This number is displayed in the default Visual Basic error message dialog box. For example, Run-time error '3707'.</span></span>

- <span data-ttu-id="bf2ec-109">Decimal negativo  A conversão decimal de um número completo do erro.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-109">Negative decimal — The decimal translation of the full error number.</span></span>

- <span data-ttu-id="bf2ec-110">Hexadecimal  A representação hexadecimal do número completo do erro.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-110">Hexadecimal — The hexadecimal representation of the full error number.</span></span> <span data-ttu-id="bf2ec-111">O código de recurso do Windows está no quarto dígito.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-111">The Windows facility code is in the fourth digit.</span></span> <span data-ttu-id="bf2ec-112">O código de facilidade para números de erro do ADO é *um*. Por exemplo: 0x800***um***0E7B.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-112">The facility code for ADO error numbers is *A*. For example: 0x800***A***0E7B.</span></span>

> [!NOTE]
> <span data-ttu-id="bf2ec-113">Os erros do OLE DB podem ser transmitidos para seu aplicativo ADO.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-113">OLE DB errors may be passed to your ADO application.</span></span> <span data-ttu-id="bf2ec-114">Em geral, eles podem ser identificados por um código de recursos do Windows de *4*.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-114">Typically, these can be identified by a Windows facility code of *4*.</span></span> <span data-ttu-id="bf2ec-115">Por exemplo, 0x800_**4**_.... Para obter mais informações sobre esses números, consulte o capítulo 16 da *referência do programador do OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="bf2ec-115">For example, 0x800_**4**_.... For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf2ec-116">Constant</span><span class="sxs-lookup"><span data-stu-id="bf2ec-116">Constant</span></span></p></th>
<th><p><span data-ttu-id="bf2ec-117">Valor</span><span class="sxs-lookup"><span data-stu-id="bf2ec-117">Value</span></span></p></th>
<th><p><span data-ttu-id="bf2ec-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf2ec-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-119"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-119"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-120">3707</span><span class="sxs-lookup"><span data-stu-id="bf2ec-120">3707</span></span><br />
<span data-ttu-id="bf2ec-121">-2146824581</span><span class="sxs-lookup"><span data-stu-id="bf2ec-121">-2146824581</span></span><br />
<span data-ttu-id="bf2ec-122">0x800A0E7B</span><span class="sxs-lookup"><span data-stu-id="bf2ec-122">0x800A0E7B</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-123">Não pode alterar a propriedade <strong>ActiveConnection</strong> de um objeto <strong>Recordset</strong> que tem um objeto <strong>Command</strong> como sua fonte.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-123">Cannot change the <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object which has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-124"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-124"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-125">3732</span><span class="sxs-lookup"><span data-stu-id="bf2ec-125">3732</span></span><br />
<span data-ttu-id="bf2ec-126">-2146824556</span><span class="sxs-lookup"><span data-stu-id="bf2ec-126">-2146824556</span></span><br />
<span data-ttu-id="bf2ec-127">0x800A0E94</span><span class="sxs-lookup"><span data-stu-id="bf2ec-127">0x800A0E94</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-128">O servidor não pode concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-128">Server cannot complete the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-129"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-129"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-130">3748</span><span class="sxs-lookup"><span data-stu-id="bf2ec-130">3748</span></span><br />
<span data-ttu-id="bf2ec-131">-2146824540</span><span class="sxs-lookup"><span data-stu-id="bf2ec-131">-2146824540</span></span><br />
<span data-ttu-id="bf2ec-132">0x800A0EA4</span><span class="sxs-lookup"><span data-stu-id="bf2ec-132">0x800A0EA4</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-133">A conexão foi negada.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-133">Connection was denied.</span></span> <span data-ttu-id="bf2ec-134">A nova conexão solicitada tem diferentes recursos em relação àquela que está em uso.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-134">New connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-135"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-135"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-136">3220</span><span class="sxs-lookup"><span data-stu-id="bf2ec-136">3220</span></span><br />
<span data-ttu-id="bf2ec-137">-2146825068</span><span class="sxs-lookup"><span data-stu-id="bf2ec-137">-2146825068</span></span><br />
<span data-ttu-id="bf2ec-138">0X800A0C94</span><span class="sxs-lookup"><span data-stu-id="bf2ec-138">0X800A0C94</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-139">O provedor designado é diferente daquele que está em uso.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-139">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-140"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-140"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-141">3724</span><span class="sxs-lookup"><span data-stu-id="bf2ec-141">3724</span></span><br />
<span data-ttu-id="bf2ec-142">-2146824564</span><span class="sxs-lookup"><span data-stu-id="bf2ec-142">-2146824564</span></span><br />
<span data-ttu-id="bf2ec-143">0x800A0E8C</span><span class="sxs-lookup"><span data-stu-id="bf2ec-143">0x800A0E8C</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-144">O valor dos dados não pode ser convertido por razões diferentes de incompatibilidade assinada ou estouro de dados.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-144">Data value cannot be converted for reasons other than sign mismatch or data overflow.</span></span> <span data-ttu-id="bf2ec-145">Por exemplo, a conversão truncaria os dados.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-145">For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-146"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-146"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-147">3725</span><span class="sxs-lookup"><span data-stu-id="bf2ec-147">3725</span></span><br />
<span data-ttu-id="bf2ec-148">-2146824563</span><span class="sxs-lookup"><span data-stu-id="bf2ec-148">-2146824563</span></span><br />
<span data-ttu-id="bf2ec-149">0x800A0E8D</span><span class="sxs-lookup"><span data-stu-id="bf2ec-149">0x800A0E8D</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-150">O valor dos dados não pode ser definido ou recuperado porque o tipo de dados do campo é desconhecido ou o provedor tem recursos insuficientes para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-150">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-151"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-151"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-152">3747</span><span class="sxs-lookup"><span data-stu-id="bf2ec-152">3747</span></span><br />
<span data-ttu-id="bf2ec-153">-2146824541</span><span class="sxs-lookup"><span data-stu-id="bf2ec-153">-2146824541</span></span><br />
<span data-ttu-id="bf2ec-154">0x800A0EA3</span><span class="sxs-lookup"><span data-stu-id="bf2ec-154">0x800A0EA3</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-155">A operação requer um <strong>ParentCatalog</strong> válido.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-155">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-156"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-156"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-157">3726</span><span class="sxs-lookup"><span data-stu-id="bf2ec-157">3726</span></span><br />
<span data-ttu-id="bf2ec-158">-2146824562</span><span class="sxs-lookup"><span data-stu-id="bf2ec-158">-2146824562</span></span><br />
<span data-ttu-id="bf2ec-159">0x800A0E8E</span><span class="sxs-lookup"><span data-stu-id="bf2ec-159">0x800A0E8E</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-160">O registro não contém esse campo.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-160">Record does not contain this field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-161"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-161"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-162">3421</span><span class="sxs-lookup"><span data-stu-id="bf2ec-162">3421</span></span><br />
<span data-ttu-id="bf2ec-163">-2146824867</span><span class="sxs-lookup"><span data-stu-id="bf2ec-163">-2146824867</span></span><br />
<span data-ttu-id="bf2ec-164">0x800A0D5D</span><span class="sxs-lookup"><span data-stu-id="bf2ec-164">0x800A0D5D</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-165">O aplicativo usa um valor de tipo incorreto para a operação atual.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-165">Application uses a value of the wrong type for the current operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-166"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-166"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-167">3721</span><span class="sxs-lookup"><span data-stu-id="bf2ec-167">3721</span></span><br />
<span data-ttu-id="bf2ec-168">-2146824567</span><span class="sxs-lookup"><span data-stu-id="bf2ec-168">-2146824567</span></span><br />
<span data-ttu-id="bf2ec-169">0x800A0E89</span><span class="sxs-lookup"><span data-stu-id="bf2ec-169">0x800A0E89</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-170">O valor dos dados é muito grande para ser representado pelo tipo de dados do campo.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-170">Data value is too large to be represented by the field data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-171"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-171"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-172">3738</span><span class="sxs-lookup"><span data-stu-id="bf2ec-172">3738</span></span><br />
<span data-ttu-id="bf2ec-173">-2146824550</span><span class="sxs-lookup"><span data-stu-id="bf2ec-173">-2146824550</span></span><br />
<span data-ttu-id="bf2ec-174">0x800A0E9A</span><span class="sxs-lookup"><span data-stu-id="bf2ec-174">0x800A0E9A</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-175">A URL do objeto a ser excluído está fora do escopo do registro atual.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-175">URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-176"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-176"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-177">3750</span><span class="sxs-lookup"><span data-stu-id="bf2ec-177">3750</span></span><br />
<span data-ttu-id="bf2ec-178">-2146824538</span><span class="sxs-lookup"><span data-stu-id="bf2ec-178">-2146824538</span></span><br />
<span data-ttu-id="bf2ec-179">0x800A0EA6</span><span class="sxs-lookup"><span data-stu-id="bf2ec-179">0x800A0EA6</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-180">O provedor não oferece suporte a restrições de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-180">Provider does not support sharing restrictions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-181"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-181"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-182">3751</span><span class="sxs-lookup"><span data-stu-id="bf2ec-182">3751</span></span><br />
<span data-ttu-id="bf2ec-183">-2146824537</span><span class="sxs-lookup"><span data-stu-id="bf2ec-183">-2146824537</span></span><br />
<span data-ttu-id="bf2ec-184">0x800A0EA7</span><span class="sxs-lookup"><span data-stu-id="bf2ec-184">0x800A0EA7</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-185">O provedor não oferece suporte ao tipo solicitado de restrição de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-185">Provider does not support the requested kind of sharing restriction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-186"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-186"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-187">3251</span><span class="sxs-lookup"><span data-stu-id="bf2ec-187">3251</span></span><br />
<span data-ttu-id="bf2ec-188">-2146825037</span><span class="sxs-lookup"><span data-stu-id="bf2ec-188">-2146825037</span></span><br />
<span data-ttu-id="bf2ec-189">0x800A0CB3</span><span class="sxs-lookup"><span data-stu-id="bf2ec-189">0x800A0CB3</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-190">O objeto ou o provedor não pode executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-190">Object or provider is not capable of performing requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-191"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-191"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-192">3749</span><span class="sxs-lookup"><span data-stu-id="bf2ec-192">3749</span></span><br />
<span data-ttu-id="bf2ec-193">-2146824539</span><span class="sxs-lookup"><span data-stu-id="bf2ec-193">-2146824539</span></span><br />
<span data-ttu-id="bf2ec-194">0x800A0EA5</span><span class="sxs-lookup"><span data-stu-id="bf2ec-194">0x800A0EA5</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-195">A atualização dos campos falhou.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-195">Fields update failed.</span></span> <span data-ttu-id="bf2ec-196">Para obter outras informações, analise a propriedade <strong>Status</strong> dos objetos de campo individuais.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-196">For further information, examine the <strong>Status</strong> property of individual field objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-197"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-197"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-198">3219</span><span class="sxs-lookup"><span data-stu-id="bf2ec-198">3219</span></span><br />
<span data-ttu-id="bf2ec-199">-2146825069</span><span class="sxs-lookup"><span data-stu-id="bf2ec-199">-2146825069</span></span><br />
<span data-ttu-id="bf2ec-200">0x800A0C93</span><span class="sxs-lookup"><span data-stu-id="bf2ec-200">0x800A0C93</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-201">A operação não é permitida nesse contexto.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-201">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-202"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-202"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-203">3719</span><span class="sxs-lookup"><span data-stu-id="bf2ec-203">3719</span></span><br />
<span data-ttu-id="bf2ec-204">-2146824569</span><span class="sxs-lookup"><span data-stu-id="bf2ec-204">-2146824569</span></span><br />
<span data-ttu-id="bf2ec-205">0x800A0E87</span><span class="sxs-lookup"><span data-stu-id="bf2ec-205">0x800A0E87</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-206">O valor de dados está em conflito com as restrições de integridade do campo.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-206">Data value conflicts with the integrity constraints of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-207"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-207"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-208">3246</span><span class="sxs-lookup"><span data-stu-id="bf2ec-208">3246</span></span><br />
<span data-ttu-id="bf2ec-209">-2146825042</span><span class="sxs-lookup"><span data-stu-id="bf2ec-209">-2146825042</span></span><br />
<span data-ttu-id="bf2ec-210">0x800A0CAE</span><span class="sxs-lookup"><span data-stu-id="bf2ec-210">0x800A0CAE</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-211">O objeto <strong>Connection</strong> não pode ser explicitamente fechado durante uma transação.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-211"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-212"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-212"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-213">3001</span><span class="sxs-lookup"><span data-stu-id="bf2ec-213">3001</span></span><br />
<span data-ttu-id="bf2ec-214">-2146825287</span><span class="sxs-lookup"><span data-stu-id="bf2ec-214">-2146825287</span></span><br />
<span data-ttu-id="bf2ec-215">0x800A0BB9</span><span class="sxs-lookup"><span data-stu-id="bf2ec-215">0x800A0BB9</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-216">Os argumentos são do tipo incorreto, estão fora do intervalo aceitável ou estão em conflito uns com os outros.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-216">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-217"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-217"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-218">3709</span><span class="sxs-lookup"><span data-stu-id="bf2ec-218">3709</span></span><br />
<span data-ttu-id="bf2ec-219">-2146824579</span><span class="sxs-lookup"><span data-stu-id="bf2ec-219">-2146824579</span></span><br />
<span data-ttu-id="bf2ec-220">0x800A0E7D</span><span class="sxs-lookup"><span data-stu-id="bf2ec-220">0x800A0E7D</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-221">A conexão não pode ser usada para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-221">The connection cannot be used to perform this operation.</span></span> <span data-ttu-id="bf2ec-222">Ela está fechada ou é inválida nesse contexto.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-222">It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-223"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-223"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-224">3708</span><span class="sxs-lookup"><span data-stu-id="bf2ec-224">3708</span></span><br />
<span data-ttu-id="bf2ec-225">-2146824580</span><span class="sxs-lookup"><span data-stu-id="bf2ec-225">-2146824580</span></span><br />
<span data-ttu-id="bf2ec-226">0x800A0E7C</span><span class="sxs-lookup"><span data-stu-id="bf2ec-226">0x800A0E7C</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-227">O objeto <strong>Parameter</strong> é definido de forma incorreta.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-227"><strong>Parameter</strong> object is improperly defined.</span></span> <span data-ttu-id="bf2ec-228">Foram fornecidas informações inconsistentes ou incompletas.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-228">Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-229"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-229"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-230">3714</span><span class="sxs-lookup"><span data-stu-id="bf2ec-230">3714</span></span><br />
<span data-ttu-id="bf2ec-231">-2146824574</span><span class="sxs-lookup"><span data-stu-id="bf2ec-231">-2146824574</span></span><br />
<span data-ttu-id="bf2ec-232">0x800A0E82</span><span class="sxs-lookup"><span data-stu-id="bf2ec-232">0x800A0E82</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-233">A transação de coordenação é inválida ou não foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-233">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-234"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-234"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-235">3729</span><span class="sxs-lookup"><span data-stu-id="bf2ec-235">3729</span></span><br />
<span data-ttu-id="bf2ec-236">-2146824559</span><span class="sxs-lookup"><span data-stu-id="bf2ec-236">-2146824559</span></span><br />
<span data-ttu-id="bf2ec-237">0x800A0E91</span><span class="sxs-lookup"><span data-stu-id="bf2ec-237">0x800A0E91</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-238">A URL contém caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-238">URL contains invalid characters.</span></span> <span data-ttu-id="bf2ec-239">Certifique-se de que a URL esteja digitada corretamente.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-239">Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-240"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-240"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-241">3265</span><span class="sxs-lookup"><span data-stu-id="bf2ec-241">3265</span></span><br />
<span data-ttu-id="bf2ec-242">-2146825023</span><span class="sxs-lookup"><span data-stu-id="bf2ec-242">-2146825023</span></span><br />
<span data-ttu-id="bf2ec-243">0x800A0CC1</span><span class="sxs-lookup"><span data-stu-id="bf2ec-243">0x800A0CC1</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-244">O item não pode ser localizado na coleção correspondente para o nome ou ordinal solicitado.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-244">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-245"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-245"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-246">3021</span><span class="sxs-lookup"><span data-stu-id="bf2ec-246">3021</span></span><br />
<span data-ttu-id="bf2ec-247">-2146825267</span><span class="sxs-lookup"><span data-stu-id="bf2ec-247">-2146825267</span></span><br />
<span data-ttu-id="bf2ec-248">0x800A0BCD</span><span class="sxs-lookup"><span data-stu-id="bf2ec-248">0x800A0BCD</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-249"><strong>BOF</strong> ou <strong>EOF</strong> é True ou o registro atual foi excluído.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-249">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted.</span></span> <span data-ttu-id="bf2ec-250">A operação solicitada requer um registro atual.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-250">Requested operation requires a current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-251"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-251"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-252">3715</span><span class="sxs-lookup"><span data-stu-id="bf2ec-252">3715</span></span><br />
<span data-ttu-id="bf2ec-253">-2146824573</span><span class="sxs-lookup"><span data-stu-id="bf2ec-253">-2146824573</span></span><br />
<span data-ttu-id="bf2ec-254">0x800A0E83</span><span class="sxs-lookup"><span data-stu-id="bf2ec-254">0x800A0E83</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-255">A operação não pode ser executada sozinha.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-255">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-256"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-256"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-257">3710</span><span class="sxs-lookup"><span data-stu-id="bf2ec-257">3710</span></span><br />
<span data-ttu-id="bf2ec-258">-2146824578</span><span class="sxs-lookup"><span data-stu-id="bf2ec-258">-2146824578</span></span><br />
<span data-ttu-id="bf2ec-259">0x800A0E7E</span><span class="sxs-lookup"><span data-stu-id="bf2ec-259">0x800A0E7E</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-260">A operação não pode ser executada durante o processamento do evento.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-260">Operation cannot be performed while processing event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-261"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-261"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-262">3704</span><span class="sxs-lookup"><span data-stu-id="bf2ec-262">3704</span></span><br />
<span data-ttu-id="bf2ec-263">-2146824584</span><span class="sxs-lookup"><span data-stu-id="bf2ec-263">-2146824584</span></span><br />
<span data-ttu-id="bf2ec-264">0x800A0E78</span><span class="sxs-lookup"><span data-stu-id="bf2ec-264">0x800A0E78</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-265">A operação não é permitida quando o objeto está fechado.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-265">Operation is not allowed when the object is closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-266"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-266"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-267">3367</span><span class="sxs-lookup"><span data-stu-id="bf2ec-267">3367</span></span><br />
<span data-ttu-id="bf2ec-268">-2146824921</span><span class="sxs-lookup"><span data-stu-id="bf2ec-268">-2146824921</span></span><br />
<span data-ttu-id="bf2ec-269">0x800A0D27</span><span class="sxs-lookup"><span data-stu-id="bf2ec-269">0x800A0D27</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-270">O objeto já está na coleção.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-270">Object is already in collection.</span></span> <span data-ttu-id="bf2ec-271">Não é possível anexá-lo.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-271">Cannot append.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-272"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-272"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-273">3420</span><span class="sxs-lookup"><span data-stu-id="bf2ec-273">3420</span></span><br />
<span data-ttu-id="bf2ec-274">-2146824868</span><span class="sxs-lookup"><span data-stu-id="bf2ec-274">-2146824868</span></span><br />
<span data-ttu-id="bf2ec-275">0x800A0D5C</span><span class="sxs-lookup"><span data-stu-id="bf2ec-275">0x800A0D5C</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-276">O objeto não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-276">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-277"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-277"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-278">3705</span><span class="sxs-lookup"><span data-stu-id="bf2ec-278">3705</span></span><br />
<span data-ttu-id="bf2ec-279">-2146824583</span><span class="sxs-lookup"><span data-stu-id="bf2ec-279">-2146824583</span></span><br />
<span data-ttu-id="bf2ec-280">0x800A0E79</span><span class="sxs-lookup"><span data-stu-id="bf2ec-280">0x800A0E79</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-281">A operação não é permitida quando o objeto está aberto.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-281">Operation is not allowed when the object is open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-282"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-282"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-283">3002</span><span class="sxs-lookup"><span data-stu-id="bf2ec-283">3002</span></span><br />
<span data-ttu-id="bf2ec-284">-2146825286</span><span class="sxs-lookup"><span data-stu-id="bf2ec-284">-2146825286</span></span><br />
<span data-ttu-id="bf2ec-285">0x800A0BBA</span><span class="sxs-lookup"><span data-stu-id="bf2ec-285">0x800A0BBA</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-286">O arquivo não pôde ser aberto.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-286">File could not be opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-287"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-287"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-288">3712</span><span class="sxs-lookup"><span data-stu-id="bf2ec-288">3712</span></span><br />
<span data-ttu-id="bf2ec-289">-2146824576</span><span class="sxs-lookup"><span data-stu-id="bf2ec-289">-2146824576</span></span><br />
<span data-ttu-id="bf2ec-290">0x800A0E80</span><span class="sxs-lookup"><span data-stu-id="bf2ec-290">0x800A0E80</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-291">A operação foi cancelada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-291">Operation has been cancelled by the user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-292"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-292"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-293">3734</span><span class="sxs-lookup"><span data-stu-id="bf2ec-293">3734</span></span><br />
<span data-ttu-id="bf2ec-294">-2146824554</span><span class="sxs-lookup"><span data-stu-id="bf2ec-294">-2146824554</span></span><br />
<span data-ttu-id="bf2ec-295">0x800A0E96</span><span class="sxs-lookup"><span data-stu-id="bf2ec-295">0x800A0E96</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-296">A operação não pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-296">Operation cannot be performed.</span></span> <span data-ttu-id="bf2ec-297">O provedor não pode obter espaço de repositório suficiente.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-297">Provider cannot obtain enough storage space.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-298"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-298"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-299">3720</span><span class="sxs-lookup"><span data-stu-id="bf2ec-299">3720</span></span><br />
<span data-ttu-id="bf2ec-300">-2146824568</span><span class="sxs-lookup"><span data-stu-id="bf2ec-300">-2146824568</span></span><br />
<span data-ttu-id="bf2ec-301">0x800A0E88</span><span class="sxs-lookup"><span data-stu-id="bf2ec-301">0x800A0E88</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-302">Permissão insuficiente impede escrever no campo.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-302">Insufficent permission prevents writing to the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-303"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-303"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-304">3000</span><span class="sxs-lookup"><span data-stu-id="bf2ec-304">3000</span></span><br />
<span data-ttu-id="bf2ec-305">-2146825288</span><span class="sxs-lookup"><span data-stu-id="bf2ec-305">-2146825288</span></span><br />
<span data-ttu-id="bf2ec-306">0x800A0BB8</span><span class="sxs-lookup"><span data-stu-id="bf2ec-306">0x800A0BB8</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-307">O provedor falhou em executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-307">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-308"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-308"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-309">3706</span><span class="sxs-lookup"><span data-stu-id="bf2ec-309">3706</span></span><br />
<span data-ttu-id="bf2ec-310">-2146824582</span><span class="sxs-lookup"><span data-stu-id="bf2ec-310">-2146824582</span></span><br />
<span data-ttu-id="bf2ec-311">0x800A0E7A</span><span class="sxs-lookup"><span data-stu-id="bf2ec-311">0x800A0E7A</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-312">O provedor não pode ser localizado.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-312">Provider cannot be found.</span></span> <span data-ttu-id="bf2ec-313">Ele não pode ser instalado corretamente.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-313">It may not be properly installed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-314"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-314"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-315">3003</span><span class="sxs-lookup"><span data-stu-id="bf2ec-315">3003</span></span><br />
<span data-ttu-id="bf2ec-316">-2146825285</span><span class="sxs-lookup"><span data-stu-id="bf2ec-316">-2146825285</span></span><br />
<span data-ttu-id="bf2ec-317">0x800A0BBB</span><span class="sxs-lookup"><span data-stu-id="bf2ec-317">0x800A0BBB</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-318">O arquivo não pôde ser lido.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-318">File could not be read.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-319"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-319"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-320">3731</span><span class="sxs-lookup"><span data-stu-id="bf2ec-320">3731</span></span><br />
<span data-ttu-id="bf2ec-321">-2146824557</span><span class="sxs-lookup"><span data-stu-id="bf2ec-321">-2146824557</span></span><br />
<span data-ttu-id="bf2ec-322">0x800A0E93</span><span class="sxs-lookup"><span data-stu-id="bf2ec-322">0x800A0E93</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-323">A operação Copy não pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-323">Copy operation cannot be performed.</span></span> <span data-ttu-id="bf2ec-324">O objeto nomeado pela URL de destino já existe.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-324">Object named by destination URL already exists.</span></span> <span data-ttu-id="bf2ec-325">Especifique <strong>adCopyOverwrite</strong> para substituir o objeto.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-325">Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-326"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-326"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-327">3730</span><span class="sxs-lookup"><span data-stu-id="bf2ec-327">3730</span></span><br />
<span data-ttu-id="bf2ec-328">-2146824558</span><span class="sxs-lookup"><span data-stu-id="bf2ec-328">-2146824558</span></span><br />
<span data-ttu-id="bf2ec-329">0x800A0E92</span><span class="sxs-lookup"><span data-stu-id="bf2ec-329">0x800A0E92</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-p115">O objeto representado pela URL especificada está bloqueado por um ou mais processos diferentes. Aguarde até que o processo seja finalizado e tente executar a operação novamente.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-p115">Object represented by the specified URL is locked by one or more other processes. Wait until the process has finished and attempt the operation again.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-332"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-332"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-333">3735</span><span class="sxs-lookup"><span data-stu-id="bf2ec-333">3735</span></span><br />
<span data-ttu-id="bf2ec-334">-2146824553</span><span class="sxs-lookup"><span data-stu-id="bf2ec-334">-2146824553</span></span><br />
<span data-ttu-id="bf2ec-335">0x800A0E97</span><span class="sxs-lookup"><span data-stu-id="bf2ec-335">0x800A0E97</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-336">A URL de origem ou de destino está fora do escopo do registro atual.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-336">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-337"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-337"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-338">3722</span><span class="sxs-lookup"><span data-stu-id="bf2ec-338">3722</span></span><br />
<span data-ttu-id="bf2ec-339">-2146824566</span><span class="sxs-lookup"><span data-stu-id="bf2ec-339">-2146824566</span></span><br />
<span data-ttu-id="bf2ec-340">0x800A0E8A</span><span class="sxs-lookup"><span data-stu-id="bf2ec-340">0x800A0E8A</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-341">O valor dos dados está em conflito com o tipo de dados ou com as restrições do campo.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-341">Data value conflicts with the data type or constraints of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-342"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-342"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-343">3723</span><span class="sxs-lookup"><span data-stu-id="bf2ec-343">3723</span></span><br />
<span data-ttu-id="bf2ec-344">-2146824565</span><span class="sxs-lookup"><span data-stu-id="bf2ec-344">-2146824565</span></span><br />
<span data-ttu-id="bf2ec-345">0x800A0E8B</span><span class="sxs-lookup"><span data-stu-id="bf2ec-345">0x800A0E8B</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-346">A conversão falhou porque o valor dos dados era assinado e o tipo de dados do campo utilizado pelo provedor não era.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-346">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-347"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-347"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-348">3713</span><span class="sxs-lookup"><span data-stu-id="bf2ec-348">3713</span></span><br />
<span data-ttu-id="bf2ec-349">-2146824575</span><span class="sxs-lookup"><span data-stu-id="bf2ec-349">-2146824575</span></span><br />
<span data-ttu-id="bf2ec-350">0x800A0E81</span><span class="sxs-lookup"><span data-stu-id="bf2ec-350">0x800A0E81</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-351">A operação não pode ser executado durante uma conexão assíncrona.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-351">Operation cannot be performed while connecting aynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-352"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-352"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-353">3711</span><span class="sxs-lookup"><span data-stu-id="bf2ec-353">3711</span></span><br />
<span data-ttu-id="bf2ec-354">-2146824577</span><span class="sxs-lookup"><span data-stu-id="bf2ec-354">-2146824577</span></span><br />
<span data-ttu-id="bf2ec-355">0x800A0E7F</span><span class="sxs-lookup"><span data-stu-id="bf2ec-355">0x800A0E7F</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-356">A operação não pode ser executada durante uma execução assíncrona.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-356">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-357"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-357"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-358">3728</span><span class="sxs-lookup"><span data-stu-id="bf2ec-358">3728</span></span><br />
<span data-ttu-id="bf2ec-359">-2146824560</span><span class="sxs-lookup"><span data-stu-id="bf2ec-359">-2146824560</span></span><br />
<span data-ttu-id="bf2ec-360">0x800A0E90</span><span class="sxs-lookup"><span data-stu-id="bf2ec-360">0x800A0E90</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-361">As permissões são insuficientes para acessar a árvore ou a subárvore.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-361">Permissions are insufficient to access tree or subtree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-362"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-362"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-363">3736</span><span class="sxs-lookup"><span data-stu-id="bf2ec-363">3736</span></span><br />
<span data-ttu-id="bf2ec-364">-2146824552</span><span class="sxs-lookup"><span data-stu-id="bf2ec-364">-2146824552</span></span><br />
<span data-ttu-id="bf2ec-365">0x800A0E98</span><span class="sxs-lookup"><span data-stu-id="bf2ec-365">0x800A0E98</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-366">Houve falha na conclusão da operação, e o status não está disponível.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-366">Operation failed to complete and the status is unavailable.</span></span> <span data-ttu-id="bf2ec-367">O campo pode estar indisponível ou a operação não foi repetida.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-367">The field may be unavailable or the operation was not attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-368"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-368"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-369">3716</span><span class="sxs-lookup"><span data-stu-id="bf2ec-369">3716</span></span><br />
<span data-ttu-id="bf2ec-370">-2146824572</span><span class="sxs-lookup"><span data-stu-id="bf2ec-370">-2146824572</span></span><br />
<span data-ttu-id="bf2ec-371">0x800A0E84</span><span class="sxs-lookup"><span data-stu-id="bf2ec-371">0x800A0E84</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-372">As configurações de segurança nesse computador proíbem o acesso à fonte de dados em outro domínio.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-372">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-373"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-373"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-374">3727</span><span class="sxs-lookup"><span data-stu-id="bf2ec-374">3727</span></span><br />
<span data-ttu-id="bf2ec-375">-2146824561</span><span class="sxs-lookup"><span data-stu-id="bf2ec-375">-2146824561</span></span><br />
<span data-ttu-id="bf2ec-376">0x800A0E8F</span><span class="sxs-lookup"><span data-stu-id="bf2ec-376">0x800A0E8F</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-377">A URL de origem ou o pai da URL de destino não existe.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-377">Either the source URL or the parent of the destination URL does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-378"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-378"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-379">3737</span><span class="sxs-lookup"><span data-stu-id="bf2ec-379">3737</span></span><br />
<span data-ttu-id="bf2ec-380">-2146824551</span><span class="sxs-lookup"><span data-stu-id="bf2ec-380">-2146824551</span></span><br />
<span data-ttu-id="bf2ec-381">0x800A0E99</span><span class="sxs-lookup"><span data-stu-id="bf2ec-381">0x800A0E99</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-382">O registro chamado por essa URL não existe.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-382">Record named by this URL does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-383"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-383"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-384">3733</span><span class="sxs-lookup"><span data-stu-id="bf2ec-384">3733</span></span><br />
<span data-ttu-id="bf2ec-385">-2146824555</span><span class="sxs-lookup"><span data-stu-id="bf2ec-385">-2146824555</span></span><br />
<span data-ttu-id="bf2ec-386">0x800A0E95</span><span class="sxs-lookup"><span data-stu-id="bf2ec-386">0x800A0E95</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-387">O provedor não pode localizar o dispositivo de repositório indicado pela URL.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-387">Provider cannot locate the storage device indicated by the URL.</span></span> <span data-ttu-id="bf2ec-388">Certifique-se de que a URL esteja digitada corretamente.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-388">Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-389"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-389"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-390">3004</span><span class="sxs-lookup"><span data-stu-id="bf2ec-390">3004</span></span><br />
<span data-ttu-id="bf2ec-391">-2146825284</span><span class="sxs-lookup"><span data-stu-id="bf2ec-391">-2146825284</span></span><br />
<span data-ttu-id="bf2ec-392">0x800A0BBC</span><span class="sxs-lookup"><span data-stu-id="bf2ec-392">0x800A0BBC</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-393">Falha ao gravar no arquivo.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-393">Write to file failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-394"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-394"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-395">3717</span><span class="sxs-lookup"><span data-stu-id="bf2ec-395">3717</span></span><br />
<span data-ttu-id="bf2ec-396">-2146824571</span><span class="sxs-lookup"><span data-stu-id="bf2ec-396">-2146824571</span></span><br />
<span data-ttu-id="bf2ec-397">0x800A0E85</span><span class="sxs-lookup"><span data-stu-id="bf2ec-397">0x800A0E85</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-398">Para uso interno apenas.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-398">For internal use only.</span></span> <span data-ttu-id="bf2ec-399">Não use.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-399">Don't use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-400"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="bf2ec-400"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="bf2ec-401">3718</span><span class="sxs-lookup"><span data-stu-id="bf2ec-401">3718</span></span><br />
<span data-ttu-id="bf2ec-402">-2146824570</span><span class="sxs-lookup"><span data-stu-id="bf2ec-402">-2146824570</span></span><br />
<span data-ttu-id="bf2ec-403">0x800A0E86</span><span class="sxs-lookup"><span data-stu-id="bf2ec-403">0x800A0E86</span></span></p></td>
<td><p><span data-ttu-id="bf2ec-404">Para uso interno apenas.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-404">For internal use only.</span></span> <span data-ttu-id="bf2ec-405">Não use.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-405">Don't use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="bf2ec-406">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="bf2ec-406">ADO/WFC equivalent</span></span>

<span data-ttu-id="bf2ec-407">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="bf2ec-407">Package: **com.ms.wfc.data**</span></span>

<span data-ttu-id="bf2ec-408">Somente os seguintes subconjuntos de equivalentes do ADO/WFC estão definidos.</span><span class="sxs-lookup"><span data-stu-id="bf2ec-408">Only the following subsets of ADO/WFC equivalents are defined.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf2ec-409">Constant</span><span class="sxs-lookup"><span data-stu-id="bf2ec-409">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-410">AdoEnums. Errorvalue. BOUNDTOCOMMAND</span><span class="sxs-lookup"><span data-stu-id="bf2ec-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-411">AdoEnums. Errorvalue. dataCONVERSION</span><span class="sxs-lookup"><span data-stu-id="bf2ec-411">AdoEnums.ErrorValue.DATACONVERSION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-412">AdoEnums. Errorvalue. FEATURENOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="bf2ec-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-413">AdoEnums. Errorvalue. ILLEGALOPERATION</span><span class="sxs-lookup"><span data-stu-id="bf2ec-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-414">AdoEnums. Errorvalue. inTRANSACTION</span><span class="sxs-lookup"><span data-stu-id="bf2ec-414">AdoEnums.ErrorValue.INTRANSACTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-415">AdoEnums. Errorvalue. INVALIDARGUMENT</span><span class="sxs-lookup"><span data-stu-id="bf2ec-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-416">AdoEnums. Errorvalue. INVALIDCONNECTION</span><span class="sxs-lookup"><span data-stu-id="bf2ec-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-417">AdoEnums. Errorvalue. INVALIDPARAMINFO</span><span class="sxs-lookup"><span data-stu-id="bf2ec-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-418">AdoEnums. Errorvalue. ITEMNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="bf2ec-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-419">AdoEnums. Errorvalue. NOCURRENTRECORD</span><span class="sxs-lookup"><span data-stu-id="bf2ec-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-420">AdoEnums. Errorvalue. não está em execução</span><span class="sxs-lookup"><span data-stu-id="bf2ec-420">AdoEnums.ErrorValue.NOTEXECUTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-421">AdoEnums. Errorvalue. NOTREENTRANT</span><span class="sxs-lookup"><span data-stu-id="bf2ec-421">AdoEnums.ErrorValue.NOTREENTRANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-422">AdoEnums. Errorvalue. objectCLOSEd</span><span class="sxs-lookup"><span data-stu-id="bf2ec-422">AdoEnums.ErrorValue.OBJECTCLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-423">AdoEnums. Errorvalue. OBJECTINCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="bf2ec-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-424">AdoEnums. Errorvalue. objectNOTSET</span><span class="sxs-lookup"><span data-stu-id="bf2ec-424">AdoEnums.ErrorValue.OBJECTNOTSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-425">AdoEnums. Errorvalue. objectOPEN</span><span class="sxs-lookup"><span data-stu-id="bf2ec-425">AdoEnums.ErrorValue.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-426">AdoEnums. Errorvalue. OPERATIONCANCELLED</span><span class="sxs-lookup"><span data-stu-id="bf2ec-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-427">AdoEnums. Errorvalue. PROVIDERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="bf2ec-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-428">AdoEnums. Errorvalue. STILLCONNECTING</span><span class="sxs-lookup"><span data-stu-id="bf2ec-428">AdoEnums.ErrorValue.STILLCONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf2ec-429">AdoEnums. Errorvalue. STILLEXECUTING</span><span class="sxs-lookup"><span data-stu-id="bf2ec-429">AdoEnums.ErrorValue.STILLEXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf2ec-430">AdoEnums. Errorvalue. UNSAFEOPERATION</span><span class="sxs-lookup"><span data-stu-id="bf2ec-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span></span></p></td>
</tr>
</tbody>
</table>

