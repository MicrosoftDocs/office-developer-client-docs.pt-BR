---
title: Evitar tecnologias sem suporte em suplementos gerenciados do Outlook
TOCTitle: Avoiding unsupported technologies in managed Outlook add-ins
ms:assetid: 365fd319-725f-4c4b-b6e7-575f78ed8bda
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610014(v=office.15)
ms:contentKeyID: 55119789
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 3ad968b856e67183172adfd5829cdc06e7551ab5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405697"
---
# <a name="avoiding-unsupported-technologies-in-managed-outlook-add-ins"></a>Evitar tecnologias sem suporte em suplementos gerenciados do Outlook

Determinadas tecnologias que antecedem o .NET Framework não são compatíveis com a programação de código gerenciado. Essas tecnologias incluem CDO (Collaboration Data Objects), MAPI (Messaging Application Programming Interface), conhecido como MAPI estendido, e Simple MAPI. Essas tecnologias foram projetadas e desenvolvidas com código não gerenciado e a Microsoft não fornece wrappers gerenciados oficiais para suportar seu uso em aplicativos gerenciados. 

Para saber mais, confira a seção "APIs que têm suporte no código gerenciado" no artigo [KB 266353: as diretrizes de suporte para desenvolvimento de mensagens do lado do cliente](https://go.microsoft.com/fwlink/?linkid=89209).

No entanto, o Microsoft Outlook oferece muitos recursos de modelo de objeto que realizam o que, anteriormente, apenas o ECO e o ECE (Exchange Client Extensions) resolviam para os desenvolvedores. Se você usa o CDO em um aplicativo do Outlook não gerenciado existente e a falta de suporte para CDO em soluções gerenciadas tiver impedido a migração do aplicativo para código gerenciado, considere atualizar sua solução para código gerenciado usando apenas o modelo de objeto do Outlook e o Assembly de Interoperabilidade Primário (PIA), sem ter que recorrer ao CDO. 

Para ver mais informações sobre uma plataforma do Outlook mais abrangente introduzida no Outlook 2007 para reduzir a dependência do CDO e do ECE, confira [Novidades para desenvolvedores no Outlook 2007 (Parte 1 de 2)](https://msdn.microsoft.com/library/bb226711\(v=office.15\)).

