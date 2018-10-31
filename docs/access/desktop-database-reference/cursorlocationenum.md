---
title: CursorLocationEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7f8eedd1245be16d87a2d3b2cd2b9121853529c5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863623"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="268df-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="268df-102">CursorLocationEnum</span></span>

<span data-ttu-id="268df-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="268df-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="268df-104">Especifica o local do serviço do cursor.</span><span class="sxs-lookup"><span data-stu-id="268df-104">Specifies the location of the cursor service.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="268df-105">Constante</span><span class="sxs-lookup"><span data-stu-id="268df-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="268df-106">Valor</span><span class="sxs-lookup"><span data-stu-id="268df-106">Value</span></span></p></th>
<th><p><span data-ttu-id="268df-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="268df-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="268df-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="268df-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="268df-109">3</span><span class="sxs-lookup"><span data-stu-id="268df-109">3</span></span></p></td>
<td><p><span data-ttu-id="268df-110">Utiliza cursores do lado do cliente fornecidos por uma biblioteca de cursor local.</span><span class="sxs-lookup"><span data-stu-id="268df-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="268df-111">Serviços do local do cursor frequentemente permitirá que muitos recursos fornecidos pelo driver cursores não podem, portanto o uso dessa configuração pode fornecer uma vantagem com relação a recursos que será habilitado.</span><span class="sxs-lookup"><span data-stu-id="268df-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="268df-112">Para compatibilidade com versões anteriores, o sinônimo <strong>adUseClientBatch</strong> também é suportada.</span><span class="sxs-lookup"><span data-stu-id="268df-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="268df-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="268df-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="268df-114">1</span><span class="sxs-lookup"><span data-stu-id="268df-114">1</span></span></p></td>
<td><p><span data-ttu-id="268df-p102">Não usa os serviços de cursor. (Essa constante é obsoleta e aparece somente para fins de compatibilidade com versões anteriores.)</span><span class="sxs-lookup"><span data-stu-id="268df-p102">Does not use cursor services. (This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="268df-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="268df-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="268df-118">2</span><span class="sxs-lookup"><span data-stu-id="268df-118">2</span></span></p></td>
<td><p><span data-ttu-id="268df-119">Padrão.</span><span class="sxs-lookup"><span data-stu-id="268df-119">Default.</span></span> <span data-ttu-id="268df-120">Usa o provedor de dados ou cursores fornecidos pelo driver.</span><span class="sxs-lookup"><span data-stu-id="268df-120">Uses data-provider or driver-supplied cursors.</span></span> <span data-ttu-id="268df-121">Esses cursores às vezes são muito flexíveis e permitem a sensibilidade adicional sobre as alterações que outras pessoas fazem à fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="268df-121">These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source.</span></span> <span data-ttu-id="268df-122">No entanto, alguns recursos do <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service para OLE DB</a> (por exemplo, os objetos <a href="recordset-object-ado.md">Recordset</a> desassociados) não podem ser simulados com cursores do servidor e esses recursos estarão indisponíveis com essa configuração.</span><span class="sxs-lookup"><span data-stu-id="268df-122">However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors, and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="268df-123">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="268df-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="268df-124">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="268df-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="268df-125">Constante</span><span class="sxs-lookup"><span data-stu-id="268df-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="268df-126">AdoEnums.CursorLocation.CLIENT</span><span class="sxs-lookup"><span data-stu-id="268df-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="268df-127">AdoEnums.CursorLocation.NONE</span><span class="sxs-lookup"><span data-stu-id="268df-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="268df-128">AdoEnums.CursorLocation.SERVER</span><span class="sxs-lookup"><span data-stu-id="268df-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

