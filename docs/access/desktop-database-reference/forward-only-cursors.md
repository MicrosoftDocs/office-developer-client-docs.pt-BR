---
title: Cursores somente de encaminhamento
TOCTitle: Forward-only cursors
ms:assetid: 27541bac-077b-bfe6-d9d8-713e4a945125
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249035(v=office.15)
ms:contentKeyID: 48543834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e742e3a6903faf7ab817b79675b100d026e25885
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946759"
---
# <a name="forward-only-cursors"></a>Cursores somente de encaminhamento

**Aplica-se a**: Access 2013, o Office 2013

O tipo de cursor padrão comum, chamado cursor apenas de avanço (ou não-rolável), pode mover apenas para frente no conjunto de resultados. Um cursor apenas de avanço não oferece suporte para rolagem (a capacidade de mover para frente e para trás no conjunto de resultados); ele só oferece suporte à busca de linhas do início ao fim desse conjunto. Com alguns cursores apenas de avanço (como os da biblioteca de cursores do SQL Server), todas instruções de inserção, atualização e exclusão realizadas pelo usuário final (ou confirmadas por outros usuários) que afetam linhas no conjunto de resultados ficam visíveis à medida que as linhas são buscadas. No entanto, como o cursor não pode ser rolado para trás, as alterações feitas nas linhas do banco de dados após a busca da linha não ficam visíveis através do cursor.

Depois que os dados da linha atual são processados, o cursor apenas de avanço libera os recursos que foram usados para armazenar os dados. Os cursores apenas de avanço são dinâmicos por padrão, significando que todas as alterações são detectadas à medida que a linha atual é processada. Consequentemente, a abertura do cursor torna-se mais rápida, permitindo que o conjunto de resultados exiba as atualizações feitas nas tabelas subjacentes.

Como os cursores apenas de avanço não oferecem suporte à rolagem para trás, seu aplicativo pode retornar ao início do conjunto de resultados fechando e reabrindo o cursor. Essa é uma maneira eficiente de trabalhar com pequenos volumes de dados. Como alternativa, o aplicativo pode ler o conjunto de resultados uma vez, armazenar os dados no cache local e, depois, navegar nesse cache.

Se o seu aplicativo não exigir rolagem no conjunto de resultados, o cursor apenas de avanço será a melhor maneira de recuperar dados rapidamente com sobrecarga mínima. Use **adOpenForwardOnly** **CursorTypeEnum** para indicar que você deseja usar um cursor apenas de avanço no ADO.

