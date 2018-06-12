---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 28f6471f74fb0fcc4f7e2f4114f0790e1564e17e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766479"
---
# <a name="dtbllabel"></a>DTBLLABEL

  
  
**Aplica-se a**: Outlook 
  
Descreve um rótulo que será usado em uma caixa de diálogo que é construída a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Macro relacionada  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>Membros

 **ulbLpszLabelName**
  
> Posição na memória do rótulo de cadeia de caracteres do caractere.
    
 **ulFlags**
  
> Bitmask dos sinalizadores usados para designar o formato do rótulo apontado pelo membro **ulbLpszLabelName** . O seguinte sinalizador pode ser definido: 
    
MAPI_UNICODE 
  
> O rótulo está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo está no formato ANSI.
    
## <a name="remarks"></a>Coment�rios

Uma estrutura **DTBLLABEL** descreve um texto de controle do rótulo que é exibido com outro tipo de controle para adicionar o significado a esse controle. Por exemplo, a maioria dos controles de edição posicionados ao lado de rótulos para informar ao usuário sobre o tipo de informação a ser inserido. Alguns controles, como caixas de grupo e os botões de opção, mantenha suas próprias rótulos. 
  
O rótulo pode incluir um acelerador do Windows, identificado como o caractere seguinte o e comercial (&amp;). Pressionar a tecla aceleradora coloca o foco do primeiro nonlabel, seguindo este rótulo na tabela a exibição de controle de nonbutton.
  
Não há nenhum suporte para os rótulos de várias linhas. Mostrar várias linhas requer várias etiquetas.
  
Não é possível usar um rótulo como um controle de edição de somente leitura. A diferença é que um controle de edição pode ser selecionado e copiado enquanto um rótulo não é possível. 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

