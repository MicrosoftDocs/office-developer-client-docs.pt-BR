---
title: Enviando entre domínios de mensagens
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
# <a name="sending-across-messaging-domains"></a>Enviando entre domínios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um domínio de mensagens representa um ou mais sistemas de mensagens que compartilham um formato de endereço comum. A comunicação entre vários domínios de mensagens envolve a conversão de uma mensagem enviada no formato do domínio de mensagens original no formato do domínio de mensagens de destino. Como nem todos os formatos de endereço são compatíveis, um gateway é necessário para traduzir as informações de endereçamento do formato de origem para o formato de destino. Para garantir a validade em domínios de mensagens, os aplicativos cliente armazenam informações importantes de endereçamento em propriedades MAPI. Além disso, os gateways realizam a tradução, examinando as propriedades conhecidas que precisam de tradução e alterando-as para um formato que o domínio de mensagens de destino possa usar.
  
Anteriormente, o MAPI permitia que essas informações de endereçamento sejam associadas somente aos usuários que compõem a lista de destinatários atual de uma mensagem. As propriedades que descrevem cada membro da lista de destinatários underwent a tradução necessária pelo gateway para garantir a validade em domínios de mensagens. No enTanto, alguns aplicativos exigem que suas mensagens incluam informações de endereçamento sobre usuários que talvez eram destinatários no passado, serão destinatários no futuro ou nunca serão destinatários. Por exemplo, aplicativos de roteamento, que enviam mensagens em uma ordem especificada para um grupo de usuários, inserem informações de endereçamento sobre esses usuários nas mensagens. As informações incorporadas normalmente incluem o endereço e o tipo de destinatários futuros, e talvez também suas funções e cargos na ordem de roteamento, seus nomes e um ou mais identificadores binários por destinatário.
  
Para permitir que as mensagens incluam informações sobre esses usuários não-destinatários, o MAPI agora inclui uma estratégia para garantir que essas informações não-destinatários também sejam convertidas corretamente nos domínios de mensagens. Essa estratégia é baseada no conceito de propriedades mapeadas pelo Gateway.
  

