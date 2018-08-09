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
ms.openlocfilehash: 7fee3c84d6a4d4a94397f5197f45637b0c7dd2be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766925"
---
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="5de5f-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="5de5f-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="5de5f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5de5f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5de5f-105">Fornece acesso às listas de distribuição no endereço modificável contêineres de catálogo.</span><span class="sxs-lookup"><span data-stu-id="5de5f-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="5de5f-106">**IDistList** pode criar, copiar e excluir listas de distribuição, além de executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="5de5f-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5de5f-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5de5f-107">Header file:</span></span>  <br/> |<span data-ttu-id="5de5f-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5de5f-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5de5f-109">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="5de5f-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="5de5f-110">Objetos de lista de distribuição</span><span class="sxs-lookup"><span data-stu-id="5de5f-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="5de5f-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="5de5f-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="5de5f-112">Provedores de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="5de5f-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="5de5f-113">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="5de5f-113">Called by:</span></span>  <br/> |<span data-ttu-id="5de5f-114">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="5de5f-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="5de5f-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="5de5f-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5de5f-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="5de5f-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="5de5f-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="5de5f-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="5de5f-118">LPDISTLIST</span><span class="sxs-lookup"><span data-stu-id="5de5f-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="5de5f-119">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="5de5f-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="5de5f-120">Transacionadas</span><span class="sxs-lookup"><span data-stu-id="5de5f-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5de5f-121">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="5de5f-121">Vtable order</span></span>

<span data-ttu-id="5de5f-122">Essa interface não tem quaisquer métodos exclusivos.</span><span class="sxs-lookup"><span data-stu-id="5de5f-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="5de5f-123">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="5de5f-123">**Required properties**</span></span>|<span data-ttu-id="5de5f-124">**Access**</span><span class="sxs-lookup"><span data-stu-id="5de5f-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5de5f-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5de5f-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5de5f-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5de5f-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="5de5f-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5de5f-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5de5f-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5de5f-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="5de5f-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5de5f-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5de5f-130">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5de5f-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="5de5f-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5de5f-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5de5f-132">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5de5f-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="5de5f-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5de5f-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5de5f-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5de5f-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5de5f-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="5de5f-135">Remarks</span></span>

<span data-ttu-id="5de5f-136">A interface **IDistList** herda de [IMAPIContainer](imapicontainerimapiprop.md) e inclui os mesmos métodos como recipientes do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="5de5f-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="5de5f-137">Portanto, como os métodos da interface **IDistList** são idênticos da interface [IABContainer](iabcontainerimapicontainer.md) , eles não são duplicados aqui.</span><span class="sxs-lookup"><span data-stu-id="5de5f-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="5de5f-138">Uma lista de distribuição ou um objeto que implementa **IDistList** é uma coleção de objetos de usuário de mensagens ou destinatários individuais.</span><span class="sxs-lookup"><span data-stu-id="5de5f-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="5de5f-139">Uma lista de distribuição pode consistir em todos os objetos de usuário de mensagens, ou alguns usuários de mensagens e algumas listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="5de5f-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="5de5f-140">Geralmente, há dois tipos de listas de distribuição:</span><span class="sxs-lookup"><span data-stu-id="5de5f-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="5de5f-141">Listas de distribuição expandidas pelo sistema de mensagens subjacente.</span><span class="sxs-lookup"><span data-stu-id="5de5f-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="5de5f-142">Esse tipo de lista possui um endereço, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) e é tratada da mesma como se fosse um destinatário individual.</span><span class="sxs-lookup"><span data-stu-id="5de5f-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="5de5f-143">Listas de distribuição que existem em um contêiner de local e são expandidas pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="5de5f-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="5de5f-144">Propriedades da lista de distribuição opcionais incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5de5f-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="5de5f-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5de5f-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="5de5f-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5de5f-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="5de5f-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5de5f-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="5de5f-148">Observe que **PR_ADDRTYPE** é obrigatório, mas **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) não está.</span><span class="sxs-lookup"><span data-stu-id="5de5f-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="5de5f-149">Isso acontece porque sem um endereço de email de uma lista de distribuição ainda poderá receber mensagens, mas sua lista de membros deve ser expandida.</span><span class="sxs-lookup"><span data-stu-id="5de5f-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="5de5f-150">Se a propriedade **PR_ADDRTYPE** é definida como MAPIPDL, MAPI realiza a expansão.</span><span class="sxs-lookup"><span data-stu-id="5de5f-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="5de5f-151">Se **PR_ADDRTYPE** for um valor diferente de MAPIPDL, o provedor de transporte executa a expansão.</span><span class="sxs-lookup"><span data-stu-id="5de5f-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="5de5f-152">Para obter informações adicionais sobre como usar os métodos **IDistList** , consulte as entradas de referência para os métodos paralelas do **IABContainer**.</span><span class="sxs-lookup"><span data-stu-id="5de5f-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5de5f-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="5de5f-153">See also</span></span>



[<span data-ttu-id="5de5f-154">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="5de5f-154">MAPI Interfaces</span></span>](mapi-interfaces.md)

