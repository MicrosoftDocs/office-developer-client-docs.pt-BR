---
title: Evento InfoMessage (ADO)
TOCTitle: InfoMessage Event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6cc3b69eb3310d8e717605edd3d6fae32d635806
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465358"
---
# <a name="infomessage-event-ado"></a>Evento InfoMessage (ADO)


**Aplica-se a**: Access 2013 | Office 2013

O evento **InfoMessage** é chamado sempre que ocorre um aviso durante uma operação **ConnectionEvent**.

## <a name="syntax"></a>Sintaxe

InfoMessage*pError*, *adStatus*, *pConnection*

## <a name="parameters"></a>Parâmetros

  - *pError*

  - Um objeto [Error](error-object-ado.md). Este parâmetro contém quaisquer erros que são retornados. Se vários erros forem retornados, enumere a coleção de **Erros** para localizá-los.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Antes de este evento retornar, defina este parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.

  - *pConnection*

  - Um objeto [Connection](connection-object-ado.md). A conexão para a qual o aviso ocorreu. Por exemplo, os avisos podem ocorrer ao abrir um objeto **Connection** ou ao executar um [Comando](command-object-ado.md) em uma **Conexão**.

