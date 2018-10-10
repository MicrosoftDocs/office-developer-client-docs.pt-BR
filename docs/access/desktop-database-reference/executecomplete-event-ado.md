---
title: Evento ExecuteComplete (ADO)
TOCTitle: ExecuteComplete Event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c24b6c681c857dfa66f424d174bd7ce4a2cbd772
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462006"
---
# <a name="executecomplete-event-ado"></a>Evento ExecuteComplete (ADO)


**Aplica-se a**: Access 2013 | Office 2013



O evento **ExecuteComplete** é chamado depois que um comando terminar a execução.

## <a name="syntax"></a>Sintaxe

Do ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*

## <a name="parameters"></a>Parâmetros

  - *RecordsAffected*

  - Um valor **Long** que indica o número de registros afetados pelo comando.

  - *pError*

  - Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de **adStatus** for **adStatusErrorsOccurred**; caso contrário, não será definido.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Antes que esse evento seja retornado, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.

  - *pCommand*

  - O objeto [Command](command-object-ado.md) que foi executado. Contém um objeto **Command** mesmo ao chamar **Connection.Execute** ou **Recordset.Open** sem criar explicitamente um **Command**, nesses casos o objeto **Command** será criado internamente por ADO.

  - *pRecordset*

  - Um objeto [Recordset](recordset-object-ado.md) que é o resultado do comando executado. Esse **Recordset** pode estar vazio. Você nunca deve destruir esse objeto Recordset a partir dessa rotina de tratamento de eventos. Tal procedimento resultará em uma Violação de Acesso quando o ADO tentar acessar um objeto que não exista mais.

  - *pConnection*

  - Um objeto [Connection](connection-object-ado.md). A conexão sobre a qual a operação foi executada.

## <a name="remarks"></a>Comentários

Um evento **ExecuteComplete** pode ocorrer devido aos métodos **Connection.**[Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), **Command.**[Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md) ou **Recordset.**[NextRecordset](nextrecordset-method-ado.md).

