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
# <a name="hybrid-commands"></a>Comandos híbridos


**Aplica-se a**: Access 2013 | Office 2013

Os comandos híbridos são parcialmente parametrizados. Por exemplo:

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

O comportamento de armazenamento em cache de um comando híbrido é o mesmo que o de comandos parametrizados comuns.

