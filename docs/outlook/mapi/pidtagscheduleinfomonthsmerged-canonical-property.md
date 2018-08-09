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
ms.openlocfilehash: c1096df0eff4b43239978620f4ccf2e9d221095a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769977"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a>Propriedade canônica PidTagScheduleInfoMonthsMerged

  
  
**Aplica-se a**: Outlook 
  
Contém uma lista dos meses para os dados de disponibilidade do tipo ocupado ou uma ausência temporária (OOF) mensagem está presente na mensagem de livre/ocupado. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SCHDINFO_MONTHS_MERGED  <br/> |
|Identificador:  <br/> |0x684F  <br/> |
|Tipo de dados:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Informações de disponibilidade  <br/> |
   
## <a name="remarks"></a>Comentários

Eventos do tipo disponível/ocupado provisório não são incluídos nessa propriedade. O formato da sintaxe/e restrições dessa propriedade são iguais aos de **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), mas se referir a compromissos que são marcados ausência temporária ou ocupado no objeto calendário associado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publica a disponibilidade de um usuário ou recurso.
    
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

