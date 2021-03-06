---
title: Cursores dinâmicos (referência do banco de dados da área de trabalho do Access)
TOCTitle: Dynamic cursors
ms:assetid: ae599d86-6b89-6103-fda1-c899a6138e1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249823(v=office.15)
ms:contentKeyID: 48547068
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ee81b2bd0e7d40b3a426c6416111d21e2ec760c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293634"
---
# <a name="dynamic-cursors"></a>Cursores dinâmicos


**Aplica-se ao:** Access 2013, Office 2013

Os cursores dinâmicos detectam todas as alterações feitas nas linhas do conjunto de resultados, independentemente de as alterações ocorrerem dentro do cursor ou por outros usuários fora dele. Todas as instruções de inserção, atualização e exclusão realizadas por todos os usuários podem ser vistas através do cursor. O cursor dinâmico pode detectar as alterações feitas nas linhas, na ordem e nos valores do conjunto de resultados após a abertura do cursor. As atualizações feitas fora do cursor não ficam visíveis até que sejam confirmadas (a não ser que o nível de isolamento de transações do cursor seja definido como "não confirmado").

Por exemplo, suponha que um cursor dinâmico busque duas linhas e outro aplicativo e, em seguida, atualize uma dessas linha e exclua a outra. Se o cursor dinâmico buscar essas linhas, ele não encontrará a linha excluída, mas exibirá os novos valores referentes à linha atualizada.

O cursor dinâmico será uma boa opção se seu aplicativo precisar detectar todas as atualizações simultâneas realizadas por outros usuários. Use **adOpenDynamic** **CursorTypeEnum** para indicar que você deseja usar um cursor dinâmico no ADO.

[Cursores apenas de avanço](forward-only-cursors.md) | [Cursores estáticos](static-cursors.md) | [Cursores de conjunto de chaves](keyset-cursors.md)

