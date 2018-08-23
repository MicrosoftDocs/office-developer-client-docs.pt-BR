---
title: Propriedade canônica PidTagAgingPeriod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingPeriod
api_type:
- HeaderDef
ms.assetid: 762020d1-4bc8-d60d-0f66-3929aae24bfb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: caaa01982ff9e66fe7e17df4eaf37dcd25281d4e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569551"
---
# <a name="pidtagagingperiod-canonical-property"></a>Propriedade canônica PidTagAgingPeriod

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Representa o número de unidades de tempo que são usados para determinar a quantidade de tempo que um item permanece em uma pasta antes do item será arquivado.
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_AGING_PERIOD  <br/> |
|Identificador:  <br/> |0x36EC  <br/> |
|Tipo de propriedade:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

O período de tempo que um item permanece em uma pasta antes do item será arquivado é determinado pelo duas propriedades, **PR_AGING_PERIOD** e **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**. **PR_AGING_GRANULARITY** representa a unidade de tempo em que **PR_AGING_PERIOD** é expresso, ao determinar esse período de tempo. 
  
Os valores possíveis para **PR_AGING_GRANULARITY** podem ser uma das opções a seguir. 
  
****

|**Nome**|**Descrição**|
|:-----|:-----|
|**AG_MONTHS** <br/> |**PR_AGING_PERIOD** é definido no número de meses.  <br/> |
|**AG_WEEKS** <br/> |**PR_AGING_PERIOD** é definida em número de semanas.  <br/> |
|**AG_DAYS** <br/> |**PR_AGING_PERIOD** é definido no número de dias.  <br/> |
   
Por exemplo, se um arquivos de pasta é um item somente depois que o item tiver sido na pasta para duas semanas e, em seguida, **PR_AGING_GRANULARITY** **AG_WEEKS** e **PR_AGING_PERIOD** é 2. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece as definições do conjunto de propriedades.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define as estruturas de dados básicos que são usadas em operações remotas.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para os objetos de mensagem de email.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

