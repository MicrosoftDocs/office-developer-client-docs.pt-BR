---
title: Enviar mensagens com TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e2df265-b9dd-4e19-8ca5-3e31804e9120
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7ff7f79b5e74412e9bbb4b4882c6a7d45e50fe6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420847"
---
# <a name="sending-messages-with-tnef"></a>Enviar mensagens com TNEF

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Muitos provedores de transporte enviam automaticamente todas as mensagens de saída com o TNEF (Transport Neutral Encapsulation Format). O TNEF é usado para transmitir o texto formatado que muitos clientes e provedores de armazenamento de mensagens suportam em suas mensagens, anexos de vários tipos e propriedades personalizadas para classes de mensagens personalizadas. Embora o modo padrão para a maioria dos provedores de transporte seja enviar mensagens de saída com TNEF, alguns provedores de transporte não suportam. A falta de suporte para TNEF não é um problema para clientes de mensagens padrão que enviam e recebem mensagens IPM. No entanto, para clientes baseados em formulário ou clientes que exigem propriedades personalizadas, o uso de TNEF é essencial. Os designers de clientes que dependem de formulários ou propriedades personalizadas devem estar cientes dos recursos dos provedores de transporte que eles usam.
  
Os destinatários da mensagem podem controlar se um provedor de transporte transmite mensagens com TNEF definindo a **propriedade PR_SEND_RICH_INFO** transporte. Para obter mais informações, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Quando a propriedade PR_SEND_RICH_INFO **de** um destinatário é definida como TRUE, um provedor de transporte que oferece suporte a TNEF a transmite com a mensagem. Quando a propriedade é definida como FALSE, a formatação é descartada. Quando **PR_SEND_RICH_INFO** não existe, fica a responsabilidade do provedor de transporte em escolher um curso de ação padrão. 
  
Quando clientes e provedores de serviços criam um destinatário personalizado, eles podem afetar o valor de sua propriedade **PR_SEND_RICH_INFO** passando o sinalizador MAPI_SEND_NO_RICH_INFO no parâmetro _ulFlags_ para a chamada **IAddrBook::CreateOneOff** ou **IMAPISupport::CreateOneOff.** Para obter mais informações, consulte [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) e [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Passar MAPI_SEND_NO_RICH_INFO faz com que o MAPI de definir a propriedade de PR_SEND_RICH_INFO **personalizada** como FALSO; na maioria dos casos, não passar o sinalizador faz com que MAPI de definir a propriedade como TRUE. A única exceção é se o endereço do destinatário personalizado for interpretado como sendo um endereço da Internet. Nesta situação, MAPI **define** PR_SEND_RICH_INFO como FALSE. 
  

