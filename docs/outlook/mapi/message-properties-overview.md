---
title: Visão geral das propriedades da mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 447f54de-9f0d-4f73-89b6-bed9cfea9c15
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 515b4637f99b806c5c5bc6304f107f62ca6d9091
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420245"
---
# <a name="message-properties-overview"></a>Visão geral das propriedades da mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI divide as propriedades da mensagem em três tipos:
  
- Propriedades de conteúdo da mensagem.
    
- Propriedades de transmissão de mensagem, ou envelope.
    
- Propriedades do destinatário da mensagem.
    
As propriedades de conteúdo da mensagem descrevem o texto de uma mensagem. Cada classe de mensagem tem seu próprio conjunto de propriedades de conteúdo. MAPI define propriedades de conteúdo para mensagens de anotação e relatório; fica a responsabilidade dos clientes e provedores de armazenamento de mensagens que lidam com essas classes de mensagens para definir as propriedades adequadamente para suas implementações. **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) e **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) são exemplos de propriedades de conteúdo para mensagens de anotação. **PR_BODY** contém o conteúdo não formatado de  uma nota, enquanto PR_RTF_COMPRESSED contém a versão compactada do conteúdo formatado de uma nota. Para obter mais informações sobre intervalos de identificador de propriedade, consulte [Intervalos de Identificador de Propriedade.](property-identifier-ranges.md)
  
Para novas classes de mensagens, os clientes podem definir propriedades específicas do conteúdo de duas maneiras:
  
- Usando identificadores de propriedade no intervalo de propriedades de conteúdo de classe de mensagem personalizada: 0x6800 a 0x7BFF.
    
- Usando propriedades nomeadas que têm identificadores que se enquadram no 0x8000 através 0xFFFE intervalo.
    
O intervalo de identificadores para propriedades personalizadas de conteúdo de classe de mensagem está disponível para qualquer cliente que crie uma classe de mensagem personalizada. Portanto, um identificador de propriedade nesse intervalo pode ser usado para várias classes de mensagens. Os usuários das propriedades nesse intervalo não podem fazer suposições sobre o comportamento das propriedades. 
  
Para propriedades nomeadas, os clientes criam um nome que especifica um conjunto de propriedades e uma cadeia de caracteres ou um valor numérico para cada nova propriedade. Em seguida, os clientes associam a propriedade a um identificador no intervalo de propriedades nomeado. Os usuários de propriedades nomeadas os acessam por nome ou identificador por meio dos métodos [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp::GetNamesFromIDs.](imapiprop-getnamesfromids.md) 
  
As propriedades do envelope fornecem informações que são usadas para transmitir uma mensagem de um destinatário para outro. Assim como nas propriedades de conteúdo de mensagens, é possível que clientes ou provedores de serviços definam suas próprias propriedades de envelope para complementar aquelas definidas por MAPI. Os clientes e provedores de transporte definem as propriedades de envelope que o MAPI define com base na definição que o MAPI fornece. Os provedores de transporte que implementam recursos especiais podem definir suas próprias propriedades de envelope para expor esses recursos aos clientes. O MAPI reserva um intervalo de identificadores de propriedade que podem ser usados para essas propriedades especiais definidas pelo provedor. Os provedores de transporte normalmente implementam uma página de propriedades especiais para exibir essas propriedades e permitir que os clientes as alterem. **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) e **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) são exemplos de propriedades de envelope. Para obter mais informações, [consulte Intervalos de Identificador de Propriedade.](property-identifier-ranges.md)
  
As propriedades de destinatário descrevem o destino de uma mensagem enviada. Um destinatário pode ser um usuário de mensagens, uma lista de distribuição ou um computador. As propriedades de destinatário são definidas por MAPI e definidas por provedores de serviços. Algumas propriedades de destinatário são suportadas pelos provedores de listas de endereços para seus objetos de lista de distribuição e usuário de mensagens; outras propriedades de destinatário são suportadas por clientes, provedores de armazenamento de mensagens ou provedores de transporte. Por exemplo, todos os destinatários exigem um endereço e um tipo de endereço; são propriedades mantidas por um provedor de agendas de endereços quando o destinatário é armazenado em um de seus contêineres. Os destinatários também têm um tipo, **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)), que identifica um destinatário como um destinatário primário, com cópia carbono ou com cópia carbono.
  
Muitas propriedades de mensagem são opcionais, o que significa que os clientes não podem esperar que eles sejam disponibilizados ou definidos como valores válidos. Algumas propriedades de mensagem são necessárias, mas estão disponíveis somente quando uma mensagem está em um estado específico. Por exemplo, uma mensagem recém-criada não precisa ter um identificador de entrada até que a mensagem seja salva e não é necessário ter uma classe de mensagem até que a mensagem esteja pronta para ser enviada. Os clientes sempre devem verificar os resultados de suas chamadas [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::OpenProperty](imapiprop-openproperty.md) e ter valores padrão prontos como backup caso uma propriedade solicitada não esteja disponível. 
  
A maioria das propriedades de mensagens que os provedores de serviços configuram são somente leitura para clientes. 
  
## <a name="see-also"></a>Confira também



[Mensagens MAPI](mapi-messages.md)

