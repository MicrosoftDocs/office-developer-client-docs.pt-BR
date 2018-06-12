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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 04fbfb2e6938c1ae5971e90b30f5ef749e7963e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766473"
---
# <a name="dtbllbx"></a><span data-ttu-id="e6954-103">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="e6954-103">DTBLLBX</span></span>

  
  
<span data-ttu-id="e6954-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e6954-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e6954-105">Descreve uma lista que será usada em uma caixa de diálogo que é construída a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="e6954-105">Describes a list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e6954-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e6954-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6954-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e6954-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a><span data-ttu-id="e6954-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e6954-108">Members</span></span>

 <span data-ttu-id="e6954-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e6954-109">**ulFlags**</span></span>
  
> <span data-ttu-id="e6954-110">Bitmask dos sinalizadores usados para eliminar uma barra de rolagem horizontal ou vertical da lista.</span><span class="sxs-lookup"><span data-stu-id="e6954-110">Bitmask of flags used to eliminate a horizontal or vertical scroll bar from the list.</span></span> <span data-ttu-id="e6954-111">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="e6954-111">The following flags can be set:</span></span>
    
<span data-ttu-id="e6954-112">MAPI_NO_HBAR</span><span class="sxs-lookup"><span data-stu-id="e6954-112">MAPI_NO_HBAR</span></span> 
  
> <span data-ttu-id="e6954-113">Nenhuma barra de rolagem horizontal deve ser exibida com a lista.</span><span class="sxs-lookup"><span data-stu-id="e6954-113">No horizontal scroll bar should be shown with the list.</span></span>
    
<span data-ttu-id="e6954-114">MAPI_NO_VBAR</span><span class="sxs-lookup"><span data-stu-id="e6954-114">MAPI_NO_VBAR</span></span> 
  
> <span data-ttu-id="e6954-115">Nenhuma barra de rolagem vertical deve ser exibida com a lista.</span><span class="sxs-lookup"><span data-stu-id="e6954-115">No vertical scroll bar should be shown with the list.</span></span>
    
 <span data-ttu-id="e6954-116">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="e6954-116">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="e6954-117">Marca de propriedade para uma propriedade de qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="e6954-117">Property tag for a property of any type.</span></span> <span data-ttu-id="e6954-118">Essa propriedade é uma das colunas na tabela identificado pelo membro **ulPRTableTable** .</span><span class="sxs-lookup"><span data-stu-id="e6954-118">This property is one of the columns in the table identified by the **ulPRTableTable** member.</span></span> 
    
 <span data-ttu-id="e6954-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="e6954-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="e6954-120">Marca de propriedade para uma propriedade de tabela do tipo PT_OBJECT que podem ser abertos usando uma **OpenProperty** chamar.</span><span class="sxs-lookup"><span data-stu-id="e6954-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="e6954-121">O número de colunas que a tabela deve ter depende se a lista é uma lista de seleção única ou múltipla.</span><span class="sxs-lookup"><span data-stu-id="e6954-121">The number of columns that the table should have depends on whether the list is a single or multiple selection list.</span></span> <span data-ttu-id="e6954-122">Se o membro **ulPRSetProperty** é definido como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), a lista permite a seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="e6954-122">If the **ulPRSetProperty** member is set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), the list allows for multiple selection.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6954-123">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="e6954-123">Remarks</span></span>

<span data-ttu-id="e6954-124">Uma estrutura **DTBLLBX** descreve uma um controle que é usado para mostrar vários itens e permitir que o usuário selecione um ou mais dos itens de lista.</span><span class="sxs-lookup"><span data-stu-id="e6954-124">A **DTBLLBX** structure describes a list a control that is used to show multiple items and let a user select one or more of the items.</span></span> 
  
<span data-ttu-id="e6954-125">O membro **ulPRSetProperty** e o membro **ulPRTableName** trabalhar juntos; Quando um valor for escolhido da tabela, ele será gravado novamente **ulPRSetProperty** quando a caixa de diálogo é descartada.</span><span class="sxs-lookup"><span data-stu-id="e6954-125">The **ulPRSetProperty** member and **ulPRTableName** member work together; when one value is chosen from the table, it is written back to **ulPRSetProperty** when the dialog box is dismissed.</span></span> 
  
