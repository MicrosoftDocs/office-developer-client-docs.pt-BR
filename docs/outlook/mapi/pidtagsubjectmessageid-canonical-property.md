---
title: Propriedade canônica PidTagSubjectMessageId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectMessageId
api_type:
- COM
ms.assetid: d4b1a087-0986-467a-aaa9-fc643f7c56fc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c89a0a86ac733cd2cce1efc071e47fcb011fec18
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573065"
---
# <a name="pidtagsubjectmessageid-canonical-property"></a>Propriedade canônica PidTagSubjectMessageId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor binário que é copiado da mensagem para o qual um relatório está sendo gerado. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SUBJECT_IPM  <br/> |
|Identificador:  <br/> |0x0038  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Envelope MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade, como a propriedade **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)), pode ser usada para correlacionar um relatório com a mensagem original. 
  
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

