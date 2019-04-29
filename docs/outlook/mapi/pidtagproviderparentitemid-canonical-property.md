---
title: Propriedade canônica PidTagProviderParentItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0f99cf38e65c75ce1ba74bf72d88e19f4fbfa03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433413"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a>Propriedade canônica PidTagProviderParentItemId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica um identificador para o pai de uma pasta ou um item de um repositório.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROVIDER_PARENT_ITEMID  <br/> |
|Identificador:  <br/> |0x0EA4  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MAPI não-transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Os provedores de repositório podem especificar um valor para essa propriedade para um pai de uma pasta ou um item, mas deve manter o valor o mesmo entre as sessões. Provedores de repositório Use essa propriedade para identificar os resultados de pesquisa retornados de um mecanismo de pesquisa.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

