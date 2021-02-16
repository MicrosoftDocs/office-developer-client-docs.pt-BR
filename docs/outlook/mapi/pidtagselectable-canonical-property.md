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
  
Contém TRUE se a entrada na tabela única pode ser selecionada. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SELECTABLE  <br/> |
|Identificador:  <br/> |0x3609  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Contêiner do livro de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada principalmente para formatação visual de uma tabela única. Os modelos podem ser agrupados criando uma entrada que indica o título do grupo. Definir essa propriedade como FALSE para o título garante que o usuário pode selecionar apenas os modelos reais no grupo e não essa entrada de título. 
  
Essa propriedade se aplica somente a uma tabela única, não a uma tabela de hierarquia de um livro de endereços. 
  
MAPI allows an address book provider to group items visually by two means. Primeiro, determinadas linhas podem funcionar como títulos por serem inselecionáveis. Segundo, os itens selecionáveis podem ser recuados em relação a **seus títulos** usando a propriedade PR_DEPTH ([PidTagDepth](pidtagdepth-canonical-property.md)). Essa propriedade é usada nesse grupo para indicar se esse item pode ou não ser selecionado em uma lista para criar um endereço único. Por exemplo, se um cliente tiver vários modelos para construir endereços de fax, ele poderá exibi-los da seguinte forma: 
  
Modelos de FAX (profundidade 0, não selecionável)
  
 Local (profundidade 1, selecionável) 
  
 Longa distância (profundidade 1, selecionável) 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para modelos de livro de endereços.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[Propriedade canônica PidTagFolderType](pidtagfoldertype-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

