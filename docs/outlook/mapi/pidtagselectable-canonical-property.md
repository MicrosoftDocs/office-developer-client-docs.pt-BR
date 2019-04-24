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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359014"
---
# <a name="pidtagselectable-canonical-property"></a>Propriedade canônica PidTagSelectable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém TRUE se a entrada na tabela one-off pode ser selecionada. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SELECTABLE  <br/> |
|Identificador:  <br/> |0x3609  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Contêiner de catálogo de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada principalmente para formatação visual de uma tabela única. Os modelos podem ser agrupados criando uma entrada que indica o título do grupo. A definição dessa propriedade como FALSE para o título garante que o usuário possa selecionar apenas os modelos reais no grupo e não esta entrada de título. 
  
Essa propriedade só se aplica a uma tabela única, e não a uma tabela de hierarquia de catálogo de endereços. 
  
O MAPI permite que um provedor de catálogo de endereços agrupe itens visualmente por dois meios. Primeiro, determinadas linhas podem funcionar como títulos ao serem não-selecionadas. Segundo, os itens selecionáveis podem ser recuados em relação aos seus títulos usando a propriedade **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)). Essa propriedade é usada nesse agrupamento para indicar se este item pode ou não ser selecionado de uma lista para criar um endereço one-off. Por exemplo, se um cliente tiver vários modelos para a criação de endereços de fax, ele poderá exibi-los da seguinte maneira: 
  
Modelos de FAX (profundidade 0, não selecionável)
  
 Local (profundidade 1, selecionável) 
  
 Longa distância (profundidade 1, selecionável) 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para os modelos de catálogo de endereços.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[Propriedade canônica PidTagFolderType](pidtagfoldertype-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

