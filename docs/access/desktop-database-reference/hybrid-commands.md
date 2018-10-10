---
title: Comandos híbridos (referência de banco de dados da área de trabalho do Access)
TOCTitle: Hybrid Commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aa95956fb50a5cd15fa4415e65d4a701f2e48feb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463705"
---
# <a name="hybrid-commands"></a><span data-ttu-id="ef128-102">Comandos híbridos</span><span class="sxs-lookup"><span data-stu-id="ef128-102">Hybrid Commands</span></span>


<span data-ttu-id="ef128-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef128-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ef128-p101">Os comandos híbridos são parcialmente parametrizados. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ef128-p101">Hybrid commands are partially parameterized commands. For example:</span></span>

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

<span data-ttu-id="ef128-106">O comportamento de armazenamento em cache de um comando híbrido é o mesmo que o de comandos parametrizados comuns.</span><span class="sxs-lookup"><span data-stu-id="ef128-106">The caching behavior for a hybrid command is the same as that of regular parameterized commands.</span></span>

