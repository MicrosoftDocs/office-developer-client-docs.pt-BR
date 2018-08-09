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
ms.openlocfilehash: 0d75616aaa6599709828d32393a316c642bc613b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770019"
---
# <a name="pidtagserviceentryname-canonical-property"></a>Propriedade canônica PidTagServiceEntryName

  
  
**Aplica-se a**: Outlook 
  
Contém o nome da função de ponto de entrada para a configuração de um serviço de mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SERVICE_ENTRY_NAME  <br/> |
|Identificador:  <br/> |0x3D0B  <br/> |
|Tipo de dados:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

É recomendável que implementadores de serviço de mensagem fornecem um ponto de entrada de serviço de mensagem, mas o ponto de entrada não é necessário. No entanto, o ponto de entrada deve ser fornecido somente se as propriedades de configuração relacionados existirem. Se essas propriedades não existirem, MAPI pressupõe que nenhum ponto de entrada é fornecido.
  
A biblioteca de vínculo dinâmico (DLL) no qual a função do ponto de entrada aparece é nomeada pela propriedade **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).
  
Para obter mais informações sobre pontos de entrada de serviço de mensagem, consulte [Implementando uma função de ponto de entrada de provedor de serviço](implementing-a-service-provider-entry-point-function.md).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

