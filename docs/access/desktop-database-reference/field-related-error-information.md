---
title: Informações de erro relacionado ao campo
TOCTitle: Field-related error information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a0d0362b8f0ff9570a92a3c1c364061d1f9a584
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292969"
---
# <a name="field-related-error-information"></a><span data-ttu-id="5d9e7-102">Informações de erro relacionado ao campo</span><span class="sxs-lookup"><span data-stu-id="5d9e7-102">Field-related error information</span></span>


<span data-ttu-id="5d9e7-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d9e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d9e7-p101">Se um erro for diretamente relacionado a um campo (por exemplo, se os dados estiverem ausentes ou se o tipo for incorreto para o campo ), você poderá recuperar mais informações sobre a causa do problema examinando a propriedade **Status** do objeto **Field**. Essa propriedade foi aprimorada para fornecer informações específicas sobre o problema. Portanto, por exemplo, quando há falha em uma chamada de **UpdateBatch**, a causa do problema poderá ser determinada examinando-se a propriedade **Status** dos objetos **Field** em cada um dos registros afetados. A propriedade conterá um dos valores da constante **FieldStatusEnum**. A tabela a seguir inclui esses valores de particular interesse quando ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="5d9e7-p101">If an error is directly related to a field — for example, if the data is missing or if it is the wrong type for the field — you can retrieve more information about the cause of the problem by examining the **Field** object's **Status** property. This property has been enhanced to provide specific information about the problem. So, for example, when a call to **UpdateBatch** fails, the cause of the problem can be determined by examining the **Status** property of the **Fields** in each of the effected records. The property will contain one of the values in the **FieldStatusEnum** constant. The following table includes those values that are of particular interest when an error occurs.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d9e7-109">Constant</span><span class="sxs-lookup"><span data-stu-id="5d9e7-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="5d9e7-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5d9e7-110">Value</span></span></p></th>
<th><p><span data-ttu-id="5d9e7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d9e7-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d9e7-112"><strong>adFieldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="5d9e7-112"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="5d9e7-113">2 </span><span class="sxs-lookup"><span data-stu-id="5d9e7-113">2</span></span></p></td>
<td><p><span data-ttu-id="5d9e7-114">Indica que o campo não pode ser recuperado nem armazenado sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="5d9e7-114">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d9e7-115"><strong>adFieldDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="5d9e7-115"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="5d9e7-116">6 </span><span class="sxs-lookup"><span data-stu-id="5d9e7-116">6</span></span></p></td>
<td><p><span data-ttu-id="5d9e7-117">Indica que os dados retornados do provedor estouraram o tipo de dados do campo.</span><span class="sxs-lookup"><span data-stu-id="5d9e7-117">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d9e7-118"><strong>adFieldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="5d9e7-118"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="5d9e7-119">13 </span><span class="sxs-lookup"><span data-stu-id="5d9e7-119">13</span></span></p></td>
<td><p><span data-ttu-id="5d9e7-120">Indica que o valor padrão do campo foi usado durante a definição dos dados.</span><span class="sxs-lookup"><span data-stu-id="5d9e7-120">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d9e7-121"><strong>adFieldIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="5d9e7-121"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="5d9e7-122">15 </span><span class="sxs-lookup"><span data-stu-id="5d9e7-122">15</span></span></p></td>
<td><p><span data-ttu-id="5d9e7-p102">Indica que este campo foi ignorado durante a definição dos valores de dados na fonte. Nenhum valor foi definido pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="5d9e7-p102">Indicates that this field was skipped when setting data values in the source. No value was set by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d9e7-125"><strong>adFieldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="5d9e7-125"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="5d9e7-126">10 </span><span class="sxs-lookup"><span data-stu-id="5d9e7-126">10</span></span></p></td>
<td><p><span data-ttu-id="5d9e7-127">Indica que não é possível modificar o campo porque ele é uma entidade calculada ou derivada.</span><span class="sxs-lookup"><span data-stu-id="5d9e7-127">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d9e7-128"><strong>adFieldIsNull</strong></span><span class="sxs-lookup"><span data-stu-id="5d9e7-128"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="5d9e7-129">3 </span><span class="sxs-lookup"><span data-stu-id="5d9e7-129">3</span></span></p></td>
<td><p><span data-ttu-id="5d9e7-130">Indica que o provedor retornou um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="5d9e7-130">Indicates that the provider returned a null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d9e7-131"><strong>adFieldOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="5d9e7-131"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="5d9e7-132">22</span><span class="sxs-lookup"><span data-stu-id="5d9e7-132">22</span></span></p></td>
<td><p><span data-ttu-id="5d9e7-133">Indica que o provedor não conseguiu obter espaço de repositório suficiente para concluir uma operação de movimentação ou cópia.</span><span class="sxs-lookup"><span data-stu-id="5d9e7-133">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
</tbody>
</table>

