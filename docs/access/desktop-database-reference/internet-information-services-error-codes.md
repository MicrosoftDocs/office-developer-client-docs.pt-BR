---
title: Códigos de erro dos Serviços de Informações da Internet
TOCTitle: Internet Information Services Error Codes
ms:assetid: 1ed57b89-b471-88e5-e5af-85323dec18d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248978(v=office.15)
ms:contentKeyID: 48543625
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d62be19cb472673a4bdafd3574bbe1fcb7b876c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462178"
---
# <a name="internet-information-services-error-codes"></a><span data-ttu-id="5ba38-102">Códigos de erro dos Serviços de Informações da Internet</span><span class="sxs-lookup"><span data-stu-id="5ba38-102">Internet Information Services Error Codes</span></span>


<span data-ttu-id="5ba38-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ba38-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5ba38-p101">A tabela a seguir lista os códigos de erro do Microsoft IIS (Serviços de Informações da Internet) relacionados à utilização do Remote Data Service, mostrando a conversão decimal positiva dos dois bytes inferiores, a conversão decimal negativa do código de erro inteiro e os valores hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="5ba38-p101">The following table lists Microsoft Internet Information Services (IIS) error codes related to Remote Data Service usage. The positive decimal translation of the low two bytes, the negative decimal translation of the full error code, and the hexadecimal values are shown.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ba38-106">Erros dos Serviços de Informações da Internet</span><span class="sxs-lookup"><span data-stu-id="5ba38-106">Internet Information Services errors</span></span></p></th>
<th><p><span data-ttu-id="5ba38-107">Número</span><span class="sxs-lookup"><span data-stu-id="5ba38-107">Number</span></span></p></th>
<th><p><span data-ttu-id="5ba38-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ba38-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ba38-109"><strong>IDS_IIS_AccessDenied</strong></span><span class="sxs-lookup"><span data-stu-id="5ba38-109"><strong>IDS_IIS_AccessDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba38-110">8208</span><span class="sxs-lookup"><span data-stu-id="5ba38-110">8208</span></span><br />
<span data-ttu-id="5ba38-111">-2146820080</span><span class="sxs-lookup"><span data-stu-id="5ba38-111">-2146820080</span></span><br />
<span data-ttu-id="5ba38-112">0x800A2010</span><span class="sxs-lookup"><span data-stu-id="5ba38-112">0x800A2010</span></span></p></td>
<td><p><span data-ttu-id="5ba38-113">Erro do servidor de Internet: acesso negado.</span><span class="sxs-lookup"><span data-stu-id="5ba38-113">Internet Server Error: Access Denied.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba38-114"><strong>IDS_IIS_ObjectNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="5ba38-114"><strong>IDS_IIS_ObjectNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba38-115">8209</span><span class="sxs-lookup"><span data-stu-id="5ba38-115">8209</span></span><br />
<span data-ttu-id="5ba38-116">-2146820079</span><span class="sxs-lookup"><span data-stu-id="5ba38-116">-2146820079</span></span><br />
<span data-ttu-id="5ba38-117">0x800A2011</span><span class="sxs-lookup"><span data-stu-id="5ba38-117">0x800A2011</span></span></p></td>
<td><p><span data-ttu-id="5ba38-118">Erro do servidor de Internet: objeto/módulo não encontrado.</span><span class="sxs-lookup"><span data-stu-id="5ba38-118">Internet Server Error: Object/module not found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba38-119"><strong>IDS_IIS_RequestForbidden</strong></span><span class="sxs-lookup"><span data-stu-id="5ba38-119"><strong>IDS_IIS_RequestForbidden</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba38-120">8210</span><span class="sxs-lookup"><span data-stu-id="5ba38-120">8210</span></span><br />
<span data-ttu-id="5ba38-121">-2146820078</span><span class="sxs-lookup"><span data-stu-id="5ba38-121">-2146820078</span></span><br />
<span data-ttu-id="5ba38-122">0x800A2012</span><span class="sxs-lookup"><span data-stu-id="5ba38-122">0x800A2012</span></span></p></td>
<td><p><span data-ttu-id="5ba38-123">Erro do servidor de Internet: solicitação proibida.</span><span class="sxs-lookup"><span data-stu-id="5ba38-123">Internet Server Error: Request Forbidden.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba38-124"><strong>IDS_IIS_UnexpectedError</strong></span><span class="sxs-lookup"><span data-stu-id="5ba38-124"><strong>IDS_IIS_UnexpectedError</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba38-125">8447</span><span class="sxs-lookup"><span data-stu-id="5ba38-125">8447</span></span><br />
<span data-ttu-id="5ba38-126">-2146819841</span><span class="sxs-lookup"><span data-stu-id="5ba38-126">-2146819841</span></span><br />
<span data-ttu-id="5ba38-127">0x800A20FF</span><span class="sxs-lookup"><span data-stu-id="5ba38-127">0x800A20FF</span></span></p></td>
<td><p><span data-ttu-id="5ba38-128">Erro do servidor de Internet.</span><span class="sxs-lookup"><span data-stu-id="5ba38-128">Internet Server Error.</span></span></p></td>
</tr>
</tbody>
</table>

