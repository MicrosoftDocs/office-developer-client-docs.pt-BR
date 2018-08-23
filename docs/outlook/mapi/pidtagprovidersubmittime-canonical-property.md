---
title: Propriedade canônica PidTagProviderSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderSubmitTime
api_type:
- COM
ms.assetid: 9e5161d9-fefe-4a12-b7f7-5600f1d2e95b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e08b56fcfea38bf65e8628acfa481716554e2c01
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571609"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a>Propriedade canônica PidTagProviderSubmitTime

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a data e hora de que um provedor de transporte passada uma mensagem para seu sistema de mensagens subjacente.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROVIDER_SUBMIT_TIME  <br/> |
|Identificador:  <br/> |0x0048  <br/> |
|Tipo de dados:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Envelope MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é definida pelo provedor de transporte de saída no momento em que uma mensagem é enviada.
  
Essa propriedade corresponde a um atributo por mensagem de envelope de envio de x. 400. 
  
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

