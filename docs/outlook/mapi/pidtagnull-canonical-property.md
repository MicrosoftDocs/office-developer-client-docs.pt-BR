---
title: Propriedade canônica PidTagNull
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7e9c3340dfad47a811b56c86e8e6104fb6aac7c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329264"
---
# <a name="pidtagnull-canonical-property"></a>Propriedade canônica PidTagNull

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Representa um valor nulo ou uma configuração de uma propriedade ou reserva espaço de matriz.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_NULL  <br/> |
|Identificador:  <br/> |0x0000  <br/> |
|Tipo de dados:  <br/> |PT_NULL  <br/> |
|Área:  <br/> |Comum  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada para reservar espaço em matrizes de [estruturas SPropValue.](spropvalue.md) Ele é usado em uma matriz de [estruturas SPropTagArray](sproptagarray.md) para dizer ao método para reservar espaço na matriz retornada de **estruturas SPropValue.** Isso permite que as propriedades computadas sejam preenchidas de maneira barata. 
  
Para obter mais informações, consulte [Visão geral do tipo de propriedade MAPI.](mapi-property-type-overview.md)
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas em contatos e listas de distribuição pessoais.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

