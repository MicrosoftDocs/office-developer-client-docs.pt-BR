---
title: Propriedade canônica PidTagRecipientTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatus
api_type:
- COM
ms.assetid: d619b5e7-2867-44fc-9b42-123bb1bf7bde
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 074bcf7c051b78bc32caf66502747e7fb1ab6b79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355283"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a>Propriedade canônica PidTagRecipientTrackStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica o status de resposta retornado pelo participante.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RECIPIENT_TRACKSTATUS  <br/> |
|Identificador:  <br/> |0x5FFF  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Destinatário de transporte  <br/> |
   
## <a name="remarks"></a>Comentários

Se esse valor não for definido, ele deverá ser assumido como respNone. Caso contrário, ele deve ser um dos seguintes:
  
|**Status da resposta**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |Nenhuma resposta é necessária para este objeto. Esse é o caso para objetos de compromisso e objetos de resposta de reunião.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Esse valor no objeto de reunião do participante indica que o participante aceitou provisadamente o objeto de solicitação de reunião.  <br/> |
|respAccepted  <br/> |0x00000003  <br/> |Esse valor no objeto de reunião do participante indica que o participante aceitou o objeto de solicitação de reunião.  <br/> |
|respDeclined  <br/> |0x00000004  <br/> |Esse valor no objeto de reunião do participante indica que o participante recusou o objeto de solicitação de reunião.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
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

