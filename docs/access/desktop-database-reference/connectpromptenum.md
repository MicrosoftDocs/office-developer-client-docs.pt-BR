---
title: ConnectPromptEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54643a66316d7f534553c20ecc3aafdf755fb857
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295664"
---
# <a name="connectpromptenum"></a><span data-ttu-id="4b21c-102">ConnectPromptEnum</span><span class="sxs-lookup"><span data-stu-id="4b21c-102">ConnectPromptEnum</span></span>

<span data-ttu-id="4b21c-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b21c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b21c-104">Especifica se uma caixa de diálogo deve ser exibida para avisar sobre parâmetros ausentes ao abrir uma conexão para uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="4b21c-104">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to a data source.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b21c-105">Constant</span><span class="sxs-lookup"><span data-stu-id="4b21c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="4b21c-106">Valor</span><span class="sxs-lookup"><span data-stu-id="4b21c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="4b21c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b21c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b21c-108"><strong>adPromptAlways</strong></span><span class="sxs-lookup"><span data-stu-id="4b21c-108"><strong>adPromptAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="4b21c-109">1</span><span class="sxs-lookup"><span data-stu-id="4b21c-109">1</span></span></p></td>
<td><p><span data-ttu-id="4b21c-110">Avisar sempre.</span><span class="sxs-lookup"><span data-stu-id="4b21c-110">Prompts always.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b21c-111"><strong>adPromptComplete</strong></span><span class="sxs-lookup"><span data-stu-id="4b21c-111"><strong>adPromptComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="4b21c-112">duas</span><span class="sxs-lookup"><span data-stu-id="4b21c-112">2</span></span></p></td>
<td><p><span data-ttu-id="4b21c-113">Avisar se mais informações forem necessárias.</span><span class="sxs-lookup"><span data-stu-id="4b21c-113">Prompts if more information is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b21c-114"><strong>adPromptCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="4b21c-114"><strong>adPromptCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="4b21c-115">3D</span><span class="sxs-lookup"><span data-stu-id="4b21c-115">3</span></span></p></td>
<td><p><span data-ttu-id="4b21c-116">Avisar se mais informações forem necessárias, mas se os parâmetros opcionais não forem permitidos.</span><span class="sxs-lookup"><span data-stu-id="4b21c-116">Prompts if more information is required but optional parameters are not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b21c-117"><strong>adPromptNever</strong></span><span class="sxs-lookup"><span data-stu-id="4b21c-117"><strong>adPromptNever</strong></span></span></p></td>
<td><p><span data-ttu-id="4b21c-118">quatro</span><span class="sxs-lookup"><span data-stu-id="4b21c-118">4</span></span></p></td>
<td><p><span data-ttu-id="4b21c-119">Nunca avisar.</span><span class="sxs-lookup"><span data-stu-id="4b21c-119">Never prompts.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="4b21c-120">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="4b21c-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="4b21c-121">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="4b21c-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b21c-122">Constant</span><span class="sxs-lookup"><span data-stu-id="4b21c-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b21c-123">AdoEnums. ConnectPrompt. ALWAYs</span><span class="sxs-lookup"><span data-stu-id="4b21c-123">AdoEnums.ConnectPrompt.ALWAYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b21c-124">AdoEnums. ConnectPrompt. COMPLETE</span><span class="sxs-lookup"><span data-stu-id="4b21c-124">AdoEnums.ConnectPrompt.COMPLETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b21c-125">AdoEnums. ConnectPrompt. COMPLETEREQUIRED</span><span class="sxs-lookup"><span data-stu-id="4b21c-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b21c-126">AdoEnums. ConnectPrompt. NEVEr</span><span class="sxs-lookup"><span data-stu-id="4b21c-126">AdoEnums.ConnectPrompt.NEVER</span></span></p></td>
</tr>
</tbody>
</table>

