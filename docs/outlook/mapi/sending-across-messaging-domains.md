---
title: Enviar entre domínios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 65594253-66cd-486a-aa5b-0bc719f761f0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 40c12a4010d51cb433b62558b5fe1d12afb583dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567061"
---
# <a name="sending-across-messaging-domains"></a>Enviar entre domínios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um domínio de mensagens representa um ou mais sistemas de mensagens que compartilham um formato de endereço comum. Comunicação entre vários domínios de mensagens envolve traduzir uma mensagem enviada no formato do domínio mensagens original para o formato do domínio de mensagens de destino. Porque nem todos os formatos de endereço são compatíveis, um gateway é necessária para traduzir as informações de endereçamento do formato de origem para o formato de destino. Para garantir a validade entre domínios de mensagens, aplicativos cliente armazenam informações de endereçamento importantes nas propriedades MAPI. Além disso, os gateways executam a conversão examinando as propriedades necessitam de conversão e alterá-los em um formato que o domínio de destino de mensagens pode usar.
  
MAPI permitido anteriormente, essas informações de endereçamento a ser associado a apenas os usuários que compõem a lista de destinatários da mensagem atual. As propriedades descrevendo cada membro da lista de destinatários sofreram a tradução necessária pelo gateway, para garantir a validade entre domínios de mensagens. No entanto, alguns aplicativos exigem que suas mensagens incluem lidando com informações sobre os usuários que estavam talvez destinatários no passado, serão destinatários no futuro ou nunca será destinatários. Por exemplo, aplicativos de roteamento, que enviar mensagens em uma ordem especificada para um grupo de usuários, incorporar lidando com informações sobre esses usuários nas mensagens. As informações inseridas normalmente incluem o endereço e o tipo de endereço de destinatários futuros e talvez também suas funções e posições em um ou mais identificadores binários por destinatário, seus nomes e a ordem de roteamento.
  
Para habilitar mensagens incluir informações sobre esses usuários nonrecipient, MAPI agora inclui uma estratégia para garantir que essas informações nonrecipient também são traduzidas corretamente entre domínios de mensagens. Essa estratégia baseia-se no conceito de propriedades podem ser mapeados gateway.
  

