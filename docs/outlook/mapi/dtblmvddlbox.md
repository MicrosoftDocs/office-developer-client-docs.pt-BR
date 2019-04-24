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
ms.openlocfilehash: 33b4fd87f33c26db15e1a6a28f077c393168db91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325757"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma lista suspensa que será usada em uma caixa de diálogo criada a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a>Membros

 **ulFlags**
  
> Serve deve ser zero.
    
 **ulMVPropTag**
  
> Marca de propriedade para uma propriedade de vários valores do tipo PT_MV_TSTRING. Os valores diferentes dessa propriedade são exibidos como entradas distintas na lista suspensa.
    
## <a name="remarks"></a>Comentários

Uma estrutura **DTBLMVDDLBOX** descreve uma lista suspensa com vários valores uma lista de itens somente leitura. Usando uma lista suspensa com vários valores, os valores são exibidos quando um usuário clica em uma barra de rolagem. 
  
Os dados exibidos vêm da propriedade identificada no membro **ulMVPropTag** . Não há nenhum requisito para ler a partir da interface de propriedade associada à tabela de exibição. Além disso, como os usuários não podem fazer seleções desses tipos de caixas de listagem, os dados não são gravados na interface de propriedade. 
  
Somente as propriedades de cadeia de caracteres de valores múltiplos têm suporte para a lista suspensa de vários valores; Não há suporte para outros tipos de propriedades de valores múltiplos. 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