<span data-ttu-id="e6954-126">O valor de flags indica se uma barra de rolagem horizontal ou vertical deve ser exibida com a lista.</span><span class="sxs-lookup"><span data-stu-id="e6954-126">The flags value indicates whether a horizontal or vertical scroll bar should be displayed with the list.</span></span> <span data-ttu-id="e6954-127">O padrão é a ter tipos de barra de rolagem aparece se for necessário.</span><span class="sxs-lookup"><span data-stu-id="e6954-127">The default is to have types of scroll bars appear if it is required.</span></span> <span data-ttu-id="e6954-128">Provedores de serviços podem definir MAPI_NO_HBAR para suprimir a uma barra de rolagem horizontal e MAPI_NO_VBAR para suprimir a uma barra de rolagem vertical.</span><span class="sxs-lookup"><span data-stu-id="e6954-128">Service providers can set MAPI_NO_HBAR to suppress a horizontal scroll bar and MAPI_NO_VBAR to suppress a vertical scroll bar.</span></span> 
  
<span data-ttu-id="e6954-129">Os membros da marca de dois propriedade funcionam juntos para exibir valores na lista e definir propriedades correspondentes, quando um item na lista é selecionado.</span><span class="sxs-lookup"><span data-stu-id="e6954-129">The two property tag members work together to display values in the list and set corresponding properties when an item in the list is selected.</span></span> <span data-ttu-id="e6954-130">Quando o MAPI primeiro exibe a lista, ele chama o método de **OpenProperty** da implementação **IMAPIProp** para recuperar a tabela identificada no membro **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="e6954-130">When MAPI first displays the list, it calls the **IMAPIProp** implementation's **OpenProperty** method to retrieve the table identified in the **ulPRTableName** member.</span></span> <span data-ttu-id="e6954-131">O número de colunas na tabela depende do valor do membro **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="e6954-131">The number of columns in the table depends on the value of the **ulPRSetProperty** member.</span></span> <span data-ttu-id="e6954-132">Se **ulPRSetProperty** for definido como **PR_NULL**, a lista é uma lista de seleção de vários com base em um objeto que contém os destinatários, como um contêiner de catálogo de endereços, uma tabela de destinatários de uma mensagem ou uma tabela de conteúdo de lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="e6954-132">If **ulPRSetProperty** is set to **PR_NULL**, the list is a multiple selection list based on an object that contains recipients, such as an address book container, a recipient table for a message, or a distribution list contents table.</span></span> 
  
<span data-ttu-id="e6954-133">Um objeto table para uma lista de seleção de vários deve incluir as seguintes colunas:</span><span class="sxs-lookup"><span data-stu-id="e6954-133">A table for a multiple selection list must include the following columns:</span></span>
  
 <span data-ttu-id="e6954-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e6954-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="e6954-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e6954-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
 <span data-ttu-id="e6954-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e6954-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
  
 <span data-ttu-id="e6954-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) e um máximo de cinco outras propriedades de cadeia de caracteres de valores múltiplos também pode ser exibido com as três colunas obrigatórias.</span><span class="sxs-lookup"><span data-stu-id="e6954-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) and a maximum of five other multivalued string properties can also be displayed with the three required columns.</span></span> 
  
<span data-ttu-id="e6954-138">Se o membro **ulPRSetProperty** não estiver definido como **PR_NULL**, a lista é uma lista de seleção única.</span><span class="sxs-lookup"><span data-stu-id="e6954-138">If the **ulPRSetProperty** member is not set to **PR_NULL**, the list is a single selection list.</span></span> <span data-ttu-id="e6954-139">O valor inicial de **ulPRSetProperty** determina a primeira linha selecionada.</span><span class="sxs-lookup"><span data-stu-id="e6954-139">The initial value of **ulPRSetProperty** determines the first selected row.</span></span> <span data-ttu-id="e6954-140">Quando um usuário seleciona uma das linhas, o membro **ulPRSetProperty** for definido como o valor selecionado e esse valor será gravado novamente a implementação de interface de propriedade com uma chamada para [IMAPIProp::SetProps](imapiprop-setprops.md).</span><span class="sxs-lookup"><span data-stu-id="e6954-140">When a user selects one of the rows, the **ulPRSetProperty** member is set to the selected value and this value is written back to the property interface implementation with a call to [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span> 
  
<span data-ttu-id="e6954-141">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e6954-141">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="e6954-142">Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e6954-142">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e6954-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6954-143">See also</span></span>



[<span data-ttu-id="e6954-144">DTCTL</span><span class="sxs-lookup"><span data-stu-id="e6954-144">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="e6954-145">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="e6954-145">MAPI Structures</span></span>](mapi-structures.md)

