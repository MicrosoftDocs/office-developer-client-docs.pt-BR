---
title: 'Capítulo 5: Atualização e dados persistentes'
TOCTitle: 'Chapter 5: Updating and Persisting Data'
ms:assetid: 77acb763-1c60-1945-791d-3e83d684fb0d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249493(v=office.15)
ms:contentKeyID: 48545732
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 487fd11112375fb0f5788505d049a4fc71e245ba
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861971"
---
# <a name="chapter-5-updating-and-persisting-data"></a>Capítulo 5: Atualização e dados persistentes


**Aplica-se a**: Access 2013 | Office 2013

Os capítulos anteriores abordavam como usar o ADO para obter dados em uma fonte de dados, como mover-se nos dados e até mesmo como editá-los. Obviamente, se o objetivo do aplicativo for permitir que os usuários façam alterações nos dados, você precisará entender como salvar essas alterações. Você pode manter as alterações do **Recordset** em um arquivo usando o método **Save** ou enviar as alterações de volta para a fonte de dados para armazenamento, usando os métodos **Update** ou **UpdateBatch**.

Nos capítulos anteriores, você alterou os dados em várias linhas do **Recordset**. O ADO oferece suporte a duas noções básicas relacionadas à adição, exclusão e modificação de linhas de dados.

A primeira noção é de que as alterações não são feitas imediatamente no **Recordset**; elas são feitas em um *buffer de cópia* interno. Se você decidir que não deseja as alterações, as modificações no buffer de cópia serão descartadas. Se você decidir mantê-las, as alterações no buffer de cópia serão aplicadas ao **Recordset**.

A segunda noção é que as alterações são que um propagadas para a fonte de dados assim que você declara o trabalho em uma linha completa (ou seja, modo *imediato* ) ou todas as alterações em um conjunto de linhas são coletadas até que você declara o trabalho para o conjunto completo (que é modo *em lote* ). A propriedade **LockType** determina quando as alterações são feitas na fonte de dados subjacente. **adLockOptimistic** ou **adLockPessimistic** especifica o modo imediato, enquanto **adLockBatchOptimistic** especifica o modo de lote. A propriedade **CursorLocation** pode afetar quais configurações **LockType** estão disponíveis. Por exemplo, não há suporte para a configuração **adLockPessimistic** se a propriedade **CursorLocation** estiver definida como **adUseClient**.

No modo imediato, cada invocação do método **Update** propaga as alterações na fonte de dados. No modo de lote, cada invocação de **Update** ou movimento da posição da linha atual salva as alterações no buffer de cópia, mas apenas o método **UpdateBatch** propaga as alterações para a fonte de dados.

Este capítulo aborda os seguintes tópicos:

- [Atualizando dados (ADO)](updating-data.md)

- [Mantendo dados (ADO)](persisting-data.md)