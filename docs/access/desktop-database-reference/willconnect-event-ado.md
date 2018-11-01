---
title: Evento WillConnect (ADO)
TOCTitle: WillConnect Event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 51d9d0b11d137fbca8bf5efdddfe51469642c405
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887167"
---
# <a name="willconnect-event-ado"></a>Evento WillConnect (ADO)


**Aplica-se a**: Access 2013, o Office 2013


O evento **WillConnect** é chamado antes que uma conexão seja iniciada.

## <a name="syntax"></a>Sintaxe

WillConnect*ConnectionString*, *UserID*, *senha*, *Opções*, *adStatus*, *pConnection*

## <a name="parameters"></a>Parâmetros

  - *ConnectionString*

  - Uma **String** que contém informações de conexão para a conexão pendente.

  - *UserID*

  - Um **String** que contém um nome de usuário para a conexão pendente.

  - *Password*

  - Uma **String** que contém uma senha para a conexão pendente.

  - *Options*

  - Um valor **Long** que indica como o provedor deve avaliar o *ConnectionString*. Sua única opção é **adAsyncOpen**.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Quando esse evento é chamado, esse parâmetro é definido como **adStatusOK**, por padrão. Ele será definido como **adStatusCantDeny** se o evento não puder solicitar o cancelamento da operação pendente.
    
    Antes que esse evento seja retornado, defina esse parâmetro como **adStatusUnwantedEvent** para impedir notificações subsequentes. Defina esse parâmetro como **adStatusCancel** para solicitar uma operação de conexão que provocou o cancelamento dessa notificação.

  - *pConnection*

  - O objeto [Connection](connection-object-ado.md) ao qual essa notificação de evento se aplica. As alterações aos parâmetros de **Connection** pela manipulador de eventos **WillConnect** não terão efeito no **Connection**.

## <a name="remarks"></a>Comentários

Quando o **WillConnect** é chamado, os parâmetros *ConnectionString*, *UserID*, *Password* e *Options* são definidos como os valores estabelecidos pela operação que provocou esse evento (a conexão pendente) e podem ser alterados antes que o evento seja retornado. O **WillConnect** pode retornar uma solicitação para que a conexão pendente seja cancelada.

Quando esse evento for cancelado, **ConnectComplete** será chamado com seu parâmetro *adStatus* definido como **adStatusErrorsOccurred**.

