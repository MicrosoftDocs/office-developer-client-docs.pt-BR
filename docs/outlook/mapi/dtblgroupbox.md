---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 324cfe9d7c412b3bb0e3150b8eec51aaeb6a0e93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438390"
---
# <a name="dtblgroupbox"></a>DTBLGROUPBOX

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um controle de caixa de grupo que será usado em uma caixa de diálogo criada a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Macro relacionada:  <br/> |[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Posição na memória da cadeia de caracteres que acompanha a caixa de grupo. Se exibido, o rótulo aparece no lado superior esquerdo da caixa.
    
 **ulFlags**
  
> Bitmask de sinalizadores usados para designar o formato do rótulo apontado pelo **membro ulbLpszLabel.** O sinalizador a seguir pode ser definido: 
    
MAPI_UNICODE 
  
> O rótulo está no formato Unicode. Se o MAPI_UNICODE sinalizador não estiver definido, o rótulo está no formato ANSI.
    
## <a name="remarks"></a>Comentários

Uma **estrutura DTBLGROUPBOX** descreve um controle de caixa de grupo que é usado para associar visualmente outros controles na caixa de diálogo. A técnica de realçamento envolve os outros controles por uma caixa. 
  
Para uma visão geral das tabelas de exibição, consulte [Display Tables](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela de exibição.](display-table-implementation.md)
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

