---
title: Propriedade canônica PidTagProviderOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4cd865fbc443a20ebf4b4cd9722fe52c44d5eddc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573807"
---
# <a name="pidtagproviderordinal-canonical-property"></a>Propriedade canônica PidTagProviderOrdinal

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o índice baseado em zero da posição de um provedor de serviços na tabela de provedor.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROVIDER_ORDINAL  <br/> |
|Identificador:  <br/> |0x300D  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI comuns  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é computada pelo MAPI.
  
Obter a tabela de provedor chamando o método [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) . Classificar a tabela de provedor nessa propriedade para exibir a ordem de transporte. 
  
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

