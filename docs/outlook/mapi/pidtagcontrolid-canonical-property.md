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
ms.openlocfilehash: 799f83b397cbef9d7dcb6c9a88154b88afe35675
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19769124"
---
# <a name="pidtagcontrolid-canonical-property"></a>Propriedade canônica PidTagControlId

  
  
**Aplica-se a**: Outlook 
  
Contém um identificador exclusivo para um controle usado em uma caixa de diálogo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTROL_ID  <br/> |
|Identificador:  <br/> |0x3F07  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Tabela de exibição MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade contém um identificador exclusivo para o controle. Esse identificador deve conter uma estrutura [GUID](guid.md) e um valor binário do tipo **LONG**. Todos os controles na caixa de diálogo devem usar o mesmo **GUID** para identificar o provedor de serviço, e cada controle deve usar um único valor **longo** para garantir que os controles não coincidem. 
  
Essa propriedade é usada em notificações. Por exemplo, notificações enviadas na tabela exibição devem definir essa propriedade para identificar exclusivamente o controle a ser atualizado. 
  
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

