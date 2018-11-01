---
title: Eventos WillChangeRecordset e RecordsetChangeComplete (ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete Events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a7bf9a69fd5a648efc86f698e82ca0ba9413a30
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886309"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a>Eventos WillChangeRecordset e RecordsetChangeComplete (ADO)


**Aplica-se a**: Access 2013, o Office 2013


O evento **WillChangeRecordset** é cancelado antes que uma operação pendente altere [Recordset](recordset-object-ado.md). O evento **RecordsetChangeComplete** é chamado depois que o **Recordset** for chamado.

## <a name="syntax"></a>Sintaxe

WillChangeRecordset*adReason*, *adStatus*, *pRecordset*

RecordsetChangeComplete*adReason*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parâmetros

  - *adReason*

  - Um valor [EventReasonEnum](eventreasonenum.md) que especifica a razão para esse evento. Seu valor pode ser **adRsnRequery**, **adRsnResynch**, **adRsnClose**, **adRsnOpen**.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Quando **WillChangeRecordset** for chamado, esse parâmetro será definido como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida. Ele será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação pendente.
    
    Quando **RecordsetChangeComplete** for chamado, esse parâmetro será configurado como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida, **adStatusErrorsOccurred** se a operação tiver falhado ou **adStatusCancel** se a operação associada ao evento **WillChangeRecordset** anteriormente aceito tiver sido cancelada.
    
    Antes que **WillChangeRecordset** seja retornado, defina esse parâmetro como **adStatusCancel** para solicitar o cancelamento da operação pendente ou defina esse parâmetro como adStatusUnwantedEvent para evitar notificações subsequentes.
    
    Antes que **WillChangeRecordset** ou **RecordsetChangeComplete** seja retornado, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.

  - *pError*

  - Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.

  - *pRecordset*

  - Um objeto **Recordset**. O **Recordset** para o qual esse evento ocorreu.

## <a name="remarks"></a>Comentários

Um **WillChangeRecordset** ou **RecordsetChangeComplete** evento pode ocorrer devido aos métodos **Recordset** [Requery](requery-method-ado.md) ou [Open](open-method-ado-recordset.md) .

Se o provedor não suportar indicadores, ocorrerá uma notificação de evento **RecordsetChange** sempre que novas linhas forem obtidas junto ao provedor. A frequência desse evento depende da propriedade **RecordsetCacheSize**.

Você deve definir o parâmetro **adStatus** como **adStatusUnwantedEvent** para cada valor **adReason** possível para parar completamente a notificação de evento para qualquer evento que inclua um parâmetro **adReason**.

