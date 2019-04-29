---
title: DTBLLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLBX
api_type:
- COM
ms.assetid: 971b4837-6823-4f28-9803-3c22b2ec091f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2bff20af2b3e9ea4e203e38ae38a8bc19074a727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438565"
---
# <a name="dtbllbx"></a><span data-ttu-id="0e65b-103">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="0e65b-103">DTBLLBX</span></span>

  
  
<span data-ttu-id="0e65b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e65b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e65b-105">Descreve uma lista que será usada em uma caixa de diálogo criada a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="0e65b-105">Describes a list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e65b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0e65b-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e65b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0e65b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a><span data-ttu-id="0e65b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0e65b-108">Members</span></span>

 <span data-ttu-id="0e65b-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="0e65b-109">**ulFlags**</span></span>
  
> <span data-ttu-id="0e65b-110">Bitmask dos sinalizadores usados para eliminar uma barra de rolagem horizontal ou vertical da lista.</span><span class="sxs-lookup"><span data-stu-id="0e65b-110">Bitmask of flags used to eliminate a horizontal or vertical scroll bar from the list.</span></span> <span data-ttu-id="0e65b-111">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="0e65b-111">The following flags can be set:</span></span>
    
<span data-ttu-id="0e65b-112">MAPI_NO_HBAR</span><span class="sxs-lookup"><span data-stu-id="0e65b-112">MAPI_NO_HBAR</span></span> 
  
> <span data-ttu-id="0e65b-113">Nenhuma barra de rolagem horizontal deve ser mostrada com a lista.</span><span class="sxs-lookup"><span data-stu-id="0e65b-113">No horizontal scroll bar should be shown with the list.</span></span>
    
<span data-ttu-id="0e65b-114">MAPI_NO_VBAR</span><span class="sxs-lookup"><span data-stu-id="0e65b-114">MAPI_NO_VBAR</span></span> 
  
> <span data-ttu-id="0e65b-115">Nenhuma barra de rolagem vertical deve ser exibida com a lista.</span><span class="sxs-lookup"><span data-stu-id="0e65b-115">No vertical scroll bar should be shown with the list.</span></span>
    
 <span data-ttu-id="0e65b-116">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="0e65b-116">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="0e65b-117">Marca de propriedade de uma propriedade de qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="0e65b-117">Property tag for a property of any type.</span></span> <span data-ttu-id="0e65b-118">Essa propriedade é uma das colunas na tabela identificadas pelo membro **ulPRTableTable** .</span><span class="sxs-lookup"><span data-stu-id="0e65b-118">This property is one of the columns in the table identified by the **ulPRTableTable** member.</span></span> 
    
 <span data-ttu-id="0e65b-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="0e65b-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="0e65b-120">Marca de propriedade de uma propriedade de tabela do tipo PT_OBJECT que pode ser aberta usando \*\*\*\* uma chamada OpenProperty.</span><span class="sxs-lookup"><span data-stu-id="0e65b-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="0e65b-121">O número de colunas que a tabela deve ter depende se a lista é uma única ou múltipla lista de seleção.</span><span class="sxs-lookup"><span data-stu-id="0e65b-121">The number of columns that the table should have depends on whether the list is a single or multiple selection list.</span></span> <span data-ttu-id="0e65b-122">Se o membro **ulPRSetProperty** estiver definido como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), a lista permitirá a seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="0e65b-122">If the **ulPRSetProperty** member is set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), the list allows for multiple selection.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e65b-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e65b-123">Remarks</span></span>

<span data-ttu-id="0e65b-124">Uma estrutura **DTBLLBX** descreve uma lista um controle que é usado para mostrar vários itens e permitir que um usuário selecione um ou mais itens.</span><span class="sxs-lookup"><span data-stu-id="0e65b-124">A **DTBLLBX** structure describes a list a control that is used to show multiple items and let a user select one or more of the items.</span></span> 
  
<span data-ttu-id="0e65b-125">O membro **ulPRSetProperty** e o membro **ulPRTableName** funcionam juntos; Quando um valor é escolhido na tabela, ele é gravado novamente no **ulPRSetProperty** quando a caixa de diálogo é descartada.</span><span class="sxs-lookup"><span data-stu-id="0e65b-125">The **ulPRSetProperty** member and **ulPRTableName** member work together; when one value is chosen from the table, it is written back to **ulPRSetProperty** when the dialog box is dismissed.</span></span> 
  
