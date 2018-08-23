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
ms.openlocfilehash: 7a6971504ec8f4f5ac8593b6b78777a12ff92b3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564560"
---
# <a name="imailuser--imapiprop"></a><span data-ttu-id="6e26f-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6e26f-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="6e26f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e26f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e26f-105">Fornece acesso às propriedades muitos que estão associados aos usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6e26f-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="6e26f-106">A interface de **IMailUser** é implementada por objetos de usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6e26f-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="6e26f-107">**IMailUser** herde a [IMAPIProp: IUnknown](imapipropiunknown.md) interface e não possui exclusivos métodos sua própria conta.</span><span class="sxs-lookup"><span data-stu-id="6e26f-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e26f-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6e26f-108">Header file:</span></span>  <br/> |<span data-ttu-id="6e26f-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e26f-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6e26f-110">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="6e26f-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="6e26f-111">Objetos de usuário de mensagens</span><span class="sxs-lookup"><span data-stu-id="6e26f-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="6e26f-112">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="6e26f-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="6e26f-113">Provedores de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="6e26f-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="6e26f-114">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="6e26f-114">Called by:</span></span>  <br/> |<span data-ttu-id="6e26f-115">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="6e26f-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="6e26f-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="6e26f-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6e26f-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="6e26f-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="6e26f-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="6e26f-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="6e26f-119">LPMAILUSER</span><span class="sxs-lookup"><span data-stu-id="6e26f-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="6e26f-120">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="6e26f-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="6e26f-121">Transacionadas</span><span class="sxs-lookup"><span data-stu-id="6e26f-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6e26f-122">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="6e26f-122">Vtable order</span></span>

<span data-ttu-id="6e26f-123">Essa interface não tem quaisquer métodos exclusivos.</span><span class="sxs-lookup"><span data-stu-id="6e26f-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="6e26f-124">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="6e26f-124">**Required properties**</span></span>|<span data-ttu-id="6e26f-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="6e26f-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6e26f-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e26f-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6e26f-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6e26f-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="6e26f-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e26f-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6e26f-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6e26f-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="6e26f-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e26f-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6e26f-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e26f-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="6e26f-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e26f-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6e26f-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6e26f-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="6e26f-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e26f-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6e26f-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e26f-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="6e26f-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e26f-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6e26f-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e26f-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="6e26f-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e26f-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6e26f-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e26f-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="6e26f-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e26f-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6e26f-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e26f-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e26f-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e26f-142">Remarks</span></span>

<span data-ttu-id="6e26f-143">Cinco das propriedades necessárias são conhecidos como as propriedades de um endereço base para destinatários:</span><span class="sxs-lookup"><span data-stu-id="6e26f-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="6e26f-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="6e26f-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="6e26f-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="6e26f-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="6e26f-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="6e26f-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="6e26f-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="6e26f-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="6e26f-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="6e26f-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="6e26f-149">Essas propriedades serão consideradas especiais porque muitos outros grupos de propriedades semelhantes se baseiam neste grupo base.</span><span class="sxs-lookup"><span data-stu-id="6e26f-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="6e26f-150">Os outros grupos são usados para descrever um destinatário em várias funções, tais como uma mensagem original ou delegar o remetente.</span><span class="sxs-lookup"><span data-stu-id="6e26f-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="6e26f-151">Para obter mais informações sobre essas propriedades e como usá-las, consulte [Tipos de endereço de MAPI](mapi-address-types.md).</span><span class="sxs-lookup"><span data-stu-id="6e26f-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="6e26f-152">Mensagens de usuários podem exibir uma coleção de suas propriedades, oferecendo suporte a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6e26f-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="6e26f-153">**PR_DETAILS_TABLE** é uma tabela de exibição que descreve o layout de uma caixa de diálogo detalhes ou uma página de propriedades com guias que exibe informações de propriedade do destinatário.</span><span class="sxs-lookup"><span data-stu-id="6e26f-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="6e26f-154">MAPI cria detalhes caixas de diálogo quando um cliente chama o método [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="6e26f-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="6e26f-155">Objetos de usuário de mensagens podem ter outras propriedades opcionais associadas a eles.</span><span class="sxs-lookup"><span data-stu-id="6e26f-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="6e26f-156">MAPI define várias propriedades que fornecem informações adicionais sobre um usuário de mensagens de endereçamento.</span><span class="sxs-lookup"><span data-stu-id="6e26f-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="6e26f-157">Todas essas propriedades são cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6e26f-157">All of these properties are character strings.</span></span> <span data-ttu-id="6e26f-158">A lista a seguir mostra mais comumente usadas propriedades:</span><span class="sxs-lookup"><span data-stu-id="6e26f-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="6e26f-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e26f-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6e26f-160">**PR_ASSISTANT** ([Pidtagassistant de MAPI](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e26f-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6e26f-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e26f-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6e26f-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e26f-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6e26f-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e26f-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6e26f-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e26f-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6e26f-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6e26f-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="6e26f-166">Para obter uma lista completa das propriedades, consulte [Mapeamento canônico nomes de propriedade para nomes de MAPI](mapping-canonical-property-names-to-mapi-names.md).</span><span class="sxs-lookup"><span data-stu-id="6e26f-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e26f-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e26f-167">See also</span></span>



[<span data-ttu-id="6e26f-168">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="6e26f-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

