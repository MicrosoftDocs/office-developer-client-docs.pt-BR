---
title: Tipos de eventos (referência de banco de dados da área de trabalho do Access)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ffb3bd48db4d8071e56553f4ea5bf79b83952466
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463632"
---
# <a name="types-of-events"></a>Tipos de eventos


**Aplica-se a**: Access 2013 | Office 2013



Há dois tipos básicos de eventos. Os "eventos Will", chamados antes do início de uma operação, geralmente incluem "Will" nos nomes  por exemplo, **WillChangeRecordset** ou **WillConnect**. Os eventos chamados após a conclusão de um evento geralmente incluem "Complete" nos nomes  por exemplo, **RecordChangeComplete** ou **ConnectComplete**. Há exceções  como no caso de **InfoMessage**  mas elas ocorrem após a conclusão da operação associada.

## <a name="will-events"></a>Eventos Will

Os manipuladores de eventos chamados antes do início da operação permitem que você examine ou modifique os parâmetros de operação e, em seguida, cancele a operação ou permita sua conclusão. Essas rotinas de manipulador de eventos geralmente têm nomes do formulário **irá*evento * * *.

## <a name="complete-events"></a>Eventos Complete

Os manipuladores de eventos chamados após a conclusão de uma operação podem notificar seu aplicativo de que a operação foi concluída. Esse manipulador de eventos também é notificado quando um manipulador de eventos Will cancela uma operação pendente. Essas rotinas de manipulador de eventos geralmente têm nomes do formulário ***evento * Complete**.

Os eventos Will e Complete geralmente são usados em pares.

## <a name="other-events"></a>Outros eventos

Manipuladores de eventos — ou seja, os eventos cujos nomes não estiverem no formato **será * evento*** ou ***evento * Complete —** são chamados somente quando uma operação for concluída. Esses eventos são o **Disconnect**, o **EndOfRecordset** e o **InfoMessage**.

