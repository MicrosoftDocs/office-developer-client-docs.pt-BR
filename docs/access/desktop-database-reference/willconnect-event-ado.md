---
title: Evento WillConnect (ADO)
TOCTitle: WillConnect event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e62a01d274752b33f7bf3f6f4af6171e7efb16b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305884"
---
# <a name="willconnect-event-ado"></a>Evento WillConnect (ADO)

**Aplica-se ao:** Access 2013, Office 2013

O evento **WillConnect** é chamado antes que uma conexão seja iniciada.

## <a name="syntax"></a>Sintaxe

WillConnect*ConnectionString*, *userid*, *senha*, *Opções*, *adStatus*, *pConnection*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*ConnectionString* |Uma **String** que contém informações de conexão para a conexão pendente.|
|*UserID* |Um **String** que contém um nome de usuário para a conexão pendente.|
|*Password* |Uma **String** que contém uma senha para a conexão pendente.|
|*Options* |Um valor **Long** que indica como o provedor deve avaliar o *ConnectionString*. Sua única opção é **adAsyncOpen**.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Quando esse evento é chamado, esse parâmetro é definido como **adStatusOK**, por padrão. Ele será definido como **adStatusCantDeny** se o evento não puder solicitar o cancelamento da operação pendente.<br/><br/>Antes que esse evento seja retornado, defina esse parâmetro como **adStatusUnwantedEvent** para impedir notificações subsequentes. Defina esse parâmetro como **adStatusCancel** para solicitar uma operação de conexão que provocou o cancelamento dessa notificação.|
|*pConnection* |O objeto [Connection](connection-object-ado.md) ao qual essa notificação de evento se aplica. As alterações aos parâmetros de **Connection** pela manipulador de eventos **WillConnect** não terão efeito no **Connection**.|

## <a name="remarks"></a>Comentários

Quando o **WillConnect** é chamado, os parâmetros *ConnectionString*, *UserID*, *Password* e *Options* são definidos como os valores estabelecidos pela operação que provocou esse evento (a conexão pendente) e podem ser alterados antes que o evento seja retornado. O **WillConnect** pode retornar uma solicitação para que a conexão pendente seja cancelada.

Quando esse evento for cancelado, **ConnectComplete** será chamado com seu parâmetro *adStatus* definido como **adStatusErrorsOccurred**.

