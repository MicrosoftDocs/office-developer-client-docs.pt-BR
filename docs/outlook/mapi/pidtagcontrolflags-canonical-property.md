---
title: Propriedade canônica PidTagControlFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f6947efe1aa6866efb7a5a3d96262d021c68013f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769130"
---
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="00616-103">Propriedade canônica PidTagControlFlags</span><span class="sxs-lookup"><span data-stu-id="00616-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="00616-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00616-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00616-105">Contém uma bitmask dos sinalizadores que controlam o comportamento de um controle usado em uma caixa de diálogo construída a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="00616-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00616-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="00616-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00616-107">PR_CONTROL_FLAGS</span><span class="sxs-lookup"><span data-stu-id="00616-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="00616-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="00616-108">Identifier:</span></span>  <br/> |<span data-ttu-id="00616-109">0x3F00</span><span class="sxs-lookup"><span data-stu-id="00616-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="00616-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="00616-110">Data type:</span></span>  <br/> |<span data-ttu-id="00616-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="00616-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="00616-112">Área:</span><span class="sxs-lookup"><span data-stu-id="00616-112">Area:</span></span>  <br/> |<span data-ttu-id="00616-113">Tabela de exibição MAPI</span><span class="sxs-lookup"><span data-stu-id="00616-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00616-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="00616-114">Remarks</span></span>

