---
title: Propriedade canônica PidTagIdentitySearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentitySearchKey
api_type:
- HeaderDef
ms.assetid: 5fe55ba7-4ecd-4a43-ab5b-2ef595c2cdd9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5f5f5eaa41d6256bed69b2cd9a91208181d5bda1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346631"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a>Propriedade canônica PidTagIdentitySearchKey

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a chave de pesquisa para a identidade de um provedor de serviços, conforme definido em um sistema de mensagens. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_IDENTITY_SEARCH_KEY  <br/> |
|Identificador:  <br/> |0x3E05  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Status de MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade não aparece como uma propriedade em qualquer objeto, mas somente como uma coluna em uma tabela de status. Ele faz parte da identidade do provedor de serviços que expõe a linha da tabela de status. A identidade do provedor geralmente se refere à sua conta no servidor, mas pode se referir a qualquer representação que o provedor define no sistema de mensagens. 
  
Um provedor de serviços que forneça qualquer uma das propriedades de identidade deve fornecer todos eles. Os provedores que pertencem ao mesmo serviço de mensagens devem expor os mesmos valores para as propriedades de identidade. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

