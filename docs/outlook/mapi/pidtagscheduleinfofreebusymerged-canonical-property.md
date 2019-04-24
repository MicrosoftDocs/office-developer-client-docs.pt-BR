---
title: Propriedade canônica PidTagScheduleInfoFreeBusyMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyMerged
api_type:
- COM
ms.assetid: 3ebfccb6-967a-4f8e-9d94-94c50ba65438
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8d15c6cb256fb1e80e3c94bdfe7e71bd8625aa35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338714"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a>Propriedade canônica PidTagScheduleInfoFreeBusyMerged

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém os horários em que o status de disponibilidade está definido como ocupado ou OOF.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SCHDINFO_FREEBUSY_MERGED  <br/> |
|Identificador:  <br/> |0x6850  <br/> |
|Tipo de dados:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Disponibilidade  <br/> |
   
## <a name="remarks"></a>Comentários

Os eventos da tentativa de tipo de disponibilidade não estão incluídos nessa propriedade. O formato, a computação e as restrições dessa propriedade são os mesmos do **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), mas se referem a compromissos que estão marcados como OOF ou inativas no calendário associado.
  
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

