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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339407"
---
# <a name="dtctl"></a><span data-ttu-id="1ada6-103">DTCTL</span><span class="sxs-lookup"><span data-stu-id="1ada6-103">DTCTL</span></span>

<span data-ttu-id="1ada6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ada6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ada6-105">Descreve um controle que será usado em uma caixa de diálogo criada a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="1ada6-105">Describes a control that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ada6-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1ada6-106">Header file:</span></span>  <br/> |<span data-ttu-id="1ada6-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1ada6-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="1ada6-108">Members</span><span class="sxs-lookup"><span data-stu-id="1ada6-108">Members</span></span>

<span data-ttu-id="1ada6-109">**ulCtlType**</span><span class="sxs-lookup"><span data-stu-id="1ada6-109">**ulCtlType**</span></span>
  
> <span data-ttu-id="1ada6-110">Tipo de controle incluído no membro **CTL** e corresponde à propriedade **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) do controle.</span><span class="sxs-lookup"><span data-stu-id="1ada6-110">Type of control that is included in the **ctl** member and corresponds to the control's **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property.</span></span> <span data-ttu-id="1ada6-111">Os valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="1ada6-111">Possible values are as follows:</span></span>
    
<span data-ttu-id="1ada6-112">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="1ada6-112">DTCT_LABEL</span></span> 
  
> <span data-ttu-id="1ada6-113">Controle de Rótulo.</span><span class="sxs-lookup"><span data-stu-id="1ada6-113">Label control.</span></span>
    
<span data-ttu-id="1ada6-114">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="1ada6-114">DTCT_EDIT</span></span> 
  
> <span data-ttu-id="1ada6-115">Controle de edição.</span><span class="sxs-lookup"><span data-stu-id="1ada6-115">Edit control.</span></span>
    
<span data-ttu-id="1ada6-116">DTCT_LBX</span><span class="sxs-lookup"><span data-stu-id="1ada6-116">DTCT_LBX</span></span> 
  
> <span data-ttu-id="1ada6-117">Controle caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="1ada6-117">List box control.</span></span>
    
<span data-ttu-id="1ada6-118">DTCT_COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="1ada6-118">DTCT_COMBOBOX</span></span> 
  
> <span data-ttu-id="1ada6-119">Controle de caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="1ada6-119">Combo box control.</span></span>
    
<span data-ttu-id="1ada6-120">DTCT_DDLBX</span><span class="sxs-lookup"><span data-stu-id="1ada6-120">DTCT_DDLBX</span></span> 
  
> <span data-ttu-id="1ada6-121">Controle de lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="1ada6-121">Drop-down list control.</span></span>
    
<span data-ttu-id="1ada6-122">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="1ada6-122">DTCT_CHECKBOX</span></span> 
  
> <span data-ttu-id="1ada6-123">Controle caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="1ada6-123">Check box control.</span></span>
    
<span data-ttu-id="1ada6-124">DTCT_GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="1ada6-124">DTCT_GROUPBOX</span></span> 
  
> <span data-ttu-id="1ada6-125">Controle de caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="1ada6-125">Group box control.</span></span>
    
<span data-ttu-id="1ada6-126">DTCT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="1ada6-126">DTCT_BUTTON</span></span> 
  
> <span data-ttu-id="1ada6-127">Controle de botão.</span><span class="sxs-lookup"><span data-stu-id="1ada6-127">Button control.</span></span>
    
<span data-ttu-id="1ada6-128">DTCT_PAGE</span><span class="sxs-lookup"><span data-stu-id="1ada6-128">DTCT_PAGE</span></span> 
  
> <span data-ttu-id="1ada6-129">Controle de página com guias.</span><span class="sxs-lookup"><span data-stu-id="1ada6-129">Tabbed page control.</span></span>
    
<span data-ttu-id="1ada6-130">DTCT_RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="1ada6-130">DTCT_RADIOBUTTON</span></span> 
  
> <span data-ttu-id="1ada6-131">Controle de botão de opção.</span><span class="sxs-lookup"><span data-stu-id="1ada6-131">Radio button control.</span></span>
    
<span data-ttu-id="1ada6-132">DTCT_MVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="1ada6-132">DTCT_MVLISTBOX</span></span> 
  
> <span data-ttu-id="1ada6-133">Controle de lista de vários valores.</span><span class="sxs-lookup"><span data-stu-id="1ada6-133">Multi-valued list control.</span></span>
    
<span data-ttu-id="1ada6-134">DTCT_MVDDLBX</span><span class="sxs-lookup"><span data-stu-id="1ada6-134">DTCT_MVDDLBX</span></span> 
  
