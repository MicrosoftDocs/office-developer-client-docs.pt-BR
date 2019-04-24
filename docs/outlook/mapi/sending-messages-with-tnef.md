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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338490"
---
# <a name="sending-messages-with-tnef"></a>Enviar mensagens com TNEF

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Muitos provedores de transporte enviam mensagens de saída automaticamente com o formato TNEF (Transport neutral Encapsulation Format). O TNEF é usado para transmitir o texto formatado que muitos clientes e provedores de repositórios de mensagens dão suporte a suas mensagens, anexos de vários tipos e propriedades personalizadas para classes de mensagens personalizadas. Embora o modo padrão para a maioria dos provedores de transporte seja enviar mensagens de saída com TNEF, alguns provedores de transporte não dão suporte a ela. A falta de suporte para TNEF não é um problema para clientes de mensagens padrão que enviam e recebem mensagens IPM. No enTanto, para clientes baseados em formulário ou clientes que exigem Propriedades personalizadas, o uso de TNEF é essencial. Os designers de clientes que dependem de formulários ou propriedades personalizadas devem estar cientes dos recursos dos provedores de transporte usados.
  
Os destinatários da mensagem podem controlar se um provedor de transporte deve ou não transmitir mensagens com TNEF, definindo a propriedade **PR_SEND_RICH_INFO** . Para obter mais informações, consulte **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Quando a propriedade **PR_SEND_RICH_INFO** de um destinatário é definida como true, um provedor de transporte que oferece suporte a TNEF transmite-a com a mensagem. Quando a propriedade é definida como FALSE, a formatação é descartada. Quando o **PR_SEND_RICH_INFO** não existe, o provedor de transporte pode escolher um curso padrão de ação. 
  
Quando clientes e provedores de serviço criam um destinatário personalizado, eles podem afetar o valor de sua propriedade **PR_SEND_RICH_INFO** passando o sinalizador MAPI_SEND_NO_RICH_INFO no parâmetro _Parâmetroulflags_ para o **IAddrBook:: CreateOneOff** ou ** IMAPISupport:: CreateOneOff** chamada. Para obter mais informações, consulte [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) e [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md). Passar MAPI_SEND_NO_RICH_INFO faz com que o MAPI defina a propriedade **PR_SEND_RICH_INFO** do destinatário personalizado como false; na maioria dos casos, não passar o sinalizador faz com que o MAPI defina a propriedade como TRUE. A única exceção é se o endereço do destinatário personalizado é interpretado como um endereço de Internet. Nesta uma situação, o MAPI define **PR_SEND_RICH_INFO** como false. 
  

