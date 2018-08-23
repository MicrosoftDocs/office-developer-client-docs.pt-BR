---
title: Escolhendo o conjunto de propriedades de um formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0ff8d9f1ae25c55d66847b8c0e5e66c406dfdfba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586148"
---
# <a name="choosing-a-forms-property-set"></a>Escolhendo o conjunto de propriedades de um formulário

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando você implementa o seu servidor de formulário, você precisa ter uma propriedade para cada parte da informação que precisa de sua classe de mensagem. Essas propriedades podem ser propriedades predefinidas de MAPI ou eles podem ser propriedades personalizadas que você define. Para obter mais informações sobre como trabalhar com propriedades, consulte [Visão geral de propriedade de MAPI](mapi-property-overview.md).
  
Seu arquivo de configuração do formulário irá conter uma lista de propriedades que seu servidor de formulário expõe para aplicativos de cliente usar, mas isso não precisa ser a lista completa de propriedades usadas pelo seu servidor do formulário. Aplicativos cliente geralmente usam as propriedades expostas para habilitar usuários ordenar as mensagens em uma pasta ou personalizar suas interfaces de alguma maneira.
  
MAPI tem um grande conjunto de propriedades predefinidas que suficiente para a maioria dos aplicativos. No entanto, haverá vezes quando uma classe de mensagem personalizado precisa de uma propriedade de MAPI não define. Você pode usar as propriedades personalizadas para estender o conjunto MAPI predefinido de propriedades para qualquer informações especiais que seu servidor de formulário precisa suportar.
  
Você pode usar qualquer uma das seguintes maneiras para definir propriedades personalizadas:
  
- Escolha um nome para a propriedade e use o método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter uma marca de propriedade para ele. A interface [IMAPIProp](imapipropiunknown.md) através do qual você chamar este método proveniente o ponteiro [IMessage](imessageimapiprop.md) que é passado para o servidor de formulário quando a mensagem é criada. Observe que o nome da propriedade deve ser uma cadeia de caracteres a toda a. 
    
- Defina uma marca de propriedade personalizada. Marcas de propriedade personalizada devem estar no intervalo 0x6800 por meio de 0x7BFF. As propriedades deste intervalo são classe de mensagem específicos.
    
Para obter mais informações sobre como definir propriedades personalizadas, consulte [Definindo novas propriedades de MAPI](defining-new-mapi-properties.md).
  
> [!NOTE]
> Servidores de formulário que têm um texto de mensagem com frequência usam a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) para armazená-lo. Se o seu servidor de formulário usa **PR_RTF_COMPRESSED**, ele também deve assegurar que a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contém uma versão somente texto do texto da mensagem, caso a mensagem resultante é lido por um cliente que não oferece suporte a Rich Text Texto da mensagem Format (RTF). 
  
## <a name="see-also"></a>Confira também

- [Desenvolver servidores de formulário MAPI](developing-mapi-form-servers.md)

