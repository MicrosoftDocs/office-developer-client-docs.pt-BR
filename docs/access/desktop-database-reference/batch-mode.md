---
title: Modo de lotes (referência de banco de dados da área de trabalho do Access)
TOCTitle: Batch Mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37f66f6ef6c4ed63b106584a6ac5118cddf20526
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861195"
---
# <a name="batch-mode"></a>Modo em Lote


**Aplica-se a**: Access 2013 | Office 2013

O modo de processamento em lotes é efetivo quando a propriedade **LockType** está definida como **adLockBatchOptimistic** e a atualização em lotes tem o suporte do provedor. Certas configurações de tipo de bloqueio não estão disponíveis, dependendo do local do cursor. Por exemplo, um tipo de bloqueio pessimista não está disponível quando **CursorLocation** está definido como **adUseClient**. Por outro lado, um provedor pode não oferecer suporte para um bloqueio otimista em lotes quando o local do cursor é no servidor. Você deve usar a atualização em lotes somente com um cursor de conjunto de chaves ou estático.

O método **UpdateBatch** é usado para enviar ao servidor as alterações de **Recordset** retidas no buffer de cópia, a fim de atualizar a fonte de dados. Na próxima seção, abriremos um **Recordset** no modo de processamento em lotes, faremos alterações no buffer de cópia e, em seguida, enviaremos as alterações para a fonte de dados usando uma chamada para **UpdateBatch**.

Esta seção inclui os seguintes tópicos:

- [Envio de atualizações: UpdateBatch](sending-the-updates-updatebatch.md)

- [Filtragem de registros atualizados](filtering-for-updated-records.md)

- [Como lidar com atualizações com falhas](dealing-with-failed-updates.md)

- [Detecção e solução de conflitos](detecting-and-resolving-conflicts.md)

- [Desconexão e reconexão do conjunto de registros](disconnecting-and-reconnecting-the-recordset.md)

- [Atualizando os resultados JOINed: Unique Table](updating-joined-results-unique-table.md)

