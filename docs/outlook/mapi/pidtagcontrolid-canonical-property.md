---
title: Propriedade canônica PidTagControlId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b27f59e0bfdcac8eca1751af2f07139f12e2b3a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334738"
---
# <a name="pidtagcontrolid-canonical-property"></a>Propriedade canônica PidTagControlId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um identificador exclusivo para um controle usado em uma caixa de diálogo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTROL_ID  <br/> |
|Identificador:  <br/> |0x3F07  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Tabela de exibição MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade contém um identificador exclusivo para o controle. Esse identificador deve conter uma estrutura [GUID](guid.md) e um valor binário do tipo **Long**. Todos os controles na caixa de diálogo devem usar o mesmo **GUID** para identificar o provedor de serviços, e cada controle deve usar um valor **Long** exclusivo para garantir que os controles não colidem. 
  
Essa propriedade é usada em notificações. Por exemplo, as notificações enviadas na tabela de exibição devem definir essa propriedade para identificar exclusivamente o controle a ser atualizado. 
  
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

