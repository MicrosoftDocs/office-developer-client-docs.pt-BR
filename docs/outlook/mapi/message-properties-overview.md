---
title: Visão geral das propriedades de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 447f54de-9f0d-4f73-89b6-bed9cfea9c15
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: edbc833b411e56e2efb26631362dd25ea42c3c9f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571406"
---
# <a name="message-properties-overview"></a>Visão geral das propriedades de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI divide propriedades da mensagem em três tipos:
  
- Propriedades de conteúdo da mensagem.
    
- Propriedades de transmissão ou envelope, da mensagem.
    
- Propriedades de destinatário da mensagem.
    
Propriedades de conteúdo da mensagem descrevem o texto de uma mensagem. Cada classe de mensagem tem seu próprio conjunto de propriedades de conteúdo. MAPI define as propriedades de conteúdo para mensagens de relatório e a nota; é até os clientes e os provedores de armazenamento de mensagem que lidam com essas classes de mensagens para definir as propriedades apropriadamente para suas implementações. **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) e **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) são exemplos de propriedades de conteúdo para mensagens de nota. **PR_BODY** contém o conteúdo não formatado de uma nota, enquanto **PR_RTF_COMPRESSED** contém a versão compactada formatada sumário de uma nota. Para obter mais informações sobre os intervalos de identificador de propriedade, consulte [Intervalos de identificador de propriedade](property-identifier-ranges.md).
  
Para novas classes de mensagem, clientes podem definir propriedades específicas do conteúdo de uma das duas maneiras:
  
- Usando os identificadores de propriedade do intervalo de propriedades de conteúdo de classe de mensagem personalizada: 0x6800 por meio de 0x7BFF.
    
- Usando propriedades que têm identificadores que se encaixam na 0x8000 através de intervalo 0xFFFE nomeadas.
    
O intervalo de identificador para propriedades de conteúdo de classe de mensagem personalizada está disponível para qualquer cliente que cria uma classe de mensagem personalizada. Portanto, um identificador de propriedade nesse intervalo pode ser usado para várias classes de mensagem. Os usuários das propriedades nesse intervalo não podem fazer suposições como para o comportamento das propriedades. 
  
Para propriedades nomeadas, clientes crie um nome que especifica um conjunto de propriedades e uma cadeia de caracteres ou um valor numérico para cada nova propriedade. Clientes, em seguida, associe a propriedade um identificador no intervalo nomeado de propriedade. Usuários de propriedades nomeadas acessá-los por nome ou identificador por meio dos métodos [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) . 
  
Propriedades de envelope fornecem informações que são usadas para transmitir uma mensagem de um destinatário para outro. Assim como acontece com propriedades de conteúdo da mensagem, é possível para os clientes ou provedores de serviço definir suas próprias propriedades de envelope para complementar aqueles que define MAPI. Clientes e provedores de transporte defina as propriedades de envelope que define MAPI baseadas na definição de MAPI fornece. Provedores de transporte que implementam recursos especiais podem definir suas próprias propriedades de envelope para expor esses recursos aos clientes. MAPI separa um intervalo de identificadores de propriedades que podem ser usados para essas propriedades especiais de definido pelo provedor. Provedores de transporte normalmente implementar uma página de propriedade especial para exibir essas propriedades e permitir que os clientes alterá-los. **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) e **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) são exemplos de propriedades de envelope. Para obter mais informações, consulte [Intervalos de identificador de propriedade](property-identifier-ranges.md).
  
Propriedades de destinatário descrevem o destino para uma mensagem enviada. Um destinatário pode ser um usuário de mensagens, lista de distribuição ou um computador. Propriedades de destinatário estão definidas pelo MAPI e definidas pelos provedores de serviços. Algumas propriedades de destinatário são suportadas por provedores de catálogo de endereços para suas mensagens de usuário e os objetos da lista de distribuição; outras propriedades de destinatário são compatíveis com os clientes, provedores de armazenamento de mensagem ou provedores de transporte. Por exemplo, todos os destinatários exigem um endereço e um tipo de endereço; Estas são propriedades mantidas por um fornecedor de catálogo de endereços quando o destinatário é armazenado em um dos seus contêineres. Destinatários também têm um tipo de **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)), que identifica um destinatário como um primário, cópia carbono ou destinatário de cópia oculta.
  
Muitas propriedades de mensagem são opcionais, o que significa que os clientes não podem esperar para que fiquem disponíveis ou está definida como valores válidos. Algumas propriedades de mensagem são necessários, mas está disponível somente quando uma mensagem estiver em um determinado estado. Por exemplo, uma mensagem recém-criado, não é necessária ter um identificador de entrada até depois que a mensagem foi salva, e não é necessário ter uma classe de mensagem até que a mensagem está pronta para ser enviado. Os clientes sempre devem verificar os resultados de suas chamadas [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::OpenProperty](imapiprop-openproperty.md) e têm valores padrão prontos como backup no caso de uma propriedade solicitada não está disponível. 
  
A maioria das propriedades de mensagem que o conjunto de provedores de serviços são somente leitura aos clientes. 
  
## <a name="see-also"></a>Confira também



[Mensagens MAPI](mapi-messages.md)

