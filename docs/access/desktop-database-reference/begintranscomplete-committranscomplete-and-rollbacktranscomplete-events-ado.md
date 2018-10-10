---
title: Eventos BeginTransComplete, CommitTransComplete, eventos de RollbackTransComplete (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 216f5a92ea4095d78b8df2b196a1607e40ae58d1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465306"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a>Eventos BeginTransComplete, CommitTransComplete e RollbackTransComplete (ADO)


**Aplica-se a**: Access 2013 | Office 2013


Esses eventos serão chamados depois que a operação associada no objeto [Connection](connection-object-ado.md) terminar a execução.

  - **BeginTransComplete** é chamado após a operação [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).

  - **CommitTransComplete** é chamado após a operação [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).

  - **RollbackTransComplete** é chamado após a operação [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).

## <a name="syntax"></a>Sintaxe

Do eventos BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*

CommitTransComplete*pError*, *adStatus*, *pConnection*

RollbackTransComplete*pError*, *adStatus*, *pConnection*

## <a name="parameters"></a>Parâmetros

  - *TransactionLevel*

  - Um valor **Long** que contém o novo nível de transação do **BeginTrans** que provocou esse evento.

  - *pError*

  - Um objeto [Error](error-object-ado.md). Ele descreve o erro que ocorreu se o valor EventStatusEnum for **adStatusErrorsOccurred**; caso contrário, ele não está definido.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Esses eventos podem impedir notificações subsequentes, definindo esse parâmetro como **adStatusUnwantedEvent** antes que o evento seja retornado.

  - *pConnection*

  - O objeto **Connection** para o qual esse evento ocorreu.

## <a name="remarks"></a>Comentários

No Visual C++, várias **Conexões** podem compartilhar o mesmo método de tratamento de eventos. O método usa o objeto **Connection** retornado para determinar o objeto que provocou o evento.

Se a propriedade [Attributes](attributes-property-ado.md) estiver definida como **adXactCommitRetaining** ou **adXactAbortRetaining**, uma nova transação será iniciada depois de confirmar ou cancelar uma transação. Use o evento **BeginTransComplete** para ignorar tudo, menos o primeiro evento de início de transação.