<span data-ttu-id="00616-115">Um ou mais dos seguintes sinalizadores podem ser definido para essa propriedade:</span><span class="sxs-lookup"><span data-stu-id="00616-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="00616-116">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="00616-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="00616-117">O controle pode ter caracteres do conjunto de caracteres de Byte duplo (DBCS) nela.</span><span class="sxs-lookup"><span data-stu-id="00616-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="00616-118">Esse sinalizador é usado com controles de edição.</span><span class="sxs-lookup"><span data-stu-id="00616-118">This flag is used with edit controls.</span></span> <span data-ttu-id="00616-119">Ele permite que os conjuntos de caracteres de vários bytes.</span><span class="sxs-lookup"><span data-stu-id="00616-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="00616-120">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="00616-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="00616-121">O controle pode ser editado; o valor associado ao controle pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="00616-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="00616-122">Quando esse sinalizador não estiver definida, o controle é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="00616-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="00616-123">Este valor será ignorado no rótulo, caixa de grupo, botão de ação padrão, suspenso multivalorado de caixa de listagem e controles de caixa de lista.</span><span class="sxs-lookup"><span data-stu-id="00616-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="00616-124">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="00616-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="00616-125">O controle de edição pode conter várias linhas.</span><span class="sxs-lookup"><span data-stu-id="00616-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="00616-126">Isso significa que um caractere de retorno pode ser digitado dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="00616-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="00616-127">Esse sinalizador é válida para apenas controles de edição.</span><span class="sxs-lookup"><span data-stu-id="00616-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="00616-128">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="00616-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="00616-129">Aplica-se para editar os controles.</span><span class="sxs-lookup"><span data-stu-id="00616-129">Applies to edit controls.</span></span> <span data-ttu-id="00616-130">O controle de edição é tratado como uma senha.</span><span class="sxs-lookup"><span data-stu-id="00616-130">The edit control is treated like a password.</span></span> <span data-ttu-id="00616-131">O valor é exibido usando asteriscos em vez de ecos os caracteres reais inseridos.</span><span class="sxs-lookup"><span data-stu-id="00616-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="00616-132">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="00616-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="00616-133">Se o controle permitir alterações (DT_EDITABLE), ele deve ter um valor antes de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="00616-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="00616-134">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="00616-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="00616-135">Permite a configuração imediata de um valor; Assim que um valor no controle é alterado, MAPI chama o método **SetProps** para a propriedade associada a esse controle.</span><span class="sxs-lookup"><span data-stu-id="00616-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="00616-136">Quando esse sinalizador não estiver definida, os valores são definidos quando a caixa de diálogo é descartada.</span><span class="sxs-lookup"><span data-stu-id="00616-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="00616-137">DT_SET_SELECTION</span><span class="sxs-lookup"><span data-stu-id="00616-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="00616-138">Quando uma seleção é feita na caixa de lista, a coluna de índice da caixa de listagem é definida como uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="00616-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="00616-139">Sempre é usado com DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="00616-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="00616-140">Essa propriedade é armazenada no membro ulCtlFlags da estrutura [DTCTL](dtctl.md) de um controle.</span><span class="sxs-lookup"><span data-stu-id="00616-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="00616-141">A maioria dos sinalizadores controle se aplicam a todos os controles que permitem a entrada do usuário; Alguns se aplicam apenas ao controle de edição.</span><span class="sxs-lookup"><span data-stu-id="00616-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="00616-142">Controles que não permitem a entrada de usuário, um botão ou um rótulo, defina 0 para seus sinalizadores de controle.</span><span class="sxs-lookup"><span data-stu-id="00616-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="00616-143">Muitos dos valores sinalizador são auto-explicativos.</span><span class="sxs-lookup"><span data-stu-id="00616-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="00616-144">Por exemplo, quando DT_REQUIRED é definida para um controle, ele deve conter um valor antes que a caixa de diálogo tem permissão para ser descartado.</span><span class="sxs-lookup"><span data-stu-id="00616-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="00616-145">O provedor de serviços pode fornecer um valor pela sua implementação **IMAPIProp** ou o usuário pode digitar um.</span><span class="sxs-lookup"><span data-stu-id="00616-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="00616-146">DT_EDITABLE indica que o valor do controle pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="00616-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="00616-147">DT_MULTILINE permite que o valor de um controle de edição abranger várias linhas.</span><span class="sxs-lookup"><span data-stu-id="00616-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="00616-148">Alguns sinalizadores de controle não são tão óbvias no seu significado.</span><span class="sxs-lookup"><span data-stu-id="00616-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="00616-149">Quando um controle define o sinalizador DT_SET_IMMEDIATE, todas as alterações feitas take seu valor afetam assim que o usuário move para um novo controle.</span><span class="sxs-lookup"><span data-stu-id="00616-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="00616-150">MAPI torna uma única chamada de método de [IMAPIProp::SetProps](imapiprop-setprops.md) da interface de propriedade para a propriedade do controle.</span><span class="sxs-lookup"><span data-stu-id="00616-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="00616-151">Isso é diferente do comportamento padrão, que é para adiar tendo alterações nos valores de controle entrarão em vigor depois que o usuário seleciona o botão **Okey** ou descarte a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="00616-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="00616-152">O sinalizador DT_SET_IMMEDIATE é frequentemente usado em combinação com notificações de tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="00616-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="00616-153">A tabela a seguir lista os tipos de controles e todos os valores de sinalizador que podem ser definidos para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="00616-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="00616-154">**Control**</span><span class="sxs-lookup"><span data-stu-id="00616-154">**Control**</span></span>|<span data-ttu-id="00616-155">**Valores válidos para esta propriedade**</span><span class="sxs-lookup"><span data-stu-id="00616-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00616-156">Botão</span><span class="sxs-lookup"><span data-stu-id="00616-156">Button</span></span>  <br/> |<span data-ttu-id="00616-157">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="00616-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="00616-158">Caixa de seleção</span><span class="sxs-lookup"><span data-stu-id="00616-158">Check box</span></span>  <br/> |<span data-ttu-id="00616-159">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="00616-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="00616-160">Caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="00616-160">Combo box</span></span>  <br/> |<span data-ttu-id="00616-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="00616-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="00616-162">Caixa de listagem drop-down</span><span class="sxs-lookup"><span data-stu-id="00616-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="00616-163">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="00616-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="00616-164">EDIT</span><span class="sxs-lookup"><span data-stu-id="00616-164">Edit</span></span>  <br/> |<span data-ttu-id="00616-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="00616-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="00616-166">Caixa de grupo</span><span class="sxs-lookup"><span data-stu-id="00616-166">Group box</span></span>  <br/> |<span data-ttu-id="00616-167">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="00616-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="00616-168">Rótulo</span><span class="sxs-lookup"><span data-stu-id="00616-168">Label</span></span>  <br/> |<span data-ttu-id="00616-169">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="00616-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="00616-170">Caixa de listagem</span><span class="sxs-lookup"><span data-stu-id="00616-170">List box</span></span>  <br/> |<span data-ttu-id="00616-171">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="00616-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="00616-172">Caixa de listagem de lista suspensa de vários valores</span><span class="sxs-lookup"><span data-stu-id="00616-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="00616-173">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="00616-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="00616-174">Caixa de listagem de vários valores</span><span class="sxs-lookup"><span data-stu-id="00616-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="00616-175">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="00616-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="00616-176">Página com guias</span><span class="sxs-lookup"><span data-stu-id="00616-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="00616-177">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="00616-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="00616-178">Botão de opção</span><span class="sxs-lookup"><span data-stu-id="00616-178">Radio button</span></span>  <br/> |<span data-ttu-id="00616-179">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="00616-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="00616-180">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="00616-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="00616-181">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="00616-181">Header files</span></span>

<span data-ttu-id="00616-182">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00616-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="00616-183">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="00616-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="00616-184">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="00616-184">Mapitags.h</span></span>
  
> <span data-ttu-id="00616-185">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="00616-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00616-186">Confira também</span><span class="sxs-lookup"><span data-stu-id="00616-186">See also</span></span>



[<span data-ttu-id="00616-187">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="00616-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00616-188">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="00616-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00616-189">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="00616-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00616-190">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="00616-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
