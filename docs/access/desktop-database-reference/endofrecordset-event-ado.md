---
title: Evento EndOfRecordset (ADO)
TOCTitle: EndOfRecordset Event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a95ae75eb71ea50e08952418058f87bf54a40e45
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888122"
---
# <a name="endofrecordset-event-ado"></a>Evento EndOfRecordset (ADO)


**Aplica-se a**: Access 2013, o Office 2013



O evento **EndOfRecordset** é chamado quando houver uma tentativa de mover para uma linha após o final do [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxe

EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parâmetros

  - *fMoreData*

  - Uma **VARIANT\_BOOL** valor que, se definida como VARIANT\_TRUE, indica que mais linhas foram adicionadas ao **conjunto de registros**.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Quando **EndOfRecordset** for chamado, esse parâmetro será definido como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida. Será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação que provocou esse evento.
    
    Antes que **EndOfRecordset** seja retornado, configure esse parâmetro como **adStatusUnwantedEvent** para impedir as notificações subsequentes.

  - *pRecordset*

  - Um objeto **Recordset**. O **Recordset** para o qual esse evento ocorreu.

## <a name="remarks"></a>Comentários

Pode ocorrer um evento **EndOfRecordset** se a operação [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) falhar.

Esse manipulador eventos é chamada quando é feita uma tentativa de mover após o final do objeto **Recordset**, talvez como resultado de chamar **MoveNext**. No entanto, enquanto estiver nesse evento, você poderia recuperar mais registros de um banco de dados e anexá-los final do **Recordset**. Nesse caso, defina *fMoreData* como VARIANT\_TRUE e o retorno de **EndOfRecordset**. Em seguida, chame **MoveNext** novamente para acessar os registros recém-recuperados.

