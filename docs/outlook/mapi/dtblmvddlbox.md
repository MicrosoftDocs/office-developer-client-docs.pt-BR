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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420742"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma lista drop-down que será usada em uma caixa de diálogo criada a partir de uma tabela de exibição.
  
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

## <a name="members"></a>Membros

 **ulFlags**
  
> Reservado; deve ser zero.
    
 **ulMVPropTag**
  
> Marca de propriedade para uma propriedade de vários valores do tipo PT_MV_TSTRING. Os valores diferentes dessa propriedade são exibidos como entradas distintas na lista lista listada.
    
## <a name="remarks"></a>Comentários

A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items. Usando uma lista de vários valores, os valores são exibidos quando um usuário clica em uma barra de rolagem. 
  
Os dados exibidos vêm da propriedade identificada no **membro ulMVPropTag.** Não há necessidade de ler a partir da interface de propriedade que está associada à tabela de exibição. Além disso, como os usuários não conseguem fazer seleções desses tipos de caixas de listagem, os dados não são gravados na interface de propriedades. 
  
Somente propriedades de cadeia de caracteres de valores múltiplos são suportadas para a lista de lista de vários valores; outros tipos de propriedade de vários valores não são suportados. 
  
Para uma visão geral das tabelas de exibição, consulte [Tabelas de Exibição.](display-tables.md) Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela de exibição.](display-table-implementation.md)
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

