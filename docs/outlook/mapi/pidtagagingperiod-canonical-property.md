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
ms.openlocfilehash: d42b58bf4fd445f34064b179c873c8bc15b11b3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360113"
---
# <a name="pidtagagingperiod-canonical-property"></a>Propriedade canônica PidTagAgingPeriod

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Representa o número de unidades de tempo que são usadas para determinar por quanto tempo um item permanece em uma pasta antes de o item ser arquivado.
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_AGING_PERIOD  <br/> |
|Identificador:  <br/> |0x36EC  <br/> |
|Tipo de propriedade:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

O período de tempo que um item permanece em uma pasta antes que o item seja arquivado é determinado por duas propriedades, **PR_AGING_PERIOD** e **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**. **PR_AGING_GRANULARITY** representa a unidade de tempo na qual **PR_AGING_PERIOD** é expressa, ao determinar esse período de tempo. 
  
Os valores possíveis **para PR_AGING_GRANULARITY** podem ser um dos seguintes. 
  
****

|**Nome**|**Descrição**|
|:-----|:-----|
|**AG_MONTHS** <br/> |**PR_AGING_PERIOD** é definido em número de meses.  <br/> |
|**AG_WEEKS** <br/> |**PR_AGING_PERIOD** é definido em número de semanas.  <br/> |
|**AG_DAYS** <br/> |**PR_AGING_PERIOD** é definido em número de dias.  <br/> |
   
Por exemplo, se uma pasta arquiva um item somente depois que  o item  estiver na pasta por duas semanas, PR_AGING_GRANULARITY será AG_WEEKS e **PR_AGING_PERIOD** será 2. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define as estruturas de dados básicas que são usadas em operações remotas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas para objetos de mensagem de email.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

