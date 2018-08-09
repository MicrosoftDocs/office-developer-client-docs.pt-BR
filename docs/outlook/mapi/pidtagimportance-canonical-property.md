---
title: Propriedade canônica PidTagImportance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9f6a67dcff6c74f44bbc64ae8b95f3e0ec284a90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769344"
---
# <a name="pidtagimportance-canonical-property"></a>Propriedade canônica PidTagImportance

  
  
**Aplica-se a**: Outlook 
  
Contém um valor que indica a opinião do remetente da mensagem a importância de uma mensagem. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_IMPORTANCE  <br/> |
|Identificador:  <br/> |0x0017  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade e a propriedade **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) não devem ser confundidos. Prioridade indica um valor para os usuários, enquanto a prioridade indica a ordem ou a velocidade na qual a mensagem deve ser enviada pelo software do sistema de mensagens. Geralmente, a prioridade mais alta indica um alto custo. Prioridade mais alta geralmente é associada uma exibição diferentes pela interface do usuário. 
  
Essa propriedade pode ter exatamente um dos seguintes valores:
  
IMPORTANCE_LOW 
  
> A mensagem tem baixa importância.
    
IMPORTANCE_HIGH 
  
> A mensagem tem alta prioridade.
    
IMPORTANCE_NORMAL 
  
> A mensagem tem prioridade normal.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
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

