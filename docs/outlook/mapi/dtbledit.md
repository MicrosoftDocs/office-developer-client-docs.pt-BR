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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b07ea265b5dcc6b9a9abb15c6be7ac9e0f94e8ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404677"
---
# <a name="dtbledit"></a>DTBLEDIT

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um controle de edição que será usado em uma caixa de diálogo criada a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
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

## <a name="members"></a>Members

 **ulbLpszCharsAllowed**
  
> Um offset do início da estrutura **DTBLEDIT** para um filtro de cadeia de caracteres que descreve as restrições, se houver, para os caracteres que podem ser inseridos no controle de edição. O filtro não é interpretado como uma expressão regular e o mesmo filtro é aplicado a todos os caracteres inseridos. O formato do filtro é o seguinte: 
    
|**Caractere**|**Descrição**|
|:-----|:-----|
| `*` <br/> |Qualquer caractere é permitido (por exemplo, `"*"`).  <br/> |
| `[ ]` <br/> |Define um conjunto de caracteres (por exemplo, `"[0123456789]".`)  <br/> |
| `-` <br/> |Indica um intervalo de caracteres (por exemplo, `"[a-z]"`).  <br/> |
| `~` <br/> |Indica que esses caracteres não são permitidos (por exemplo, `"[~0-9]"`).  <br/> |
| `\` <br/> |Usado para citar qualquer um dos símbolos anteriores (por exemplo, `"[\-\\\[\]]"` os caracteres significa \, -, [e] são permitidos).  <br/> |
   
 **ulFlags**
  
> Bitmask dos sinalizadores usados para designar o formato do filtro de caracteres. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE
  
> O filtro está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o filtro estará no formato ANSI.
    
 **ulNumCharsAllowed**
  
> Número máximo de caracteres que o usuário pode digitar na caixa de texto.
    
 **ulPropTag**
  
> Marca de propriedade de uma propriedade do tipo PT_TSTRING. O membro **ulPropTag** identifica a propriedade de cadeia de caracteres cujos dados são exibidos e editados no controle de edição. 
    
## <a name="remarks"></a>Comentários

Uma estrutura **DTBLEDIT** descreve um controle de edição uma área em uma caixa de diálogo que contém informações alfanuméricas. Quase todas as caixas de diálogo têm pelo menos um controle de edição. Os controles de edição podem ser modificados por um usuário ou somente leitura. 
  
Os controles de edição também podem ser de linha única ou várias linhas. Os controles de edição de várias linhas normalmente têm uma barra de rolagem associada a eles. 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[Propriedade canônica PidTagControlType](pidtagcontroltype-canonical-property.md)


[Estruturas MAPI](mapi-structures.md)

