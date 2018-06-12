---
title: Propriedade canônico de PidTagServiceUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceUid
api_type:
- COM
ms.assetid: 9d99a3b6-d0b4-4e8a-8f08-f46fdeb6b3e7
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 304efc3f4ea903f9ed0e9fcf95c7100fa6ebfc95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770045"
---
# <a name="pidtagserviceuid-canonical-property"></a>Propriedade canônico de PidTagServiceUid

  
  
**Aplica-se a**: Outlook 
  
Contém a estrutura [MAPIUID](mapiuid.md) para um serviço de mensagem. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SERVICE_UID  <br/> |
|Identificador:  <br/> |0x3D0C  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Coment�rios

Essa propriedade é computada pelo MAPI em objetos de seção de perfil. MAPI utiliza para todos os provedores que pertencem ao mesmo serviço de mensagem de grupo. Essa propriedade é fornecida como um parâmetro para a maioria dos métodos [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Ele não deve aparecer em MAPISVC. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedade canônico para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes de MAPI para nomes de propriedade canônico](mapping-mapi-names-to-canonical-property-names.md)

