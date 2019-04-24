---
title: StreamOpenOptionsEnum
TOCTitle: StreamOpenOptionsEnum
ms:assetid: d4bbd6be-41f1-cdf2-9d8f-b77ce83fb88e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250069(v=office.15)
ms:contentKeyID: 48547951
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f335f8572fbade23b949abacce8dd3690d205e32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314746"
---
# <a name="streamopenoptionsenum"></a><span data-ttu-id="8ad75-102">StreamOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="8ad75-102">StreamOpenOptionsEnum</span></span>


<span data-ttu-id="8ad75-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ad75-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ad75-104">Especifica as opções para abrir um objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8ad75-104">Specifies options for opening a [Stream](stream-object-ado.md) object.</span></span> <span data-ttu-id="8ad75-105">Os valores podem ser combinados com um operador OR.</span><span class="sxs-lookup"><span data-stu-id="8ad75-105">The values can be combined with an OR operation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ad75-106">Constant</span><span class="sxs-lookup"><span data-stu-id="8ad75-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="8ad75-107">Valor</span><span class="sxs-lookup"><span data-stu-id="8ad75-107">Value</span></span></p></th>
<th><p><span data-ttu-id="8ad75-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ad75-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ad75-109"><strong>adOpenStreamAsync</strong></span><span class="sxs-lookup"><span data-stu-id="8ad75-109"><strong>adOpenStreamAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="8ad75-110">1</span><span class="sxs-lookup"><span data-stu-id="8ad75-110">1</span></span></p></td>
<td><p><span data-ttu-id="8ad75-111">Abre o objeto <strong>Stream</strong> no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="8ad75-111">Opens the <strong>Stream</strong> object in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ad75-112"><strong>Openoptions</strong></span><span class="sxs-lookup"><span data-stu-id="8ad75-112"><strong>adOpenStreamFromRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="8ad75-113">quatro</span><span class="sxs-lookup"><span data-stu-id="8ad75-113">4</span></span></p></td>
<td><p><span data-ttu-id="8ad75-p102">Identifica o conteúdo do parâmetro <em>Source</em> para ser um objeto <a href="record-object-ado.md">Record</a> já aberto. O comportamento padrão é tratar <em>Source</em> com um URL que aponta diretamente para um nó em uma estrutura em árvore. O fluxo padrão associado àquele nó é aberto.</span><span class="sxs-lookup"><span data-stu-id="8ad75-p102">Identifies the contents of the <em>Source</em> parameter to be an already open <a href="record-object-ado.md">Record</a> object. The default behavior is to treat <em>Source</em> as a URL that points directly to a node in a tree structure. The default stream associated with that node is opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ad75-117"><strong>adOpenStreamUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="8ad75-117"><strong>adOpenStreamUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="8ad75-118">-1</span><span class="sxs-lookup"><span data-stu-id="8ad75-118">-1</span></span></p></td>
<td><p><span data-ttu-id="8ad75-p103">Padrão. Especifica a abertura do objeto <strong>Stream</strong> com as opções padrão.</span><span class="sxs-lookup"><span data-stu-id="8ad75-p103">Default. Specifies opening the <strong>Stream</strong> object with default options.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8ad75-121">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="8ad75-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="8ad75-122">Essas constantes não têm ADO/WFC equivalentes.</span><span class="sxs-lookup"><span data-stu-id="8ad75-122">These constants do not have ADO/WFC equivalents.</span></span>

