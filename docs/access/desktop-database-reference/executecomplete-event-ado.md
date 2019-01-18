---
title: Evento ExecuteComplete (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8a094968e70ace5e6cba1df184bf0ba57c2d7789
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698089"
---
# <a name="executecomplete-event-ado"></a>Evento ExecuteComplete (ADO)

**Aplica-se a**: Access 2013, o Office 2013

O evento **ExecuteComplete** é chamado depois que um comando terminar a execução.

## <a name="syntax"></a>Sintaxe

Do ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*RecordsAffected* |Um valor **Long** que indica o número de registros afetados pelo comando.|
|*pError* |Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de **adStatus** for **adStatusErrorsOccurred**; caso contrário, não será definido.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Antes que esse evento seja retornado, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.|
|*pCommand* |O objeto [Command](command-object-ado.md) que foi executado. Contém um objeto **Command** mesmo ao chamar **Connection.Execute** ou **Recordset.Open** sem criar explicitamente um **Command**, nesses casos o objeto **Command** será criado internamente por ADO.|
|*pRecordset* |Um objeto [Recordset](recordset-object-ado.md) que é o resultado do comando executado. Esse **Recordset** pode estar vazio. Você nunca deve destruir esse objeto Recordset a partir dessa rotina de tratamento de eventos. Tal procedimento resultará em uma Violação de Acesso quando o ADO tentar acessar um objeto que não exista mais.|
|*pConnection* |Um objeto [Connection](connection-object-ado.md). A conexão sobre a qual a operação foi executada.|

## <a name="remarks"></a>Comentários

Um evento **ExecuteComplete** pode ocorrer devido aos métodos **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md) ou **Recordset.**[NextRecordset](nextrecordset-method-ado.md).

