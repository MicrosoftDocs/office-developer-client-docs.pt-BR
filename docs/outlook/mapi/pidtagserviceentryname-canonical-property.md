---
title: Propriedade canônica PidTagServiceEntryName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceEntryName
api_type:
- COM
ms.assetid: 783f08aa-fb5a-432d-b8bd-48d69f0e5c38
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2c771f1d97305271b70102c148e62f30512974fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432468"
---
# <a name="pidtagserviceentryname-canonical-property"></a>Propriedade canônica PidTagServiceEntryName

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome da função de ponto de entrada para configuração de um serviço de mensagens.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SERVICE_ENTRY_NAME  <br/> |
|Identificador:  <br/> |0x3D0B  <br/> |
|Tipo de dados:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

É recomendável que os implementadores de serviço de mensagens forneçam um ponto de entrada de serviço de mensagens, mas o ponto de entrada não é necessário. No enTanto, o ponto de entrada deve ser fornecido somente se as propriedades de configuração relacionadas existirem. Se essas propriedades não existirem, MAPI pressupõe que nenhum ponto de entrada seja fornecido.
  
A biblioteca de vínculo dinâmico (DLL) na qual a função de ponto de entrada aparece é nomeada pela propriedade **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).
  
Para obter mais informações sobre os pontos de entrada do serviço de mensagens, consulte [implementando uma função de ponto de entrada do provedor de serviços](implementing-a-service-provider-entry-point-function.md).
  
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

