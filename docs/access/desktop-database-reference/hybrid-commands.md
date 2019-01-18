---
title: Comandos híbridos (referência de banco de dados da área de trabalho do Access)
TOCTitle: Hybrid commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fe3e6d0afbba82cacd5a55c630f1ca41f3e318a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709149"
---
# <a name="hybrid-commands"></a><span data-ttu-id="1f059-102">Comandos híbridos</span><span class="sxs-lookup"><span data-stu-id="1f059-102">Hybrid commands</span></span>


<span data-ttu-id="1f059-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f059-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f059-p101">Os comandos híbridos são parcialmente parametrizados. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1f059-p101">Hybrid commands are partially parameterized commands. For example:</span></span>

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

<span data-ttu-id="1f059-106">O comportamento de armazenamento em cache de um comando híbrido é o mesmo que o de comandos parametrizados comuns.</span><span class="sxs-lookup"><span data-stu-id="1f059-106">The caching behavior for a hybrid command is the same as that of regular parameterized commands.</span></span>