<span data-ttu-id="0e65b-126">O valor flags indica se uma barra de rolagem horizontal ou vertical deve ser exibida com a lista.</span><span class="sxs-lookup"><span data-stu-id="0e65b-126">The flags value indicates whether a horizontal or vertical scroll bar should be displayed with the list.</span></span> <span data-ttu-id="0e65b-127">O padrão é que os tipos de barras de rolagem apareçam se necessário.</span><span class="sxs-lookup"><span data-stu-id="0e65b-127">The default is to have types of scroll bars appear if it is required.</span></span> <span data-ttu-id="0e65b-128">Os provedores de serviços podem definir MAPI_NO_HBAR para suprimir uma barra de rolagem horizontal e MAPI_NO_VBAR para suprimir uma barra de rolagem vertical.</span><span class="sxs-lookup"><span data-stu-id="0e65b-128">Service providers can set MAPI_NO_HBAR to suppress a horizontal scroll bar and MAPI_NO_VBAR to suppress a vertical scroll bar.</span></span> 
  
<span data-ttu-id="0e65b-129">Os dois membros da marca de propriedade trabalham juntos para exibir valores na lista e definir as propriedades correspondentes quando um item da lista é selecionado.</span><span class="sxs-lookup"><span data-stu-id="0e65b-129">The two property tag members work together to display values in the list and set corresponding properties when an item in the list is selected.</span></span> <span data-ttu-id="0e65b-130">Quando MAPI exibe primeiro a lista, ele chama o método OpenProperty \*\*\*\* da implementação do **IMAPIProp** para recuperar a tabela identificada no membro **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="0e65b-130">When MAPI first displays the list, it calls the **IMAPIProp** implementation's **OpenProperty** method to retrieve the table identified in the **ulPRTableName** member.</span></span> <span data-ttu-id="0e65b-131">O número de colunas na tabela depende do valor do membro **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="0e65b-131">The number of columns in the table depends on the value of the **ulPRSetProperty** member.</span></span> <span data-ttu-id="0e65b-132">Se **ulPRSetProperty** estiver definido como **PR_NULL**, a lista é uma lista de seleção múltipla com base em um objeto que contém destinatários, como um contêiner de catálogo de endereços, uma tabela de destinatários para uma mensagem ou uma tabela de conteúdo da lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="0e65b-132">If **ulPRSetProperty** is set to **PR_NULL**, the list is a multiple selection list based on an object that contains recipients, such as an address book container, a recipient table for a message, or a distribution list contents table.</span></span> 
  
<span data-ttu-id="0e65b-133">Uma tabela para uma lista de seleção múltipla deve incluir as seguintes colunas:</span><span class="sxs-lookup"><span data-stu-id="0e65b-133">A table for a multiple selection list must include the following columns:</span></span>
  
 <span data-ttu-id="0e65b-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0e65b-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="0e65b-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0e65b-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
 <span data-ttu-id="0e65b-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0e65b-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
  
 <span data-ttu-id="0e65b-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) e um máximo de cinco outras propriedades de cadeia de caracteres com valores múltiplos também podem ser exibidos com as três colunas obrigatórias.</span><span class="sxs-lookup"><span data-stu-id="0e65b-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) and a maximum of five other multivalued string properties can also be displayed with the three required columns.</span></span> 
  
<span data-ttu-id="0e65b-138">Se o membro **ulPRSetProperty** não estiver definido como **PR_NULL**, a lista será uma única lista de seleção.</span><span class="sxs-lookup"><span data-stu-id="0e65b-138">If the **ulPRSetProperty** member is not set to **PR_NULL**, the list is a single selection list.</span></span> <span data-ttu-id="0e65b-139">O valor inicial de **ulPRSetProperty** determina a primeira linha selecionada.</span><span class="sxs-lookup"><span data-stu-id="0e65b-139">The initial value of **ulPRSetProperty** determines the first selected row.</span></span> <span data-ttu-id="0e65b-140">Quando um usuário seleciona uma das linhas, o membro **ulPRSetProperty** é definido para o valor selecionado e esse valor é gravado novamente na implementação da interface de propriedade com uma chamada para [IMAPIProp::](imapiprop-setprops.md)SetProps.</span><span class="sxs-lookup"><span data-stu-id="0e65b-140">When a user selects one of the rows, the **ulPRSetProperty** member is set to the selected value and this value is written back to the property interface implementation with a call to [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span> 
  
<span data-ttu-id="0e65b-141">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="0e65b-141">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="0e65b-142">Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="0e65b-142">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0e65b-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e65b-143">See also</span></span>



[<span data-ttu-id="0e65b-144">DTCTL</span><span class="sxs-lookup"><span data-stu-id="0e65b-144">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="0e65b-145">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="0e65b-145">MAPI Structures</span></span>](mapi-structures.md)

