---
title: DTBLEDIT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLEDIT
api_type:
- COM
ms.assetid: ec3566a0-75ad-466d-a61e-f7d61ccb946d
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: d0418ac2ec5d01d58c63e4ad48a1066cc386e946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766472"
---
# <a name="dtbledit"></a>DTBLEDIT

  
  
**Aplica-se a**: Outlook 
  
Descreve um controle de edição que será usado em uma caixa de diálogo construída a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Macro relacionada:  <br/> |[SizedDtblEdit](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a>Membros

 **ulbLpszCharsAllowed**
  
> Deslocamento desde o início da estrutura **DTBLEDIT** para um filtro de sequência de caracteres que descreve restrições, se houver, com os caracteres que podem ser inseridos em um controle de edição. O filtro não será interpretado como uma expressão regular e o mesmo filtro é aplicado a cada caractere inserido. O formato do filtro é da seguinte maneira: 
    
|**Caractere**|**Descrição**|
|:-----|:-----|
| `*` <br/> |Qualquer caractere é permitido (por exemplo, `"*"`).  <br/> |
| `[ ]` <br/> |Define um conjunto de caracteres (por exemplo, `"[0123456789]".`)  <br/> |
| `-` <br/> |Indica um intervalo de caracteres (por exemplo, `"[a-z]"`).  <br/> |
| `~` <br/> |Indica que esses caracteres não são permitidos (por exemplo, `"[~0-9]"`).  <br/> |
| `\` <br/> |Usado para quote qualquer um dos símbolos anteriores (por exemplo, `"[\-\\\[\]]"` significa-, \, [, e] caracteres são permitidos).  <br/> |
   
 **ulFlags**
  
> Bitmask dos sinalizadores usado para designar o formato do filtro caractere. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE
  
> O filtro está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o filtro está no formato ANSI.
    
 **ulNumCharsAllowed**
  
> Número máximo de caracteres que o usuário pode digitar na caixa de texto.
    
 **ulPropTag**
  
> Marca de propriedade para uma propriedade do tipo PT_TSTRING. O membro **ulPropTag** identifica a propriedade de cadeia de caracteres cujos dados são exibidos e editados no controle de edição. 
    
## <a name="remarks"></a>Coment�rios

Uma estrutura **DTBLEDIT** descreve um controle de edição de uma área em uma caixa de diálogo que contém informações alfanuméricos. Quase todas as caixas de diálogo possuem o controle de edição de pelo menos um. Controles de edição podem ser modificável por um usuário ou somente leitura. 
  
Controles de edição também podem ser único linha ou multiline. Controles de edição de várias linhas geralmente têm uma barra de rolagem associada a eles. 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[Propriedade canônico de PidTagControlType](pidtagcontroltype-canonical-property.md)


[Estruturas MAPI](mapi-structures.md)

