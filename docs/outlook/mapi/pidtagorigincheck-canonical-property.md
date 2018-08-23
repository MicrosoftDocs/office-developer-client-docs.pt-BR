---
title: Propriedade canônica PidTagOriginCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 27b967b885ef35c04d52699c289dd60248e9abd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581080"
---
# <a name="pidtagorigincheck-canonical-property"></a>Propriedade canônica PidTagOriginCheck

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor binário de verificação que permite que um destinatário de relatório de entrega verificar a origem da mensagem original.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ORIGIN_CHECK  <br/> |
|Identificador:  <br/> |0x0027  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Servidor  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade oferece um meio de um terceiro, como um agente de transferência de mensagem (MTA) ou um usuário receber uma notificação de entrega de mensagens para verificar a origem da mensagem enviada. Se estiverem presentes em uma mensagem recebida, esta propriedade deve ser copiada em qualquer relatório de entrega gerado em resposta à mensagem.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

