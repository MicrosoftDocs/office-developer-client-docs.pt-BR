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
ms.openlocfilehash: ddbaa4aeacf17f2c266ccc0ff963d005f9e403ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410109"
---
# <a name="sending-across-messaging-domains"></a>Enviar entre domínios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um domínio de mensagens representa um ou mais sistemas de mensagens que compartilham um formato de endereço comum. A comunicação entre vários domínios de mensagens envolve a tradução de uma mensagem enviada no formato do domínio de mensagens original para o formato do domínio de mensagens de destino. Como nem todos os formatos de endereço são compatíveis, um gateway é necessário para traduzir as informações de endereçamento do formato de origem para o formato de destino. Para garantir a validade entre domínios de mensagens, os aplicativos cliente armazenam informações de endereçamento importantes nas propriedades MAPI. Além disso, os gateways executam a tradução, examinando as propriedades conhecidas por precisar de tradução e alterando-as para um formato que o domínio de mensagens de destino pode usar.
  
Anteriormente, o MAPI permitia que essas informações de endereçamento fosse associadas apenas aos usuários que compõem a lista de destinatários atual de uma mensagem. As propriedades que descrevem cada membro da lista de destinatários subscreviam a tradução necessária pelo gateway para garantir a validade entre domínios de mensagens. No entanto, alguns aplicativos exigem que suas mensagens incluam informações de endereçamento sobre usuários que talvez eram destinatários no passado, sejam destinatários no futuro ou nunca serão destinatários. Por exemplo, os aplicativos de roteamento, que enviam mensagens em uma ordem especificada para um grupo de usuários, incorporam informações de endereçamento sobre esses usuários nas mensagens. As informações incorporadas normalmente incluem o endereço e o tipo de endereço dos futuros destinatários, e talvez também suas funções e posições na ordem de roteamento, seus nomes e um ou mais identificadores binários por destinatário.
  
Para permitir que as mensagens incluam informações sobre esses usuários não-cipientes, o MAPI agora inclui uma estratégia para garantir que essas informações não-cipientes também são traduzidas corretamente entre domínios de mensagens. Essa estratégia baseia-se no conceito de propriedades de gateway mappable.
  

