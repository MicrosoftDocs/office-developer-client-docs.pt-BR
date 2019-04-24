---
title: Tipos de eventos (referência de banco de dados de área de trabalho do Access)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3bcf631ffc6c9b4b847af3f973114d6b271d26f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314151"
---
# <a name="types-of-events"></a>Tipos de eventos


**Aplica-se ao:** Access 2013, Office 2013



Há dois tipos básicos de eventos. Os "eventos Will", chamados antes do início de uma operação, geralmente incluem "Will" nos nomes  por exemplo, **WillChangeRecordset** ou **WillConnect**. Os eventos chamados após a conclusão de um evento geralmente incluem "Complete" nos nomes  por exemplo, **RecordChangeComplete** ou **ConnectComplete**. Há exceções  como no caso de **InfoMessage**  mas elas ocorrem após a conclusão da operação associada.

## <a name="will-events"></a>Eventos Will

Os manipuladores de eventos chamados antes do início da operação permitem que você examine ou modifique os parâmetros de operação e, em seguida, cancele a operação ou permita sua conclusão. Essas rotinas de manipulador de eventos normalmente têm nomes do formulário **será*evento * * *.

## <a name="complete-events"></a>Eventos Complete

Os manipuladores de eventos chamados após a conclusão de uma operação podem notificar seu aplicativo de que a operação foi concluída. Esse manipulador de eventos também é notificado quando um manipulador de eventos Will cancela uma operação pendente. Essas rotinas de manipulador de eventos normalmente têm nomes do formulário ***evento * concluído**.

Os eventos Will e Complete geralmente são usados em pares.

## <a name="other-events"></a>Outros eventos

Os outros manipuladores de eventos, ou seja, os eventos cujos nomes não estão no formulário **serão * Event*** ou ***Event * Complete,** serão chamados apenas após a conclusão da operação. Esses eventos são o **Disconnect**, o **EndOfRecordset** e o **InfoMessage**.

