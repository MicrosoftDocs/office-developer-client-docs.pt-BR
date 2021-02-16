---
title: DTCTL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTCTL
api_type:
- COM
ms.assetid: 6d1589e9-b171-427a-9a3e-b4154ee8ceb6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2a2ca1fba5dceb45b41c2f25a96e163f02c41440
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421498"
---
# <a name="dtctl"></a>DTCTL

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um controle que será usado em uma caixa de diálogo criada a partir de uma tabela de exibição. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulCtlType;
  ULONG ulCtlFlags;
  LPBYTE lpbNotif;
  ULONG cbNotif;
  LPSTR lpszFilter;
  ULONG ulItemID;
  union
  {
    LPVOID lpv;
    LPDTBLLABEL lplabel;
    LPDTBLEDIT lpedit;
    LPDTBLLBX lplbx;
    LPDTBLCOMBOBOX lpcombobox;
    LPDTBLDDLBX lpddlbx;
    LPDTBLCHECKBOX lpcheckbox;
    LPDTBLGROUPBOX lpgroupbox;
    LPDTBLBUTTON lpbutton;
    LPDTBLRADIOBUTTON lpradiobutton;
    LPDTBLMVLISTBOX lpmvlbx;
    LPDTBLMVDDLBX lpmvddlbx;
    LPDTBLPAGE lppage;
  } ctl;
} DTCTL, FAR *LPDTCTL;

