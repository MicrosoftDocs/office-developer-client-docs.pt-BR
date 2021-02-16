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
ms.openlocfilehash: 7bd5a030d11577c2afabb8a2253cf4f6129814cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407099"
---
# <a name="pidtagsubjectmessageid-canonical-property"></a>Propriedade canônica PidTagSubjectMessageId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor binário que é copiado da mensagem para a qual um relatório está sendo gerado. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SUBJECT_IPM  <br/> |
|Identificador:  <br/> |0x0038  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Envelope MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade, como a **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)), pode ser usada para correlacionar um relatório com a mensagem original. 
  
## <a name="related-resources"></a>Recursos relacionados

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

