---
title: Propriedade canônica PidTagListSubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5030e48ac87408f983696a365d3234c3362346c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769442"
---
# <a name="pidtaglistsubscribe-canonical-property"></a>Propriedade canônica PidTagListSubscribe

  
  
**Aplica-se a**: Outlook 
  
Contém o valor do campo de cabeçalho de assinar a lista de uma mensagem de email extensões MIME (Multipurpose Internet).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W  <br/> |
|Identificador:  <br/> |0x1044  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

Para gerar um campo de cabeçalho se inscrever lista, os clientes devem definir o valor dessas propriedades com o valor desejado. Os autores MIME devem copiar o valor dessas propriedades no campo de cabeçalho assine a lista.
  
Para definir o valor das propriedades relacionadas ao servidor como essas, os clientes MIME devem gravar os campos de cabeçalho, conforme especificado na tabela a seguir.
  
|**Propriedade**|**Nome do campo de cabeçalho preferencial**|**Nome do campo de cabeçalho alternativo**|
|:-----|:-----|:-----|
|**PidTagListSubscribe** <br/> |Assine a lista  <br/> |Inscrever-se lista X  <br/> |
   
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

