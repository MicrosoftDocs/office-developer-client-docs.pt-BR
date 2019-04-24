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
  
Uma marca de propriedade é um número de bits de 32 que contém um identificador de propriedade exclusivo em bits 16 a 31 e um tipo de propriedade em bits 0 a 15, conforme mostrado na ilustração a seguir. 
  
**Property tag elements**
  
![Elementos de marca de propriedade] (media/amapi_10.gif "Elementos de marca de propriedade")
  
As marcas de propriedade são usadas para identificar propriedades MAPI e cada propriedade deve ter um, independentemente de a propriedade ser definida por MAPI, um cliente ou um provedor de serviços. MAPI define um conjunto de constantes de marca de propriedade para suas propriedades no arquivo de cabeçalho Mapitags. h; essas propriedades são referidas como "Propriedades definidas por MAPI". 
  
As constantes de marca de propriedade seguem uma Convenção de nomenclatura para consistência e facilidade de uso. Há duas partes para o nome de cada marca de propriedade: um prefixo PR_ e uma ou mais cadeias de caracteres que descrevem o conteúdo da propriedade. Várias cadeias de caracteres são separadas por sublinhados. Por exemplo, a marca de propriedade para o tipo de endereço de um destinatário de mensagem é **PR\_ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) e o identificador de entrada da pasta designada para receber uma cópia de todas as mensagens de saída é **PR_IPM_SENTMAIL_ ENTRYid** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
  
Algumas macros estão disponíveis para ajudar a trabalhar com marcas de propriedade, entre elas [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md)e [PROP_TAG](prop_tag.md). **O\_tipo prop** extrai o tipo de propriedade da marca de propriedade; **A\_ID de prop** extrai o identificador. **PROP_TAG** cria uma marca de propriedade a partir de um tipo de propriedade e identificador. 
  
## <a name="see-also"></a>Confira também

- [Visão geral da propriedade MAPI](mapi-property-overview.md)

