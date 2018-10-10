---
title: Cursores estáticos (referência de banco de dados da área de trabalho do Access)
TOCTitle: Static Cursors
ms:assetid: 1acf7fc5-fb12-e59e-f480-dde378a29c53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248950(v=office.15)
ms:contentKeyID: 48543524
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8878333c8390ffcc075c0160f246e7f16757d226
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464271"
---
# <a name="static-cursors"></a>Cursores estáticos


**Aplica-se a**: Access 2013 | Office 2013

O cursor estático sempre exibe o conjunto de resultados como ele era antes de o cursor ser aberto pela primeira vez. Dependendo da implementação, cursores estáticos são somente leitura ou de leitura/gravação, e fornecem rolamento de avanço e de recuo, O cursor estático geralmente não detecta alterações feitas em associações, pedidos, valores ou valores do conjunto de resultados depois que o cursor é aberto. Os cursores estáticos podem detectar suas próprias atualizações, exclusões e inserções, apesar de não serem solicitados a fazê-lo.

Os cursores estátivos nunca detectam outras atualizações, exclusões e inserções. Por exemplo, suponha que um cursor estático busque uma linha e outro aplicativo, e depois atualize essa linha. Se o aplicativo buscar novamente a linha a partir do cursor estático, os valores que encontra são inalterados, apesar das alterações feitas pelo outro aplicativo. Todos os tipos de rolagem têm suporte, mas os provedores podem suportar ou não indicadores.

Se seu aplicativo não precisar detectar alterações de dados e precisar de rolagem, o cursor estático é a melhor alternativa. Use o **adOpenStatic** **CursorTypeEnum** para indicar que deseja usar um cursor estático no ADO.

