---
title: Propriedade canônica PidTagAgingGranularity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingGranularity
api_type:
- HeaderDef
ms.assetid: b79ec87d-d97c-4e6c-899b-78ebf1b485a7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b4006b62758b32598a64eaa4eb333c7ce5b12605
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325582"
---
# <a name="pidtagaginggranularity-canonical-property"></a>Propriedade canônica PidTagAgingGranularity

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Representa a unidade de tempo usada para determinar o período de tempo que um item permanece em uma pasta antes de o item ser arquivado.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_AGING_GRANULARITY  <br/> |
|Identificador:  <br/> |0x36EE  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

Os valores possíveis para **PR_AGING_GRANULARITY** podem ser um dos seguintes. 
  
|**Nome**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**AG_MONTHS** <br/> |,0  <br/> |**PR_AGING_PERIOD** é definido em número de meses.  <br/> |
|**AG_WEEKS** <br/> |1  <br/> |**PR_AGING_PERIOD** é definido em número de semanas.  <br/> |
|**AG_DAYS** <br/> |duas  <br/> |**PR_AGING_PERIOD** é definido em número de dias.  <br/> |
   
O período de tempo em que um item permanece em uma pasta antes de o item ser arquivado é determinado por duas propriedades, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) e **PR_AGING_GRANULARITY**. **PR_AGING_PERIOD** representa o número de unidades de tempo que o item permanece na pasta antes de ser arquivado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define as estruturas de dados básicas que são usadas em operações remotas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.
    
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

