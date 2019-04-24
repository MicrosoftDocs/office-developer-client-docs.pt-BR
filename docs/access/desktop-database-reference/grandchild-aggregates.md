---
title: Agregações de netos
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4c50898626488f909616977c6bb50c936434563
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292143"
---
# <a name="grandchild-aggregates"></a>Agregações de netos


**Aplica-se ao:** Access 2013, Office 2013

À coluna do capítulo criada em uma cláusula de um comando shape pode ser fornecida um *nome do alias do capítulo* (geralmente com a palavra-chave AS). Você pode identificar qualquer coluna em qualquer capítulo do **Recordset** com forma com um nome totalmente qualificado que identifica o filho que contém a coluna. Por exemplo, se o capítulo pai, chap1, contém um capítulo filho, chap2, que tem uma coluna de valor, amt, então o nome qualificado seria chap1.chap2.amt. O nome qualificado pode então ser usado como um argumento para uma das funções agregadas (SUM, AVG, MAX, MIN, COUNT, STDEV ou ANY).

