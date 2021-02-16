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
ms.openlocfilehash: d6e189f78dec2fc92f1804be93e7885b61734b03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431418"
---
# <a name="pidtagidentitydisplay-canonical-property"></a>Propriedade canônica PidTagIdentityDisplay

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome para exibição da identidade de um provedor de serviços, conforme definido em um sistema de mensagens. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W  <br/> |
|Identificador:  <br/> |0x3E00  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Status de MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades não aparecem como propriedades em nenhum objeto, mas apenas como uma coluna em uma tabela de status. Ele faz parte da identidade do provedor de serviços expondo a linha da tabela de status. A identidade do provedor normalmente se refere à sua conta no servidor, mas pode se referir a qualquer representação que o provedor define dentro do sistema de mensagens. 
  
Um provedor de serviços que fornece qualquer uma das propriedades de identidade deve fornecer todas elas. Provedores que pertencem ao mesmo serviço de mensagens devem expor os mesmos valores para as propriedades de identidade. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

