---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ede0a448a32565446e614fc2d14f2a72a9549dad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766482"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**Aplica-se a**: Outlook 
  
Descreve uma lista suspensa que será usada em uma caixa de diálogo que é construída a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a>Members

 **ulFlags**
  
> Reservado; deve ser zero.
    
 **ulMVPropTag**
  
> Marca de propriedade para uma propriedade de valores múltiplos do tipo PT_MV_TSTRING. Os diferentes valores dessa propriedade são exibidos como distintas entradas na lista suspensa.
    
## <a name="remarks"></a>Comentários

Uma estrutura **DTBLMVDDLBOX** descreve uma lista suspensa de valores múltiplos uma lista de somente leitura de itens. Usando uma lista suspensa de valores múltiplos, os valores são exibidos quando um usuário clica em uma barra de rolagem. 
  
Os dados que são exibidos provêm a propriedade identificada no membro **ulMVPropTag** . Não há nenhum requisito para a interface de propriedade que está associada com a tabela de exibição de leitura. Além disso, como os usuários não são capazes de realizar seleções contra esses tipos de caixas de listagem, dados não são gravados na interface de propriedade. 
  
Somente as propriedades de cadeia de caracteres de valores múltiplos são suportadas para a lista de valores múltiplos suspensa; Não há suporte para outros tipos de propriedade de valores múltiplos. 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

