---
title: Propriedade canônica PidTagServiceName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e5659113b1c6579913042ae0c8dfcd03e9802621
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438957"
---
# <a name="pidtagservicename-canonical-property"></a>Propriedade canônica PidTagServiceName

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome de um serviço de mensagens, conforme definido pelo usuário no arquivo MapiSvc. inf.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W  <br/> |
|Identificador:  <br/> |0x3D09  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

O nome contido nessas propriedades é específico para o serviço de mensagens. Ele vem da seção [serviços] no MapiSvc. inf.
  
Essas propriedades aparecem como uma coluna na tabela de serviço de mensagens e podem ser usadas para filtrar serviços. Como ele é usado para identificar e filtrar serviços, o valor não deve ser localizado.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

