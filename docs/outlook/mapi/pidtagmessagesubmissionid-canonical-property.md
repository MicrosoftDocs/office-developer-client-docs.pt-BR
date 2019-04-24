---
title: Propriedade canônica PidTagMessageSubmissionId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSubmissionId
api_type:
- HeaderDef
ms.assetid: 0a799fe5-04e2-4e1d-b0cd-9bdd2577d299
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 723affa054cb35a9cc7a2ee28e051e3b9a6d04e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329397"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a>Propriedade canônica PidTagMessageSubmissionId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um identificador MTS (sistema de transferência de mensagens) para o MTA (agente de transferência de mensagens).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_SUBMISSION_ID  <br/> |
|Identificador:  <br/> |0x0047  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é retornada pelo MTA após a conclusão bem-sucedida do envio de mensagens. Qualquer contato futuro com o MTA referente a essa mensagem, como solicitar o cancelamento, usa o identificador MTS nessa propriedade.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

