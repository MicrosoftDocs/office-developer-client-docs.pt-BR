---
title: Propriedade canônica PidTagReplyRecipientEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientEntries
api_type:
- COM
ms.assetid: a903fd22-a3f2-464f-99b0-c087e211b124
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 000132f052abb666ae844ec7d21b59c85ab43613
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355052"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a>Propriedade canônica PidTagReplyRecipientEntries

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz dimensionada de identificadores de entrada para destinatários que receberão uma resposta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_REPLY_RECIPIENT_ENTRIES  <br/> |
|Identificador:  <br/> |0x004F  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Envelope MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade contém uma [estrutura FLATENTRYLIST](flatentrylist.md) e não é uma propriedade de múltiplos valores. 
  
Quando essa propriedade não está presente, uma resposta é enviada apenas para o usuário identificado pela propriedade **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)). Quando essa e as **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) são definidas, a resposta é enviada a todos os destinatários identificados por essas duas propriedades. Um provedor de transporte usa essas propriedades para substituir a lógica de resposta comum.
  
Se essa propriedade ou a **propriedade PR_REPLY_RECIPIENT_NAMES** estiver definida, a outra propriedade deverá ser definida também. Essas propriedades devem conter o mesmo número de destinatários e devem contê-los na mesma ordem. A falha ao observar esses requisitos pode causar resultados imprevisíveis. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas em mensagens de email.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet em objetos de mensagem.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

