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
ms.openlocfilehash: 74eae4a4ed742c3bb90496f5975ad7dac6ff798f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419251"
---
# <a name="pidtagdetailstable-canonical-property"></a>Propriedade canônica PidTagDetailsTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um objeto de tabela de exibição incorporado.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DETAILS_TABLE  <br/> |
|Identificador:  <br/> |0x3605  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Contêiner MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Transmitir essa propriedade para o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para o objeto retorna uma interface IMAPITable que permite a criação da tabela de exibição. [](imapitableiunknown.md) MAPI usa esta tabela para exibir folhas de propriedades para um objeto de catálogo de endereços em resposta a uma chamada de [IAddrBook::D etails](iaddrbook-details.md) . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[Propriedade canônica PidTagSearch](pidtagsearch-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

