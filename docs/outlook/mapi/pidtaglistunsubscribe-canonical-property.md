---
title: Propriedade canônica PidTagListUnsubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListUnsubscribe
api_type:
- HeaderDef
ms.assetid: 4e6bfbc7-7586-43cc-9380-daa0fe3d85a5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 87f5c3fc8475f9795847e4680babb26682608a5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769439"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a>Propriedade canônica PidTagListUnsubscribe

  
  
**Aplica-se a**: Outlook 
  
Contém o valor do campo de cabeçalho de cancelar a lista de uma mensagem de email extensões MIME (Multipurpose Internet).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W  <br/> |
|Identificador:  <br/> |0x1045  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

Para gerar um campo de cabeçalho Cancelar assinatura de lista, os clientes devem definir essas propriedades para o valor desejado. Os autores MIME devem copiar o valor dessas propriedades no campo de cabeçalho de cancelar a lista.
  
Para definir o valor dessas propriedades relacionadas ao servidor de lista, os clientes MIME devem gravar os campos de cabeçalho, conforme especificado na tabela a seguir.
  
|**Propriedade**|**Nome do campo de cabeçalho preferencial**|**Nome do campo de cabeçalho alternativo**|
|:-----|:-----|:-----|
|**PR_LIST_UNSUBSCRIBE** <br/> |Cancelar assinatura de lista  <br/> |Cancelar assinatura lista X  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
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

