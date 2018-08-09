---
title: DTBLCHECKBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCHECKBOX
api_type:
- COM
ms.assetid: 0dd12990-5431-4768-9d64-27d4ef6b7b20
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c6726b852176fa31bf879b5a32b63c35ce2be514
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766456"
---
# <a name="dtblcheckbox"></a><span data-ttu-id="4f59c-103">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="4f59c-103">DTBLCHECKBOX</span></span>

  
  
<span data-ttu-id="4f59c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f59c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f59c-105">Contém informações sobre uma caixa de seleção que será usada em uma caixa de diálogo construída a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="4f59c-105">Contains information about a check box that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f59c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4f59c-106">Header file:</span></span>  <br/> |<span data-ttu-id="4f59c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f59c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4f59c-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="4f59c-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="4f59c-109">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="4f59c-109">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a><span data-ttu-id="4f59c-110">Members</span><span class="sxs-lookup"><span data-stu-id="4f59c-110">Members</span></span>

 <span data-ttu-id="4f59c-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="4f59c-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="4f59c-112">Posição na memória da sequência de caracteres que é exibida com a caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="4f59c-112">Position in memory of the character string that is displayed with the check box.</span></span> 
    
 <span data-ttu-id="4f59c-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="4f59c-113">**ulFlags**</span></span>
  
> <span data-ttu-id="4f59c-114">Bitmask dos sinalizadores usado para designar o formato do rótulo da caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="4f59c-114">Bitmask of flags used to designate the format of the check box label.</span></span> <span data-ttu-id="4f59c-115">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="4f59c-115">The following flag can be set:</span></span>
    
<span data-ttu-id="4f59c-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4f59c-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4f59c-117">O rótulo está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="4f59c-117">The label is in Unicode format.</span></span> <span data-ttu-id="4f59c-118">Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo está no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="4f59c-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="4f59c-119">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="4f59c-119">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="4f59c-120">Marca de propriedade para uma propriedade do tipo PT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="4f59c-120">Property tag for a property of type PT_BOOLEAN.</span></span> <span data-ttu-id="4f59c-121">O valor dessa propriedade é afetado pelo estado da caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="4f59c-121">The value of this property is affected by the state of the check box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f59c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f59c-122">Remarks</span></span>

<span data-ttu-id="4f59c-123">Uma estrutura **DTBLCHECKBOX** descreve uma caixa de seleção de um controle que reflete a um dos dois estados: habilitado (uma caixa checked) ou não (uma caixa vazia).</span><span class="sxs-lookup"><span data-stu-id="4f59c-123">A **DTBLCHECKBOX** structure describes a check box a control that reflects one of two states: enabled (a checked box) or disabled (an empty box).</span></span> 
  
<span data-ttu-id="4f59c-124">O membro **ulPRPropertyName** descreve uma propriedade booleana cujo valor é manipulado, alterando o estado da caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="4f59c-124">The **ulPRPropertyName** member describes a Boolean property whose value is manipulated by changing the state of the check box.</span></span> <span data-ttu-id="4f59c-125">Quando a caixa de seleção é exibida pela primeira vez, MAPI chama o método de **GetProps** da implementação **IMAPIProp** associado com a tabela de exibição para recuperar um conjunto de propriedades padrão.</span><span class="sxs-lookup"><span data-stu-id="4f59c-125">When the check box is first displayed, MAPI calls the **GetProps** method of the **IMAPIProp** implementation that is associated with the display table to retrieve a set of default properties.</span></span> <span data-ttu-id="4f59c-126">Se uma das propriedades é mapeado para a marca de propriedade na estrutura de **DTBLCHECKBOX** , o valor para essa propriedade é exibido como o valor inicial da caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="4f59c-126">If one of the properties maps to the property tag in the **DTBLCHECKBOX** structure, the value for that property is displayed as the check box's initial value.</span></span> 
  
<span data-ttu-id="4f59c-127">Controles de caixa de seleção podem ser pode ser modificados.</span><span class="sxs-lookup"><span data-stu-id="4f59c-127">Check box controls can be modifiable.</span></span> <span data-ttu-id="4f59c-128">Isso permite que um usuário alterar seus estados.</span><span class="sxs-lookup"><span data-stu-id="4f59c-128">This allows a user to change their states.</span></span> <span data-ttu-id="4f59c-129">Caixas de seleção modificáveis definir o sinalizador DT_EDITABLE no membro **ulCtlFlags** sua estrutura [DTCTL](dtctl.md) e sua propriedade **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4f59c-129">Modifiable check boxes set the DT_EDITABLE flag in the **ulCtlFlags** member of their [DTCTL](dtctl.md) structure and in their **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="4f59c-130">Quando uma caixa de seleção é alterada seu estado, chamadas de MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) para definir a propriedade identificada no membro de marca de propriedade da estrutura de **DTBLCHECKBOX** para o novo estado.</span><span class="sxs-lookup"><span data-stu-id="4f59c-130">When a check box changes its state, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the property identified in the property tag member of the **DTBLCHECKBOX** structure to the new state.</span></span> 
  
<span data-ttu-id="4f59c-131">Por exemplo, um provedor de catálogo de endereços pode incluir um controle de caixa de seleção modificável em sua caixa de diálogo de configuração para ajustar a configuração da propriedade de **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) de um destinatário.</span><span class="sxs-lookup"><span data-stu-id="4f59c-131">For example, an address book provider might include a modifiable check box control in its configuration dialog box to adjust the setting of a recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="4f59c-132">Quando o usuário seleciona a caixa de seleção, MAPI define essa propriedade como TRUE.</span><span class="sxs-lookup"><span data-stu-id="4f59c-132">When the user selects the check box, MAPI sets this property to TRUE.</span></span> <span data-ttu-id="4f59c-133">Quando a caixa de seleção estiver desmarcada, a propriedade é definida como FALSE.</span><span class="sxs-lookup"><span data-stu-id="4f59c-133">When the check box is unselected, the property is set to FALSE.</span></span>
  
<span data-ttu-id="4f59c-134">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="4f59c-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="4f59c-135">Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="4f59c-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="4f59c-136">Para obter informações sobre os tipos de propriedade, consulte [Visão geral do tipo de propriedade de MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4f59c-136">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4f59c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f59c-137">See also</span></span>



[<span data-ttu-id="4f59c-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="4f59c-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="4f59c-139">Propriedade canônica PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="4f59c-139">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="4f59c-140">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="4f59c-140">MAPI Structures</span></span>](mapi-structures.md)

