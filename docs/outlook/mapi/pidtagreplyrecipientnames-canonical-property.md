---
title: Propriedade canônica PidTagReplyRecipientNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientNames
api_type:
- COM
ms.assetid: f5ae6124-3e44-400f-95c2-24b19f3085b5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5abbe14576bec9f03f0b1bf5578b68032f95f8a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769823"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a>Propriedade canônica PidTagReplyRecipientNames

  
  
**Aplica-se a**: Outlook 
  
Contém uma lista de nomes de exibição dos destinatários que devem receber uma resposta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W  <br/> |
|Identificador:  <br/> |0x0050  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Envelope MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades contenham os nomes de exibição separados por ponto e vírgula.
  
Quando essa propriedade não estiver presente, uma resposta é enviada apenas para o usuário identificado pela propriedade **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)). Quando essas propriedades e **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) são definidas, a resposta é enviada para todos os destinatários identificados por essas duas propriedades. Um provedor de transporte usa essas propriedades para substituir a lógica de resposta comum.
  
Se **PR_REPLY_RECIPIENT_ENTRIES** ou essas propriedades estiverem definidas, a outra propriedade deve ser definida também. Essas propriedades devem conter o mesmo número de destinatários, e eles devem armazená-los na mesma ordem. Falha para observar esses requisitos pode causar resultados imprevisíveis. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas em mensagens de email.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet para os objetos de mensagem.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

