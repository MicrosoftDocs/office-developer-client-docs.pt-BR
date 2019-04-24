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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350887"
---
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="c3f13-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c3f13-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="c3f13-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3f13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3f13-105">Fornece acesso a listas de distribuição em contêineres de catálogos de endereços modificáveis.</span><span class="sxs-lookup"><span data-stu-id="c3f13-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="c3f13-106">O **IDistList** pode criar, copiar e excluir listas de distribuição, além de executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="c3f13-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c3f13-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c3f13-107">Header file:</span></span>  <br/> |<span data-ttu-id="c3f13-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c3f13-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c3f13-109">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="c3f13-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="c3f13-110">Objetos de lista de distribuição</span><span class="sxs-lookup"><span data-stu-id="c3f13-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="c3f13-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c3f13-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="c3f13-112">Provedores de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="c3f13-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="c3f13-113">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="c3f13-113">Called by:</span></span>  <br/> |<span data-ttu-id="c3f13-114">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="c3f13-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="c3f13-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="c3f13-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c3f13-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="c3f13-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="c3f13-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="c3f13-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="c3f13-118">LPDISTLIST</span><span class="sxs-lookup"><span data-stu-id="c3f13-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="c3f13-119">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="c3f13-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="c3f13-120">Transact</span><span class="sxs-lookup"><span data-stu-id="c3f13-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c3f13-121">Vtable order</span><span class="sxs-lookup"><span data-stu-id="c3f13-121">Vtable order</span></span>

<span data-ttu-id="c3f13-122">Esta interface não tem nenhum método exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c3f13-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="c3f13-123">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="c3f13-123">**Required properties**</span></span>|<span data-ttu-id="c3f13-124">**Access**</span><span class="sxs-lookup"><span data-stu-id="c3f13-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c3f13-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c3f13-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c3f13-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c3f13-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="c3f13-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c3f13-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c3f13-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c3f13-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="c3f13-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c3f13-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c3f13-130">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3f13-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="c3f13-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c3f13-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c3f13-132">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3f13-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="c3f13-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c3f13-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c3f13-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3f13-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3f13-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3f13-135">Remarks</span></span>

<span data-ttu-id="c3f13-136">A interface **IDistList** herda de [IMAPIContainer](imapicontainerimapiprop.md) e inclui os mesmos métodos que os contêineres do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="c3f13-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="c3f13-137">Portanto, como os métodos da interface **IDistList** são idênticos aos da interface [IABContainer](iabcontainerimapicontainer.md) , eles não são duplicados aqui.</span><span class="sxs-lookup"><span data-stu-id="c3f13-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="c3f13-138">Uma lista de distribuição ou um objeto que implementa **IDistList** é uma coleção de objetos de usuário de mensagens ou destinatários individuais.</span><span class="sxs-lookup"><span data-stu-id="c3f13-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="c3f13-139">Uma lista de distribuição pode consistir em todos os objetos de usuário de mensagens ou alguns usuários de mensagens e algumas listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="c3f13-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="c3f13-140">Normalmente, há dois tipos de listas de distribuição:</span><span class="sxs-lookup"><span data-stu-id="c3f13-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="c3f13-141">Listas de distribuição que são expandidas pelo sistema de mensagens subjacente.</span><span class="sxs-lookup"><span data-stu-id="c3f13-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="c3f13-142">Esse tipo de lista tem um endereço, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) e é tratado como se fosse um destinatário individual.</span><span class="sxs-lookup"><span data-stu-id="c3f13-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="c3f13-143">As listas de distribuição que existem em um contêiner local e são expandidas pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="c3f13-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="c3f13-144">As propriedades de lista de distribuição opcional incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3f13-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="c3f13-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c3f13-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="c3f13-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c3f13-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="c3f13-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c3f13-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="c3f13-148">Observe que **PR_ADDRTYPE** é necessário, mas **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) não é.</span><span class="sxs-lookup"><span data-stu-id="c3f13-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="c3f13-149">Isso ocorre porque uma lista de distribuição sem um endereço de email ainda pode receber mensagens, mas sua lista de membros deve ser expandida.</span><span class="sxs-lookup"><span data-stu-id="c3f13-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="c3f13-150">Se a propriedade **PR_ADDRTYPE** estiver definida como MAPIPDL, MAPI executará a expansão.</span><span class="sxs-lookup"><span data-stu-id="c3f13-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="c3f13-151">Se **PR_ADDRTYPE** for um valor diferente de MAPIPDL, o provedor de transporte executará a expansão.</span><span class="sxs-lookup"><span data-stu-id="c3f13-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="c3f13-152">Para obter informações adicionais sobre como usar os métodos **IDistList** , consulte as entradas de referência para os métodos paralelos do **IABContainer**.</span><span class="sxs-lookup"><span data-stu-id="c3f13-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c3f13-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3f13-153">See also</span></span>



[<span data-ttu-id="c3f13-154">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="c3f13-154">MAPI Interfaces</span></span>](mapi-interfaces.md)

