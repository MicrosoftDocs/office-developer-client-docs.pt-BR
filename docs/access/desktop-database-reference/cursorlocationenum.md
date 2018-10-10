---
title: CursorLocationEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90226413579a8fac7586cbd5ef08510a36a42959
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463329"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="0df39-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="0df39-102">CursorLocationEnum</span></span>


<span data-ttu-id="0df39-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0df39-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0df39-104">Especifica o local do serviço do cursor.</span><span class="sxs-lookup"><span data-stu-id="0df39-104">Specifies the location of the cursor service.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0df39-105">Constante</span><span class="sxs-lookup"><span data-stu-id="0df39-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0df39-106">Valor</span><span class="sxs-lookup"><span data-stu-id="0df39-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0df39-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0df39-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0df39-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="0df39-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="0df39-109">3</span><span class="sxs-lookup"><span data-stu-id="0df39-109">3</span></span></p></td>
<td><p><span data-ttu-id="0df39-110">Utiliza cursores do lado do cliente fornecidos por uma biblioteca de cursor local.</span><span class="sxs-lookup"><span data-stu-id="0df39-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="0df39-111">Serviços do local do cursor frequentemente permitirá que muitos recursos fornecidos pelo driver cursores não podem, portanto o uso dessa configuração pode fornecer uma vantagem com relação a recursos que será habilitado.</span><span class="sxs-lookup"><span data-stu-id="0df39-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="0df39-112">Para compatibilidade com versões anteriores, o sinônimo <strong>adUseClientBatch</strong> também é suportada.</span><span class="sxs-lookup"><span data-stu-id="0df39-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0df39-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="0df39-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="0df39-114">1</span><span class="sxs-lookup"><span data-stu-id="0df39-114">1</span></span></p></td>
<td><p><span data-ttu-id="0df39-p102">Não usa os serviços de cursor. (Essa constante é obsoleta e aparece somente para fins de compatibilidade com versões anteriores.)</span><span class="sxs-lookup"><span data-stu-id="0df39-p102">Does not use cursor services. (This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0df39-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="0df39-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="0df39-118">2</span><span class="sxs-lookup"><span data-stu-id="0df39-118">2</span></span></p></td>
<td><p><span data-ttu-id="0df39-p103">Padrão. Usa os cursores de provedores de dados ou fornecidos pelo driver. Esses cursores são, algumas vezes, muito flexíveis e permitem sensibilidade adicional para alterações que os outros fazem na fonte de dados. Contudo, alguns recursos do <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (como os objetos <a href="recordset-object-ado.md">Recordset</a> desassociados) não podem ser simulados com os cursores do lado do servidor e esses recursos não estarão disponíveis com esta configuração.</span><span class="sxs-lookup"><span data-stu-id="0df39-p103">Default. Uses data-provider or driver-supplied cursors. These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source. However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0df39-123">**ADO/WFC Equivalente**</span><span class="sxs-lookup"><span data-stu-id="0df39-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="0df39-124">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="0df39-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0df39-125">Constante</span><span class="sxs-lookup"><span data-stu-id="0df39-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0df39-126">AdoEnums.CursorLocation.CLIENT</span><span class="sxs-lookup"><span data-stu-id="0df39-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0df39-127">AdoEnums.CursorLocation.NONE</span><span class="sxs-lookup"><span data-stu-id="0df39-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0df39-128">AdoEnums.CursorLocation.SERVER</span><span class="sxs-lookup"><span data-stu-id="0df39-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

