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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332057"
---
# <a name="choosing-a-forms-property-set"></a>Escolher um conjunto de propriedades do formulário

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao implementar seu servidor de formulários, você precisa ter uma propriedade para cada informação de que sua classe de mensagens precisa. Essas propriedades podem ser propriedades MAPI predefinidas ou podem ser Propriedades personalizadas definidas por você. Para obter mais informações sobre como trabalhar com propriedades, consulte [MAPI Property Overview](mapi-property-overview.md).
  
Seu arquivo de configuração de formulário conterá uma lista de propriedades que seu servidor de formulário expõe para que os aplicativos cliente usem, mas isso não precisa ser a lista completa de propriedades usadas pelo seu servidor de formulários. Os aplicativos clientes normalmente usam as propriedades expostas para permitir que os usuários classifiquem mensagens em uma pasta ou personalizem suas interfaces de alguma forma.
  
O MAPI tem um amplo conjunto de propriedades predefinidas que são suficientes para a maioria dos aplicativos. No enTanto, haverá ocasiões em que uma classe de mensagem personalizada precisa de uma propriedade que MAPI não define. Você pode usar propriedades personalizadas para estender o conjunto de propriedades predefinido MAPI para qualquer informação especial que seu servidor de formulário precisa suportar.
  
Você pode usar uma das seguintes maneiras para definir propriedades personalizadas:
  
- Escolha um nome para a propriedade e use o método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obter uma marca de propriedade para ela. A interface [IMAPIProp](imapipropiunknown.md) através da qual você chama esse método vem do ponteiro [IMessage](imessageimapiprop.md) que é passado para o servidor de formulário quando a mensagem é criada. Observe que o nome da propriedade deve ser uma cadeia de caracteres largos. 
    
- Defina você mesmo uma marca de propriedade personalizada. As marcas de propriedade personalizada devem estar no intervalo 0x6800 a 0x7BFF. As propriedades desse intervalo são específicas de classe de mensagem.
    
Para obter mais informações sobre como definir propriedades personalizadas, consulte [definindo novas propriedades MAPI](defining-new-mapi-properties.md).
  
> [!NOTE]
> Os servidores de formulário que possuem um texto de mensagem geralmente usam a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) para armazená-lo. Se o seu servidor de formulário usa o **PR_RTF_COMPRESSED**, ele também deve garantir que a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contenha uma versão somente texto do texto da mensagem, caso a mensagem resultante seja lida por um cliente que não ofereça suporte a Rich Text Texto da mensagem de formato (RTF). 
  
## <a name="see-also"></a>Confira também

- [Desenvolver servidores de formulário MAPI](developing-mapi-form-servers.md)

