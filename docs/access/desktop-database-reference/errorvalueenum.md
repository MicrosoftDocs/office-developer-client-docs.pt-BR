---
title: ErrorValueEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ErrorValueEnum
ms:assetid: 2af99f32-6004-1225-367c-45d693f447b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249058(v=office.15)
ms:contentKeyID: 48543921
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 23040dd7311d659fb5e3308053a3bcdc8aa27fe0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879862"
---
# <a name="errorvalueenum"></a><span data-ttu-id="840b2-102">ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="840b2-102">ErrorValueEnum</span></span>

<span data-ttu-id="840b2-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="840b2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="840b2-104">Especifica o tipo de erro de tempo de execução do ADO.</span><span class="sxs-lookup"><span data-stu-id="840b2-104">Specifies the type of ADO run-time error.</span></span>

<span data-ttu-id="840b2-105">Três formatos de número de erro são listados:</span><span class="sxs-lookup"><span data-stu-id="840b2-105">Three forms of the error number are listed:</span></span>

- <span data-ttu-id="840b2-p101">Decimal positivo  os dois bytes baixos de um número completo em formato decimal. Esse número é exibido na caixa de diálogo de erros padrão do Visual Basic. Por exemplo, Erro de tempo de execução '3707'.</span><span class="sxs-lookup"><span data-stu-id="840b2-p101">Positive decimal — the low two bytes of the full number in decimal format. This number is displayed in the default Visual Basic error message dialog box. For example, Run-time error '3707'.</span></span>

- <span data-ttu-id="840b2-109">Decimal negativo  A conversão decimal de um número completo do erro.</span><span class="sxs-lookup"><span data-stu-id="840b2-109">Negative decimal — The decimal translation of the full error number.</span></span>

- <span data-ttu-id="840b2-p102">Hexadecimal  — A representação hexadecimal do número completo do erro. O código de recurso do Windows está no quarto dígito. O código de recurso para números de erro do ADO é *A*. Por exemplo: 0x800***A***0E7B.</span><span class="sxs-lookup"><span data-stu-id="840b2-p102">Hexadecimal — The hexadecimal representation of the full error number. The Windows facility code is in the fourth digit. The facility code for ADO error numbers is *A*. For example: 0x800***A***0E7B.</span></span>

