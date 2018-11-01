---
title: Eventos WillMove e MoveComplete (ADO)
TOCTitle: WillMove and MoveComplete Events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3b1a0e119d857947b78eb6adcfc9a5b1ba87e055
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868830"
---
# <a name="willmove-and-movecomplete-events-ado"></a>Eventos WillMove e MoveComplete (ADO)


**Aplica-se a**: Access 2013, o Office 2013

O evento **WillMove** é chamado antes que a operação pendente altere a sua posição atual no [Recordset](recordset-object-ado.md). O evento **MoveComplete** é chamado depois da alteração da posição atual no **Recordset**.

## <a name="syntax"></a>Sintaxe

WillMove*adReason*, *adStatus*, *pRecordset*

MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parâmetros

  - *adReason*

  - Um valor [EventReasonEnum](eventreasonenum.md) que especifica a razão para esse evento. Seu valor pode ser **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** ou **adRsnRequery**.

  - *pError*

  - Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Quando **WillMove** é chamado, esse parâmetro é definido como **adStatusOK** se a operação que gerou o evento foi bem-sucedida. Ele será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação pendente.
    
    Quando **MoveComplete** é chamado, esse parâmetro é definido como **adStatusOK** se a operação que gerou o evento foi bem-sucedida, ou como **adStatusErrorsOccurred** se a operação falhar.
    
    Antes do retorno de **WillMove**, defina esse parâmetro como **adStatusCancel**, para solicitar o cancelamento da operação pendente, ou como adStatusUnwantedEvent para evitar notificações subsequentes.
    
    Antes do retorno de **MoveComplete**, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.

  - *pRecordset*

  - Um objeto [Recordset](recordset-object-ado.md). O **Recordset** para o qual esse evento ocorreu.

## <a name="remarks"></a>Comentários

Um evento **WillMove** ou **MoveComplete** pode ocorrer devido às seguintes operações de **Recordset**: [Open](open-method-ado-recordset.md), [Move](move-method-ado.md), [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [AddNew](addnew-method-ado.md) e [Requery](requery-method-ado.md). Esses eventos podem ocorrer devido às seguintes propriedades: [Filter](filter-property-ado.md), [Index](index-property-ado.md), [Bookmark](bookmark-property-ado.md), [AbsolutePage](absolutepage-property-ado.md) e [AbsolutePosition](absoluteposition-property-ado.md). Esses eventos também ocorrerão se um **Recordset** filho tiver eventos **Recordset** conectados e se o **Recordset** pai for movido.

Você deve definir o parâmetro **adStatus** como **adStatusUnwantedEvent** para cada valor adReason possível, a fim de interromper totalmente as notificações de qualquer evento que inclua o parâmetro adReason.

