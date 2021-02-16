---
title: Marcas de propriedade MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 96211d3b6e1e4dfbd4c93a98c8dd04de10eac884
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328229"
---
# <a name="mapi-property-tags"></a>Marcas de propriedade MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A property tag is a 32-bit number that contains a unique property identifier in bits 16 through 31 and a property type in bits 0 through 15 as shown in the following illustration. 
  
**Property tag elements**
  
![Elementos de marca de propriedade]Elementos de marca de(media/amapi_10.gif "propriedade")
  
As marcas de propriedade são usadas para identificar propriedades MAPI e cada propriedade deve ter uma, independentemente de a propriedade ser definida por MAPI, um cliente ou um provedor de serviços. MAPI define um conjunto de constantes de marca de propriedade para suas propriedades no arquivo de título Mapitags.h; essas propriedades são conhecidas como "propriedades definidas por MAPI". 
  
As constantes de marca de propriedade seguem uma convenção de nomen por consistência e facilidade de uso. Há duas partes no nome de cada marca de propriedade: um prefixo PR_ e uma ou mais cadeias de caracteres que descrevem o conteúdo da propriedade. Várias cadeias de caracteres são separadas por sublinhados. Por exemplo, a marca de propriedade para o tipo de endereço de um destinatário de mensagem é **PR \_ ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) e o identificador de entrada para a pasta designada para receber uma cópia de cada mensagem de saída é **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
  
Algumas macros estão disponíveis para ajudar a trabalhar com marcas de propriedade, entre [elas PROP_TYPE,](prop_type.md) [PROP_ID](prop_id.md)e [PROP_TAG](prop_tag.md). **PROP \_ TYPE** extrai o tipo de propriedade da marca de propriedade; **PROP \_ A ID** extrai o identificador. **PROP_TAG** cria uma marca de propriedade de um tipo de propriedade e identificador. 
  
## <a name="see-also"></a>Confira também

- [Visão geral da propriedade MAPI](mapi-property-overview.md)

