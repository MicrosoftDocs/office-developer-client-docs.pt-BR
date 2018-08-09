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
ms.openlocfilehash: dee12ba9da83d2167afe13d00270a900bf0d73d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766481"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**Aplica-se a**: Outlook 
  
Descreve um botão de opção que farão parte de um grupo de botão de opção. O grupo de botão de opção será usado em uma caixa de diálogo que é construída a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
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
  
> Posição na memória do rótulo de cadeia de caracteres de caractere para o botão de opção.
    
 **ulFlags**
  
> Bitmask dos sinalizadores usados para designar o formato do rótulo apontado pelo membro **ulbLpszLabel** . O seguinte sinalizador pode ser definido: 
    
MAPI_UNICODE 
  
> O rótulo está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo está no formato ANSI.
    
 **ulcButtons**
  
> Contagem de botões do grupo de botão de rádio. As estruturas de **DTBLRADIOBUTTON** para os outros botões no grupo devem estar contidas em sucessivas linhas da tabela exibição. Cada um nessas linhas deve conter o mesmo valor para o membro **ulcButtons** . 
    
 **ulPropTag**
  
> Marca de propriedade para uma propriedade do tipo PT_LONG. A seleção inicial no grupo de botões de rádio baseia-se no valor inicial dessa propriedade. Cada botão do grupo deve ter **ulPropTag** definido para a mesma propriedade. 
    
 **lReturnValue**
  
> Número exclusivo que identifica o botão selecionado.
    
## <a name="remarks"></a>Comentários

Uma estrutura **DTBLRADIOBUTTON** descreve um botão de opção de um controle de botão que está associado um grupo de botões. Somente um botão do grupo pode ser verificado; a definição de um botão faz com que os outros botões no grupo a ser desfeito. 
  
A contagem de botão é o número de botões de opção no grupo. As estruturas para os outros botões de opção no grupo devem estar no subsequentes linhas da tabela de exibição. Cada uma dessas estruturas deve ter o mesmo valor para sua contagem de botão.
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[Estruturas MAPI](mapi-structures.md)

