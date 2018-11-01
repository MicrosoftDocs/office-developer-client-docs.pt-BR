---
title: Informações sobre erros relacionados a campos
TOCTitle: Field-Related Error Information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de2a737e314322064894142b2494e3b3793d1625
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884853"
---
# <a name="field-related-error-information"></a><span data-ttu-id="dc116-102">Informações sobre erros relacionados a campos</span><span class="sxs-lookup"><span data-stu-id="dc116-102">Field-Related Error Information</span></span>


<span data-ttu-id="dc116-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc116-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc116-p101">Se um erro for diretamente relacionado a um campo (por exemplo, se os dados estiverem ausentes ou se o tipo for incorreto para o campo ), você poderá recuperar mais informações sobre a causa do problema examinando a propriedade **Status** do objeto **Field**. Essa propriedade foi aprimorada para fornecer informações específicas sobre o problema. Portanto, por exemplo, quando há falha em uma chamada de **UpdateBatch**, a causa do problema poderá ser determinada examinando-se a propriedade **Status** dos objetos **Field** em cada um dos registros afetados. A propriedade conterá um dos valores da constante **FieldStatusEnum**. A tabela a seguir inclui esses valores de particular interesse quando ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="dc116-p101">If an error is directly related to a field — for example, if the data is missing or if it is the wrong type for the field — you can retrieve more information about the cause of the problem by examining the **Field** object's **Status** property. This property has been enhanced to provide specific information about the problem. So, for example, when a call to **UpdateBatch** fails, the cause of the problem can be determined by examining the **Status** property of the **Fields** in each of the effected records. The property will contain one of the values in the **FieldStatusEnum** constant. The following table includes those values that are of particular interest when an error occurs.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc116-109">Constant</span><span class="sxs-lookup"><span data-stu-id="dc116-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="dc116-110">Valor</span><span class="sxs-lookup"><span data-stu-id="dc116-110">Value</span></span></p></th>
<th><p><span data-ttu-id="dc116-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc116-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc116-112"><strong>adFieldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="dc116-112"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="dc116-113">2</span><span class="sxs-lookup"><span data-stu-id="dc116-113">2</span></span></p></td>
<td><p><span data-ttu-id="dc116-114">Indica que o campo não pode ser recuperado nem armazenado sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="dc116-114">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc116-115"><strong>adFieldDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="dc116-115"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="dc116-116">6</span><span class="sxs-lookup"><span data-stu-id="dc116-116">6</span></span></p></td>
<td><p><span data-ttu-id="dc116-117">Indica que os dados retornados do provedor sobrecarregaram o tipo de dados do campo.</span><span class="sxs-lookup"><span data-stu-id="dc116-117">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc116-118"><strong>adFieldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="dc116-118"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="dc116-119">13</span><span class="sxs-lookup"><span data-stu-id="dc116-119">13</span></span></p></td>
<td><p><span data-ttu-id="dc116-120">Indica que o valor padrão do campo foi usado durante a definição dos dados.</span><span class="sxs-lookup"><span data-stu-id="dc116-120">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc116-121"><strong>adFieldIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="dc116-121"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="dc116-122">15</span><span class="sxs-lookup"><span data-stu-id="dc116-122">15</span></span></p></td>
<td><p><span data-ttu-id="dc116-p102">Indica que este campo foi ignorado durante a definição dos valores de dados na fonte. Nenhum valor foi definido pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="dc116-p102">Indicates that this field was skipped when setting data values in the source. No value was set by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc116-125"><strong>adFieldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="dc116-125"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="dc116-126">10</span><span class="sxs-lookup"><span data-stu-id="dc116-126">10</span></span></p></td>
<td><p><span data-ttu-id="dc116-127">Indica que não é possível modificar o campo porque ele é uma entidade calculada ou derivada.</span><span class="sxs-lookup"><span data-stu-id="dc116-127">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc116-128"><strong>adFieldIsNull</strong></span><span class="sxs-lookup"><span data-stu-id="dc116-128"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="dc116-129">3</span><span class="sxs-lookup"><span data-stu-id="dc116-129">3</span></span></p></td>
<td><p><span data-ttu-id="dc116-130">Indica que o provedor retornou um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="dc116-130">Indicates that the provider returned a null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc116-131"><strong>adFieldOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="dc116-131"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="dc116-132">22</span><span class="sxs-lookup"><span data-stu-id="dc116-132">22</span></span></p></td>
<td><p><span data-ttu-id="dc116-133">Indica que o provedor não conseguiu obter espaço de repositório suficiente para concluir uma operação de movimentação ou cópia.</span><span class="sxs-lookup"><span data-stu-id="dc116-133">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
</tbody>
</table>

