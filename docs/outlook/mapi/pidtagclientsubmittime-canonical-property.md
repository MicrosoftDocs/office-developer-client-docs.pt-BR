---
title: Propriedade canônica PidTagClientSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagClientSubmitTime
api_type:
- HeaderDef
ms.assetid: d46e1063-6421-410d-a445-7477fea42089
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 851441e419c17d8f5fef27c785ea4b829a4ae443
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345714"
---
# <a name="pidtagclientsubmittime-canonical-property"></a>Propriedade canônica PidTagClientSubmitTime

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a data e a hora em que o remetente da mensagem enviou uma mensagem. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CLIENT_SUBMIT_TIME  <br/> |
|Identificador:  <br/> |0x0039  <br/> |
|Tipo de dados:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Hora da mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

O provedor da loja **PR_CLIENT_SUBMIT_TIME** o horário em que o aplicativo cliente chamou [IMessage::SubmitMessage](imessage-submitmessage.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
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

