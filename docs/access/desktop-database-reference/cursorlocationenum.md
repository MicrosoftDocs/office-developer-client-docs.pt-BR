---
title: CursorLocationEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95e5744d5e19e7c3d40de19e240bbe338b2d5d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295209"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="e695b-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="e695b-102">CursorLocationEnum</span></span>

<span data-ttu-id="e695b-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e695b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e695b-104">Especifica o local do serviço do cursor.</span><span class="sxs-lookup"><span data-stu-id="e695b-104">Specifies the location of the cursor service.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e695b-105">Constant</span><span class="sxs-lookup"><span data-stu-id="e695b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e695b-106">Valor</span><span class="sxs-lookup"><span data-stu-id="e695b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e695b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e695b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e695b-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="e695b-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="e695b-109">3D</span><span class="sxs-lookup"><span data-stu-id="e695b-109">3</span></span></p></td>
<td><p><span data-ttu-id="e695b-110">Usa cursores do lado do cliente fornecidos por uma biblioteca de cursores local.</span><span class="sxs-lookup"><span data-stu-id="e695b-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="e695b-111">Os serviços de cursores locais permitirão, com frequência, muitos recursos que os cursores fornecidos por drivers não permitirão, portanto, usar essa configuração poderá oferecer uma vantagem com relação aos recursos que estarão ativados.</span><span class="sxs-lookup"><span data-stu-id="e695b-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="e695b-112">Para compatibilidade com versões anteriores, também há suporte para o sinônimo <strong>adUseClientBatch</strong>.</span><span class="sxs-lookup"><span data-stu-id="e695b-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e695b-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="e695b-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="e695b-114">1</span><span class="sxs-lookup"><span data-stu-id="e695b-114">1</span></span></p></td>
<td><p><span data-ttu-id="e695b-p102">Não usa os serviços de cursor. (Essa constante é obsoleta e aparece somente para fins de compatibilidade com versões anteriores.)</span><span class="sxs-lookup"><span data-stu-id="e695b-p102">Does not use cursor services. (This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e695b-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="e695b-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="e695b-118">duas</span><span class="sxs-lookup"><span data-stu-id="e695b-118">2</span></span></p></td>
<td><p><span data-ttu-id="e695b-119">Padrão.</span><span class="sxs-lookup"><span data-stu-id="e695b-119">Default.</span></span> <span data-ttu-id="e695b-120">Usa os cursores de provedores de dados ou fornecidos pelo driver.</span><span class="sxs-lookup"><span data-stu-id="e695b-120">Uses data-provider or driver-supplied cursors.</span></span> <span data-ttu-id="e695b-121">Esses cursores são, algumas vezes, muito flexíveis e permitem sensibilidade adicional para alterações que os outros fazem na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="e695b-121">These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source.</span></span> <span data-ttu-id="e695b-122">No enTanto, alguns recursos do <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">serviço de cursor da Microsoft para OLE DB</a> (como objetos <a href="recordset-object-ado.md">Recordset</a> desassociados) não podem ser simulados com cursores do lado do servidor e esses recursos não estarão disponíveis nessa configuração.</span><span class="sxs-lookup"><span data-stu-id="e695b-122">However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors, and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="e695b-123">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="e695b-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="e695b-124">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="e695b-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e695b-125">Constant</span><span class="sxs-lookup"><span data-stu-id="e695b-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e695b-126">AdoEnums. CursorLocation. CLIENT</span><span class="sxs-lookup"><span data-stu-id="e695b-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e695b-127">AdoEnums. CursorLocation. NONE</span><span class="sxs-lookup"><span data-stu-id="e695b-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e695b-128">AdoEnums. CursorLocation. SERVER</span><span class="sxs-lookup"><span data-stu-id="e695b-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

