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
ms.openlocfilehash: 717494f30fd4d43e94a7c6a37770e2eab8ebb59e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593596"
---
# <a name="sending-message-delivery-reports"></a>Enviar relatórios de entrega de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Alguns sistemas de mensagens subjacentes ofereçam suporte a notificações de entrega e outros não. Como o provedor de transporte determina se os relatórios de entrega ou não entrega de mensagem podem ser enviados para aplicativos cliente é um detalhe da implementação específico de provedores de transporte individual. Se podem ser enviadas notificações de entrega para aplicativos clientes, provedores de transporte usam o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para notificar o MAPI de entrega ou não êxito para um ou mais destinatários. MAPI, em seguida, gera relatórios de entrega ou NDRs correspondente a esses destinatários. Provedores de transporte também podem converter a entrada relatórios de entrega e de não entrega são nativos do sistema de mensagens para entrega MAPI e NDRs por meio de **StatusRecips**.
  

