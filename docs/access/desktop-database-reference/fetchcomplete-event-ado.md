---
title: Evento FetchComplete (ADO)
TOCTitle: FetchComplete Event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 299fec4a831bbde5d3fd2d58e0f76edb2acea0f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464037"
---
# <a name="fetchcomplete-event-ado"></a>Evento FetchComplete (ADO)


**Aplica-se a**: Access 2013 | Office 2013


O evento **FetchComplete** é chamado depois de todos os registros em uma operação assíncrona prolongada terem sido recuperados no [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxe

FetchComplete*pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parâmetros

  - *pError*

  - Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de **adStatus** for **adStatusErrorsOccurred**; caso contrário, não será definido.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Antes de este evento retornar, defina este parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.

  - *pRecordset*

  - Um objeto **Recordset**. O objeto para o qual os registros foram recuperados.

## <a name="remarks"></a>Comentários

Para usar **FetchComplete** com o Microsoft Visual Basic, é necessário o Visual Basic 6.0 ou posterior.

