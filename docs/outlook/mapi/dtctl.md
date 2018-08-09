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
ms.openlocfilehash: 68c621f5f73073ed127767cc1db189769dab227d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766504"
---
# <a name="dtctl"></a>DTCTL

**Aplica-se a**: Outlook 
  
Descreve um controle que será usado em uma caixa de diálogo construída a partir de uma tabela de exibição. 
  
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
  
> Tipo de controle que está incluído no membro **ctl** e corresponde à propriedade de **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) do controle. Os valores possíveis são:
    
DTCT_LABEL 
  
> Controle de Rótulo.
    
DTCT_EDIT 
  
> Controle de edição.
    
DTCT_LBX 
  
> Controle de caixa de listagem.
    
DTCT_COMBOBOX 
  
> Controle de caixa de combinação.
    
DTCT_DDLBX 
  
> Controle de lista suspensa.
    
DTCT_CHECKBOX 
  
> Controle de caixa de seleção.
    
DTCT_GROUPBOX 
  
> Controle de caixa de grupo.
    
DTCT_BUTTON 
  
> Controle de botão.
    
DTCT_PAGE 
  
> Controle de páginas com guias.
    
DTCT_RADIOBUTTON 
  
> Controle de botão de opção.
    
DTCT_MVLISTBOX 
  
> Controle de lista de valores múltiplos.
    
DTCT_MVDDLBX 
  
> Controle de lista de lista suspensa de valores múltiplos.
    
**ulCtlFlags**
  
> Bitmask dos sinalizadores que descreve os recursos do controle e corresponde à propriedade de **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) do controle. Esses sinalizadores podem ser definidas para caixas de seleção, caixas de combinação, caixas de listagem e apenas controles de edição. Os valores possíveis são:
    
DT_ACCEPT_DBCS 
  
> O ANSI DBCS formato ou será aceito. Esse sinalizador é válida para apenas controles de edição.
    
DT_EDITABLE 
  
> Um usuário pode modificar o texto no controle. 
    
DT_MULTILINE 
  
> O controle pode conter várias linhas de texto. Esse sinalizador é válida para apenas controles de edição.
    
DT_PASSWORD_EDIT 
  
> O controle contém uma senha; Portanto, o conteúdo do controle não deve ser exibido para o usuário. Esse sinalizador é válida para apenas controles de edição.
    
DT_REQUIRED 
  
> O controle de caixa de diálogo é necessário. Esse sinalizador é válida apenas para os controles de caixa de combinação e de editar.
    
DT_SET_IMMEDIATE 
  
> Permite a saída imediata de um valor após uma alteração no controle. Isso permite que uma relação de dependência a ser estabelecida entre dois controles. 
    
**lpbNotif**
  
> Ponteiro para uma estrutura que consiste em uma estrutura [GUID](guid.md) , para representar o provedor de serviço e um identificador para o controle. Os membros **lpbNotif** e **cbNotif** correspondem à propriedade de **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) do controle e são usados para notificar a interface do usuário quando o controle tem a ser atualizado.
    
**cbNotif**
  
> Contagem de bytes na estrutura apontado pelo membro **lpbNotif** . 
    
**lpszFilter**
  
> Ponteiro para uma cadeia de caracteres que descreve quais caracteres podem ser inseridos em um controle de caixa de combinação ou editar. Para outros tipos de controles, o membro **lpszFilter** pode ser NULL. Para controles de caixa de combinação e de editar, ele deve ser uma expressão regular que se aplica a um único caractere por vez. O mesmo filtro é aplicado a todos os caracteres no controle. O formato da cadeia de caracteres de filtro é da seguinte maneira: 
    
|**Caractere**|**Descrição**|
|:-----|:-----|
| `*` <br/> | Qualquer caractere é permitido (por exemplo, `"*"`).  <br/> |
| `[ ]` <br/> |Define um conjunto de caracteres (por exemplo, `"[0123456789]"`.)  <br/> |
| `-` <br/> |Indica um intervalo de caracteres (por exemplo, `"[a-z]"`).  <br/> |
| `~` <br/> |Indica que esses caracteres não são permitidos (por exemplo, `"[~0-9]")`. <br/>|   
| `\` <br/> |Usado para quote qualquer um dos símbolos anteriores (por exemplo, `"[\-\\\[\]]"` significa-, \, [, e] caracteres são permitidos).  <br/> |
   
**ulItemID**
  
> Valor que identifica o controle do recurso de caixa de diálogo. Para controles de páginas com guias do tipo DTCT_PAGE o **ulItemID** membro opcionalmente é usado para carregar o nome do componente para a página de um recurso de cadeia de caracteres. Posição e informações sobre as etiquetas serão lidas a partir do recurso de caixa de diálogo. 
    
**CTL**
  
> Uma estrutura que contém os dados para o controle e corresponde à propriedade de **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) do controle. Cada tipo de controle tem uma estrutura diferente.
    
## <a name="remarks"></a>Comentários

A estrutura **DTCTL** descreve um controle de qualquer tipo. A maioria dos seus membros é usada para definir as propriedades do controle. 
  
O membro de **ctl** é uma união de estruturas que se relacionam com um determinado tipo de controle. Se a estrutura **DTCTL** é descrevendo um controle de edição, por exemplo, o membro **ctl** irá apontar para uma estrutura [DTBLEDIT](dtbledit.md) . Essa estrutura corresponde à propriedade **PR_CONTROL_STRUCTURE** do controle. A união tem como seu primeiro membro em uma variável do tipo LPVOID para permitir a inicialização do tempo de compilação da estrutura **DTCTL** . 
  
Embora a função de [BuildDisplayTable](builddisplaytable.md) usa a estrutura **DTCTL** para construir a tabela de exibição de recursos de controle, a estrutura **DTCTL** nunca será exibida na tabela a exibição em si. Essa estrutura apenas fornece informações para **BuildDisplayTable**.
  
No membro **ulCtlFlags** , quatro sinalizadores DT_ACCEPT_DBCS, DT_EDITABLE, afetam DT_MULTILINE_and DT_PASSWORD_EDIT somente controles de edição. Duas outras pessoas DT_REQUIRED e DT_SET_IMMEDIATE afetam qualquer controle editável. 
  
Os controles disponíveis para uma caixa de diálogo são rótulo, caixa de texto, caixa de texto de reconhecimento de tinta, lista, lista suspensa, caixa de combinação, caixa de seleção, caixa de grupo, botão, botão de opção e página com guias.
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).
  
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

