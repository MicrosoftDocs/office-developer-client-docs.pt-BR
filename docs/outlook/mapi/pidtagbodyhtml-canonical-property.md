---
title: Propriedade canônica PidTagBodyHtml
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6ed59228ee06a1d3e362115a99bf4b859dfeb698
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359042"
---
# <a name="pidtagbodyhtml-canonical-property"></a>Propriedade canônica PidTagBodyHtml

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a versão HTML (Hypertext Markup Language) do texto da mensagem. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W  <br/> |
|Identificador:  <br/> |0x1013  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades contêm o mesmo texto da **mensagem PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), mas em HTML. 
  
Um repositório de mensagens que oferece suporte a HTML indica isso definindo o **sinalizador STORE_HTML_OK** em seu **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). 
  
 **Observe** **STORE_HTML_OK** não está definido nas versões de Mapidefs.h incluídas no Microsoft® Exchange 2000 Server e versões anteriores. Se **STORE_HTML_OK** for indefinido, use o valor 0x00010000 em vez disso. 
  
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



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

