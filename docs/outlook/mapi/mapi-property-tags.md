---
title: Marcas de propriedade MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 96211d3b6e1e4dfbd4c93a98c8dd04de10eac884
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390013"
---
# <a name="mapi-property-tags"></a>Marcas de propriedade MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma marca de propriedade é um número de 32 bits que contém um identificador exclusivo de propriedade em bits 31 até 16 e um tipo de propriedade em bits 0 a 15, conforme mostrado na ilustração a seguir. 
  
**Property tag elements**
  
![Elementos de marca de propriedade] (media/amapi_10.gif "Elementos de marca de propriedade")
  
Marcas de propriedade são usadas para identificar as propriedades MAPI e cada propriedade deve ter um, independentemente se a propriedade é definida por um provedor de serviços, um cliente ou MAPI. MAPI define um conjunto de constantes da propriedade tag para suas propriedades no arquivo de cabeçalho Mapitags.h; Essas propriedades são referidas como "propriedades definidas pelo MAPI". 
  
As constantes da propriedade tag siga uma convenção de nomenclatura para consistência e facilidade de uso. Há duas partes com o nome da marca de cada propriedade: um ou mais cadeias de caracteres que descrevem o conteúdo da propriedade e um prefixo PR_. Várias cadeias de caracteres são separadas por sublinhados. Por exemplo, a marca de propriedade para o tipo de endereço de um destinatário de mensagem é **PR\_ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) e o identificador de entrada para a pasta designado para receber uma cópia de todas as mensagens de saída é **PR_IPM_SENTMAIL_ ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
  
Algumas macros estão disponíveis para ajudar a trabalhar com marcas de propriedade, entre eles [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md)e [PROP_TAG](prop_tag.md). **PROP\_tipo** extrai o tipo de propriedade da marca a propriedade; **PROP\_ID** extrai o identificador. **PROP_TAG** constrói uma marca de propriedade de um tipo de propriedade e o identificador. 
  
## <a name="see-also"></a>Confira também

- [Visão geral da propriedade MAPI](mapi-property-overview.md)

