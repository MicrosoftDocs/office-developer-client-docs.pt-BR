---
title: Propriedade canônica PidTagDetailsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1602d1753d9f7f6e6f407a85dab0a33255db7aae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585784"
---
# <a name="pidtagdetailstable-canonical-property"></a>Propriedade canônica PidTagDetailsTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um objeto table de vídeo incorporado.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DETAILS_TABLE  <br/> |
|Identificador:  <br/> |0x3605  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Contêiner MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Passar essa propriedade para o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para o objeto retorna uma interface de [IMAPITable](imapitableiunknown.md) que permite a criação da tabela de exibição. MAPI usa esta tabela para exibir as folhas de propriedades para um objeto do catálogo de endereços em resposta a uma chamada [IAddrBook::Details](iaddrbook-details.md) . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[Propriedade canônica PidTagSearch](pidtagsearch-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

