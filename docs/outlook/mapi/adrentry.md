---
title: ADRENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRENTRY
api_type:
- COM
ms.assetid: 5fa091a4-3a84-4881-91b3-e34fd9ca6f38
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 36e0218c9e4e312a138bef7517242f74079212c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421435"
---
# <a name="adrentry"></a><span data-ttu-id="69c01-103">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="69c01-103">ADRENTRY</span></span>

  
  
<span data-ttu-id="69c01-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69c01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69c01-105">Descreve zero ou mais propriedades que pertencem a um destinatário.</span><span class="sxs-lookup"><span data-stu-id="69c01-105">Describes zero or more properties that belong to a recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69c01-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="69c01-106">Header file:</span></span>  <br/> |<span data-ttu-id="69c01-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69c01-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a><span data-ttu-id="69c01-108">Members</span><span class="sxs-lookup"><span data-stu-id="69c01-108">Members</span></span>

 <span data-ttu-id="69c01-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="69c01-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="69c01-110">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="69c01-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="69c01-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="69c01-111">**cValues**</span></span>
  
> <span data-ttu-id="69c01-112">Contagem de propriedades na matriz de valores de propriedade apontada pelo **membro rgPropVals.**</span><span class="sxs-lookup"><span data-stu-id="69c01-112">Count of properties in the property value array pointed to by the **rgPropVals** member.</span></span> <span data-ttu-id="69c01-113">O **membro cValues** pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="69c01-113">The **cValues** member can be zero.</span></span> 
    
 <span data-ttu-id="69c01-114">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="69c01-114">**rgPropVals**</span></span>
  
> <span data-ttu-id="69c01-115">Ponteiro para uma matriz de valores de propriedade descrevendo as propriedades do destinatário.</span><span class="sxs-lookup"><span data-stu-id="69c01-115">Pointer to a property value array describing the properties for the recipient.</span></span> <span data-ttu-id="69c01-116">O **membro rgPropVals** pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="69c01-116">The **rgPropVals** member can be NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="69c01-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="69c01-117">Remarks</span></span>

<span data-ttu-id="69c01-118">Uma **estrutura ADRENTRY** descreve as propriedades que pertencem a um único destinatário.</span><span class="sxs-lookup"><span data-stu-id="69c01-118">An **ADRENTRY** structure describes properties that belong to a single recipient.</span></span> <span data-ttu-id="69c01-119">As propriedades que normalmente são usadas para descrever um destinatário incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="69c01-119">The properties that are typically used to describe a recipient include the following:</span></span> 
  
 <span data-ttu-id="69c01-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69c01-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="69c01-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69c01-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
  
 <span data-ttu-id="69c01-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69c01-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
  
 <span data-ttu-id="69c01-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69c01-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="69c01-124">Quando um identificador de entrada **ou PR_ENTRYID** propriedade aparece na matriz [SPropValue](spropvalue.md) de um destinatário, isso indica que o destinatário foi resolvido.</span><span class="sxs-lookup"><span data-stu-id="69c01-124">When an entry identifier or **PR_ENTRYID** property appears in the [SPropValue](spropvalue.md) array for a recipient, this indicates that the recipient has been resolved.</span></span> <span data-ttu-id="69c01-125">Os clientes chamam [o método IAddrBook::ResolveName](iaddrbook-resolvename.md) para garantir que todos os destinatários na lista de destinatários de uma mensagem de saída tenham sido resolvidos.</span><span class="sxs-lookup"><span data-stu-id="69c01-125">Clients call the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method to make sure that all recipients in the recipient list of an outgoing message have been resolved.</span></span> <span data-ttu-id="69c01-126">Somente destinatários resolvidos podem ser enviados com mensagens.</span><span class="sxs-lookup"><span data-stu-id="69c01-126">Only resolved recipients can be sent with messages.</span></span> 
  
 <span data-ttu-id="69c01-127">**Estruturas ADRENTRY** são normalmente combinadas para formar uma matriz para o membro **aEntries** de uma [estrutura ADRLIST.](adrlist.md)</span><span class="sxs-lookup"><span data-stu-id="69c01-127">**ADRENTRY** structures are typically combined to form an array for the **aEntries** member of an [ADRLIST](adrlist.md) structure.</span></span> 
  
 <span data-ttu-id="69c01-128">**Estruturas ADRENTRY** e [SRow](srow.md) são idênticas porque ambas contêm um membro reservado, uma matriz de valores de propriedade e uma contagem de valores na matriz.</span><span class="sxs-lookup"><span data-stu-id="69c01-128">**ADRENTRY** structures and [SRow](srow.md) structures are identical because they both contain a reserved member, an array of property values, and a count of values in the array.</span></span> <span data-ttu-id="69c01-129">Enquanto as **estruturas ADRENTRY** são combinadas para formar o membro **aEntries** de uma estrutura **ADRLIST,** as estruturas **SRow** são combinadas para formar o membro **aRow** de uma [estrutura SRowSet.](srowset.md)</span><span class="sxs-lookup"><span data-stu-id="69c01-129">Whereas **ADRENTRY** structures are combined to form the **aEntries** member of an **ADRLIST** structure, **SRow** structures are combined to form the **aRow** member of an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="69c01-130">Os dois tipos de estruturas seguem as mesmas regras de alocação, indicando que uma estrutura **SRowSet** recuperada do índice de um contêiner de um livro de endereços pode ser lançada em uma estrutura **ADRLIST** e usada como está.</span><span class="sxs-lookup"><span data-stu-id="69c01-130">Both types of structures follow the same allocation rules, implying that an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="69c01-131">Uma **estrutura ADRENTRY** pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="69c01-131">An **ADRENTRY** structure can be empty.</span></span> <span data-ttu-id="69c01-132">Por exemplo, uma estrutura **ADRENTRY** contida na estrutura **ADRLIST** apontada pelo parâmetro  _lppAdrList_ em uma chamada para **IAddrBook::Address** pode estar vazia quando um destinatário está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="69c01-132">For example, an **ADRENTRY** structure that is contained in the **ADRLIST** structure pointed to by the  _lppAdrList_ parameter in a call to **IAddrBook::Address** can be empty when a recipient is being removed.</span></span> 
  
<span data-ttu-id="69c01-133">Para obter mais informações sobre como alocar memória para estruturas **ADRENTRY,** consulte Gerenciando memória para [estruturas ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="69c01-133">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="69c01-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="69c01-134">See also</span></span>



[<span data-ttu-id="69c01-135">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="69c01-135">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="69c01-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="69c01-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="69c01-137">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="69c01-137">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="69c01-138">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="69c01-138">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="69c01-139">SRow</span><span class="sxs-lookup"><span data-stu-id="69c01-139">SRow</span></span>](srow.md)
  
[<span data-ttu-id="69c01-140">SRowSet</span><span class="sxs-lookup"><span data-stu-id="69c01-140">SRowSet</span></span>](srowset.md)


[<span data-ttu-id="69c01-141">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="69c01-141">MAPI Structures</span></span>](mapi-structures.md)

