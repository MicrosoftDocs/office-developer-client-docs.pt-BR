---
title: DTBLCOMBOBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCOMBOBOX
api_type:
- COM
ms.assetid: 73b68614-6aca-4669-b879-5631c5d6483c
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 3a5188ea9f83d05722c6b5ab81d9e796b33ef254
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766461"
---
# <a name="dtblcombobox"></a>DTBLCOMBOBOX

  
  
**Aplica-se a**: Outlook 
  
Descreve um controle de caixa de combinação que será usado em uma caixa de diálogo construída a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Macro relacionada:  <br/> |[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |
   
```cpp
typedef struct _DTBLCOMBOBOX
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPRPropertyName;
  ULONG ulPRTableName;
} DTBLCOMBOBOX, FAR *LPDTBLCOMBOBOX;

```

## <a name="members"></a>Membros

 **ulbLpszCharsAllowed**
  
> Deslocamento desde o início da estrutura **DTBLCOMBOBOX** para um filtro de cadeia de caracteres de caracteres que descreve restrições, caso haja alguma, para os caracteres que podem ser inseridos em da caixa de combinação controle de edição. O filtro não será interpretado como uma expressão regular e o mesmo filtro é aplicado a cada caractere inserido. O formato do filtro é da seguinte maneira: 
    
|**Caractere**|**Descrição**|
|:-----|:-----|
| `*` <br/> |Qualquer caractere é permitido (por exemplo, `"*"`).  <br/> |
| `[ ]` <br/> |Define um conjunto de caracteres (por exemplo, `"[0123456789]"`).  <br/> |
| `-` <br/> |Indica um intervalo de caracteres (por exemplo, `"[a-z]"`).  <br/> |
| `~` <br/> |Indica que esses caracteres não são permitidos. (por exemplo, `"[~0-9]"`).  <br/> |
| `\` <br/> |Usado para quote qualquer um dos símbolos anteriores (por exemplo, `"[\-\\\[\]]"` significa-, \, [, e] caracteres são permitidos).  <br/> |
   
 **ulFlags**
  
> Bitmask dos sinalizadores usado para designar o formato do filtro de cadeia de caracteres do caractere. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> O filtro está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o filtro está no formato ANSI.
    
 **ulNumCharsAllowed**
  
> Número máximo de caracteres que podem ser inseridos na caixa de texto da caixa de combinação.
    
 **ulPRPropertyName**
  
> Marca de propriedade para uma propriedade do tipo PT_TSTRING. 
    
 **ulPRTableName**
  
> Marca de propriedade para uma propriedade de PT_OBJECT tipo no qual uma interface **IMAPITable** pode ser aberta usando uma chamada **OpenProperty** . A tabela deve ter uma coluna com uma propriedade que é o mesmo tipo que a propriedade identificada pelo membro **ulPRPropertyName** . As linhas da tabela são usadas para preencher a lista. 
    
## <a name="remarks"></a>Coment�rios

Uma estrutura **DTBLCOMBOBOX** descreve uma caixa de combinação de um controle que consiste em uma lista e um campo da seleção. A lista apresenta as informações a partir do qual um usuário pode selecionar e o campo de seleção exibir a seleção atual. O campo de seleção é um controle de edição que também pode ser usado para inserir texto ainda não estiver na lista. 
  
Os membros da marca de dois propriedade funcionam juntos para coordenar a exibição de lista com o controle de edição. Quando MAPI primeiro exibe a caixa de combinação, ele chama o método **OpenProperty** da implementação **IMAPIProp** associado com a tabela de exibição para recuperar a tabela representada pelo membro **ulPRTableName** . Esta tabela tem uma coluna de uma coluna que contém os valores da propriedade representado pelo membro **ulPRPropertyName** . Portanto, essa coluna deve ser do mesmo tipo que a propriedade **ulPRPropertyName** e as duas colunas devem ser cadeias de caracteres. 
  
Os valores da coluna são exibidos na seção lista da caixa de combinação. Portanto, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) não é uma marca de propriedade válido para **ulPRPropertyName**. Quando um usuário seleciona uma das linhas ou insere novos dados na caixa de texto, a propriedade **ulPRPropertyName** é definida como o valor digitado ou selecionado. 
  
Para exibir um valor inicial para o controle de edição, MAPI chama [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar os valores de propriedade para a exibição de tabela. Se uma das propriedades recuperadas corresponder a propriedade representada pelo membro **ulPRPropertyName** , seu valor torna-se o valor inicial. 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)
  
[Propriedade canônico de PidTagControlType](pidtagcontroltype-canonical-property.md)


[Estruturas MAPI](mapi-structures.md)

