---
title: Propriedade canônica PidTagBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 243a59798980d8c0cfaf1a726d6408dbd66ebba8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326632"
---
# <a name="pidtagbody-canonical-property"></a>Propriedade canônica PidTagBody

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o texto da mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_BODY, PR_BODY_A, PR_BODY_W  <br/> |
|Identificador:  <br/> |0x1000  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são normalmente usadas apenas em uma mensagem interpersonal (IPM). 
  
Os armazenamentos de mensagens que suportam RTF (Rich Text Format) ignoram qualquer alteração no espaço em branco no texto da mensagem. Quando **PR_BODY** é armazenado pela primeira vez, o armazenamento de mensagens também gera e armazena a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), a versão RTF do texto da mensagem. Se o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) for chamado posteriormente e PR_BODY tiver sido modificado, o armazenamento de mensagens chamará a função [RTFSync](rtfsync.md) para garantir a sincronização com **a** versão RTF. Se apenas o espaço em branco tiver sido alterado, as propriedades permanecerão inalteradas. Isso preserva qualquer formatação RTF nãotrivial quando a mensagem passa por clientes não cientes de RTF e sistemas de mensagens. 
  
O valor dessa propriedade deve ser expresso na página de código do sistema operacional em que o MAPI está sendo executado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

