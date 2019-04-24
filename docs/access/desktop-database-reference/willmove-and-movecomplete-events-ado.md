---
title: Eventos WillMove e MoveComplete (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e663e18a13803097d490e0e315d139e6e15400da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306047"
---
# <a name="willmove-and-movecomplete-events-ado"></a>Eventos WillMove e MoveComplete (ADO)

**Aplica-se ao:** Access 2013, Office 2013

O evento **WillMove** é chamado antes que a operação pendente altere a sua posição atual no [Recordset](recordset-object-ado.md). O evento **MoveComplete** é chamado depois da alteração da posição atual no **Recordset**.

## <a name="syntax"></a>Sintaxe

WillMove*adReason*, *adStatus*, ** precaboset

MoveComplete*adReason*, *perror*, *adStatus*, ** precaboset

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*adReason* |Um valor [EventReasonEnum](eventreasonenum.md) que especifica a razão para esse evento. Seu valor pode ser **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** ou **adRsnRequery**.|
|*pError* |Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Quando **WillMove** é chamado, esse parâmetro é definido como **adStatusOK** se a operação que gerou o evento foi bem-sucedida. Ele será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação pendente. <br/><br/>Quando **MoveComplete** é chamado, esse parâmetro é definido como **adStatusOK** se a operação que gerou o evento foi bem-sucedida, ou como **adStatusErrorsOccurred** se a operação falhar. <br/><br/>Antes do retorno de **WillMove**, defina esse parâmetro como **adStatusCancel**, para solicitar o cancelamento da operação pendente, ou como adStatusUnwantedEvent para evitar notificações subsequentes. <br/><br/>Antes do retorno de **MoveComplete**, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.|
|*precaboset* |Um objeto [Recordset](recordset-object-ado.md). O **Recordset** para o qual esse evento ocorreu.|

## <a name="remarks"></a>Comentários

Um evento **WillMove** ou **MoveComplete** pode ocorrer devido às seguintes operações de **Recordset** :

- [Open](open-method-ado-recordset.md)
- [Move](move-method-ado.md)
- [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [AddNew](addnew-method-ado.md)
- [Requery](requery-method-ado.md)

Esses eventos podem ocorrer devido às seguintes propriedades:

- [Filter](filter-property-ado.md)
- [Índice](index-property-ado.md)
- [Bookmark](bookmark-property-ado.md)
- [AbsolutePage](absolutepage-property-ado.md)
- [AbsolutePosition](absoluteposition-property-ado.md)

Esses eventos também ocorrerão se um **Recordset** filho tiver eventos **Recordset** conectados e se o **Recordset** pai for movido.

Você deve definir o parâmetro *adStatus* como **adStatusUnwantedEvent** para cada valor *adReason* possível para parar completamente a notificação de evento para qualquer evento que inclua um parâmetro *adReason*.

