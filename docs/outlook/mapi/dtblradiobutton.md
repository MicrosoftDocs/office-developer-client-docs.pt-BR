---
title: DTBLRADIOBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLRADIOBUTTON
api_type:
- COM
ms.assetid: 64cef938-ef6f-43bb-8f6e-d4cd4d6c9888
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339414"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um botão de opção que fará parte de um grupo de botões de opção. O grupo de botões de opção será usado em uma caixa de diálogo criada a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _DTBLRADIOBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulcButtons;
  ULONG ulPropTag;
  long lReturnValue;
} DTBLRADIOBUTTON, FAR *LPDTBLRADIOBUTTON;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Posição na memória do rótulo de cadeia de caracteres do botão de opção.
    
 **ulFlags**
  
> Bitmask dos sinalizadores usados para designar o formato do rótulo apontado pelo membro **ulbLpszLabel** . O seguinte sinalizador pode ser definido: 
    
MAPI_UNICODE 
  
> O rótulo está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo estará no formato ANSI.
    
 **ulcButtons**
  
> Contagem de botões no grupo de botões de opção. As estruturas **DTBLRADIOBUTTON** para os outros botões no grupo devem estar contidas em linhas sucessivas da tabela de exibição. Cada uma dessas linhas deve conter o mesmo valor para o membro **ulcButtons** . 
    
 **ulPropTag**
  
> Marca de propriedade de uma propriedade do tipo PT_LONG. A seleção inicial no grupo de botões de opção é baseada no valor inicial dessa propriedade. Cada botão no grupo deve ter **ulPropTag** definido para a mesma propriedade. 
    
 **lReturnValue**
  
> Número exclusivo que identifica o botão selecionado.
    
## <a name="remarks"></a>Comentários

Uma estrutura **DTBLRADIOBUTTON** descreve um botão de opção um controle de botão que é associado a um grupo de botões. Somente um botão no grupo pode ser verificado; definir um botão faz com que os outros botões do grupo sejam desdefinidos. 
  
A contagem de botões é o número de botões de opção no grupo. As estruturas dos outros botões de opção no grupo devem estar nas linhas subsequentes na tabela de exibição. Cada uma dessas estruturas deve ter o mesmo valor para a contagem de botão.
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[Estruturas MAPI](mapi-structures.md)

