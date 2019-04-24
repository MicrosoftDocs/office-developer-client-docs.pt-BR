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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aa3345740c534b5ff156f062e731c98bc6164eed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287157"
---
# <a name="dtbllabel"></a>DTBLLABEL

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um rótulo que será usado em uma caixa de diálogo criada a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Macro relacionada  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>Members

 **ulbLpszLabelName**
  
> Posição na memória do rótulo de cadeia de caracteres.
    
 **ulFlags**
  
> Bitmask dos sinalizadores usados para designar o formato do rótulo apontado pelo membro **ulbLpszLabelName** . O seguinte sinalizador pode ser definido: 
    
MAPI_UNICODE 
  
> O rótulo está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo estará no formato ANSI.
    
## <a name="remarks"></a>Comentários

Uma estrutura **DTBLLABEL** descreve um texto de controle de rótulo que é exibido com outro tipo de controle para adicionar significado a esse controle. Por exemplo, a maioria dos controles de edição são posicionados ao lado de rótulos para informar ao usuário sobre o tipo de informação a ser inserido. Alguns controles, como caixas de grupo e botões de opção, mantêm seus próprios rótulos. 
  
O rótulo pode incluir um acelerador do Windows, identificado como o caractere após o&amp;e comercial (). Pressionar a tecla aceleradora coloca o foco no primeiro controle não rótulo, sem botão, seguindo este rótulo na tabela de exibição.
  
Não há suporte para rótulos de várias linhas. Mostrar várias linhas requer vários rótulos.
  
Não é possível usar um rótulo como um controle de edição somente leitura. A diferença é que um controle de edição pode ser selecionado e copiado, enquanto um rótulo não pode. 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