```

## <a name="members"></a>Members

**ulCtlType**
  
> Tipo de controle incluído no membro **ctl** e que corresponde à propriedade **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) do controle. Os valores possíveis são:
    
DTCT_LABEL 
  
> Controle de Rótulo.
    
DTCT_EDIT 
  
> Controle de edição.
    
DTCT_LBX 
  
> Controle de caixa de listagem.
    
DTCT_COMBOBOX 
  
> Controle de caixa de combinação.
    
DTCT_DDLBX 
  
> Controle de lista drop-down.
    
DTCT_CHECKBOX 
  
> Controle de caixa de seleção.
    
DTCT_GROUPBOX 
  
> Controle de caixa de grupo.
    
DTCT_BUTTON 
  
> Controle de botão.
    
DTCT_PAGE 
  
> Controle de página com guias.
    
DTCT_RADIOBUTTON 
  
> Controle de botão de botão de rádio.
    
DTCT_MVLISTBOX 
  
> Controle de lista de valores múltiplos.
    
DTCT_MVDDLBX 
  
> Controle de lista de valores múltiplos.
    
**ulCtlFlags**
  
> Bitmask de sinalizadores que descreve os recursos do controle e corresponde à propriedade **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) do controle. Esses sinalizadores podem ser definidos apenas para caixas de seleção, caixas de combinação, caixas de listagem e editar controles. Os valores possíveis são:
    
DT_ACCEPT_DBCS 
  
> O formato ANSI ou DBCS é aceito. Esse sinalizador é válido somente para controles de edição.
    
DT_EDITABLE 
  
> Um usuário pode modificar o texto no controle. 
    
DT_MULTILINE 
  
> O controle pode conter várias linhas de texto. Esse sinalizador é válido somente para controles de edição.
    
DT_PASSWORD_EDIT 
  
> O controle contém uma senha; portanto, o conteúdo do controle não deve ser exibido para o usuário. Esse sinalizador é válido somente para controles de edição.
    
DT_REQUIRED 
  
> O controle da caixa de diálogo é necessário. Esse sinalizador só é válido para controles de caixa de combinação e edição.
    
DT_SET_IMMEDIATE 
  
> Habilita a saída imediata de um valor após uma alteração no controle. Isso permite que uma relação de dependência seja estabelecida entre dois controles. 
    
**lpbNotif**
  
> Ponteiro para uma estrutura que consiste em uma [estrutura GUID,](guid.md) para representar o provedor de serviços e um identificador para o controle. Os **membros lpbNotif** e **cbNotif** correspondem à propriedade **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) do controle e são usados para notificar a interface do usuário quando o controle precisa ser atualizado.
    
**cbNotif**
  
> Contagem de bytes na estrutura apontada pelo membro **lpbNotif.** 
    
**lpszFilter**
  
> Ponteiro para uma cadeia de caracteres que descreve quais caracteres podem ser inseridos em um controle de caixa de combinação ou edição. Para outros tipos de controles, o **membro lpszFilter** pode ser NULL. Para controles de caixa de combinação e edição, ele deve ser uma expressão regular que se aplica a um único caractere de cada vez. O mesmo filtro é aplicado a todos os caracteres no controle. O formato da cadeia de caracteres de filtro é o seguinte: 
    
|**Caractere**|**Descrição**|
|:-----|:-----|
| `*` <br/> | Qualquer caractere é permitido (por exemplo, `"*"` ).  <br/> |
| `[ ]` <br/> |Define um conjunto de caracteres (por exemplo, `"[0123456789]"` .)  <br/> |
| `-` <br/> |Indica um intervalo de caracteres (por exemplo, `"[a-z]"` ).  <br/> |
| `~` <br/> |Indica que esses caracteres não são permitidos (por exemplo, `"[~0-9]")` . <br/>|   
| `\` <br/> |Usado para citação de qualquer um dos símbolos anteriores (por exemplo, os caracteres `"[\-\\\[\]]"` -, \, [e ] são permitidos).  <br/> |
   
**ulItemID**
  
> Valor que identifica o controle no recurso da caixa de diálogo. Para controles de páginas com guias do tipo DTCT_PAGE o membro **ulItemID** é opcionalmente usado para carregar o nome do componente para a página a partir de um recurso de cadeia de caracteres. As informações de posição e rótulo são lidas a partir do recurso da caixa de diálogo. 
    
**ctl**
  
> Uma estrutura que mantém os dados para o controle e corresponde à propriedade **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) do controle. Cada tipo de controle tem uma estrutura diferente.
    
## <a name="remarks"></a>Comentários

A **estrutura DTCTL** descreve um controle de qualquer tipo. A maioria de seus membros é usada para definir propriedades no controle. 
  
O **membro ctl** é uma união de estruturas relacionadas a um tipo específico de controle. Se a **estrutura DTCTL estiver** descrevendo um controle de edição, por exemplo, o membro **ctl** apontará para uma [estrutura DTBLEDIT.](dtbledit.md) Essa estrutura corresponde à propriedade PR_CONTROL_STRUCTURE **controle.** A união tem como primeiro membro uma variável do tipo LPVOID para permitir a inicialização do tempo de compilação da **estrutura DTCTL.** 
  
Embora a [função BuildDisplayTable](builddisplaytable.md) use a estrutura **DTCTL** para criar a tabela de exibição a partir de recursos de controle, a estrutura **DTCTL** nunca aparece na própria tabela de exibição. Essa estrutura fornece apenas informações para **BuildDisplayTable**.
  
No membro **ulCtlFlags,** quatro sinalizadores DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT somente controles de edição. Duas outras DT_REQUIRED e DT_SET_IMMEDIATE afetam qualquer controle editável. 
  
Os controles disponíveis para uma caixa de diálogo são rótulo, caixa de texto, caixa de texto com tinta, lista, lista drop-down, caixa de combinação, caixa de seleção, caixa de seleção, caixa de grupo, botão, botão de rádio e página com guias.
  
Para uma visão geral das tabelas de exibição, consulte [Tabelas de Exibição.](display-tables.md) Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela de exibição.](display-table-implementation.md)
  
## <a name="see-also"></a>Confira também

- [BuildDisplayTable](builddisplaytable.md)
- [DTBLBUTTON](dtblbutton.md)
- [DTBLCHECKBOX](dtblcheckbox.md)
- [DTBLCOMBOBOX](dtblcombobox.md)
- [DTBLDDLBX](dtblddlbx.md)
- [DTBLEDIT](dtbledit.md)
- [DTBLGROUPBOX](dtblgroupbox.md)
- [DTBLLABEL](dtbllabel.md)
- [DTBLLBX](dtbllbx.md)
- [DTBLMVDDLBOX](dtblmvddlbox.md)
- [DTBLMVLISTBOX](dtblmvlistbox.md)
- [DTBLPAGE](dtblpage.md)
- [DTBLRADIOBUTTON](dtblradiobutton.md)
- [Estruturas MAPI](mapi-structures.md)