> [!NOTE]
> <span data-ttu-id="840b2-113">Erros do OLE DB podem ser passados ao seu aplicativo do ADO.</span><span class="sxs-lookup"><span data-stu-id="840b2-113">OLE DB errors may be passed to your ADO application.</span></span> <span data-ttu-id="840b2-114">Normalmente, esses itens podem ser identificados por um código de instalações do Windows de *4*.</span><span class="sxs-lookup"><span data-stu-id="840b2-114">Typically, these can be identified by a Windows facility code of *4*.</span></span> <span data-ttu-id="840b2-115">Por exemplo, _**4**0x800_ … Para obter mais informações sobre esses números, consulte o capítulo 16 do *referência do programador DB OLE.*</span><span class="sxs-lookup"><span data-stu-id="840b2-115">For example, 0x800_**4**_.... For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="840b2-116">Constant</span><span class="sxs-lookup"><span data-stu-id="840b2-116">Constant</span></span></p></th>
<th><p><span data-ttu-id="840b2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="840b2-117">Value</span></span></p></th>
<th><p><span data-ttu-id="840b2-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="840b2-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="840b2-119"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-119"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-120">3707</span><span class="sxs-lookup"><span data-stu-id="840b2-120">3707</span></span><br />
<span data-ttu-id="840b2-121">-2146824581</span><span class="sxs-lookup"><span data-stu-id="840b2-121">-2146824581</span></span><br />
<span data-ttu-id="840b2-122">0x800A0E7B</span><span class="sxs-lookup"><span data-stu-id="840b2-122">0x800A0E7B</span></span></p></td>
<td><p><span data-ttu-id="840b2-123">Não pode alterar a propriedade <strong>ActiveConnection</strong> de um objeto <strong>Recordset</strong> que tem um objeto <strong>Command</strong> como sua fonte.</span><span class="sxs-lookup"><span data-stu-id="840b2-123">Cannot change the <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object which has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-124"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-124"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-125">3732</span><span class="sxs-lookup"><span data-stu-id="840b2-125">3732</span></span><br />
<span data-ttu-id="840b2-126">-2146824556</span><span class="sxs-lookup"><span data-stu-id="840b2-126">-2146824556</span></span><br />
<span data-ttu-id="840b2-127">0x800A0E94</span><span class="sxs-lookup"><span data-stu-id="840b2-127">0x800A0E94</span></span></p></td>
<td><p><span data-ttu-id="840b2-128">O servidor não pode concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="840b2-128">Server cannot complete the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-129"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-129"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-130">3748</span><span class="sxs-lookup"><span data-stu-id="840b2-130">3748</span></span><br />
<span data-ttu-id="840b2-131">-2146824540</span><span class="sxs-lookup"><span data-stu-id="840b2-131">-2146824540</span></span><br />
<span data-ttu-id="840b2-132">0x800A0EA4</span><span class="sxs-lookup"><span data-stu-id="840b2-132">0x800A0EA4</span></span></p></td>
<td><p><span data-ttu-id="840b2-p104">A conexão foi negada. A nova conexão solicitada tem diferentes recursos em relação àquela que está em uso.</span><span class="sxs-lookup"><span data-stu-id="840b2-p104">Connection was denied. New connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-135"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-135"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-136">3220</span><span class="sxs-lookup"><span data-stu-id="840b2-136">3220</span></span><br />
<span data-ttu-id="840b2-137">-2146825068</span><span class="sxs-lookup"><span data-stu-id="840b2-137">-2146825068</span></span><br />
<span data-ttu-id="840b2-138">0X800A0C94</span><span class="sxs-lookup"><span data-stu-id="840b2-138">0X800A0C94</span></span></p></td>
<td><p><span data-ttu-id="840b2-139">O provedor designado é diferente daquele que está em uso.</span><span class="sxs-lookup"><span data-stu-id="840b2-139">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-140"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-140"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-141">3724</span><span class="sxs-lookup"><span data-stu-id="840b2-141">3724</span></span><br />
<span data-ttu-id="840b2-142">-2146824564</span><span class="sxs-lookup"><span data-stu-id="840b2-142">-2146824564</span></span><br />
<span data-ttu-id="840b2-143">0x800A0E8C</span><span class="sxs-lookup"><span data-stu-id="840b2-143">0x800A0E8C</span></span></p></td>
<td><p><span data-ttu-id="840b2-p105">O valor dos dados não pode ser convertido por razões diferentes de incompatibilidade assinada ou estouro de dados. Por exemplo, a conversão truncaria os dados.</span><span class="sxs-lookup"><span data-stu-id="840b2-p105">Data value cannot be converted for reasons other than sign mismatch or data overflow. For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-146"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-146"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-147">3725</span><span class="sxs-lookup"><span data-stu-id="840b2-147">3725</span></span><br />
<span data-ttu-id="840b2-148">-2146824563</span><span class="sxs-lookup"><span data-stu-id="840b2-148">-2146824563</span></span><br />
<span data-ttu-id="840b2-149">0x800A0E8D</span><span class="sxs-lookup"><span data-stu-id="840b2-149">0x800A0E8D</span></span></p></td>
<td><p><span data-ttu-id="840b2-150">O valor dos dados não pode ser definido ou recuperado porque o tipo de dados do campo é desconhecido ou o provedor tem recursos insuficientes para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="840b2-150">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-151"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-151"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-152">3747</span><span class="sxs-lookup"><span data-stu-id="840b2-152">3747</span></span><br />
<span data-ttu-id="840b2-153">-2146824541</span><span class="sxs-lookup"><span data-stu-id="840b2-153">-2146824541</span></span><br />
<span data-ttu-id="840b2-154">0x800A0EA3</span><span class="sxs-lookup"><span data-stu-id="840b2-154">0x800A0EA3</span></span></p></td>
<td><p><span data-ttu-id="840b2-155">A operação requer um <strong>ParentCatalog</strong> válido.</span><span class="sxs-lookup"><span data-stu-id="840b2-155">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-156"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-156"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-157">3726</span><span class="sxs-lookup"><span data-stu-id="840b2-157">3726</span></span><br />
<span data-ttu-id="840b2-158">-2146824562</span><span class="sxs-lookup"><span data-stu-id="840b2-158">-2146824562</span></span><br />
<span data-ttu-id="840b2-159">0x800A0E8E</span><span class="sxs-lookup"><span data-stu-id="840b2-159">0x800A0E8E</span></span></p></td>
<td><p><span data-ttu-id="840b2-160">O registro não contém esse campo.</span><span class="sxs-lookup"><span data-stu-id="840b2-160">Record does not contain this field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-161"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-161"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-162">3421</span><span class="sxs-lookup"><span data-stu-id="840b2-162">3421</span></span><br />
<span data-ttu-id="840b2-163">-2146824867</span><span class="sxs-lookup"><span data-stu-id="840b2-163">-2146824867</span></span><br />
<span data-ttu-id="840b2-164">0x800A0D5D</span><span class="sxs-lookup"><span data-stu-id="840b2-164">0x800A0D5D</span></span></p></td>
<td><p><span data-ttu-id="840b2-165">O aplicativo usa um valor de tipo incorreto para a operação atual.</span><span class="sxs-lookup"><span data-stu-id="840b2-165">Application uses a value of the wrong type for the current operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-166"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-166"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-167">3721</span><span class="sxs-lookup"><span data-stu-id="840b2-167">3721</span></span><br />
<span data-ttu-id="840b2-168">-2146824567</span><span class="sxs-lookup"><span data-stu-id="840b2-168">-2146824567</span></span><br />
<span data-ttu-id="840b2-169">0x800A0E89</span><span class="sxs-lookup"><span data-stu-id="840b2-169">0x800A0E89</span></span></p></td>
<td><p><span data-ttu-id="840b2-170">O valor dos dados é muito grande para ser representado pelo tipo de dados do campo.</span><span class="sxs-lookup"><span data-stu-id="840b2-170">Data value is too large to be represented by the field data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-171"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-171"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-172">3738</span><span class="sxs-lookup"><span data-stu-id="840b2-172">3738</span></span><br />
<span data-ttu-id="840b2-173">-2146824550</span><span class="sxs-lookup"><span data-stu-id="840b2-173">-2146824550</span></span><br />
<span data-ttu-id="840b2-174">0x800A0E9A</span><span class="sxs-lookup"><span data-stu-id="840b2-174">0x800A0E9A</span></span></p></td>
<td><p><span data-ttu-id="840b2-175">A URL do objeto a ser excluído está fora do escopo do registro atual.</span><span class="sxs-lookup"><span data-stu-id="840b2-175">URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-176"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-176"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-177">3750</span><span class="sxs-lookup"><span data-stu-id="840b2-177">3750</span></span><br />
<span data-ttu-id="840b2-178">-2146824538</span><span class="sxs-lookup"><span data-stu-id="840b2-178">-2146824538</span></span><br />
<span data-ttu-id="840b2-179">0x800A0EA6</span><span class="sxs-lookup"><span data-stu-id="840b2-179">0x800A0EA6</span></span></p></td>
<td><p><span data-ttu-id="840b2-180">O provedor não oferece suporte a restrições de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="840b2-180">Provider does not support sharing restrictions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-181"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-181"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-182">3751</span><span class="sxs-lookup"><span data-stu-id="840b2-182">3751</span></span><br />
<span data-ttu-id="840b2-183">-2146824537</span><span class="sxs-lookup"><span data-stu-id="840b2-183">-2146824537</span></span><br />
<span data-ttu-id="840b2-184">0x800A0EA7</span><span class="sxs-lookup"><span data-stu-id="840b2-184">0x800A0EA7</span></span></p></td>
<td><p><span data-ttu-id="840b2-185">O provedor não oferece suporte ao tipo solicitado de restrição de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="840b2-185">Provider does not support the requested kind of sharing restriction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-186"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-186"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-187">3251</span><span class="sxs-lookup"><span data-stu-id="840b2-187">3251</span></span><br />
<span data-ttu-id="840b2-188">-2146825037</span><span class="sxs-lookup"><span data-stu-id="840b2-188">-2146825037</span></span><br />
<span data-ttu-id="840b2-189">0x800A0CB3</span><span class="sxs-lookup"><span data-stu-id="840b2-189">0x800A0CB3</span></span></p></td>
<td><p><span data-ttu-id="840b2-190">O objeto ou o provedor não pode executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="840b2-190">Object or provider is not capable of performing requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-191"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-191"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-192">3749</span><span class="sxs-lookup"><span data-stu-id="840b2-192">3749</span></span><br />
<span data-ttu-id="840b2-193">-2146824539</span><span class="sxs-lookup"><span data-stu-id="840b2-193">-2146824539</span></span><br />
<span data-ttu-id="840b2-194">0x800A0EA5</span><span class="sxs-lookup"><span data-stu-id="840b2-194">0x800A0EA5</span></span></p></td>
<td><p><span data-ttu-id="840b2-p106">A atualização dos campos falhou. Para obter outras informações, analise a propriedade <strong>Status</strong> dos objetos de campo individuais.</span><span class="sxs-lookup"><span data-stu-id="840b2-p106">Fields update failed. For further information, examine the <strong>Status</strong> property of individual field objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-197"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-197"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-198">3219</span><span class="sxs-lookup"><span data-stu-id="840b2-198">3219</span></span><br />
<span data-ttu-id="840b2-199">-2146825069</span><span class="sxs-lookup"><span data-stu-id="840b2-199">-2146825069</span></span><br />
<span data-ttu-id="840b2-200">0x800A0C93</span><span class="sxs-lookup"><span data-stu-id="840b2-200">0x800A0C93</span></span></p></td>
<td><p><span data-ttu-id="840b2-201">A operação não é permitida nesse contexto.</span><span class="sxs-lookup"><span data-stu-id="840b2-201">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-202"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-202"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-203">3719</span><span class="sxs-lookup"><span data-stu-id="840b2-203">3719</span></span><br />
<span data-ttu-id="840b2-204">-2146824569</span><span class="sxs-lookup"><span data-stu-id="840b2-204">-2146824569</span></span><br />
<span data-ttu-id="840b2-205">0x800A0E87</span><span class="sxs-lookup"><span data-stu-id="840b2-205">0x800A0E87</span></span></p></td>
<td><p><span data-ttu-id="840b2-206">O valor de dados está em conflito com as restrições de integridade do campo.</span><span class="sxs-lookup"><span data-stu-id="840b2-206">Data value conflicts with the integrity constraints of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-207"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-207"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-208">3246</span><span class="sxs-lookup"><span data-stu-id="840b2-208">3246</span></span><br />
<span data-ttu-id="840b2-209">-2146825042</span><span class="sxs-lookup"><span data-stu-id="840b2-209">-2146825042</span></span><br />
<span data-ttu-id="840b2-210">0x800A0CAE</span><span class="sxs-lookup"><span data-stu-id="840b2-210">0x800A0CAE</span></span></p></td>
<td><p><span data-ttu-id="840b2-211">O objeto <strong>Connection</strong> não pode ser explicitamente fechado durante uma transação.</span><span class="sxs-lookup"><span data-stu-id="840b2-211"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-212"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-212"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-213">3001</span><span class="sxs-lookup"><span data-stu-id="840b2-213">3001</span></span><br />
<span data-ttu-id="840b2-214">-2146825287</span><span class="sxs-lookup"><span data-stu-id="840b2-214">-2146825287</span></span><br />
<span data-ttu-id="840b2-215">0x800A0BB9</span><span class="sxs-lookup"><span data-stu-id="840b2-215">0x800A0BB9</span></span></p></td>
<td><p><span data-ttu-id="840b2-216">Os argumentos são do tipo incorreto, estão fora do intervalo aceitável ou estão em conflito uns com os outros.</span><span class="sxs-lookup"><span data-stu-id="840b2-216">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-217"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-217"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-218">3709</span><span class="sxs-lookup"><span data-stu-id="840b2-218">3709</span></span><br />
<span data-ttu-id="840b2-219">-2146824579</span><span class="sxs-lookup"><span data-stu-id="840b2-219">-2146824579</span></span><br />
<span data-ttu-id="840b2-220">0x800A0E7D</span><span class="sxs-lookup"><span data-stu-id="840b2-220">0x800A0E7D</span></span></p></td>
<td><p><span data-ttu-id="840b2-p107">A conexão não pode ser usada para executar essa operação. Ela está fechada ou é inválida nesse contexto.</span><span class="sxs-lookup"><span data-stu-id="840b2-p107">The connection cannot be used to perform this operation. It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-223"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-223"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-224">3708</span><span class="sxs-lookup"><span data-stu-id="840b2-224">3708</span></span><br />
<span data-ttu-id="840b2-225">-2146824580</span><span class="sxs-lookup"><span data-stu-id="840b2-225">-2146824580</span></span><br />
<span data-ttu-id="840b2-226">0x800A0E7C</span><span class="sxs-lookup"><span data-stu-id="840b2-226">0x800A0E7C</span></span></p></td>
<td><p><span data-ttu-id="840b2-p108">O objeto <strong>Parameter</strong> é definido de forma incorreta. Foram fornecidas informações inconsistentes ou incompletas.</span><span class="sxs-lookup"><span data-stu-id="840b2-p108"><strong>Parameter</strong> object is improperly defined. Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-229"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-229"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-230">3714</span><span class="sxs-lookup"><span data-stu-id="840b2-230">3714</span></span><br />
<span data-ttu-id="840b2-231">-2146824574</span><span class="sxs-lookup"><span data-stu-id="840b2-231">-2146824574</span></span><br />
<span data-ttu-id="840b2-232">0x800A0E82</span><span class="sxs-lookup"><span data-stu-id="840b2-232">0x800A0E82</span></span></p></td>
<td><p><span data-ttu-id="840b2-233">A transação de coordenação é inválida ou não foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="840b2-233">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-234"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-234"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-235">3729</span><span class="sxs-lookup"><span data-stu-id="840b2-235">3729</span></span><br />
<span data-ttu-id="840b2-236">-2146824559</span><span class="sxs-lookup"><span data-stu-id="840b2-236">-2146824559</span></span><br />
<span data-ttu-id="840b2-237">0x800A0E91</span><span class="sxs-lookup"><span data-stu-id="840b2-237">0x800A0E91</span></span></p></td>
<td><p><span data-ttu-id="840b2-p109">A URL contém caracteres inválidos. Certifique-se de que a URL esteja digitada corretamente.</span><span class="sxs-lookup"><span data-stu-id="840b2-p109">URL contains invalid characters. Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-240"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-240"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-241">3265</span><span class="sxs-lookup"><span data-stu-id="840b2-241">3265</span></span><br />
<span data-ttu-id="840b2-242">-2146825023</span><span class="sxs-lookup"><span data-stu-id="840b2-242">-2146825023</span></span><br />
<span data-ttu-id="840b2-243">0x800A0CC1</span><span class="sxs-lookup"><span data-stu-id="840b2-243">0x800A0CC1</span></span></p></td>
<td><p><span data-ttu-id="840b2-244">O item não pode ser localizado na coleção correspondente para o nome ou ordinal solicitado.</span><span class="sxs-lookup"><span data-stu-id="840b2-244">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-245"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-245"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-246">3021</span><span class="sxs-lookup"><span data-stu-id="840b2-246">3021</span></span><br />
<span data-ttu-id="840b2-247">-2146825267</span><span class="sxs-lookup"><span data-stu-id="840b2-247">-2146825267</span></span><br />
<span data-ttu-id="840b2-248">0x800A0BCD</span><span class="sxs-lookup"><span data-stu-id="840b2-248">0x800A0BCD</span></span></p></td>
<td><p><span data-ttu-id="840b2-p110"><strong>BOF</strong> ou <strong>EOF</strong> é True ou o registro atual foi excluído. A operação solicitada requer um registro atual.</span><span class="sxs-lookup"><span data-stu-id="840b2-p110">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted. Requested operation requires a current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-251"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-251"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-252">3715</span><span class="sxs-lookup"><span data-stu-id="840b2-252">3715</span></span><br />
<span data-ttu-id="840b2-253">-2146824573</span><span class="sxs-lookup"><span data-stu-id="840b2-253">-2146824573</span></span><br />
<span data-ttu-id="840b2-254">0x800A0E83</span><span class="sxs-lookup"><span data-stu-id="840b2-254">0x800A0E83</span></span></p></td>
<td><p><span data-ttu-id="840b2-255">A operação não pode ser executada sozinha.</span><span class="sxs-lookup"><span data-stu-id="840b2-255">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-256"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-256"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-257">3710</span><span class="sxs-lookup"><span data-stu-id="840b2-257">3710</span></span><br />
<span data-ttu-id="840b2-258">-2146824578</span><span class="sxs-lookup"><span data-stu-id="840b2-258">-2146824578</span></span><br />
<span data-ttu-id="840b2-259">0x800A0E7E</span><span class="sxs-lookup"><span data-stu-id="840b2-259">0x800A0E7E</span></span></p></td>
<td><p><span data-ttu-id="840b2-260">A operação não pode ser executada durante o processamento do evento.</span><span class="sxs-lookup"><span data-stu-id="840b2-260">Operation cannot be performed while processing event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-261"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-261"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-262">3704</span><span class="sxs-lookup"><span data-stu-id="840b2-262">3704</span></span><br />
<span data-ttu-id="840b2-263">-2146824584</span><span class="sxs-lookup"><span data-stu-id="840b2-263">-2146824584</span></span><br />
<span data-ttu-id="840b2-264">0x800A0E78</span><span class="sxs-lookup"><span data-stu-id="840b2-264">0x800A0E78</span></span></p></td>
<td><p><span data-ttu-id="840b2-265">A operação não é permitida quando o objeto está fechado.</span><span class="sxs-lookup"><span data-stu-id="840b2-265">Operation is not allowed when the object is closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-266"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-266"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-267">3367</span><span class="sxs-lookup"><span data-stu-id="840b2-267">3367</span></span><br />
<span data-ttu-id="840b2-268">-2146824921</span><span class="sxs-lookup"><span data-stu-id="840b2-268">-2146824921</span></span><br />
<span data-ttu-id="840b2-269">0x800A0D27</span><span class="sxs-lookup"><span data-stu-id="840b2-269">0x800A0D27</span></span></p></td>
<td><p><span data-ttu-id="840b2-p111">O objeto já está na coleção. Não é possível anexá-lo.</span><span class="sxs-lookup"><span data-stu-id="840b2-p111">Object is already in collection. Cannot append.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-272"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-272"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-273">3420</span><span class="sxs-lookup"><span data-stu-id="840b2-273">3420</span></span><br />
<span data-ttu-id="840b2-274">-2146824868</span><span class="sxs-lookup"><span data-stu-id="840b2-274">-2146824868</span></span><br />
<span data-ttu-id="840b2-275">0x800A0D5C</span><span class="sxs-lookup"><span data-stu-id="840b2-275">0x800A0D5C</span></span></p></td>
<td><p><span data-ttu-id="840b2-276">O objeto não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="840b2-276">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-277"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-277"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-278">3705</span><span class="sxs-lookup"><span data-stu-id="840b2-278">3705</span></span><br />
<span data-ttu-id="840b2-279">-2146824583</span><span class="sxs-lookup"><span data-stu-id="840b2-279">-2146824583</span></span><br />
<span data-ttu-id="840b2-280">0x800A0E79</span><span class="sxs-lookup"><span data-stu-id="840b2-280">0x800A0E79</span></span></p></td>
<td><p><span data-ttu-id="840b2-281">A operação não é permitida quando o objeto está aberto.</span><span class="sxs-lookup"><span data-stu-id="840b2-281">Operation is not allowed when the object is open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-282"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-282"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-283">3002</span><span class="sxs-lookup"><span data-stu-id="840b2-283">3002</span></span><br />
<span data-ttu-id="840b2-284">-2146825286</span><span class="sxs-lookup"><span data-stu-id="840b2-284">-2146825286</span></span><br />
<span data-ttu-id="840b2-285">0x800A0BBA</span><span class="sxs-lookup"><span data-stu-id="840b2-285">0x800A0BBA</span></span></p></td>
<td><p><span data-ttu-id="840b2-286">O arquivo não pôde ser aberto.</span><span class="sxs-lookup"><span data-stu-id="840b2-286">File could not be opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-287"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-287"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-288">3712</span><span class="sxs-lookup"><span data-stu-id="840b2-288">3712</span></span><br />
<span data-ttu-id="840b2-289">-2146824576</span><span class="sxs-lookup"><span data-stu-id="840b2-289">-2146824576</span></span><br />
<span data-ttu-id="840b2-290">0x800A0E80</span><span class="sxs-lookup"><span data-stu-id="840b2-290">0x800A0E80</span></span></p></td>
<td><p><span data-ttu-id="840b2-291">A operação foi cancelada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="840b2-291">Operation has been cancelled by the user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-292"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-292"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-293">3734</span><span class="sxs-lookup"><span data-stu-id="840b2-293">3734</span></span><br />
<span data-ttu-id="840b2-294">-2146824554</span><span class="sxs-lookup"><span data-stu-id="840b2-294">-2146824554</span></span><br />
<span data-ttu-id="840b2-295">0x800A0E96</span><span class="sxs-lookup"><span data-stu-id="840b2-295">0x800A0E96</span></span></p></td>
<td><p><span data-ttu-id="840b2-p112">A operação não pode ser executada. O provedor não pode obter espaço de repositório suficiente.</span><span class="sxs-lookup"><span data-stu-id="840b2-p112">Operation cannot be performed. Provider cannot obtain enough storage space.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-298"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-298"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-299">3720</span><span class="sxs-lookup"><span data-stu-id="840b2-299">3720</span></span><br />
<span data-ttu-id="840b2-300">-2146824568</span><span class="sxs-lookup"><span data-stu-id="840b2-300">-2146824568</span></span><br />
<span data-ttu-id="840b2-301">0x800A0E88</span><span class="sxs-lookup"><span data-stu-id="840b2-301">0x800A0E88</span></span></p></td>
<td><p><span data-ttu-id="840b2-302">Permissão insuficiente impede escrever no campo.</span><span class="sxs-lookup"><span data-stu-id="840b2-302">Insufficent permission prevents writing to the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-303"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-303"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-304">3000</span><span class="sxs-lookup"><span data-stu-id="840b2-304">3000</span></span><br />
<span data-ttu-id="840b2-305">-2146825288</span><span class="sxs-lookup"><span data-stu-id="840b2-305">-2146825288</span></span><br />
<span data-ttu-id="840b2-306">0x800A0BB8</span><span class="sxs-lookup"><span data-stu-id="840b2-306">0x800A0BB8</span></span></p></td>
<td><p><span data-ttu-id="840b2-307">O provedor falhou em executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="840b2-307">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-308"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-308"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-309">3706</span><span class="sxs-lookup"><span data-stu-id="840b2-309">3706</span></span><br />
<span data-ttu-id="840b2-310">-2146824582</span><span class="sxs-lookup"><span data-stu-id="840b2-310">-2146824582</span></span><br />
<span data-ttu-id="840b2-311">0x800A0E7A</span><span class="sxs-lookup"><span data-stu-id="840b2-311">0x800A0E7A</span></span></p></td>
<td><p><span data-ttu-id="840b2-p113">O provedor não pode ser localizado. Ele não pode ser instalado corretamente.</span><span class="sxs-lookup"><span data-stu-id="840b2-p113">Provider cannot be found. It may not be properly installed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-314"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-314"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-315">3003</span><span class="sxs-lookup"><span data-stu-id="840b2-315">3003</span></span><br />
<span data-ttu-id="840b2-316">-2146825285</span><span class="sxs-lookup"><span data-stu-id="840b2-316">-2146825285</span></span><br />
<span data-ttu-id="840b2-317">0x800A0BBB</span><span class="sxs-lookup"><span data-stu-id="840b2-317">0x800A0BBB</span></span></p></td>
<td><p><span data-ttu-id="840b2-318">O arquivo não pôde ser lido.</span><span class="sxs-lookup"><span data-stu-id="840b2-318">File could not be read.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-319"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-319"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-320">3731</span><span class="sxs-lookup"><span data-stu-id="840b2-320">3731</span></span><br />
<span data-ttu-id="840b2-321">-2146824557</span><span class="sxs-lookup"><span data-stu-id="840b2-321">-2146824557</span></span><br />
<span data-ttu-id="840b2-322">0x800A0E93</span><span class="sxs-lookup"><span data-stu-id="840b2-322">0x800A0E93</span></span></p></td>
<td><p><span data-ttu-id="840b2-p114">A operação Copy não pode ser executada. O objeto nomeado pela URL de destino já existe. Especifique <strong>adCopyOverwrite</strong> para substituir o objeto.</span><span class="sxs-lookup"><span data-stu-id="840b2-p114">Copy operation cannot be performed. Object named by destination URL already exists. Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-326"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-326"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-327">3730</span><span class="sxs-lookup"><span data-stu-id="840b2-327">3730</span></span><br />
<span data-ttu-id="840b2-328">-2146824558</span><span class="sxs-lookup"><span data-stu-id="840b2-328">-2146824558</span></span><br />
<span data-ttu-id="840b2-329">0x800A0E92</span><span class="sxs-lookup"><span data-stu-id="840b2-329">0x800A0E92</span></span></p></td>
<td><p><span data-ttu-id="840b2-p115">O objeto representado pela URL especificada está bloqueado por um ou mais processos diferentes. Aguarde até que o processo seja finalizado e tente executar a operação novamente.</span><span class="sxs-lookup"><span data-stu-id="840b2-p115">Object represented by the specified URL is locked by one or more other processes. Wait until the process has finished and attempt the operation again.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-332"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-332"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-333">3735</span><span class="sxs-lookup"><span data-stu-id="840b2-333">3735</span></span><br />
<span data-ttu-id="840b2-334">-2146824553</span><span class="sxs-lookup"><span data-stu-id="840b2-334">-2146824553</span></span><br />
<span data-ttu-id="840b2-335">0x800A0E97</span><span class="sxs-lookup"><span data-stu-id="840b2-335">0x800A0E97</span></span></p></td>
<td><p><span data-ttu-id="840b2-336">A URL de origem ou de destino está fora do escopo do registro atual.</span><span class="sxs-lookup"><span data-stu-id="840b2-336">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-337"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-337"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-338">3722</span><span class="sxs-lookup"><span data-stu-id="840b2-338">3722</span></span><br />
<span data-ttu-id="840b2-339">-2146824566</span><span class="sxs-lookup"><span data-stu-id="840b2-339">-2146824566</span></span><br />
<span data-ttu-id="840b2-340">0x800A0E8A</span><span class="sxs-lookup"><span data-stu-id="840b2-340">0x800A0E8A</span></span></p></td>
<td><p><span data-ttu-id="840b2-341">O valor dos dados está em conflito com o tipo de dados ou com as restrições do campo.</span><span class="sxs-lookup"><span data-stu-id="840b2-341">Data value conflicts with the data type or constraints of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-342"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-342"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-343">3723</span><span class="sxs-lookup"><span data-stu-id="840b2-343">3723</span></span><br />
<span data-ttu-id="840b2-344">-2146824565</span><span class="sxs-lookup"><span data-stu-id="840b2-344">-2146824565</span></span><br />
<span data-ttu-id="840b2-345">0x800A0E8B</span><span class="sxs-lookup"><span data-stu-id="840b2-345">0x800A0E8B</span></span></p></td>
<td><p><span data-ttu-id="840b2-346">A conversão falhou porque o valor dos dados era assinado e o tipo de dados do campo utilizado pelo provedor não era.</span><span class="sxs-lookup"><span data-stu-id="840b2-346">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-347"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-347"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-348">3713</span><span class="sxs-lookup"><span data-stu-id="840b2-348">3713</span></span><br />
<span data-ttu-id="840b2-349">-2146824575</span><span class="sxs-lookup"><span data-stu-id="840b2-349">-2146824575</span></span><br />
<span data-ttu-id="840b2-350">0x800A0E81</span><span class="sxs-lookup"><span data-stu-id="840b2-350">0x800A0E81</span></span></p></td>
<td><p><span data-ttu-id="840b2-351">A operação não pode ser executado durante uma conexão assíncrona.</span><span class="sxs-lookup"><span data-stu-id="840b2-351">Operation cannot be performed while connecting aynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-352"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-352"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-353">3711</span><span class="sxs-lookup"><span data-stu-id="840b2-353">3711</span></span><br />
<span data-ttu-id="840b2-354">-2146824577</span><span class="sxs-lookup"><span data-stu-id="840b2-354">-2146824577</span></span><br />
<span data-ttu-id="840b2-355">0x800A0E7F</span><span class="sxs-lookup"><span data-stu-id="840b2-355">0x800A0E7F</span></span></p></td>
<td><p><span data-ttu-id="840b2-356">A operação não pode ser executada durante uma execução assíncrona.</span><span class="sxs-lookup"><span data-stu-id="840b2-356">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-357"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-357"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-358">3728</span><span class="sxs-lookup"><span data-stu-id="840b2-358">3728</span></span><br />
<span data-ttu-id="840b2-359">-2146824560</span><span class="sxs-lookup"><span data-stu-id="840b2-359">-2146824560</span></span><br />
<span data-ttu-id="840b2-360">0x800A0E90</span><span class="sxs-lookup"><span data-stu-id="840b2-360">0x800A0E90</span></span></p></td>
<td><p><span data-ttu-id="840b2-361">As permissões são insuficientes para acessar a árvore ou a subárvore.</span><span class="sxs-lookup"><span data-stu-id="840b2-361">Permissions are insufficient to access tree or subtree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-362"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-362"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-363">3736</span><span class="sxs-lookup"><span data-stu-id="840b2-363">3736</span></span><br />
<span data-ttu-id="840b2-364">-2146824552</span><span class="sxs-lookup"><span data-stu-id="840b2-364">-2146824552</span></span><br />
<span data-ttu-id="840b2-365">0x800A0E98</span><span class="sxs-lookup"><span data-stu-id="840b2-365">0x800A0E98</span></span></p></td>
<td><p><span data-ttu-id="840b2-p116">Houve falha na conclusão da operação, e o status não está disponível. O campo pode estar indisponível ou a operação não foi repetida.</span><span class="sxs-lookup"><span data-stu-id="840b2-p116">Operation failed to complete and the status is unavailable. The field may be unavailable or the operation was not attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-368"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-368"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-369">3716</span><span class="sxs-lookup"><span data-stu-id="840b2-369">3716</span></span><br />
<span data-ttu-id="840b2-370">-2146824572</span><span class="sxs-lookup"><span data-stu-id="840b2-370">-2146824572</span></span><br />
<span data-ttu-id="840b2-371">0x800A0E84</span><span class="sxs-lookup"><span data-stu-id="840b2-371">0x800A0E84</span></span></p></td>
<td><p><span data-ttu-id="840b2-372">As configurações de segurança nesse computador proíbem o acesso à fonte de dados em outro domínio.</span><span class="sxs-lookup"><span data-stu-id="840b2-372">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-373"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-373"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-374">3727</span><span class="sxs-lookup"><span data-stu-id="840b2-374">3727</span></span><br />
<span data-ttu-id="840b2-375">-2146824561</span><span class="sxs-lookup"><span data-stu-id="840b2-375">-2146824561</span></span><br />
<span data-ttu-id="840b2-376">0x800A0E8F</span><span class="sxs-lookup"><span data-stu-id="840b2-376">0x800A0E8F</span></span></p></td>
<td><p><span data-ttu-id="840b2-377">A URL de origem ou o pai da URL de destino não existe.</span><span class="sxs-lookup"><span data-stu-id="840b2-377">Either the source URL or the parent of the destination URL does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-378"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-378"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-379">3737</span><span class="sxs-lookup"><span data-stu-id="840b2-379">3737</span></span><br />
<span data-ttu-id="840b2-380">-2146824551</span><span class="sxs-lookup"><span data-stu-id="840b2-380">-2146824551</span></span><br />
<span data-ttu-id="840b2-381">0x800A0E99</span><span class="sxs-lookup"><span data-stu-id="840b2-381">0x800A0E99</span></span></p></td>
<td><p><span data-ttu-id="840b2-382">O registro chamado por essa URL não existe.</span><span class="sxs-lookup"><span data-stu-id="840b2-382">Record named by this URL does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-383"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-383"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-384">3733</span><span class="sxs-lookup"><span data-stu-id="840b2-384">3733</span></span><br />
<span data-ttu-id="840b2-385">-2146824555</span><span class="sxs-lookup"><span data-stu-id="840b2-385">-2146824555</span></span><br />
<span data-ttu-id="840b2-386">0x800A0E95</span><span class="sxs-lookup"><span data-stu-id="840b2-386">0x800A0E95</span></span></p></td>
<td><p><span data-ttu-id="840b2-p117">O provedor não pode localizar o dispositivo de repositório indicado pela URL. Certifique-se de que a URL esteja digitada corretamente.</span><span class="sxs-lookup"><span data-stu-id="840b2-p117">Provider cannot locate the storage device indicated by the URL. Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-389"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-389"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-390">3004</span><span class="sxs-lookup"><span data-stu-id="840b2-390">3004</span></span><br />
<span data-ttu-id="840b2-391">-2146825284</span><span class="sxs-lookup"><span data-stu-id="840b2-391">-2146825284</span></span><br />
<span data-ttu-id="840b2-392">0x800A0BBC</span><span class="sxs-lookup"><span data-stu-id="840b2-392">0x800A0BBC</span></span></p></td>
<td><p><span data-ttu-id="840b2-393">Falha ao gravar no arquivo.</span><span class="sxs-lookup"><span data-stu-id="840b2-393">Write to file failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-394"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-394"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-395">3717</span><span class="sxs-lookup"><span data-stu-id="840b2-395">3717</span></span><br />
<span data-ttu-id="840b2-396">-2146824571</span><span class="sxs-lookup"><span data-stu-id="840b2-396">-2146824571</span></span><br />
<span data-ttu-id="840b2-397">0x800A0E85</span><span class="sxs-lookup"><span data-stu-id="840b2-397">0x800A0E85</span></span></p></td>
<td><p><span data-ttu-id="840b2-p118">Para uso interno apenas. Não use.</span><span class="sxs-lookup"><span data-stu-id="840b2-p118">For internal use only. Don't use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-400"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="840b2-400"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="840b2-401">3718</span><span class="sxs-lookup"><span data-stu-id="840b2-401">3718</span></span><br />
<span data-ttu-id="840b2-402">-2146824570</span><span class="sxs-lookup"><span data-stu-id="840b2-402">-2146824570</span></span><br />
<span data-ttu-id="840b2-403">0x800A0E86</span><span class="sxs-lookup"><span data-stu-id="840b2-403">0x800A0E86</span></span></p></td>
<td><p><span data-ttu-id="840b2-p119">Para uso interno apenas. Não use.</span><span class="sxs-lookup"><span data-stu-id="840b2-p119">For internal use only. Don't use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="840b2-406">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="840b2-406">ADO/WFC equivalent</span></span>

