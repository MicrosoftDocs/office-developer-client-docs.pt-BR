---
title: O RDS retorna o erro "Stream não lido"
TOCTitle: RDS Returns "Stream Not Read" Error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 312d6f7e29a7573237bf8e4ddab17b9f8796cc4b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870013"
---
# <a name="rds-returns-stream-not-read-error"></a>RDS retorna \"Stream não lido\" erro


**Aplica-se a**: Access 2013, o Office 2013

"O objeto Stream não pôde ser lido porque está vazio ou a posição atual está no final do Stream. Para Streams não vazios, defina a posição atual com a propriedade Position. Para determinar se um Stream está vazio, verifique a propriedade Size."

Se você receber o erro acima, ele poderá ser o resultado de uma tentativa de uso de uma consulta hierárquica parametrizada por http. O RDS não permite que você mantenha hierarquias parametrizadas remotas.

