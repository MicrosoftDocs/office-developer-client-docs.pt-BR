---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f7c1241f2ad31dee8277f3b3b77ac02137067a12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576306"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma lista de valores múltiplos que será exibida em uma caixa de diálogo que é construída a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a>Members

 **ulFlags**
  
> Reservado; deve ser zero.
    
 **ulMVPropTag**
  
> Marca de propriedade para uma propriedade de valores múltiplos do tipo PT_MV_TSTRING.
    
## <a name="remarks"></a>Comentários

Uma estrutura **DTBLMVLISTBOX** descreve uma lista de valores múltiplos padrão que tem uma lista de itens de somente leitura. Usando uma lista de valores múltiplos padrão, os valores são exibidos imediatamente. 
  
Os dados que são exibidos provêm a propriedade identificada no membro **ulMVPropTag** . Não há nenhum requisito para a interface de propriedade que está associada com a tabela de exibição de leitura. Além disso, como os usuários não são capazes de realizar seleções desses tipos de listas, dados não são gravados na interface de propriedade. 
  
Somente as propriedades de cadeia de caracteres de valores múltiplos são suportadas para a lista de valores múltiplos; Não há suporte para outros tipos de propriedade de valores múltiplos. 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