<span data-ttu-id="840b2-407">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="840b2-407">Package: **com.ms.wfc.data**</span></span>

<span data-ttu-id="840b2-408">Somente os seguintes subconjuntos de equivalentes do ADO/WFC estão definidos.</span><span class="sxs-lookup"><span data-stu-id="840b2-408">Only the following subsets of ADO/WFC equivalents are defined.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="840b2-409">Constante</span><span class="sxs-lookup"><span data-stu-id="840b2-409">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="840b2-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span><span class="sxs-lookup"><span data-stu-id="840b2-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-411">AdoEnums.ErrorValue.DATACONVERSION</span><span class="sxs-lookup"><span data-stu-id="840b2-411">AdoEnums.ErrorValue.DATACONVERSION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="840b2-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span><span class="sxs-lookup"><span data-stu-id="840b2-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-414">AdoEnums.ErrorValue.INTRANSACTION</span><span class="sxs-lookup"><span data-stu-id="840b2-414">AdoEnums.ErrorValue.INTRANSACTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span><span class="sxs-lookup"><span data-stu-id="840b2-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span><span class="sxs-lookup"><span data-stu-id="840b2-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span><span class="sxs-lookup"><span data-stu-id="840b2-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="840b2-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span><span class="sxs-lookup"><span data-stu-id="840b2-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-420">AdoEnums.ErrorValue.NOTEXECUTING</span><span class="sxs-lookup"><span data-stu-id="840b2-420">AdoEnums.ErrorValue.NOTEXECUTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-421">AdoEnums.ErrorValue.NOTREENTRANT</span><span class="sxs-lookup"><span data-stu-id="840b2-421">AdoEnums.ErrorValue.NOTREENTRANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-422">AdoEnums.ErrorValue.OBJECTCLOSED</span><span class="sxs-lookup"><span data-stu-id="840b2-422">AdoEnums.ErrorValue.OBJECTCLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="840b2-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-424">AdoEnums.ErrorValue.OBJECTNOTSET</span><span class="sxs-lookup"><span data-stu-id="840b2-424">AdoEnums.ErrorValue.OBJECTNOTSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-425">AdoEnums.ErrorValue.OBJECTOPEN</span><span class="sxs-lookup"><span data-stu-id="840b2-425">AdoEnums.ErrorValue.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span><span class="sxs-lookup"><span data-stu-id="840b2-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="840b2-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-428">AdoEnums.ErrorValue.STILLCONNECTING</span><span class="sxs-lookup"><span data-stu-id="840b2-428">AdoEnums.ErrorValue.STILLCONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="840b2-429">AdoEnums.ErrorValue.STILLEXECUTING</span><span class="sxs-lookup"><span data-stu-id="840b2-429">AdoEnums.ErrorValue.STILLEXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="840b2-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span><span class="sxs-lookup"><span data-stu-id="840b2-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span></span></p></td>
</tr>
</tbody>
</table>

