---
title: Tipos de cursores (referência do banco de dados da área de trabalho do Access)
TOCTitle: Types of Cursors
ms:assetid: 589f3755-3cf5-9470-bd66-8e8afa218fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249299(v=office.15)
ms:contentKeyID: 48544996
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6493d746f43ac8d923e5b1b9d6dcd3de44b411ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314025"
---
# <a name="types-of-cursors"></a>Tipos de cursor


**Aplica-se ao:** Access 2013, Office 2013

Como regra geral, o aplicativo deve usar o cursor mais simples que forneça o acesso a dados necessário. Cada característica adicional do cursor, além das básicas (somente encaminhamento, somente leitura, estático, rolagem, sem buffer) tem um preço  em memória do cliente, em carga ou em desempenho da rede. Em muitos casos, as opções padrão de cursor geram um cursor mais complexo do que a necessidade real do aplicativo.

A sua escolha do tipo de cursor depende de como o seu aplicativo usa o conjunto de resultados e também de várias considerações sobre design, inclusive o tamanho do conjunto de resultados, a porcentagem de dados com probabilidade de uso, a sensibilidade às alterações dos dados e os requisitos de desempenho do aplicativo.

Na sua forma mais básica, a escolha do cursor depende da sua necessidade de alterar os dados ou apenas de exibi-los:

  - Se você precisa apenas rolar um conjunto de resultados, sem alterar os dados, use um cursor [somente de encaminhamento](forward-only-cursors.md) ou [estático](static-cursors.md).

  - Se você tiver um grande conjunto de resultados e precisar selecionar apenas algumas linhas, use um cursor de [conjunto de chaves](keyset-cursors.md).

  - Se desejar sincronizar um conjunto de resultados com inclusões, alterações e exclusões recentes feitas por todos os usuários atuais, use um cursor [dinâmico](dynamic-cursors.md).

Embora cada tipo de cursor pareça distinto, lembre-se de que esses tipos não são variedades tão diferentes, mas o simples resultado da sobreposição de características e opções.

