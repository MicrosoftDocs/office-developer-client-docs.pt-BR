---
title: IMailUser IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMailUser
api_type:
- COM
ms.assetid: 74c25870-62d9-484a-9a99-4dc35c52479e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a0e109fe95120483e700bab5b82f6d7cb75e2e28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436591"
---
# <a name="imailuser--imapiprop"></a><span data-ttu-id="30395-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="30395-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="30395-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30395-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30395-105">Fornece acesso a muitas propriedades associadas a usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="30395-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="30395-106">A interface **IMailUser** é implementada por objetos de usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="30395-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="30395-107">**IMailUser** herda da interface [IMAPIProp : IUnknown](imapipropiunknown.md) e não tem métodos exclusivos próprios.</span><span class="sxs-lookup"><span data-stu-id="30395-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30395-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="30395-108">Header file:</span></span>  <br/> |<span data-ttu-id="30395-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30395-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="30395-110">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="30395-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="30395-111">Objetos de usuário de mensagens</span><span class="sxs-lookup"><span data-stu-id="30395-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="30395-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="30395-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="30395-113">Provedores de lista de endereços</span><span class="sxs-lookup"><span data-stu-id="30395-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="30395-114">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="30395-114">Called by:</span></span>  <br/> |<span data-ttu-id="30395-115">Aplicativos do cliente</span><span class="sxs-lookup"><span data-stu-id="30395-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="30395-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="30395-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="30395-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="30395-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="30395-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="30395-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="30395-119">LPMAILUSER</span><span class="sxs-lookup"><span data-stu-id="30395-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="30395-120">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="30395-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="30395-121">Transacted</span><span class="sxs-lookup"><span data-stu-id="30395-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="30395-122">Vtable order</span><span class="sxs-lookup"><span data-stu-id="30395-122">Vtable order</span></span>

<span data-ttu-id="30395-123">Essa interface não tem métodos exclusivos.</span><span class="sxs-lookup"><span data-stu-id="30395-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="30395-124">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="30395-124">**Required properties**</span></span>|<span data-ttu-id="30395-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="30395-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30395-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30395-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="30395-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="30395-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="30395-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30395-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="30395-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="30395-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="30395-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30395-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="30395-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30395-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="30395-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30395-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="30395-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="30395-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="30395-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30395-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="30395-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30395-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="30395-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30395-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="30395-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30395-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="30395-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30395-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="30395-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30395-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="30395-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30395-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="30395-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30395-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30395-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="30395-142">Remarks</span></span>

<span data-ttu-id="30395-143">Cinco das propriedades necessárias são conhecidas como propriedades de endereço base para destinatários:</span><span class="sxs-lookup"><span data-stu-id="30395-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="30395-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="30395-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="30395-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="30395-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="30395-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="30395-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="30395-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="30395-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="30395-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="30395-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="30395-149">Essas propriedades são consideradas especiais porque muitos outros grupos de propriedades semelhantes são construídos sobre esse grupo base.</span><span class="sxs-lookup"><span data-stu-id="30395-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="30395-150">Os outros grupos são usados para descrever um destinatário em várias funções, como o remetente original ou delegado de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="30395-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="30395-151">Para obter mais informações sobre essas propriedades e como usá-las, consulte [MAPI Address Types](mapi-address-types.md).</span><span class="sxs-lookup"><span data-stu-id="30395-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="30395-152">Os usuários de mensagens podem exibir uma coleção de suas propriedades dando suporte à **propriedade PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="30395-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="30395-153">**PR_DETAILS_TABLE** é uma tabela de exibição que descreve o layout de uma caixa de diálogo de detalhes ou uma página de propriedades com guias que exibe informações de propriedade do destinatário.</span><span class="sxs-lookup"><span data-stu-id="30395-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="30395-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::D etails](iaddrbook-details.md) method.</span><span class="sxs-lookup"><span data-stu-id="30395-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="30395-155">Os objetos de usuário de mensagens podem ter outras propriedades opcionais associadas a eles.</span><span class="sxs-lookup"><span data-stu-id="30395-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="30395-156">MAPI define muitas propriedades que fornecem informações de endereçamento adicionais sobre um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="30395-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="30395-157">Todas essas propriedades são cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="30395-157">All of these properties are character strings.</span></span> <span data-ttu-id="30395-158">A lista a seguir mostra as propriedades mais comumente usadas:</span><span class="sxs-lookup"><span data-stu-id="30395-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="30395-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30395-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="30395-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30395-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="30395-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30395-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="30395-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30395-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="30395-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30395-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="30395-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30395-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="30395-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30395-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="30395-166">Para uma lista completa de propriedades, consulte Mapeamento de nomes de propriedades [canônicas para nomes MAPI.](mapping-canonical-property-names-to-mapi-names.md)</span><span class="sxs-lookup"><span data-stu-id="30395-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="30395-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="30395-167">See also</span></span>



[<span data-ttu-id="30395-168">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="30395-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

