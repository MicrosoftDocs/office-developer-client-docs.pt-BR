---
title: Eventos WillChangeRecord e RecordChangeComplete (ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0113a7b22d0bba8e843ce9583e93eef848f872a5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710836"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a>Eventos WillChangeRecord e RecordChangeComplete (ADO)

**Aplica-se a**: Access 2013, o Office 2013

O evento **WillChangeRecord** é chamado antes da alteração de um ou mais registros (linhas) no [Recordset](recordset-object-ado.md). O evento **RecordChangeComplete** é chamado depois da alteração de um ou mais registros.

## <a name="syntax"></a>Sintaxe

WillChangeRecord*adReason*, *cRecords*, *adStatus*, *pRecordset*

RecordChangeComplete*adReason*, *cRecords*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*adReason* |Um valor [EventReasonEnum](eventreasonenum.md) que especifica a razão para esse evento. Seu valor pode ser **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** ou **adRsnFirstChange**.|
|*cRecords* |Um valor **Long** que indica o número de registros que foram alterados (afetados).|
|*pError* |Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Quando **WillChangeRecord** é chamado, esse parâmetro é definido como **adStatusOK** se a operação que gerou o evento foi bem-sucedida. Ele será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação pendente. <br/><br/>Quando **RecordChangeComplete** é chamado, esse parâmetro é definido como **adStatusOK** se a operação que gerou o evento foi bem-sucedida, ou como **adStatusErrorsOccurred** se a operação falhar. <br/><br/>Antes do retorno de **WillChangeRecord**, defina esse parâmetro como **adStatusCancel**, para solicitar o cancelamento da operação que gerou esse evento, ou como adStatusUnwantedEvent para evitar notificações subsequentes. <br/><br/>Antes do retorno de **RecordChangeComplete**, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.|
|*pRecordset* |Um objeto **Recordset**. O **Recordset** para o qual esse evento ocorreu.|

## <a name="remarks"></a>Comentários

Um evento **WillChangeRecord** ou **RecordChangeComplete** pode ocorrer para o campo alterado em uma linha devido às seguintes operações de **Recordset**: [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) e [CancelBatch](cancelbatch-method-ado.md). O valor do **Recordset** [CursorType](cursortype-property-ado.md) determina quais operações causam os eventos ocorra.

Durante o evento **WillChangeRecord** , a propriedade de [filtro](filter-property-ado.md) de **conjunto de registros** é definida como **adFilterAffectedRecords**. Você não poderá alterar essa propriedade enquanto estiver processando o evento.

Você deve definir o parâmetro adStatus como adStatusUnwantedEvent para cada valor adReason possível, a fim de interromper totalmente as notificações de qualquer evento que inclua o parâmetro adReason.