> <span data-ttu-id="1ada6-135">Controle de lista suspensa de vários valores.</span><span class="sxs-lookup"><span data-stu-id="1ada6-135">Multi-valued drop-down list control.</span></span>
    
<span data-ttu-id="1ada6-136">**ulCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="1ada6-136">**ulCtlFlags**</span></span>
  
> <span data-ttu-id="1ada6-137">Bitmask de sinalizadores que descreve os recursos do controle e corresponde à propriedade **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) do controle.</span><span class="sxs-lookup"><span data-stu-id="1ada6-137">Bitmask of flags that describes the control's features and corresponds to the control's **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="1ada6-138">Esses sinalizadores podem ser definidos para caixas de seleção, caixas de combinação, caixas de listagem e controles de edição.</span><span class="sxs-lookup"><span data-stu-id="1ada6-138">These flags can be set for check boxes, combo boxes, list boxes, and edit controls only.</span></span> <span data-ttu-id="1ada6-139">Os valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="1ada6-139">Possible values are as follows:</span></span>
    
<span data-ttu-id="1ada6-140">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="1ada6-140">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="1ada6-141">O formato ANSI ou DBCS é aceito.</span><span class="sxs-lookup"><span data-stu-id="1ada6-141">Either the ANSI or DBCS format is accepted.</span></span> <span data-ttu-id="1ada6-142">Este sinalizador é válido apenas para controles de edição.</span><span class="sxs-lookup"><span data-stu-id="1ada6-142">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="1ada6-143">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="1ada6-143">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="1ada6-144">Um usuário pode modificar o texto no controle.</span><span class="sxs-lookup"><span data-stu-id="1ada6-144">A user can modify the text in the control.</span></span> 
    
<span data-ttu-id="1ada6-145">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="1ada6-145">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="1ada6-146">O controle pode conter várias linhas de texto.</span><span class="sxs-lookup"><span data-stu-id="1ada6-146">The control can contain multiple text lines.</span></span> <span data-ttu-id="1ada6-147">Este sinalizador é válido apenas para controles de edição.</span><span class="sxs-lookup"><span data-stu-id="1ada6-147">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="1ada6-148">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="1ada6-148">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="1ada6-149">O controle contém uma senha; Portanto, o conteúdo do controle não deve ser exibido para o usuário.</span><span class="sxs-lookup"><span data-stu-id="1ada6-149">The control contains a password; therefore, the contents of the control should not be displayed to the user.</span></span> <span data-ttu-id="1ada6-150">Este sinalizador é válido apenas para controles de edição.</span><span class="sxs-lookup"><span data-stu-id="1ada6-150">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="1ada6-151">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="1ada6-151">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="1ada6-152">O controle da caixa de diálogo é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1ada6-152">The dialog box control is required.</span></span> <span data-ttu-id="1ada6-153">Este sinalizador é válido somente para controles de caixa de edição e de combinação.</span><span class="sxs-lookup"><span data-stu-id="1ada6-153">This flag is valid only for edit and combo box controls.</span></span>
    
<span data-ttu-id="1ada6-154">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="1ada6-154">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="1ada6-155">Permite a saída imediata de um valor após uma alteração no controle.</span><span class="sxs-lookup"><span data-stu-id="1ada6-155">Enables immediate output of a value upon a change in the control.</span></span> <span data-ttu-id="1ada6-156">Isso permite que uma relação de dependência seja estabelecida entre dois controles.</span><span class="sxs-lookup"><span data-stu-id="1ada6-156">This allows a dependency relationship to be established between two controls.</span></span> 
    
<span data-ttu-id="1ada6-157">**lpbNotif**</span><span class="sxs-lookup"><span data-stu-id="1ada6-157">**lpbNotif**</span></span>
  
> <span data-ttu-id="1ada6-158">Ponteiro para uma estrutura que consiste em uma estrutura [GUID](guid.md) , para representar o provedor de serviço e um identificador para o controle.</span><span class="sxs-lookup"><span data-stu-id="1ada6-158">Pointer to a structure that consists of a [GUID](guid.md) structure, to represent the service provider and an identifier for the control.</span></span> <span data-ttu-id="1ada6-159">Os membros **lpbNotif** e **cbNotif** correspondem à propriedade do **PR_CONTROL_ID** do controle ([PidTagControlId](pidtagcontrolid-canonical-property.md)) e são usados para notificar a interface do usuário quando o controle precisa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="1ada6-159">The **lpbNotif** and **cbNotif** members correspond to the control's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property and are used to notify the user interface when the control has to be updated.</span></span>
    
<span data-ttu-id="1ada6-160">**cbNotif**</span><span class="sxs-lookup"><span data-stu-id="1ada6-160">**cbNotif**</span></span>
  
