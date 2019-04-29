---
title: Propriedade canônica PidTagRecipientNumberForAdvice
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientNumberForAdvice
api_type:
- COM
ms.assetid: 636c1e75-3024-43ca-a7dd-1bb480dfbb5b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 79ef85955f15e0ca829ac6f206dddc17031b0562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420637"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a>Propriedade canônica PidTagRecipientNumberForAdvice

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Esta propriedade contém o número de telefone do destinatário da mensagem para chamar o aviso da entrega física de uma mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W  <br/> |
|Identificador:  <br/> |0x0C14  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Destinatário MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades devem ser usadas em conjunto com a entrega para um destino físico, em vez de uma caixa de correio eletrônica, quando o destinatário humano não deve estar presente na entrega. Um exemplo é o número de telefone em uma folha de rosto de fax.
  
## <a name="related-resources"></a>Recursos relacionados

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

