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
ms.openlocfilehash: 962e8c92ae61e8b60862a3ae26a7cdfbf5034e89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359511"
---
# <a name="pidtagrowtype-canonical-property"></a>Propriedade canônica PidTagRowType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor que indica o tipo de uma linha em uma tabela.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ROW_TYPE  <br/> |
|Identificador:  <br/> |0x0FF5  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI não-transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade só aparece em tabelas de conteúdo. Uma categoria só existe quando tem itens.
  
Essa propriedade pode ter exatamente um dos seguintes valores:
  
TBL_LEAF_ROW 
  
> Representa dados reais, em vez de uma linha de categoria.
    
TBL_EMPTY_CATEGORY 
  
> Não usado no momento.
    
TBL_EXPANDED_CATEGORY 
  
> A categoria é expandida; a interface do usuário geralmente exibe isso com o sinal de menos (-) ao lado dele.
    
TBL_COLLAPSED_CATEGORY 
  
> A categoria é recolhida; a interface do usuário geralmente exibe isso com o sinal de adição (+) ao lado dele.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclui operações permissíveis para os objetos da tabela principal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagRowid](pidtagrowid-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

