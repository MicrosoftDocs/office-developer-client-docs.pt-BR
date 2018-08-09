---
title: Propriedade canônica PidTagRowType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7fdb8781c39d7814ff2c38ff4df4545511d28a5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769870"
---
# <a name="pidtagrowtype-canonical-property"></a>Propriedade canônica PidTagRowType

  
  
**Aplica-se a**: Outlook 
  
Contém um valor que indica o tipo de uma linha em uma tabela.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ROW_TYPE  <br/> |
|Identificador:  <br/> |0x0FF5  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI não transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é exibida somente nas tabelas de conteúdo. Só existe uma categoria quando ele tem itens.
  
Essa propriedade pode ter exatamente um dos seguintes valores:
  
TBL_LEAF_ROW 
  
> Representa os dados reais, em vez de uma linha de categoria.
    
TBL_EMPTY_CATEGORY 
  
> Não usado no momento.
    
TBL_EXPANDED_CATEGORY 
  
> A categoria é expandida; a interface do usuário geralmente exibe isso com o sinal de menos (-) ao lado dela.
    
TBL_COLLAPSED_CATEGORY 
  
> A categoria estiver recolhida; a interface do usuário geralmente exibe isso com o sinal de adição (+) ao lado dela.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclui as operações permitidas para os objetos de tabela principal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagRowid](pidtagrowid-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

