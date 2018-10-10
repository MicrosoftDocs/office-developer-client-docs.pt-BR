---
title: Agregados netos
TOCTitle: Grandchild Aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e79cfe863e80e70e75d7f8e65c10764df67a39df
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464515"
---
# <a name="grandchild-aggregates"></a>Agregados netos


**Aplica-se a**: Access 2013 | Office 2013

A coluna de capítulo criada em uma cláusula de um comando de forma pode ser dado um *nome de alias de capítulo* (geralmente com a palavra-chave). Você pode identificar qualquer coluna qualquer capítulo do **Recordset** com formato com um nome totalmente qualificado que identifica o filho que contém a coluna. Por exemplo, se o capítulo pai, Cap1, contém um capítulo de filho, chap2, que tem uma coluna de quantidade amt, então o nome qualificado seria chap1.chap2.amt. O nome qualificado, em seguida, pode ser usado como um argumento para uma das funções agregadas (soma, média, MAX, MIN, contagem, DESVPAD ou qualquer).