> <span data-ttu-id="1ada6-161">Contagem de bytes na estrutura apontada pelo membro **lpbNotif** .</span><span class="sxs-lookup"><span data-stu-id="1ada6-161">Count of bytes in the structure pointed to by the **lpbNotif** member.</span></span> 
    
<span data-ttu-id="1ada6-162">**lpszFilter**</span><span class="sxs-lookup"><span data-stu-id="1ada6-162">**lpszFilter**</span></span>
  
> <span data-ttu-id="1ada6-163">Ponteiro para uma cadeia de caracteres que descreve quais caracteres podem ser inseridos em um controle de caixa de combinação ou edição.</span><span class="sxs-lookup"><span data-stu-id="1ada6-163">Pointer to a character string that describes which characters can be entered into an edit or combo box control.</span></span> <span data-ttu-id="1ada6-164">Para outros tipos de controles, o membro **lpszFilter** pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="1ada6-164">For other types of controls, the **lpszFilter** member can be NULL.</span></span> <span data-ttu-id="1ada6-165">Para controles de caixa de edição e de combinação, deve ser uma expressão regular que se aplica a um único caractere por vez.</span><span class="sxs-lookup"><span data-stu-id="1ada6-165">For edit and combo box controls, it should be a regular expression that applies to a single character at a time.</span></span> <span data-ttu-id="1ada6-166">O mesmo filtro é aplicado a todos os caracteres no controle.</span><span class="sxs-lookup"><span data-stu-id="1ada6-166">The same filter is applied to all characters in the control.</span></span> <span data-ttu-id="1ada6-167">O formato da cadeia de caracteres de filtro é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1ada6-167">The format of the filter string is as follows:</span></span> 
    
|<span data-ttu-id="1ada6-168">**Caractere**</span><span class="sxs-lookup"><span data-stu-id="1ada6-168">**Character**</span></span>|<span data-ttu-id="1ada6-169">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1ada6-169">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> | <span data-ttu-id="1ada6-170">Qualquer caractere é permitido (por exemplo, `"*"`).</span><span class="sxs-lookup"><span data-stu-id="1ada6-170">Any character is allowed (for example, `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="1ada6-171">Define um conjunto de caracteres (por exemplo, `"[0123456789]"`.)</span><span class="sxs-lookup"><span data-stu-id="1ada6-171">Defines a set of characters (for example, `"[0123456789]"`.)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="1ada6-172">Indica um intervalo de caracteres (por exemplo, `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="1ada6-172">Indicates a range of characters (for example, `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="1ada6-173">Indica que esses caracteres não são permitidos (por exemplo, `"[~0-9]")`.</span><span class="sxs-lookup"><span data-stu-id="1ada6-173">Indicates that these characters are not allowed (for example, `"[~0-9]")`.</span></span> <br/>|   
| `\` <br/> |<span data-ttu-id="1ada6-174">Usado para citar qualquer um dos símbolos anteriores (por exemplo, `"[\-\\\[\]]"` os caracteres significa \, -, [e] são permitidos).</span><span class="sxs-lookup"><span data-stu-id="1ada6-174">Used to quote any of the previous symbols (for example, `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
<span data-ttu-id="1ada6-175">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="1ada6-175">**ulItemID**</span></span>
  
> <span data-ttu-id="1ada6-176">O valor que identifica o controle no recurso da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1ada6-176">Value that identifies the control in the dialog box resource.</span></span> <span data-ttu-id="1ada6-177">Para controles de páginas com guias do tipo DTCT_PAGE o membro **ulItemID** é opcionalmente usado para carregar o nome do componente da página de um recurso de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1ada6-177">For tabbed pages controls of type DTCT_PAGE the **ulItemID** member is optionally used to load the component name for the page from a string resource.</span></span> <span data-ttu-id="1ada6-178">As informações de posição e rótulo são lidas no recurso caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1ada6-178">Position and label information are read from the dialog box resource.</span></span> 
    
<span data-ttu-id="1ada6-179">**CTL**</span><span class="sxs-lookup"><span data-stu-id="1ada6-179">**ctl**</span></span>
  
> <span data-ttu-id="1ada6-180">Uma estrutura que armazena os dados do controle e corresponde à propriedade **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) do controle.</span><span class="sxs-lookup"><span data-stu-id="1ada6-180">A structure that holds the data for the control and corresponds to the control's **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) property.</span></span> <span data-ttu-id="1ada6-181">Cada tipo de controle tem uma estrutura diferente.</span><span class="sxs-lookup"><span data-stu-id="1ada6-181">Each type of control has a different structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ada6-182">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ada6-182">Remarks</span></span>

