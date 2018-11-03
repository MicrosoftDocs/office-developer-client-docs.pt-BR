---
title: Modo de lotes (referência de banco de dados da área de trabalho do Access)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9541e8b7888f5fb5f16bcfb343d545cf304b1afd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945786"
---
# <a name="batch-mode"></a>Modo de lotes

**Aplica-se a**: Access 2013, o Office 2013

O modo de processamento em lotes é efetivo quando a propriedade **LockType** está definida como **adLockBatchOptimistic** e a atualização em lotes tem o suporte do provedor. Certas configurações de tipo de bloqueio não estão disponíveis, dependendo do local do cursor. Por exemplo, um tipo de bloqueio pessimista não está disponível quando **CursorLocation** está definido como **adUseClient**. Por outro lado, um provedor pode não oferecer suporte para um bloqueio otimista em lotes quando o local do cursor é no servidor. Você deve usar a atualização em lotes somente com um cursor de conjunto de chaves ou estático.

O método **UpdateBatch** é usado para enviar ao servidor as alterações de **Recordset** retidas no buffer de cópia, a fim de atualizar a fonte de dados. Na próxima seção, abriremos um **Recordset** no modo de processamento em lotes, faremos alterações no buffer de cópia e, em seguida, enviaremos as alterações para a fonte de dados usando uma chamada para **UpdateBatch**.

Esta seção inclui os seguintes tópicos:

- [Enviando atualizações: UpdateBatch](sending-the-updates-updatebatch.md)
- [Filtrando registros atualizados](filtering-for-updated-records.md)
- [Lidando com falhas de atualização](dealing-with-failed-updates.md)
- [Detectando e resolvendo conflitos](detecting-and-resolving-conflicts.md)
- [Desconectando e reconectando o Recordset](disconnecting-and-reconnecting-the-recordset.md)
- [Atualizando ingressado for resultados: Unique Table](updating-joined-results-unique-table.md)

