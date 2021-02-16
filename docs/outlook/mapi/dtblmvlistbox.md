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
ms.openlocfilehash: ae8f3ab28837bf0579549ead46c28477f815f35c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439699"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma lista de vários valores que será exibida em uma caixa de diálogo criada a partir de uma tabela de exibição.
  
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

## <a name="members"></a>Membros

 **ulFlags**
  
> Reservado; deve ser zero.
    
 **ulMVPropTag**
  
> Marca de propriedade para uma propriedade de vários valores do tipo PT_MV_TSTRING.
    
## <a name="remarks"></a>Comentários

Uma **estrutura DTBLMVLISTBOX** descreve uma lista de valores múltiplos padrão que tem uma lista de itens somente leitura. Usando uma lista de valores múltiplos padrão, os valores são exibidos imediatamente. 
  
Os dados exibidos vêm da propriedade identificada no **membro ulMVPropTag.** Não há necessidade de ler a partir da interface de propriedade que está associada à tabela de exibição. Além disso, como os usuários não conseguem fazer seleções desses tipos de listas, os dados não são gravados na interface de propriedades. 
  
Somente propriedades de cadeia de caracteres de valores múltiplos são suportadas para a lista de valores múltiplos; outros tipos de propriedade de vários valores não são suportados. 
  
Para uma visão geral das tabelas de exibição, consulte [Tabelas de Exibição.](display-tables.md) Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela de exibição.](display-table-implementation.md)
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

