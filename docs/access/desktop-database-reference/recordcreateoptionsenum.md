---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bc0d378428c00882c49f7783892ca2bf4d4638c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300690"
---
# <a name="recordcreateoptionsenum"></a><span data-ttu-id="740f2-102">RecordCreateOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="740f2-102">RecordCreateOptionsEnum</span></span>


<span data-ttu-id="740f2-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="740f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="740f2-p101">Especifica se um **Record** existente deve ser aberto ou um novo **Record** criado para o método [Open](record-object-ado.md) do objeto [Record](open-method-ado-record.md). Os valores podem ser combinados com um operador AND.</span><span class="sxs-lookup"><span data-stu-id="740f2-p101">Specifies whether an existing **Record** should be opened or a new **Record** created for the [Record](record-object-ado.md) object [Open](open-method-ado-record.md) method. The values can be combined with an AND operator.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="740f2-106">Constant</span><span class="sxs-lookup"><span data-stu-id="740f2-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="740f2-107">Valor</span><span class="sxs-lookup"><span data-stu-id="740f2-107">Value</span></span></p></th>
<th><p><span data-ttu-id="740f2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="740f2-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="740f2-109"><strong>adCreateCollection</strong></span><span class="sxs-lookup"><span data-stu-id="740f2-109"><strong>adCreateCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="740f2-110">0x2000</span><span class="sxs-lookup"><span data-stu-id="740f2-110">0x2000</span></span></p></td>
<td><p><span data-ttu-id="740f2-p102">Cria um novo <strong>Record</strong> no nó especificado pelo parâmetro <em>Source</em>, em vez abrir um <strong>Record</strong> existente. Se a origem apontar para um nó existente, ocorrerá um erro de tempo de execução, a menos que <strong>adCreateCollection</strong> seja combinado com <strong>adOpenIfExists</strong> ou <strong>adCreateOverwrite</strong>.</span><span class="sxs-lookup"><span data-stu-id="740f2-p102">Creates a new <strong>Record</strong> at the node specified by <em>Source</em> parameter, instead of opening an existing <strong>Record</strong>. If the source points to an existing node, then a run-time error occurs, unless <strong>adCreateCollection</strong> is combined with <strong>adOpenIfExists</strong> or <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="740f2-113"><strong>adCreateNonCollection</strong></span><span class="sxs-lookup"><span data-stu-id="740f2-113"><strong>adCreateNonCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="740f2-114">,0</span><span class="sxs-lookup"><span data-stu-id="740f2-114">0</span></span></p></td>
<td><p><span data-ttu-id="740f2-115">Cria um novo <strong>Record</strong> do tipo <a href="recordtypeenum.md">adSimpleRecord</a>.</span><span class="sxs-lookup"><span data-stu-id="740f2-115">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adSimpleRecord</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="740f2-116"><strong>adCreateOverwrite</strong></span><span class="sxs-lookup"><span data-stu-id="740f2-116"><strong>adCreateOverwrite</strong></span></span></p></td>
<td><p><span data-ttu-id="740f2-117">0x4000000</span><span class="sxs-lookup"><span data-stu-id="740f2-117">0x4000000</span></span></p></td>
<td><p><span data-ttu-id="740f2-p103">Modifica os sinalizadores de criação <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong> e <strong>adCreateStructDoc</strong>. Quando OR for usado com esse valor e um dos valores do sinalizador de criação, se a URL de origem apontar para o nó existente ou <strong>Record</strong>, o <strong>Record</strong> existente será sobregravado e um novo será criado em seu local. Esse valor não pode ser usado juntamente com <strong>adOpenIfExists</strong>.</span><span class="sxs-lookup"><span data-stu-id="740f2-p103">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>. When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong>, then the existing <strong>Record</strong> is overwritten and a new one is created in its place. This value cannot be used together with <strong>adOpenIfExists</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="740f2-121"><strong>adCreateStructDoc</strong></span><span class="sxs-lookup"><span data-stu-id="740f2-121"><strong>adCreateStructDoc</strong></span></span></p></td>
<td><p><span data-ttu-id="740f2-122">0x80000000</span><span class="sxs-lookup"><span data-stu-id="740f2-122">0x80000000</span></span></p></td>
<td><p><span data-ttu-id="740f2-123">Cria um novo <strong>Record</strong> de tipo <a href="recordtypeenum.md">adStructDoc</a>, em vez abrir um <strong>Record</strong> existente.</span><span class="sxs-lookup"><span data-stu-id="740f2-123">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adStructDoc</a>, instead of opening an existing <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="740f2-124"><strong>adFailIfNotExists</strong></span><span class="sxs-lookup"><span data-stu-id="740f2-124"><strong>adFailIfNotExists</strong></span></span></p></td>
<td><p><span data-ttu-id="740f2-125">-1</span><span class="sxs-lookup"><span data-stu-id="740f2-125">-1</span></span></p></td>
<td><p><span data-ttu-id="740f2-p104">Padrão. Resulta em um erro de tempo de execução se <em>Source</em> apontar para um nó não existente.</span><span class="sxs-lookup"><span data-stu-id="740f2-p104">Default. Results in a run-time error if <em>Source</em> points to a non-existent node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="740f2-128"><strong>adOpenIfExists</strong></span><span class="sxs-lookup"><span data-stu-id="740f2-128"><strong>adOpenIfExists</strong></span></span></p></td>
<td><p><span data-ttu-id="740f2-129">0x2000000</span><span class="sxs-lookup"><span data-stu-id="740f2-129">0x2000000</span></span></p></td>
<td><p><span data-ttu-id="740f2-p105">Modifica os sinalizadores <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong> e <strong>adCreateStructDoc</strong>. Quando OR for usado com esse valor e um dos valores do sinalizador de criação, se a URL de origem apontar para um nó existente ou objeto <strong>Record</strong>, o provedor deve abrir o <strong>Record</strong> existente em vez de criar um novo. Esse valor não pode ser usado com <strong>adCreateOverwrite</strong>.</span><span class="sxs-lookup"><span data-stu-id="740f2-p105">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>. When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong> object, then the provider must open the existing <strong>Record</strong> instead of creating a new one. This value cannot be used together with <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="740f2-133">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="740f2-133">ADO/WFC equivalent</span></span>

<span data-ttu-id="740f2-134">Essas constantes não têm ADO/WFC equivalentes.</span><span class="sxs-lookup"><span data-stu-id="740f2-134">These constants do not have ADO/WFC equivalents.</span></span>

