---
title: ADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRLIST
api_type:
- COM
ms.assetid: 85f0d8a5-6dd3-4f33-b31a-246d286d6286
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 87b91b66807ce79533029a8d5b5c4956bc4d5ce9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565764"
---
# <a name="adrlist"></a><span data-ttu-id="761cb-103">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="761cb-103">ADRLIST</span></span>

<span data-ttu-id="761cb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="761cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="761cb-105">Descreve as propriedades de zero ou mais que pertencem a um ou mais destinatários.</span><span class="sxs-lookup"><span data-stu-id="761cb-105">Describes zero or more properties that belong to one or more recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="761cb-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="761cb-106">Header file:</span></span>  <br/> |<span data-ttu-id="761cb-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="761cb-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="761cb-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="761cb-108">Related macros:</span></span>  <br/> |<span data-ttu-id="761cb-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span><span class="sxs-lookup"><span data-stu-id="761cb-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span></span> <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a><span data-ttu-id="761cb-110">Members</span><span class="sxs-lookup"><span data-stu-id="761cb-110">Members</span></span>

<span data-ttu-id="761cb-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="761cb-111">**cEntries**</span></span>
  
> <span data-ttu-id="761cb-112">Contagem de entradas na matriz especificada pelo membro **aEntries** .</span><span class="sxs-lookup"><span data-stu-id="761cb-112">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
<span data-ttu-id="761cb-113">**aEntries**</span><span class="sxs-lookup"><span data-stu-id="761cb-113">**aEntries**</span></span>
  
> <span data-ttu-id="761cb-114">Matriz de estruturas [ADRENTRY](adrentry.md) , uma estrutura de cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="761cb-114">Array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="761cb-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="761cb-115">Remarks</span></span>

<span data-ttu-id="761cb-116">Uma estrutura **ADRLIST** contém uma ou mais estruturas **ADRENTRY** , cada uma delas descreve as propriedades de um destinatário.</span><span class="sxs-lookup"><span data-stu-id="761cb-116">An **ADRLIST** structure contains one or more **ADRENTRY** structures, each describing the properties of a recipient.</span></span> <span data-ttu-id="761cb-117">Um destinatário pode ser não resolvido.</span><span class="sxs-lookup"><span data-stu-id="761cb-117">A recipient can be unresolved.</span></span> <span data-ttu-id="761cb-118">Isso significa que ele está faltando um identificador de entrada na sua matriz de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="761cb-118">This means that it is lacking an entry identifier in its array of property values.</span></span> <span data-ttu-id="761cb-119">Um destinatário resolvido significa que o **PR\_ENTRYID** propriedade ([PidTagEntryId](pidtagentryid-canonical-property.md)) esteja incluída.</span><span class="sxs-lookup"><span data-stu-id="761cb-119">A resolved recipient means that the **PR\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included.</span></span> <span data-ttu-id="761cb-120">Geralmente, destinatários resolvidos também têm um email a propriedade **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) de endereços.</span><span class="sxs-lookup"><span data-stu-id="761cb-120">Typically, resolved recipients also have an email address the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="761cb-121">No entanto, o endereço de email não é necessário.</span><span class="sxs-lookup"><span data-stu-id="761cb-121">However, the email address is not required.</span></span> <span data-ttu-id="761cb-122">Estruturas **ADRLIST** são usadas, por exemplo, para descrever a lista de destinatários para uma mensagem de saída e por MAPI para exibir as entradas no catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="761cb-122">**ADRLIST** structures are used, for example, to describe the recipient list for an outgoing message and by MAPI to display the entries in the address book.</span></span> 
  
