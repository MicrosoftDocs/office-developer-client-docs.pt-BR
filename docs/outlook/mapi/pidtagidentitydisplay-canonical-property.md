---
title: Propriedade canônica PidTagIdentityDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityDisplay
api_type:
- HeaderDef
ms.assetid: ad9756c1-c1f9-4ab3-a58a-31e574dd9530
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6cfc4d6eab5b2f19bcfd4c7e2a8fc9fa1494afa4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585574"
---
# <a name="pidtagidentitydisplay-canonical-property"></a>Propriedade canônica PidTagIdentityDisplay

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome de exibição para a identidade de um provedor de serviços, conforme definido em um sistema de mensagens. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W  <br/> |
|Identificador:  <br/> |0x3E00  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Status MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades não aparecem como propriedades em qualquer objeto, mas apenas como uma coluna em uma tabela de status. Ele é parte da identidade do provedor de serviços expondo a linha da tabela de status. Normalmente, a identidade do provedor refere-se a sua conta no servidor, mas pode se referir a qualquer representação que o provedor define dentro do sistema de mensagens. 
  
Um provedor de serviços que forneçam qualquer uma das propriedades identity deve fornecer aos todos eles. Os provedores que pertencem ao mesmo serviço de mensagem devem expor os mesmos valores para as propriedades de identidade. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

