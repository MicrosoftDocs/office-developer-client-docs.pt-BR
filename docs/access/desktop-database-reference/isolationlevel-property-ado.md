---
title: Propriedade IsolationLevel (ADO)
TOCTitle: IsolationLevel Property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7424258f4b5a69764189f33a902956f370a56094
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463769"
---
# <a name="isolationlevel-property-ado"></a>Propriedade IsolationLevel (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica o nível de isolamento de um objeto [Connection](connection-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor [IsolationLevelEnum](isolationlevelenum.md). O padrão é **adXactChaos**.

## <a name="remarks"></a>Comentários

Use a propriedade **IsolationLevel** para definir o nível de isolamento de um objeto **Connection**. A configuração só entrará em vigor na próxima vez em que você chamar o método [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Se o nível de isolamento solicitado estiver indisponível, o provedor poderá retornar o maior nível seguinte de isolamento.

A propriedade **IsolationLevel** é leitura/gravação.

**Uso de serviço de dados remotos** Quando usado em um objeto de Conexão do cliente, a propriedade **IsolationLevel** pode ser definida somente para **adXactUnspecified**.

Como os usuários estão trabalhando com objetos **Recordset** desconectados em um cache do lado do cliente, pode haver problemas com vários usuários. Por exemplo, quando dois usuários diferentes tentam atualizar o mesmo registro, o Remote Data Service simplesmente permite que o usuário que atualizar o registro primeiro "ganhe". A solicitação de atualização do segundo usuário falhará, apresentando um erro.