<span data-ttu-id="1ada6-183">A estrutura **DTCTL** descreve um controle de qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="1ada6-183">The **DTCTL** structure describes one control of any type.</span></span> <span data-ttu-id="1ada6-184">A maioria dos seus membros é usada para definir propriedades no controle.</span><span class="sxs-lookup"><span data-stu-id="1ada6-184">Most of its members are used to set properties on the control.</span></span> 
  
<span data-ttu-id="1ada6-185">O membro **CTL** é uma União de estruturas que se relacionam a um tipo específico de controle.</span><span class="sxs-lookup"><span data-stu-id="1ada6-185">The **ctl** member is a union of structures that relate to a particular type of control.</span></span> <span data-ttu-id="1ada6-186">Se a estrutura **DTCTL** estiver descrevendo um controle de edição, por exemplo, o membro **CTL** apontará para uma estrutura [DTBLEDIT](dtbledit.md) .</span><span class="sxs-lookup"><span data-stu-id="1ada6-186">If the **DTCTL** structure is describing an edit control, for example, the **ctl** member will point to a [DTBLEDIT](dtbledit.md) structure.</span></span> <span data-ttu-id="1ada6-187">Essa estrutura corresponde à propriedade **PR_CONTROL_STRUCTURE** do controle.</span><span class="sxs-lookup"><span data-stu-id="1ada6-187">This structure corresponds to the control's **PR_CONTROL_STRUCTURE** property.</span></span> <span data-ttu-id="1ada6-188">A União tem como seu primeiro membro uma variável do tipo LPVOID para permitir a inicialização de tempo de compilação da estrutura **DTCTL** .</span><span class="sxs-lookup"><span data-stu-id="1ada6-188">The union has as its first member a variable of type LPVOID to allow compile time initialization of the **DTCTL** structure.</span></span> 
  
<span data-ttu-id="1ada6-189">Embora a função [BuildDisplayTable](builddisplaytable.md) use a estrutura **DTCTL** para criar a tabela de exibição a partir de recursos de controle, a estrutura **DTCTL** nunca aparece na própria tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="1ada6-189">Although the [BuildDisplayTable](builddisplaytable.md) function uses the **DTCTL** structure for building the display table from control resources, the **DTCTL** structure never appears in the display table itself.</span></span> <span data-ttu-id="1ada6-190">Essa estrutura apenas fornece informações para o **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="1ada6-190">This structure just supplies information to **BuildDisplayTable**.</span></span>
  
<span data-ttu-id="1ada6-191">No membro **ulCtlFlags** , quatro sinalizadores DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT afetam somente os controles de edição.</span><span class="sxs-lookup"><span data-stu-id="1ada6-191">In the **ulCtlFlags** member, four flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affect edit controls only.</span></span> <span data-ttu-id="1ada6-192">Dois outros DT_REQUIRED e DT_SET_IMMEDIATE afetam qualquer controle editável.</span><span class="sxs-lookup"><span data-stu-id="1ada6-192">Two others DT_REQUIRED and DT_SET_IMMEDIATE affect any editable control.</span></span> 
  
<span data-ttu-id="1ada6-193">Os controles disponíveis para uma caixa de diálogo são rótulo, caixa de texto, caixa de texto sensível à tinta, lista, lista suspensa, caixa de combinação, caixa de seleção, caixa de grupo, botão, botão de opção e página com tabulação.</span><span class="sxs-lookup"><span data-stu-id="1ada6-193">The controls available for a dialog box are label, text box, ink-aware text box, list, drop-down list, combo box, check box, group box, button, radio button, and tabbed page.</span></span>
  
<span data-ttu-id="1ada6-194">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1ada6-194">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="1ada6-195">Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="1ada6-195">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1ada6-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ada6-196">See also</span></span>

- [<span data-ttu-id="1ada6-197">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="1ada6-197">BuildDisplayTable</span></span>](builddisplaytable.md)
- [<span data-ttu-id="1ada6-198">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="1ada6-198">DTBLBUTTON</span></span>](dtblbutton.md)
- [<span data-ttu-id="1ada6-199">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="1ada6-199">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="1ada6-200">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="1ada6-200">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="1ada6-201">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="1ada6-201">DTBLDDLBX</span></span>](dtblddlbx.md)
- [<span data-ttu-id="1ada6-202">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="1ada6-202">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="1ada6-203">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="1ada6-203">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="1ada6-204">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="1ada6-204">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="1ada6-205">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="1ada6-205">DTBLLBX</span></span>](dtbllbx.md)
- [<span data-ttu-id="1ada6-206">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="1ada6-206">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md)
- [<span data-ttu-id="1ada6-207">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="1ada6-207">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md)
- [<span data-ttu-id="1ada6-208">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="1ada6-208">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="1ada6-209">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="1ada6-209">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md)
- [<span data-ttu-id="1ada6-210">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="1ada6-210">MAPI Structures</span></span>](mapi-structures.md)

