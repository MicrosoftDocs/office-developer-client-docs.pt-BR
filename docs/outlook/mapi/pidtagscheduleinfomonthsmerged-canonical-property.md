---
title: Propriedade canônica PidTagScheduleInfoMonthsMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsMerged
api_type:
- COM
ms.assetid: b13b5d7b-413e-4405-8a35-0422477a9e86
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 53bc27b4ddd05b4a52328c605a6d4f673c91afd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336474"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a>Propriedade canônica PidTagScheduleInfoMonthsMerged

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma lista dos meses nos quais os dados de disponibilidade do tipo ocupado ou uma mensagem de ausência temporária (OOF) estão presentes na mensagem de disponibilidade. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SCHDINFO_MONTHS_MERGED  <br/> |
|Identificador:  <br/> |0x684F  <br/> |
|Tipo de dados:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Disponibilidade  <br/> |
   
## <a name="remarks"></a>Comentários

Os eventos da tentativa de tipo de disponibilidade não estão incluídos nessa propriedade. A sintaxe/o formato e as restrições dessa propriedade são os mesmos do **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), mas se referem aos compromissos marcados como OOF ou inatividade no objeto Calendar associado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publica a disponibilidade de um usuário ou recurso.
    
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

