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
ms.openlocfilehash: a82b1351c9d2d19c32e34b03a537a12bf93deb8a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435758"
---
# <a name="pidtagorigincheck-canonical-property"></a>Propriedade canônica PidTagOriginCheck

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor de verificação binária que permite que um destinatário de relatório de entrega verifique a origem da mensagem original.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ORIGIN_CHECK  <br/> |
|Identificador:  <br/> |0x0027  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Servidor  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade fornece um meio para terceiros, como um agente de transferência de mensagens (MTA) ou um usuário de mensagens receber um relatório de entrega, para verificar a origem da mensagem enviada. Se presente em uma mensagem recebida, essa propriedade deve ser copiada para qualquer relatório de entrega gerado em resposta à mensagem.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

