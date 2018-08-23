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
ms.openlocfilehash: efb0812a88ad435c2456a729a6e950b371cc0250
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595346"
---
# <a name="pidtagnull-canonical-property"></a>Propriedade canônica PidTagNull

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Representa um valor nulo ou configuração de uma propriedade ou reserva espaço de matriz.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_NULL  <br/> |
|Identificador:  <br/> |0x0000  <br/> |
|Tipo de dados:  <br/> |PT_NULL  <br/> |
|Área:  <br/> |Comuns  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada para reservar espaço em matrizes de estruturas de [SPropValue](spropvalue.md) . Ele é usado em uma matriz de estruturas de [SPropTagArray](sproptagarray.md) para informar o método para reservar espaço na matriz retornada de estruturas de **SPropValue** . Isso permite que as propriedades computadas ser preenchido uma maneira barata. 
  
Para obter mais informações, consulte [Visão geral do tipo de propriedade de MAPI](mapi-property-type-overview.md).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas em contatos e listas de distribuição pessoal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

