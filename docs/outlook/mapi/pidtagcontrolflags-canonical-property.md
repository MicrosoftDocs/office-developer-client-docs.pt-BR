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
ms.openlocfilehash: 099f08876eadc83ebb66b9e4226eeeee6277bf01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430879"
---
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="31885-103">Propriedade canônica PidTagControlFlags</span><span class="sxs-lookup"><span data-stu-id="31885-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="31885-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31885-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31885-105">Contém uma bitmask de sinalizadores que regem o comportamento de um controle usado em uma caixa de diálogo criada a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="31885-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="31885-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="31885-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="31885-107">PR_CONTROL_FLAGS</span><span class="sxs-lookup"><span data-stu-id="31885-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="31885-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="31885-108">Identifier:</span></span>  <br/> |<span data-ttu-id="31885-109">0x3F00</span><span class="sxs-lookup"><span data-stu-id="31885-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="31885-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="31885-110">Data type:</span></span>  <br/> |<span data-ttu-id="31885-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="31885-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="31885-112">Área:</span><span class="sxs-lookup"><span data-stu-id="31885-112">Area:</span></span>  <br/> |<span data-ttu-id="31885-113">Tabela de exibição MAPI</span><span class="sxs-lookup"><span data-stu-id="31885-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31885-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="31885-114">Remarks</span></span>

