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
ms.openlocfilehash: ac4da2d4082cac632548594411528b7bf1d6dc64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769769"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a>Propriedade canônica PidTagRecipientNumberForAdvice

  
  
**Aplica-se a**: Outlook 
  
Essa propriedade contém o número de telefone de um destinatário de mensagem a chamada para a execução física de uma mensagem de aviso.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W  <br/> |
|Identificador:  <br/> |0x0C14  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Destinatário MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades devem ser usados em conjunto com a entrega um destino físico, ao invés de uma caixa de correio eletrônica, quando o destinatário humano não deve estar presente na entrega. Um exemplo é o número de telefone em uma folha de rosto de fax.
  
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

