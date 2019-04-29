---
title: Propriedade canônica PidTagOriginalAuthorEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEntryId
api_type:
- COM
ms.assetid: 34654660-b003-42f5-9fcd-24ebaccd735d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 866c28bc08f669d18487c99c9a13bc7347b605fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425586"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a>Propriedade canônica PidTagOriginalAuthorEntryId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o identificador de entrada do autor da primeira versão de uma mensagem, ou seja, a mensagem antes de ser encaminhada ou respondida.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ORIGINAL_AUTHOR_ENTRYID  <br/> |
|Identificador:  <br/> |0x004C  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é uma das propriedades de endereço para o autor de uma mensagem. No primeiro envio da mensagem, o aplicativo cliente deve definir essa propriedade com o valor de **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)). Ela nunca é alterada quando a mensagem é encaminhada ou respondida. 
  
A propriedade Author original permite preservar as informações de fora do domínio de mensagens local. Quando uma mensagem chega de outro domínio de mensagens, como a partir da Internet, essa propriedade oferece uma maneira de garantir que as informações originais não sejam perdidas.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

