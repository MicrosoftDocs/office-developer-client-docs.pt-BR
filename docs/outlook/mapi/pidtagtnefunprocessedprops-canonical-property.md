---
title: Propriedade canônica PidTagTnefUnprocessedProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefUnprocessedProps
api_type:
- COM
ms.assetid: df9cd614-1198-44a2-9bf5-36c57179a9a9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c25888353857f9233ba487661f5f27d64cd678cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577426"
---
# <a name="pidtagtnefunprocessedprops-canonical-property"></a>Propriedade canônica PidTagTnefUnprocessedProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Serializa propriedades ao filtrar TNEF Transport Neutral Encapsulation Format ().
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_TNEF_UNPROCESSED_PROPS  <br/> |
|Identificador:  <br/> |0x0E9C  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MAPI não transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Usada pelo Microsoft Outlook e Outlook Web Access (OWA) para salvar o TNEF original em casos onde o TNEF contém propriedades nomeadas que não podem ser criadas no repositório.
  
## <a name="related-resources"></a>Recursos relacionados

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

