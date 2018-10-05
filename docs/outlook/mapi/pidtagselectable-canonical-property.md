---
title: Propriedade canônica PidTagSelectable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSelectable
api_type:
- COM
ms.assetid: eeecd957-dd50-4849-9698-8bc7106301e9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383454"
---
# <a name="pidtagselectable-canonical-property"></a>Propriedade canônica PidTagSelectable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Conterá TRUE se a entrada na tabela único pode ser selecionada. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SELECTABLE  <br/> |
|Identificador:  <br/> |0x3609  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Contêiner de catálogo de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada principalmente para formatação visual de uma tabela único. Modelos podem ser agrupados, criando uma entrada que indica o título para o grupo. A definição dessa propriedade como FALSE para o título garante que o usuário pode selecionar somente os modelos de reais do grupo e não essa entrada de título. 
  
Essa propriedade só se aplica a uma tabela único, não em uma tabela de hierarquia de catálogo de endereço. 
  
MAPI permite visualmente um provedor de catálogo de endereços para agrupar itens por meio de duas. Em primeiro lugar, determinadas linhas podem funcionar como títulos por sendo não-selecionável. Em segundo lugar, os itens selecionável podem ser recuados em relação ao seus títulos usando a propriedade **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)). Essa propriedade é usada em tal agrupamento para indicar se ou não esse item pode ser selecionado em uma lista para criar um endereço one-off. Por exemplo, se um cliente tiver vários modelos para construir endereços de fax, ele poderá exibi-las da seguinte maneira: 
  
Modelos de FAX (profundidade 0, não selecionável)
  
 Local (profundidade 1, selecionável) 
  
 Longa distância (profundidade 1, selecionável) 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para modelos de catálogo de endereços.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[Propriedade canônica PidTagFolderType](pidtagfoldertype-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

