---
title: Propriedade canônica PidTagDepth
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDepth
api_type:
- HeaderDef
ms.assetid: 04d444a5-e97f-48e6-89a5-8a6cb2136408
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 25af87004ef5616a6c6fc575c647fdd1794d710f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769169"
---
# <a name="pidtagdepth-canonical-property"></a>Propriedade canônica PidTagDepth

  
  
**Aplica-se a**: Outlook 
  
Contém um número inteiro que representa o nível relativo de recuo ou profundidade, de um objeto em uma tabela de hierarquia.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DEPTH  <br/> |
|Identificador:  <br/> |0x3005  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI comuns  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade também pode especificar o nível de categorização de uma linha em uma tabela de conteúdo ou a profundidade da hierarquia em uma tabela de hierarquia. A intensidade é baseado em zero, onde zero representa a categoria mais à esquerda. Em todos os casos, o valor da propriedade representa um valor relativo em vez de um valor absoluto. Na tabela de hierarquia, por exemplo, o valor de profundidade é em relação ao contêiner do qual a tabela de hierarquia foi recuperada. A intensidade do contêiner raiz não representa uma profundidade absoluta. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclui as operações permitidas para os objetos de tabela principal.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[Propriedade canônica PidTagSelectable](pidtagselectable-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

