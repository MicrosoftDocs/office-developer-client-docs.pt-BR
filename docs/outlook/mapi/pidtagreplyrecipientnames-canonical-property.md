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
ms.openlocfilehash: 02dcbcccd003fb0b53356da11a3b90b38e632c2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355171"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a>Propriedade canônica PidTagReplyRecipientNames

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma lista de nomes de exibição para destinatários que devem receber uma resposta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W  <br/> |
|Identificador:  <br/> |0x0050  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Envelope MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades contêm os nomes de exibição separados por ponto e vírgula.
  
Quando essa propriedade não está presente, uma resposta é enviada somente para o usuário identificado pela propriedade **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)). Quando **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) e essas propriedades são definidas, a resposta é enviada a todos os destinatários identificados por essas duas propriedades. Um provedor de transporte usa essas propriedades para substituir a lógica de resposta usual.
  
Se **PR_REPLY_RECIPIENT_ENTRIES** ou essas propriedades estiverem definidas, a outra propriedade também deverá ser definida. Essas propriedades devem conter o mesmo número de destinatários, e devem contê-los na mesma ordem. A falha ao observar esses requisitos pode causar resultados imprevisíveis. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas em mensagens de email.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte as convenções de email padrão da Internet em objetos de mensagem.
    
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

