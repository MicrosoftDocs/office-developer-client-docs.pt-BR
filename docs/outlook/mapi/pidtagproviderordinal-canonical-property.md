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
ms.openlocfilehash: fbeb63bbae23f8f7f78c92d3abed6bea1c3ac85d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438348"
---
# <a name="pidtagproviderordinal-canonical-property"></a>Propriedade canônica PidTagProviderOrdinal

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o índice baseado em zero da posição de um provedor de serviços na tabela do provedor.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROVIDER_ORDINAL  <br/> |
|Identificador:  <br/> |0x300D  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI comum  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é calculada por MAPI.
  
Obtenha a tabela do provedor chamando o [método IMsgServiceAdmin::GetProviderTable.](imsgserviceadmin-getprovidertable.md) Classificar a tabela do provedor nessa propriedade para exibir o pedido de transporte. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

