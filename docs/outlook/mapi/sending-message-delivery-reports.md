---
title: Enviar relatórios de entrega de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d94785df9becf46bbfad66465facea35202c6079
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770360"
---
# <a name="sending-message-delivery-reports"></a>Enviar relatórios de entrega de mensagens

  
  
**Aplica-se a**: Outlook 
  
Alguns sistemas de mensagens subjacentes ofereçam suporte a notificações de entrega e outros não. Como o provedor de transporte determina se os relatórios de entrega ou não entrega de mensagem podem ser enviados para aplicativos cliente é um detalhe da implementação específico de provedores de transporte individual. Se podem ser enviadas notificações de entrega para aplicativos clientes, provedores de transporte usam o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para notificar o MAPI de entrega ou não êxito para um ou mais destinatários. MAPI, em seguida, gera relatórios de entrega ou NDRs correspondente a esses destinatários. Provedores de transporte também podem converter a entrada relatórios de entrega e de não entrega são nativos do sistema de mensagens para entrega MAPI e NDRs por meio de **StatusRecips**.
  