<span data-ttu-id="761cb-123">Estruturas **ADRLIST** assemelhar [SRowSet](srowset.md) estruturas as estruturas usadas para representar as linhas em tabelas.</span><span class="sxs-lookup"><span data-stu-id="761cb-123">**ADRLIST** structures resemble [SRowSet](srowset.md) structures the structures used for representing rows in tables.</span></span> <span data-ttu-id="761cb-124">Na verdade, essas duas estruturas foram projetadas para que possa ser usados de forma intercambiável.</span><span class="sxs-lookup"><span data-stu-id="761cb-124">In fact, these two structures are designed so that they can be used interchangeably.</span></span> <span data-ttu-id="761cb-125">Ambos contêm uma matriz de estruturas que descrevem um grupo de propriedades e uma contagem dos valores na matriz.</span><span class="sxs-lookup"><span data-stu-id="761cb-125">Both contain an array of structures describing a group of properties and a count of the values in the array.</span></span> <span data-ttu-id="761cb-126">Enquanto na estrutura de **ADRLIST** , a matriz contém estruturas [ADRENTRY](adrentry.md) , na estrutura de **SRowSet** a matriz contém estruturas [SRow](srow.md) .</span><span class="sxs-lookup"><span data-stu-id="761cb-126">Whereas in the **ADRLIST** structure, the array contains [ADRENTRY](adrentry.md) structures, in the **SRowSet** structure the array contains [SRow](srow.md) structures.</span></span> <span data-ttu-id="761cb-127">Estruturas **ADRENTRY** e estruturas de **SRow** são idênticas em layout.</span><span class="sxs-lookup"><span data-stu-id="761cb-127">**ADRENTRY** structures and **SRow** structures are identical in layout.</span></span> <span data-ttu-id="761cb-128">Como **ADRLIST** e **SRowSet** estruturas seguem as mesmas regras de alocação, uma estrutura **SRowSet** que é recuperada no índice de conteúdo de um contêiner de catálogo de endereços pode ser convertida em uma estrutura **ADRLIST** e usada como está.</span><span class="sxs-lookup"><span data-stu-id="761cb-128">Because **ADRLIST** and **SRowSet** structures follow the same allocation rules, an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="761cb-129">A ilustração a seguir mostra o layout de uma estrutura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="761cb-129">The following illustration shows the layout of an **ADRLIST** structure.</span></span> 
  
<span data-ttu-id="761cb-130">**ADRLIST components**</span><span class="sxs-lookup"><span data-stu-id="761cb-130">**ADRLIST components**</span></span>
  
<span data-ttu-id="761cb-131">![Componentes ADRLIST] (media/amapi_18.gif "Componentes ADRLIST")</span><span class="sxs-lookup"><span data-stu-id="761cb-131">![ADRLIST components](media/amapi_18.gif "ADRLIST components")</span></span>
  
<span data-ttu-id="761cb-132">As partes **ADRENTRY** e [SPropValue](spropvalue.md) em uma estrutura **ADRLIST** devem ser alocadas e liberadas independentemente das outras partes.</span><span class="sxs-lookup"><span data-stu-id="761cb-132">The **ADRENTRY** and [SPropValue](spropvalue.md) portions in an **ADRLIST** structure must be allocated and freed independently of the other parts.</span></span> <span data-ttu-id="761cb-133">Ou seja, cada estrutura **SPropValue** deve ser alocada individualmente depois que a memória para a estrutura de **ADRENTRY** foi alocada e liberada antes que a estrutura **ADRENTRY** é liberada.</span><span class="sxs-lookup"><span data-stu-id="761cb-133">That is, each **SPropValue** structure must be allocated individually after memory for the **ADRENTRY** structure has been allocated and freed before the **ADRENTRY** structure is freed.</span></span> <span data-ttu-id="761cb-134">Essa independência na manipulação de memória permite que os destinatários e propriedades de destinatário individuais livremente sejam adicionados ou excluídos da lista de endereços.</span><span class="sxs-lookup"><span data-stu-id="761cb-134">This independence in handling memory allows recipients and individual recipient properties to be freely added or deleted from the address list.</span></span> 
  
<span data-ttu-id="761cb-135">As funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIFreeBuffer](mapifreebuffer.md) devem ser usadas para alocar e liberar a estrutura **ADRLIST** e todas as suas partes.</span><span class="sxs-lookup"><span data-stu-id="761cb-135">The [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions must be used to allocate and free the **ADRLIST** structure and all its parts.</span></span> 
  
<span data-ttu-id="761cb-136">Se uma lista de destinatários é muito grande para caber na memória, clientes podem chamar o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) para trabalhar com um subconjunto da lista.</span><span class="sxs-lookup"><span data-stu-id="761cb-136">If a recipient list is too large to fit in memory, clients can call the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to work with a subset of the list.</span></span> <span data-ttu-id="761cb-137">Os clientes não devem usar as caixas de diálogo comuns do endereço livro nesta situação.</span><span class="sxs-lookup"><span data-stu-id="761cb-137">Clients should not use the address book common dialog boxes in this situation.</span></span> 
  
<span data-ttu-id="761cb-138">Para obter mais informações sobre como alocar memória para as estruturas **ADRENTRY** , consulte [Gerenciar memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="761cb-138">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="761cb-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="761cb-139">See also</span></span>

- [<span data-ttu-id="761cb-140">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="761cb-140">ADRENTRY</span></span>](adrentry.md)  
- [<span data-ttu-id="761cb-141">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="761cb-141">CbNewADRLIST</span></span>](cbnewadrlist.md) 
- [<span data-ttu-id="761cb-142">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="761cb-142">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md) 
- [<span data-ttu-id="761cb-143">SRowSet</span><span class="sxs-lookup"><span data-stu-id="761cb-143">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="761cb-144">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="761cb-144">MAPI Structures</span></span>](mapi-structures.md)

