---
title: Propriedade canônica PidTagDefCreateDl
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ff5d35104e9effc27c405b716cb61cf4643677b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359952"
---
# <a name="pidtagdefcreatedl-canonical-property"></a>Propriedade canônica PidTagDefCreateDl

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o identificador de entrada de modelo para uma lista de distribuição padrão. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DEF_CREATE_DL  <br/> |
|Identificador:  <br/> |0x3611  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Catálogo de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

Os aplicativos cliente usam essa propriedade para criar uma lista de distribuição dentro de um contêiner. O suporte à criação de entrada é opcional para contêineres do catálogo de endereços; os que não oferecem suporte a ele não são necessários para expor essa propriedade. 
  
Esta propriedade especifica uma entrada que pode aparecer na propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) para listas de distribuição. Após obter o identificador, o cliente o usará em uma chamada para o método [IABContainer:: createentry](iabcontainer-createentry.md) . A entrada representa o modelo da lista de distribuição padrão. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

