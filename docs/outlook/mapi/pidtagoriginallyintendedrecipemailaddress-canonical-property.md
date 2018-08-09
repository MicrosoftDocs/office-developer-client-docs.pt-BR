---
title: Propriedade canônica PidTagOriginallyIntendedRecipEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEmailAddress
api_type:
- COM
ms.assetid: 6a85b695-731a-4401-9c9c-fda6bc308558
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e24ae5f56a043d810eb805720606fd5b44d60cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769560"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a>Propriedade canônica PidTagOriginallyIntendedRecipEmailAddress

  
  
**Aplica-se a**: Outlook 
  
Contém o endereço de email do destinatário pretendido originalmente de uma mensagem de autoforwarded.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W  <br/> |
|Identificador:  <br/> |0x007C  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Servidor  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são exemplos das propriedades de endereço do destinatário pretendido originalmente da mensagem. Devem ser definidas pelo agente de automática que encaminhou a mensagem.
  
Essas propriedades correspondem ao atributo x. 400 relatório por destinatário.
  
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

