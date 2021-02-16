---
title: Escolher um conjunto de propriedades do formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d983b71c7c92c395740a8ae6f6d3666a8bc2c0c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407190"
---
# <a name="choosing-a-forms-property-set"></a>Escolher um conjunto de propriedades do formulário

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao implementar seu servidor de formulário, você precisa ter uma propriedade para cada informação que sua classe de mensagem precisa. Essas propriedades podem ser propriedades MAPI predefinidos ou podem ser propriedades personalizadas definidas por você. Para obter mais informações sobre como trabalhar com propriedades, consulte [MAPI Property Overview](mapi-property-overview.md).
  
Seu arquivo de configuração de formulário conterá uma lista de propriedades que o servidor de formulário expõe para os aplicativos cliente usarem, mas não precisa ser a lista inteira de propriedades usadas pelo servidor de formulário. Os aplicativos cliente geralmente usam as propriedades expostas para permitir que os usuários classificar mensagens em uma pasta ou personalizar suas interfaces de alguma maneira.
  
MAPI has a large set of predefined properties that suffice for most applications. No entanto, haverá ocasiões em que uma classe de mensagem personalizada precisa de uma propriedade que MAPI não define. You can use custom properties to extend the MAPI predefined set of properties for whatever special information your form server needs to support.
  
Você pode usar uma das seguintes maneiras de definir propriedades personalizadas:
  
- Escolha um nome para a propriedade e use o método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter uma marca de propriedade para ela. A interface [IMAPIProp](imapipropiunknown.md) através da qual você chama esse método vem do ponteiro [IMessage](imessageimapiprop.md) que é passado para o servidor de formulário quando a mensagem é criada. Observe que o nome da propriedade deve ser uma cadeia de caracteres de caracteres largos. 
    
- Defina uma marca de propriedade personalizada por conta própria. As marcas de propriedade personalizadas devem estar no intervalo 0x6800 a 0x7BFF. As propriedades nesse intervalo são específicas da classe message.
    
Para obter mais informações sobre como definir propriedades personalizadas, consulte [Definindo novas propriedades MAPI](defining-new-mapi-properties.md).
  
> [!NOTE]
> Os servidores de formulário que têm um texto de mensagem geralmente usam a **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) para armazená-lo. Se seu servidor de formulário usa **PR_RTF_COMPRESSED**, ele também deve garantir que a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contém uma versão somente texto do texto da mensagem, caso a mensagem resultante seja lida por um cliente que não suporta texto de mensagem RTF (Rich Text Format). 
  
## <a name="see-also"></a>Confira também

- [Desenvolvendo servidores de formulário MAPI](developing-mapi-form-servers.md)

