---
title: Propriedade canônica PidTagCreateTemplates
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreateTemplates
api_type:
- HeaderDef
ms.assetid: d2530009-5de3-4872-a0a5-be1389c4206e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 28611e442f816e4d091cc6b29e2ee69195a63d09
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563356"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>Propriedade canônica PidTagCreateTemplates

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um objeto incorporado de tabela que contém os identificadores de entrada de modelo de caixa de diálogo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CREATE_TEMPLATES  <br/> |
|Identificador:  <br/> |0x3604  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Catálogo de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

Para saber qual modelo de objetos que podem ser criados dentro de um contêiner, chame o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) nessa propriedade. O objeto resultante é a tabela único que oferece os identificadores de entrada para todos os modelos que você pode criar dentro do contêiner. 
  
Para criar os objetos do modelo, chame o método de **CreateEntry** do objeto container nos valores de coluna **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da tabela único.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

