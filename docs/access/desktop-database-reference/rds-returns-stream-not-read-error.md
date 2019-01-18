---
title: O RDS retorna o erro "Fluxo não lido"
TOCTitle: RDS returns "Stream Not Read" error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca0f54d8fdc7e37d0ee01f1ffd29c84a6a8ae799
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703752"
---
# <a name="rds-returns-stream-not-read-error"></a>RDS retorna \"Stream não lido\" erro


**Aplica-se a**: Access 2013, o Office 2013

"O objeto Stream não pôde ser lido porque está vazio ou a posição atual está no final do Stream. Para Streams não vazios, defina a posição atual com a propriedade Position. Para determinar se um Stream está vazio, verifique a propriedade Size."

Se você receber o erro acima, ele poderá ser o resultado de uma tentativa de uso de uma consulta hierárquica parametrizada por http. O RDS não permite que você mantenha hierarquias parametrizadas remotas.

