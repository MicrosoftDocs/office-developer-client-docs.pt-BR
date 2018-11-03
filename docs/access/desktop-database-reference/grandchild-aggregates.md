---
title: Agregados netos
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc7576eb8e1555ab8b00d2800242c7be24baca58
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947935"
---
# <a name="grandchild-aggregates"></a>Agregados netos


**Aplica-se a**: Access 2013, o Office 2013

A coluna de capítulo criada em uma cláusula de um comando de forma pode ser dado um *nome de alias de capítulo* (geralmente com a palavra-chave). Você pode identificar qualquer coluna qualquer capítulo do **Recordset** com formato com um nome totalmente qualificado que identifica o filho que contém a coluna. Por exemplo, se o capítulo pai, Cap1, contém um capítulo de filho, chap2, que tem uma coluna de quantidade amt, então o nome qualificado seria chap1.chap2.amt. O nome qualificado, em seguida, pode ser usado como um argumento para uma das funções agregadas (soma, média, MAX, MIN, contagem, DESVPAD ou qualquer).

