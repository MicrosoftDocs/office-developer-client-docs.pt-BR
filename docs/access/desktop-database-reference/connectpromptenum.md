---
title: ConnectPromptEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e405b1eb3a1326d56a32c432fb212de417cf3469
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465109"
---
# <a name="connectpromptenum"></a><span data-ttu-id="666a3-102">ConnectPromptEnum</span><span class="sxs-lookup"><span data-stu-id="666a3-102">ConnectPromptEnum</span></span>


<span data-ttu-id="666a3-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="666a3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="666a3-104">Especifica se uma caixa de diálogo deve ser exibida para avisar sobre parâmetros ausentes ao abrir uma conexão para uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="666a3-104">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to a data source.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="666a3-105">Constante</span><span class="sxs-lookup"><span data-stu-id="666a3-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="666a3-106">Valor</span><span class="sxs-lookup"><span data-stu-id="666a3-106">Value</span></span></p></th>
<th><p><span data-ttu-id="666a3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="666a3-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="666a3-108"><strong>adPromptAlways</strong></span><span class="sxs-lookup"><span data-stu-id="666a3-108"><strong>adPromptAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="666a3-109">1</span><span class="sxs-lookup"><span data-stu-id="666a3-109">1</span></span></p></td>
<td><p><span data-ttu-id="666a3-110">Avisar sempre.</span><span class="sxs-lookup"><span data-stu-id="666a3-110">Prompts always.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="666a3-111"><strong>adPromptComplete</strong></span><span class="sxs-lookup"><span data-stu-id="666a3-111"><strong>adPromptComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="666a3-112">2</span><span class="sxs-lookup"><span data-stu-id="666a3-112">2</span></span></p></td>
<td><p><span data-ttu-id="666a3-113">Avisar se mais informações forem necessárias.</span><span class="sxs-lookup"><span data-stu-id="666a3-113">Prompts if more information is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="666a3-114"><strong>adPromptCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="666a3-114"><strong>adPromptCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="666a3-115">3</span><span class="sxs-lookup"><span data-stu-id="666a3-115">3</span></span></p></td>
<td><p><span data-ttu-id="666a3-116">Avisar se mais informações forem necessárias, mas se os parâmetros opcionais não forem permitidos.</span><span class="sxs-lookup"><span data-stu-id="666a3-116">Prompts if more information is required but optional parameters are not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="666a3-117"><strong>adPromptNever</strong></span><span class="sxs-lookup"><span data-stu-id="666a3-117"><strong>adPromptNever</strong></span></span></p></td>
<td><p><span data-ttu-id="666a3-118">4</span><span class="sxs-lookup"><span data-stu-id="666a3-118">4</span></span></p></td>
<td><p><span data-ttu-id="666a3-119">Nunca avisar.</span><span class="sxs-lookup"><span data-stu-id="666a3-119">Never prompts.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="666a3-120">**ADO/WFC Equivalente**</span><span class="sxs-lookup"><span data-stu-id="666a3-120">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="666a3-121">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="666a3-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="666a3-122">Constante</span><span class="sxs-lookup"><span data-stu-id="666a3-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="666a3-123">AdoEnums.ConnectPrompt.ALWAYS</span><span class="sxs-lookup"><span data-stu-id="666a3-123">AdoEnums.ConnectPrompt.ALWAYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="666a3-124">AdoEnums.ConnectPrompt.COMPLETE</span><span class="sxs-lookup"><span data-stu-id="666a3-124">AdoEnums.ConnectPrompt.COMPLETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="666a3-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span><span class="sxs-lookup"><span data-stu-id="666a3-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="666a3-126">AdoEnums.ConnectPrompt.NEVER</span><span class="sxs-lookup"><span data-stu-id="666a3-126">AdoEnums.ConnectPrompt.NEVER</span></span></p></td>
</tr>
</tbody>
</table>

