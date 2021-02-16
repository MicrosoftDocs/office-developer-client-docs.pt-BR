---
title: IDistList IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IDistList
api_type:
- COM
ms.assetid: bd8e1ddb-3027-428b-8964-81614f80282d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 463d81a6692b6071cada0ad22e7343020563e41c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431544"
---
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="08689-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="08689-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="08689-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08689-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08689-105">Fornece acesso a listas de distribuição em contêineres de agendas modificáveis.</span><span class="sxs-lookup"><span data-stu-id="08689-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="08689-106">**IDistList** pode criar, copiar e excluir listas de distribuição, além de executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="08689-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08689-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="08689-107">Header file:</span></span>  <br/> |<span data-ttu-id="08689-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08689-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="08689-109">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="08689-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="08689-110">Objetos de lista de distribuição</span><span class="sxs-lookup"><span data-stu-id="08689-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="08689-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="08689-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="08689-112">Provedores de lista de endereços</span><span class="sxs-lookup"><span data-stu-id="08689-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="08689-113">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="08689-113">Called by:</span></span>  <br/> |<span data-ttu-id="08689-114">Aplicativos do cliente</span><span class="sxs-lookup"><span data-stu-id="08689-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="08689-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="08689-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="08689-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="08689-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="08689-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="08689-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="08689-118">LPDISTLIST</span><span class="sxs-lookup"><span data-stu-id="08689-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="08689-119">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="08689-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="08689-120">Transacted</span><span class="sxs-lookup"><span data-stu-id="08689-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="08689-121">Vtable order</span><span class="sxs-lookup"><span data-stu-id="08689-121">Vtable order</span></span>

<span data-ttu-id="08689-122">Essa interface não tem métodos exclusivos.</span><span class="sxs-lookup"><span data-stu-id="08689-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="08689-123">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="08689-123">**Required properties**</span></span>|<span data-ttu-id="08689-124">**Access**</span><span class="sxs-lookup"><span data-stu-id="08689-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="08689-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="08689-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="08689-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08689-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="08689-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="08689-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="08689-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08689-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="08689-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="08689-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="08689-130">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08689-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="08689-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="08689-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="08689-132">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08689-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="08689-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="08689-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="08689-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08689-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08689-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="08689-135">Remarks</span></span>

<span data-ttu-id="08689-136">A interface **IDistList** herda de [IMAPIContainer](imapicontainerimapiprop.md) e inclui os mesmos métodos que os contêineres do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="08689-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="08689-137">Portanto, como os métodos da interface **IDistList** são idênticos aos da interface [IABContainer,](iabcontainerimapicontainer.md) eles não são duplicados aqui.</span><span class="sxs-lookup"><span data-stu-id="08689-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="08689-138">Uma lista de distribuição ou objeto que implementa **IDistList** é uma coleção de objetos de usuário de mensagens ou destinatários individuais.</span><span class="sxs-lookup"><span data-stu-id="08689-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="08689-139">Uma lista de distribuição pode consistir em todos os objetos de usuário de mensagens ou algum usuário de mensagens e algumas listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="08689-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="08689-140">Normalmente, há dois tipos de listas de distribuição:</span><span class="sxs-lookup"><span data-stu-id="08689-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="08689-141">Listas de distribuição expandidas pelo sistema de mensagens subjacente.</span><span class="sxs-lookup"><span data-stu-id="08689-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="08689-142">Esse tipo de lista tem um endereço, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) e é tratado da mesma forma como se fosse um destinatário individual.</span><span class="sxs-lookup"><span data-stu-id="08689-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="08689-143">Listas de distribuição que existem em um contêiner local e são expandidas pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="08689-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="08689-144">As propriedades opcionais da lista de distribuição incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="08689-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="08689-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="08689-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="08689-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="08689-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="08689-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="08689-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="08689-148">Observe que **PR_ADDRTYPE** é necessário, **mas PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) não é.</span><span class="sxs-lookup"><span data-stu-id="08689-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="08689-149">Isso porque uma lista de distribuição sem um endereço de email ainda pode receber mensagens, mas sua lista de membros deve ser expandida.</span><span class="sxs-lookup"><span data-stu-id="08689-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="08689-150">Se a **PR_ADDRTYPE** propriedade for definida como MAPIPDL, o MAPI executará a expansão.</span><span class="sxs-lookup"><span data-stu-id="08689-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="08689-151">Se **PR_ADDRTYPE** for um valor diferente de MAPIPDL, o provedor de transporte executará a expansão.</span><span class="sxs-lookup"><span data-stu-id="08689-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="08689-152">Para obter informações adicionais sobre como usar os métodos **IDistList,** consulte as entradas de referência para os métodos paralelos de **IABContainer**.</span><span class="sxs-lookup"><span data-stu-id="08689-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08689-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="08689-153">See also</span></span>



[<span data-ttu-id="08689-154">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="08689-154">MAPI Interfaces</span></span>](mapi-interfaces.md)

