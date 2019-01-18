---
title: Cursores do conjunto de chaves (referência de banco de dados da área de trabalho do Access)
TOCTitle: Keyset cursors
ms:assetid: 4b6e5f90-4413-4fb3-0a08-2cb89d3c61f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249236(v=office.15)
ms:contentKeyID: 48544690
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 200b10599683a5b5877952664c04e94b2523cfee
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721917"
---
# <a name="keyset-cursors"></a>Cursores de conjuntos de chaves

**Aplica-se a**: Access 2013, o Office 2013

O cursor controlado por conjunto de chaves fornece uma funcionalidade entre o cursor estático e o dinâmico com sua capacidade de detectar alterações. Assim como um cursor estático, esse cursor nem sempre detecta as alterações da associação e a ordem do conjunto de resultados. Como o cursor dinâmico, esse cursor detecta os valores das linhas no conjunto de resultados.

Esse tipo de cursor é controlado por um conjunto exclusivo de identificadores (chaves), também conhecido como conjunto de chaves. As chaves são criadas a partir de um conjunto de colunas que identifica exclusivamente as linhas no conjunto de resultados. O conjunto de chaves é o conjunto de valores de chave de todas as linhas retornadas pela instrução de consulta.

Com esse tipo de cursor, é criada e salva uma chave em cada linha do cursor e armazenada na estação de trabalho do cliente ou no servidor. Quando você acessar cada linha, a chave armazenada será usada para buscar os valores de dados atuais da fonte de dados. Nesse tipo de cursor, a associação do conjunto de resultados será congelada quando o conjunto de chaves estiver totalmente preenchido. Por esse motivo, as adições ou as atualizações que afetam a associação não fazem parte do conjunto de resultados até que este seja reaberto.

As alterações dos valores de dados (feitas pelo proprietário do conjunto de chaves ou outros processos) são visíveis à medida que o usuário rolar o conjunto de resultados. As inserções feitas fora do cursor (por outros processos) serão visíveis somente se o cursor for fechado e reaberto. As inserções feitas no cursor são visíveis no final do conjunto de resultados.

Quando um cursor controlado por conjunto de chaves tenta recuperar uma linha que tenha sido excluída, essa linha aparecerá como um "buraco" no conjunto de resultados. A chave da linha existe no conjunto de chaves, mas a linha não existe mais no conjunto de resultados. Se os valores de chave na linha são atualizados, a linha será considerada como se tivesse sido excluída e depois inserida; por esse motivo, tais linhas também aparecerem como buracos no conjunto de resultados. Ao mesmo tempo em que um cursor controlado por conjunto de chaves sempre pode detectar as linhas excluídas por outros processos, pode remover opcionalmente as chaves das linhas excluídas por ele mesmo. Os cursores que fazem isso não conseguem detectar suas próprias exclusões porque a evidência foi removida.

Uma atualização de uma coluna de chave opera como uma exclusão da chave antiga seguida da inserção de uma nova chave. O valor da nova chave não será visível se a atualização não foi feita pelo cursor. Em caso positivo, o valor da nova chave será visível no final do conjunto de resultados.

Há uma variação nos cursores controlados por conjuntos de chaves denominada cursores padrão controlados por conjuntos de chaves. Nesse tipo de cursor, a associação das linhas ao conjunto de resultados e à ordem das linhas é fixada pelo tempo de abertura do cursor, mas as alterações dos valores feitas pelo proprietário do cursor e as alterações comprometidas feitas por outros processos são visíveis. Se uma alteração desqualificar uma linha da associação ou afetar a ordem de uma linha, a linha não desaparecerá ou será movida, a não ser que o cursor seja fechado e reaberto. Os dados inseridos não aparecerão, mas as alterações nos dados existentes aparecerão como as linhas buscadas.

O cursor controlado por conjunto de chaves apresenta dificuldades para ser usado corretamente porque a sensibilidade às alterações de dados depende de muitas circunstâncias diferentes, como descrito anteriormente. No entanto, se o seu aplicativo não lida com atualizações simultâneas, pode tratar, de forma programática, das chaves incorretas e acessa diretamente certas linhas chaveadas, o cursor controlado por conjunto de chaves poderá funcionar no seu caso. Use **adOpenKeyset** **CursorTypeEnum** para indicar que você deseja usar o cursor controlado por conjunto de chaves no ADO.

