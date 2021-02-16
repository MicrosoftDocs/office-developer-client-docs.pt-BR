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
ms.openlocfilehash: ed0bbe986f374648e2ee85f3a0d2dfe7bc392e0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436829"
---
# <a name="dtblcheckbox"></a><span data-ttu-id="edfa9-103">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="edfa9-103">DTBLCHECKBOX</span></span>

  
  
<span data-ttu-id="edfa9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edfa9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edfa9-105">Contém informações sobre uma caixa de seleção que será usada em uma caixa de diálogo criada a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="edfa9-105">Contains information about a check box that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="edfa9-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="edfa9-106">Header file:</span></span>  <br/> |<span data-ttu-id="edfa9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="edfa9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="edfa9-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="edfa9-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="edfa9-109">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="edfa9-109">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a><span data-ttu-id="edfa9-110">Members</span><span class="sxs-lookup"><span data-stu-id="edfa9-110">Members</span></span>

 <span data-ttu-id="edfa9-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="edfa9-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="edfa9-112">Posição na memória da cadeia de caracteres exibida com a caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="edfa9-112">Position in memory of the character string that is displayed with the check box.</span></span> 
    
 <span data-ttu-id="edfa9-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="edfa9-113">**ulFlags**</span></span>
  
> <span data-ttu-id="edfa9-114">Bitmask de sinalizadores usados para designar o formato do rótulo da caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="edfa9-114">Bitmask of flags used to designate the format of the check box label.</span></span> <span data-ttu-id="edfa9-115">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="edfa9-115">The following flag can be set:</span></span>
    
<span data-ttu-id="edfa9-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="edfa9-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="edfa9-117">O rótulo está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="edfa9-117">The label is in Unicode format.</span></span> <span data-ttu-id="edfa9-118">Se o MAPI_UNICODE sinalizador não estiver definido, o rótulo está no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="edfa9-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="edfa9-119">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="edfa9-119">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="edfa9-120">Marca de propriedade de uma propriedade do tipo PT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="edfa9-120">Property tag for a property of type PT_BOOLEAN.</span></span> <span data-ttu-id="edfa9-121">O valor dessa propriedade é afetado pelo estado da caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="edfa9-121">The value of this property is affected by the state of the check box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="edfa9-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="edfa9-122">Remarks</span></span>

<span data-ttu-id="edfa9-123">Uma **estrutura DTBLCHECKBOX** descreve uma caixa de seleção de um controle que reflete um dos dois estados: habilitado (uma caixa de seleção) ou desabilitado (uma caixa vazia).</span><span class="sxs-lookup"><span data-stu-id="edfa9-123">A **DTBLCHECKBOX** structure describes a check box a control that reflects one of two states: enabled (a checked box) or disabled (an empty box).</span></span> 
  
<span data-ttu-id="edfa9-124">O **membro ulPRPropertyName** descreve uma propriedade Boolean cujo valor é manipulado alterando o estado da caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="edfa9-124">The **ulPRPropertyName** member describes a Boolean property whose value is manipulated by changing the state of the check box.</span></span> <span data-ttu-id="edfa9-125">Quando a caixa de seleção é exibida pela primeira vez, o MAPI chama o método **GetProps** da implementação **IMAPIProp** que está associada à tabela de exibição para recuperar um conjunto de propriedades padrão.</span><span class="sxs-lookup"><span data-stu-id="edfa9-125">When the check box is first displayed, MAPI calls the **GetProps** method of the **IMAPIProp** implementation that is associated with the display table to retrieve a set of default properties.</span></span> <span data-ttu-id="edfa9-126">Se uma das propriedades for mapeada para a marca de propriedade na estrutura **DTBLCHECKBOX,** o valor dessa propriedade será exibido como o valor inicial da caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="edfa9-126">If one of the properties maps to the property tag in the **DTBLCHECKBOX** structure, the value for that property is displayed as the check box's initial value.</span></span> 
  
<span data-ttu-id="edfa9-127">Os controles de caixa de seleção podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="edfa9-127">Check box controls can be modifiable.</span></span> <span data-ttu-id="edfa9-128">Isso permite que um usuário altere seus estados.</span><span class="sxs-lookup"><span data-stu-id="edfa9-128">This allows a user to change their states.</span></span> <span data-ttu-id="edfa9-129">As caixas de seleção modificáveis configuram o sinalizador DT_EDITABLE no **membro ulCtlFlags** de sua estrutura [DTCTL](dtctl.md) e em sua propriedade **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="edfa9-129">Modifiable check boxes set the DT_EDITABLE flag in the **ulCtlFlags** member of their [DTCTL](dtctl.md) structure and in their **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="edfa9-130">Quando uma caixa de seleção altera seu estado, MAPI chama [IMAPIProp::SetProps](imapiprop-setprops.md) para definir a propriedade identificada no membro da marca de propriedade da estrutura **DTBLCHECKBOX** para o novo estado.</span><span class="sxs-lookup"><span data-stu-id="edfa9-130">When a check box changes its state, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the property identified in the property tag member of the **DTBLCHECKBOX** structure to the new state.</span></span> 
  
<span data-ttu-id="edfa9-131">Por exemplo, um provedor de livro de endereços pode incluir um controle de caixa de seleção modificável em sua caixa de diálogo de configuração para ajustar a configuração da propriedade **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) de um destinatário.</span><span class="sxs-lookup"><span data-stu-id="edfa9-131">For example, an address book provider might include a modifiable check box control in its configuration dialog box to adjust the setting of a recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="edfa9-132">Quando o usuário marca a caixa de seleção, MAPI define essa propriedade como TRUE.</span><span class="sxs-lookup"><span data-stu-id="edfa9-132">When the user selects the check box, MAPI sets this property to TRUE.</span></span> <span data-ttu-id="edfa9-133">Quando a caixa de seleção é desa eleita, a propriedade é definida como FALSE.</span><span class="sxs-lookup"><span data-stu-id="edfa9-133">When the check box is unselected, the property is set to FALSE.</span></span>
  
<span data-ttu-id="edfa9-134">Para uma visão geral das tabelas de exibição, consulte [Tabelas de Exibição.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="edfa9-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="edfa9-135">Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela de exibição.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="edfa9-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="edfa9-136">Para obter informações sobre tipos de propriedade, consulte [Visão geral do tipo de propriedade MAPI.](mapi-property-type-overview.md)</span><span class="sxs-lookup"><span data-stu-id="edfa9-136">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="edfa9-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="edfa9-137">See also</span></span>



[<span data-ttu-id="edfa9-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="edfa9-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="edfa9-139">Propriedade canônica PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="edfa9-139">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="edfa9-140">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="edfa9-140">MAPI Structures</span></span>](mapi-structures.md)

