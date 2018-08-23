---
title: Enviar mensagens com TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e2df265-b9dd-4e19-8ca5-3e31804e9120
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9de158e2f269c7b000734beb93b26df195255bcf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592280"
---
# <a name="sending-messages-with-tnef"></a>Enviar mensagens com TNEF

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Muitos provedores de transporte enviam automaticamente todas as mensagens enviadas com o TNEF Transport Neutral Encapsulation Format (). TNEF é usado para transmitir o texto formatado que o suportam de vários clientes e provedores de armazenamento de mensagem em suas mensagens, os anexos de vários tipos e propriedades personalizadas para classes de mensagem personalizada. Embora o modo padrão para a maioria dos provedores de transporte enviar mensagens de saída com o TNEF, alguns provedores de transporte não suportá-las. A falta de suporte para o TNEF não é um problema para os clientes de mensagens padrão que enviam e recebem mensagens IPM. No entanto, para clientes baseados no formulário ou clientes que requerem propriedades personalizadas, a utilização de TNEF é essencial. Os designers de clientes que dependem de formulários ou propriedades personalizadas devem estar cientes dos recursos dos provedores de transporte que eles usam.
  
Os destinatários da mensagem podem controlar ou não um provedor de transporte transmite mensagens com TNEF, definindo a propriedade **PR_SEND_RICH_INFO** . Para obter mais informações, consulte **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Quando a propriedade **PR_SEND_RICH_INFO** do destinatário é definida como TRUE, um provedor de transporte que ofereça suporte TNEF transmite com a mensagem. Quando a propriedade é definida como FALSE, a formatação é descartada. Quando **PR_SEND_RICH_INFO** não existir, é o provedor de transporte para escolher um curso padrão de ação. 
  
Quando os clientes e provedores de serviços criam um destinatário personalizado, eles podem afetar o valor de sua propriedade **PR_SEND_RICH_INFO** passando o sinalizador MAPI_SEND_NO_RICH_INFO no parâmetro _ulFlags_ ao **IAddrBook::CreateOneOff** ou ** IMAPISupport::CreateOneOff** chamada. Para obter mais informações, consulte [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) e [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Passar MAPI_SEND_NO_RICH_INFO faz com que o MAPI definir a propriedade **PR_SEND_RICH_INFO** do destinatário personalizado como FALSE; Na maioria dos casos não passando o sinalizador faz o MAPI definir a propriedade como TRUE. A única exceção é se o endereço do destinatário personalizado será interpretado deve para ser um endereço de Internet. Nessa situação um, MAPI define **PR_SEND_RICH_INFO** como FALSE. 
  

