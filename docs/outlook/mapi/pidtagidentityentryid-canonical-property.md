---
title: Propriedade canônica PidTagIdentityEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 099df2211e87e253ab1be520378b3a2b2ca7d4c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327927"
---
# <a name="pidtagidentityentryid-canonical-property"></a>Propriedade canônica PidTagIdentityEntryId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o identificador de entrada para a identidade de um provedor de serviços, conforme definido em um sistema de mensagens. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_IDENTITY_ENTRYID  <br/> |
|Identificador:  <br/> |0x3E01  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Status de MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade não aparece como uma propriedade em qualquer objeto, mas somente como uma coluna em uma tabela de status. Ele faz parte da identidade do provedor de serviços que expõe a linha da tabela de status. A identidade do provedor geralmente se refere à sua conta no servidor, mas pode se referir a qualquer representação que o provedor define no sistema de mensagens. 
  
Este propriedade é normalmente definido para o identificador de entrada do catálogo de endereços apropriado. 
  
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

