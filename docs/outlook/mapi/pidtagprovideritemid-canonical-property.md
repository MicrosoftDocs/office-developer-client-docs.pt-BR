---
title: Propriedade canônica PidTagProviderItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderItemId
api_type:
- COM
ms.assetid: fadbf1af-32c2-43ea-8475-15b31b2a9e68
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 48653b86d625da963b655dbd1acc01a46f4687dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286471"
---
# <a name="pidtagprovideritemid-canonical-property"></a>Propriedade canônica PidTagProviderItemId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica um identificador para uma pasta ou um item em um repositório.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROVIDER_ITEMID  <br/> |
|Identificador:  <br/> |0x0EA3  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MapiNonTransmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Os provedores de repositório podem especificar um valor para essa propriedade para uma pasta ou um item, mas devem manter o valor o mesmo entre as sessões. Provedores de repositório Use essa propriedade para identificar os resultados de pesquisa retornados de um mecanismo de pesquisa.
  
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

