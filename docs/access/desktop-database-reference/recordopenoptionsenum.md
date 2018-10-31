---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 54499cc9c8b45e411b4121963d1a571100b7e0e5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860943"
---
# <a name="recordopenoptionsenum"></a><span data-ttu-id="07c29-102">RecordOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="07c29-102">RecordOpenOptionsEnum</span></span>


<span data-ttu-id="07c29-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="07c29-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="07c29-p101">Especifica as opções para abrir um objeto [Record](record-object-ado.md). Esses valores podem ser combinadas usando o OR.</span><span class="sxs-lookup"><span data-stu-id="07c29-p101">Specifies options for opening a [Record](record-object-ado.md). These values may be combined by using OR.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="07c29-106">Constant</span><span class="sxs-lookup"><span data-stu-id="07c29-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="07c29-107">Valor</span><span class="sxs-lookup"><span data-stu-id="07c29-107">Value</span></span></p></th>
<th><p><span data-ttu-id="07c29-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="07c29-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07c29-109"><strong>adDelayFetchFields</strong></span><span class="sxs-lookup"><span data-stu-id="07c29-109"><strong>adDelayFetchFields</strong></span></span></p></td>
<td><p><span data-ttu-id="07c29-110">0x8000</span><span class="sxs-lookup"><span data-stu-id="07c29-110">0x8000</span></span></p></td>
<td><p><span data-ttu-id="07c29-p102">Indica para o provedor que os campos associados ao <strong>Record</strong> não precisam ser recuperados inicialmente, mas podem ser recuperados na primeira tentativa para acessar o campo. O comportamento padrão, indicado pela ausência deste indicador, é para recuperar todos os campos de objetos <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="07c29-p102">Indicates to the provider that the fields associated with the <strong>Record</strong> need not be retrieved initially, but can be retrieved at the first attempt to access the field. The default behavior, indicated by the absence of this flag, is to retrieve all the <strong>Record</strong> object fields.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07c29-113"><strong>adDelayFetchStream</strong></span><span class="sxs-lookup"><span data-stu-id="07c29-113"><strong>adDelayFetchStream</strong></span></span></p></td>
<td><p><span data-ttu-id="07c29-114">0x4000</span><span class="sxs-lookup"><span data-stu-id="07c29-114">0x4000</span></span></p></td>
<td><p><span data-ttu-id="07c29-p103">Indica ao provedor que o fluxo padrão associado ao <strong>Record</strong> não precisa ser recuperado inicialmente. O comportamento padrão, indicado pela ausência deste indicador, é para recuperar o fluxo padrão associado ao objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="07c29-p103">Indicates to the provider that the default stream associated with the <strong>Record</strong> need not be retrieved initially. The default behavior, indicated by the absence of this flag, is to retrieve the default stream associated with the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07c29-117"><strong>adOpenAsync</strong></span><span class="sxs-lookup"><span data-stu-id="07c29-117"><strong>adOpenAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="07c29-118">0x1000</span><span class="sxs-lookup"><span data-stu-id="07c29-118">0x1000</span></span></p></td>
<td><p><span data-ttu-id="07c29-119">Indica que o objeto <strong>Record</strong> é aberto no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="07c29-119">Indicates that the <strong>Record</strong> object is opened in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07c29-120"><strong>adOpenExecuteCommand</strong></span><span class="sxs-lookup"><span data-stu-id="07c29-120"><strong>adOpenExecuteCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="07c29-121">0x10000</span><span class="sxs-lookup"><span data-stu-id="07c29-121">0x10000</span></span></p></td>
<td><p><span data-ttu-id="07c29-p104">Indica que a sequência Source contém o texto do comento que deveria ser executado. Este valor é equivalente à opção <strong>adCmdText</strong> em <strong>Recordset.Open</strong>.</span><span class="sxs-lookup"><span data-stu-id="07c29-p104">Indicates that the Source string contains command text that should be executed. This value is equivalent to the <strong>adCmdText</strong> option on <strong>Recordset.Open</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07c29-124"><strong>adOpenRecordUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="07c29-124"><strong>adOpenRecordUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="07c29-125">-1</span><span class="sxs-lookup"><span data-stu-id="07c29-125">-1</span></span></p></td>
<td><p><span data-ttu-id="07c29-p105">Padrão. Indica que nenhuma opção foi especificada.</span><span class="sxs-lookup"><span data-stu-id="07c29-p105">Default. Indicates no options are specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07c29-128"><strong>adOpenOutput</strong></span><span class="sxs-lookup"><span data-stu-id="07c29-128"><strong>adOpenOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="07c29-129">0x800000</span><span class="sxs-lookup"><span data-stu-id="07c29-129">0x800000</span></span></p></td>
<td><p><span data-ttu-id="07c29-p106">Indica que se a fonte apontar para um nó que contenha um script executável (como uma página .ASP), então o <strong>Record</strong> aberto conterá os resultados do script executado. Este valor só é válido com registros que não pertencem à coleções.</span><span class="sxs-lookup"><span data-stu-id="07c29-p106">Indicates that if the source points to a node that contains an executable script (such as an .ASP page), then the opened <strong>Record</strong> will contain the results of the executed script. This value is only valid with non-collection records.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="07c29-132">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="07c29-132">ADO/WFC equivalent</span></span>

<span data-ttu-id="07c29-133">Essas constantes não têm ADO/WFC equivalentes.</span><span class="sxs-lookup"><span data-stu-id="07c29-133">These constants do not have ADO/WFC equivalents.</span></span>

