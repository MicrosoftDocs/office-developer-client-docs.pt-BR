---
title: Visão geral de propriedades de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 447f54de-9f0d-4f73-89b6-bed9cfea9c15
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 515b4637f99b806c5c5bc6304f107f62ca6d9091
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356928"
---
# <a name="message-properties-overview"></a>Visão geral de propriedades de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI divide as propriedades da mensagem em três tipos:
  
- Propriedades de conteúdo da mensagem.
    
- Transmissão de mensagens, ou envelopes, propriedades.
    
- Propriedades do destinatário da mensagem.
    
Propriedades de conteúdo da mensagem descrevem o texto de uma mensagem. Cada classe de mensagem tem seu próprio conjunto de propriedades de conteúdo. MAPI define as propriedades de conteúdo para mensagens de observação e de relatórios; Ele se baseia nos clientes e provedores de repositórios de mensagens que lidam com essas classes de mensagens para definir as propriedades apropriadamente para suas implementações. **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) e **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) são exemplos de propriedades de conteúdo para mensagens de observação. **PR_BODY** contém o conteúdo não formatado de uma nota, enquanto o **PR_RTF_COMPRESSED** contém a versão compactada do conteúdo formatado de uma anotação. Para obter mais informações sobre os intervalos de identificadores de propriedade, consulte [Property Identifier Ranges](property-identifier-ranges.md).
  
Para novas classes de mensagens, os clientes podem definir propriedades específicas de conteúdo de uma das duas maneiras:
  
- Usando identificadores de propriedade no intervalo de propriedades de conteúdo da classe de mensagem personalizada: 0x6800 a 0x7BFF.
    
- Usando propriedades nomeadas que têm identificadores que se enquadram no intervalo de 0x8000 a 0xFFFE.
    
O intervalo de identificadores das propriedades de conteúdo da classe de mensagem personalizada está disponível para qualquer cliente que crie uma classe de mensagens personalizada. Portanto, um identificador de propriedade neste intervalo pode ser usado para várias classes de mensagens. Os usuários das propriedades neste intervalo não podem fazer suposições como o comportamento das propriedades. 
  
Para propriedades nomeadas, os clientes criam um nome que especifica um conjunto de propriedades e uma cadeia de caracteres ou um valor numérico para cada nova propriedade. Em seguida, os clientes associam a propriedade a um identificador no intervalo de propriedades nomeado. Os usuários das propriedades nomeadas acessam-as por nome ou identificador por meio dos métodos [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) . 
  
As propriedades de envelope fornecem informações que são usadas para transmitir uma mensagem de um destinatário para outro. Assim como ocorre com as propriedades do conteúdo da mensagem, é possível que os clientes ou provedores de serviços definam suas próprias propriedades de envelope para suplementar aqueles que o MAPI define. Os clientes e provedores de transporte definem as propriedades de envelope que o MAPI define com base na definição que a MAPI fornece. Provedores de transporte que implementam recursos especiais podem definir suas próprias propriedades de envelope para expor esses recursos aos clientes. O MAPI define um intervalo de identificadores de propriedade que podem ser usados para essas propriedades especiais definidas pelo provedor. Geralmente, os provedores de transporte implementam uma página de propriedades especial para exibir essas propriedades e permitir que os clientes as alterem. **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) e **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) são exemplos de propriedades de envelope. Para obter mais informações, consulte [Property Identifier Ranges](property-identifier-ranges.md).
  
As propriedades de destinatário descrevem o destino de uma mensagem enviada. Um destinatário pode ser um usuário de mensagens, uma lista de distribuição ou um computador. As propriedades de destinatário são definidas por MAPI e definidas por provedores de serviços. Algumas propriedades de destinatário são compatíveis com os provedores de catálogo de endereços para seus usuários de mensagens e objetos de lista de distribuição; outras propriedades de destinatário têm suporte de clientes, provedores de repositórios de mensagens ou provedores de transporte. Por exemplo, todos os destinatários exigem um endereço e um tipo de endereço; Essas são as propriedades mantidas por um provedor de catálogos de endereços quando o destinatário é armazenado em um de seus contêineres. Os destinatários também têm um tipo, **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)), que identifica um destinatário como um destinatário de cópia primária, carbono ou oculta.
  
Muitas propriedades de mensagem são opcionais, o que significa que os clientes não podem esperar que elas estejam disponíveis ou definidas como valores válidos. Algumas propriedades de mensagem são obrigatórias, mas estão disponíveis somente quando uma mensagem está em um estado específico. Por exemplo, uma mensagem criada recentemente não precisa ter um identificador de entrada até que a mensagem tenha sido salva, e não é necessário ter uma classe de mensagem até que a mensagem esteja pronta para ser enviada. Os clientes sempre devem verificar os resultados de suas [IMAPIProp::](imapiprop-getprops.md) GetProps e [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) calls e ter os valores padrão prontos como um backup caso uma propriedade solicitada não esteja disponível. 
  
A maioria das propriedades de mensagem que os provedores de serviço define são somente leitura para os clientes. 
  
## <a name="see-also"></a>Confira também



[Mensagens MAPI](mapi-messages.md)