<span data-ttu-id="31885-115">Um ou mais dos seguintes sinalizadores podem ser definidos para esta propriedade:</span><span class="sxs-lookup"><span data-stu-id="31885-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="31885-116">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="31885-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="31885-117">O controle pode ter caracteres de conjunto de caracteres de byte duplo (DBCS).</span><span class="sxs-lookup"><span data-stu-id="31885-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="31885-118">Este sinalizador é usado com controles de edição.</span><span class="sxs-lookup"><span data-stu-id="31885-118">This flag is used with edit controls.</span></span> <span data-ttu-id="31885-119">Ele permite conjuntos de caracteres de vários bytes.</span><span class="sxs-lookup"><span data-stu-id="31885-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="31885-120">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="31885-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="31885-121">O controle pode ser editado; o valor associado ao controle pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="31885-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="31885-122">Quando esse sinalizador não é definido, o controle é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="31885-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="31885-123">Esse valor é ignorado em rótulo, caixa de grupo, botão de ação padrão, caixa de listagem suspensa de vários valores e controles de caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="31885-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="31885-124">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="31885-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="31885-125">O controle de edição pode conter várias linhas.</span><span class="sxs-lookup"><span data-stu-id="31885-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="31885-126">Isso significa que um caractere de retorno pode ser inserido dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="31885-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="31885-127">Este sinalizador é válido apenas para controles de edição.</span><span class="sxs-lookup"><span data-stu-id="31885-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="31885-128">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="31885-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="31885-129">Aplica-se a controles de edição.</span><span class="sxs-lookup"><span data-stu-id="31885-129">Applies to edit controls.</span></span> <span data-ttu-id="31885-130">O controle de edição é tratado como uma senha.</span><span class="sxs-lookup"><span data-stu-id="31885-130">The edit control is treated like a password.</span></span> <span data-ttu-id="31885-131">O valor é exibido usando asteriscos em vez de ecoar os caracteres reais inseridos.</span><span class="sxs-lookup"><span data-stu-id="31885-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="31885-132">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="31885-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="31885-133">Se o controle permitir alterações (DT_EDITABLE), ele deverá ter um valor antes que [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="31885-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="31885-134">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="31885-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="31885-135">Habilita a configuração imediata de um valor; assim que um valor no controle é alterado, o MAPI chama o \*\*\*\* método SetProps para a propriedade associada a esse controle.</span><span class="sxs-lookup"><span data-stu-id="31885-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="31885-136">Quando esse sinalizador não é definido, os valores são definidos quando a caixa de diálogo é descartada.</span><span class="sxs-lookup"><span data-stu-id="31885-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="31885-137">DT_SET_SELECTION</span><span class="sxs-lookup"><span data-stu-id="31885-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="31885-138">Quando uma seleção é feita dentro da caixa de listagem, a coluna de índice dessa caixa de listagem é definida como uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="31885-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="31885-139">Sempre usado com DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="31885-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="31885-140">Essa propriedade é armazenada no membro ulCtlFlags da estrutura [DTCTL](dtctl.md) de um controle.</span><span class="sxs-lookup"><span data-stu-id="31885-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="31885-141">A maioria dos sinalizadores de controle se aplicam a todos os controles que permitem a entrada do usuário; algumas aplicam-se apenas ao controle de edição.</span><span class="sxs-lookup"><span data-stu-id="31885-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="31885-142">Controles que não permitem a entrada do usuário, como um botão ou um rótulo, definem 0 para seus sinalizadores de controle.</span><span class="sxs-lookup"><span data-stu-id="31885-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="31885-143">Muitos dos valores de sinalizador são auto-explicativos.</span><span class="sxs-lookup"><span data-stu-id="31885-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="31885-144">Por exemplo, quando DT_REQUIRED é definido para um controle, ele deve conter um valor antes que a caixa de diálogo tenha permissão para ser descartada.</span><span class="sxs-lookup"><span data-stu-id="31885-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="31885-145">O provedor de serviços pode fornecer um valor através de sua implementação de **IMAPIProp** ou o usuário pode inserir um.</span><span class="sxs-lookup"><span data-stu-id="31885-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="31885-146">DT_EDITABLE indica que o valor do controle pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="31885-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="31885-147">DT_MULTILINE permite que o valor de um controle de edição estenda várias linhas.</span><span class="sxs-lookup"><span data-stu-id="31885-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="31885-148">Alguns sinalizadores de controle não são tão óbvios no significado.</span><span class="sxs-lookup"><span data-stu-id="31885-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="31885-149">Quando um controle define o sinalizador DT_SET_IMMEDIATE, todas as alterações feitas em seu valor são afetadas assim que o usuário move para um novo controle.</span><span class="sxs-lookup"><span data-stu-id="31885-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="31885-150">MAPI faz uma única chamada para o método [IMAPIProp::](imapiprop-setprops.md) SetProps da interface de propriedade para a propriedade do controle.</span><span class="sxs-lookup"><span data-stu-id="31885-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="31885-151">Isso é diferente do comportamento padrão, que é adiar a necessidade de alterações nos valores de controle até que o usuário selecione o botão **OK** ou disperca a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="31885-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="31885-152">O sinalizador DT_SET_IMMEDIATE é geralmente usado em combinação com notificações de tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="31885-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="31885-153">A tabela a seguir lista os tipos de controles e todos os valores de sinalizador que podem ser definidos para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="31885-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="31885-154">**Control**</span><span class="sxs-lookup"><span data-stu-id="31885-154">**Control**</span></span>|<span data-ttu-id="31885-155">**Valores válidos para essa propriedade**</span><span class="sxs-lookup"><span data-stu-id="31885-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31885-156">Botão</span><span class="sxs-lookup"><span data-stu-id="31885-156">Button</span></span>  <br/> |<span data-ttu-id="31885-157">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="31885-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="31885-158">Caixa de seleção</span><span class="sxs-lookup"><span data-stu-id="31885-158">Check box</span></span>  <br/> |<span data-ttu-id="31885-159">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="31885-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="31885-160">Caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="31885-160">Combo box</span></span>  <br/> |<span data-ttu-id="31885-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="31885-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="31885-162">Caixa de listagem suspensa</span><span class="sxs-lookup"><span data-stu-id="31885-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="31885-163">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="31885-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="31885-164">Edit</span><span class="sxs-lookup"><span data-stu-id="31885-164">Edit</span></span>  <br/> |<span data-ttu-id="31885-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="31885-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="31885-166">Caixa de grupo</span><span class="sxs-lookup"><span data-stu-id="31885-166">Group box</span></span>  <br/> |<span data-ttu-id="31885-167">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="31885-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="31885-168">Rótulo</span><span class="sxs-lookup"><span data-stu-id="31885-168">Label</span></span>  <br/> |<span data-ttu-id="31885-169">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="31885-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="31885-170">Caixa de listagem</span><span class="sxs-lookup"><span data-stu-id="31885-170">List box</span></span>  <br/> |<span data-ttu-id="31885-171">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="31885-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="31885-172">Caixa de listagem suspensa de múltiplos valores</span><span class="sxs-lookup"><span data-stu-id="31885-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="31885-173">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="31885-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="31885-174">Caixa de listagem de vários valores</span><span class="sxs-lookup"><span data-stu-id="31885-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="31885-175">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="31885-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="31885-176">Página com guias</span><span class="sxs-lookup"><span data-stu-id="31885-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="31885-177">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="31885-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="31885-178">Botão de opção</span><span class="sxs-lookup"><span data-stu-id="31885-178">Radio button</span></span>  <br/> |<span data-ttu-id="31885-179">Deve ser zero</span><span class="sxs-lookup"><span data-stu-id="31885-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="31885-180">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="31885-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="31885-181">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="31885-181">Header files</span></span>

<span data-ttu-id="31885-182">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="31885-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="31885-183">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="31885-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="31885-184">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="31885-184">Mapitags.h</span></span>
  
> <span data-ttu-id="31885-185">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="31885-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31885-186">Confira também</span><span class="sxs-lookup"><span data-stu-id="31885-186">See also</span></span>



[<span data-ttu-id="31885-187">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="31885-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="31885-188">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="31885-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="31885-189">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="31885-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="31885-190">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="31885-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

