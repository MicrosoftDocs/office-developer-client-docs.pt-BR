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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5256efbff734d4555ac263dd330e3349c789cd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406973"
---
# <a name="dtblcombobox"></a>DTBLCOMBOBOX

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um controle de caixa de combinação que será usado em uma caixa de diálogo criada a partir de uma tabela de exibição.
  
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

## <a name="members"></a>Members

 **ulbLpszCharsAllowed**
  
> Um deslocamento desde o início da estrutura **DTBLCOMBOBOX** até um filtro de cadeia de caracteres que descreve restrições, se for o caso, para os caracteres que podem ser inseridos no controle de edição da caixa de combinação. O filtro não é interpretado como uma expressão regular e o mesmo filtro é aplicado a cada caractere inserido. O formato do filtro é o seguinte: 
    
|**Caractere**|**Descrição**|
|:-----|:-----|
| `*` <br/> |Qualquer caractere é permitido (por exemplo,  `"*"` ).  <br/> |
| `[ ]` <br/> |Define um conjunto de caracteres (por exemplo,  `"[0123456789]"` ).  <br/> |
| `-` <br/> |Indica um intervalo de caracteres (por exemplo,  `"[a-z]"` ).  <br/> |
| `~` <br/> |Indica que esses caracteres não são permitidos. (por exemplo,  `"[~0-9]"` ).  <br/> |
| `\` <br/> |Usado para citação de qualquer um dos símbolos anteriores (por exemplo, os caracteres  `"[\-\\\[\]]"` -, \, [e ] são permitidos).  <br/> |
   
 **ulFlags**
  
> Bitmask de sinalizadores usados para designar o formato do filtro de cadeia de caracteres. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> O filtro está no formato Unicode. Se o MAPI_UNICODE sinalizador não estiver definido, o filtro está no formato ANSI.
    
 **ulNumCharsAllowed**
  
> Número máximo de caracteres que podem ser inseridos na caixa de texto da caixa de combinação.
    
 **ulPRPropertyName**
  
> Marca de propriedade de uma propriedade do tipo PT_TSTRING. 
    
 **ulPRTableName**
  
> Marca de propriedade de uma propriedade do tipo PT_OBJECT na qual uma interface **IMAPITable** pode ser aberta usando uma **chamada OpenProperty.** A tabela deve ter uma coluna com uma propriedade que seja do mesmo tipo que a propriedade identificada pelo **membro ulPRPropertyName.** As linhas da tabela são usadas para preencher a lista. 
    
## <a name="remarks"></a>Comentários

Uma **estrutura DTBLCOMBOBOX descreve** uma caixa de combinação um controle que consiste em uma lista e um campo de seleção. A lista apresenta as informações das quais um usuário pode selecionar, e o campo de seleção exibe a seleção atual. O campo de seleção é um controle de edição que também pode ser usado para inserir texto que ainda não está na lista. 
  
Os dois membros da marca de propriedade trabalham juntos para coordenar a exibição da lista com o controle de edição. Quando MAPI exibe pela primeira vez a caixa de combinação, ele chama o método **OpenProperty** da implementação **IMAPIProp** que está associada à tabela de exibição para recuperar a tabela representada pelo membro **ulPRTableName.** Esta tabela tem uma coluna em uma coluna que contém valores para a propriedade representada pelo **membro ulPRPropertyName.** Portanto, essa coluna deve ser do mesmo tipo que a **propriedade ulPRPropertyName** e ambas as colunas devem ser cadeias de caracteres. 
  
Os valores da coluna são exibidos na seção de lista da caixa de combinação. Portanto, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) não é uma marca de propriedade válida para **ulPRPropertyName**. Quando um usuário seleciona uma das linhas ou inser novos dados na caixa de texto, a propriedade **ulPRPropertyName** é definida como o valor selecionado ou inserido. 
  
Para exibir um valor inicial para o controle de edição, MAPI chama [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar os valores de propriedade da tabela de exibição. Se uma das propriedades recuperadas corresponde à propriedade representada pelo **membro ulPRPropertyName,** seu valor se torna o valor inicial. 
  
Para uma visão geral das tabelas de exibição, consulte [Display Tables](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela de exibição.](display-table-implementation.md)
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)
  
[Propriedade canônica PidTagControlType](pidtagcontroltype-canonical-property.md)


[Estruturas MAPI](mapi-structures.md)

