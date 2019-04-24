---
title: Enviando relatórios de entrega de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2a31e7d088d5c1f94b272cb4d307f3aff99f32ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332834"
---
# <a name="sending-message-delivery-reports"></a>Enviando relatórios de entrega de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Alguns sistemas de mensagens subjacentes dão suporte a relatórios de entrega e outros não. Como o provedor de transporte determina se as notificações de entrega de mensagens ou de não entrega podem ser enviadas para aplicativos clientes é um detalhe de implementação específico para provedores de transporte individuais. Se os relatórios de entrega podem ser enviados para aplicativos cliente, os provedores de transporte usam o método [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) para notificar o MAPI sobre a entrega bem-sucedida ou malsucedida para um ou mais destinatários. Em seguida, o MAPI gera relatórios de entrega ou não entrega correspondentes a esses destinatários. Os provedores de transporte também podem traduzir os relatórios de entrega e não entrega de entrada que são nativos do sistema de mensagens em notificações de entrega e de não-entrega de MAPI por meio do **StatusRecips**.
  

