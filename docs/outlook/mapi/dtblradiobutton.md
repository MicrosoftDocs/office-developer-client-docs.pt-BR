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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434596"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um botão de rádio que fará parte de um grupo de botões de rádio. O grupo de botões de rádio será usado em uma caixa de diálogo criada a partir de uma tabela de exibição.
  
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
  
> Posição na memória do rótulo de cadeia de caracteres do botão de rádio.
    
 **ulFlags**
  
> Bitmask de sinalizadores usados para designar o formato do rótulo apontado pelo **membro ulbLpszLabel.** O sinalizador a seguir pode ser definido: 
    
MAPI_UNICODE 
  
> O rótulo está no formato Unicode. Se o MAPI_UNICODE sinalizador não estiver definido, o rótulo está no formato ANSI.
    
 **ulcButtons**
  
> Contagem de botões no grupo de botões de rádio. As **estruturas DTBLRADIOBUTTON** dos outros botões no grupo devem estar contidas em linhas sucessivas da tabela de exibição. Cada uma dessas linhas deve conter o mesmo valor para o **membro ulcButtons.** 
    
 **ulPropTag**
  
> Marca de propriedade de uma propriedade do tipo PT_LONG. A seleção inicial no grupo de botões de rádio baseia-se no valor inicial dessa propriedade. Cada botão no grupo deve ter **ulPropTag** definido como a mesma propriedade. 
    
 **lReturnValue**
  
> Número exclusivo que identifica o botão selecionado.
    
## <a name="remarks"></a>Comentários

Uma **estrutura DTBLRADIOBUTTON** descreve um botão de botão de rádio que está associado a um grupo de botões. Somente um botão no grupo pode ser verificado; definir um botão faz com que os outros botões no grupo sejam desa definir. 
  
A contagem de botões é o número de botões de rádio no grupo. As estruturas dos outros botões de rádio no grupo devem estar em linhas subsequentes na tabela de exibição. Cada uma dessas estruturas deve ter o mesmo valor para sua contagem de botões.
  
Para uma visão geral das tabelas de exibição, consulte [Tabelas de Exibição.](display-tables.md) Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela de exibição.](display-table-implementation.md)
  
## <a name="see-also"></a>Confira também



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[Estruturas MAPI](mapi-structures.md)

