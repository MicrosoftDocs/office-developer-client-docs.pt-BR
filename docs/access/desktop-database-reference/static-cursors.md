---
title: Cursores estáticos (referência de banco de dados da área de trabalho do Access)
TOCTitle: Static cursors
ms:assetid: 1acf7fc5-fb12-e59e-f480-dde378a29c53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248950(v=office.15)
ms:contentKeyID: 48543524
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2eb019a6fc960d58771ff5ab0de7dca547c55f1c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699517"
---
# <a name="static-cursors"></a>Cursores estáticos


**Aplica-se a**: Access 2013, o Office 2013

O cursor estático sempre exibe o conjunto de resultados como ele era antes de o cursor ser aberto pela primeira vez. Dependendo da implementação, cursores estáticos são somente leitura ou de leitura/gravação, e fornecem rolamento de avanço e de recuo, O cursor estático geralmente não detecta alterações feitas em associações, pedidos, valores ou valores do conjunto de resultados depois que o cursor é aberto. Os cursores estáticos podem detectar suas próprias atualizações, exclusões e inserções, apesar de não serem solicitados a fazê-lo.

Os cursores estátivos nunca detectam outras atualizações, exclusões e inserções. Por exemplo, suponha que um cursor estático busque uma linha e outro aplicativo, e depois atualize essa linha. Se o aplicativo buscar novamente a linha a partir do cursor estático, os valores que encontra são inalterados, apesar das alterações feitas pelo outro aplicativo. Todos os tipos de rolagem têm suporte, mas os provedores podem suportar ou não indicadores.

Se seu aplicativo não precisar detectar alterações de dados e precisar de rolagem, o cursor estático é a melhor alternativa. Use o **adOpenStatic** **CursorTypeEnum** para indicar que deseja usar um cursor estático no ADO.

