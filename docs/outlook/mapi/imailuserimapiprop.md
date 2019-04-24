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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351391"
---
# <a name="imailuser--imapiprop"></a><span data-ttu-id="eefe4-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="eefe4-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="eefe4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eefe4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eefe4-105">Fornece acesso a várias propriedades que estão associadas a usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="eefe4-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="eefe4-106">A interface **IMailUser** é implementada por objetos de usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="eefe4-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="eefe4-107">O **IMailUser** herda da interface [IMAPIProp: IUnknown](imapipropiunknown.md) e não tem métodos exclusivos próprios.</span><span class="sxs-lookup"><span data-stu-id="eefe4-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eefe4-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="eefe4-108">Header file:</span></span>  <br/> |<span data-ttu-id="eefe4-109">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="eefe4-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="eefe4-110">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="eefe4-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="eefe4-111">Objetos do usuário de mensagens</span><span class="sxs-lookup"><span data-stu-id="eefe4-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="eefe4-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="eefe4-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="eefe4-113">Provedores de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="eefe4-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="eefe4-114">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="eefe4-114">Called by:</span></span>  <br/> |<span data-ttu-id="eefe4-115">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="eefe4-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="eefe4-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="eefe4-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="eefe4-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="eefe4-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="eefe4-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="eefe4-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="eefe4-119">LPMAILUSER</span><span class="sxs-lookup"><span data-stu-id="eefe4-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="eefe4-120">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="eefe4-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="eefe4-121">Transact</span><span class="sxs-lookup"><span data-stu-id="eefe4-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="eefe4-122">Vtable order</span><span class="sxs-lookup"><span data-stu-id="eefe4-122">Vtable order</span></span>

<span data-ttu-id="eefe4-123">Esta interface não tem nenhum método exclusivo.</span><span class="sxs-lookup"><span data-stu-id="eefe4-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="eefe4-124">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="eefe4-124">**Required properties**</span></span>|<span data-ttu-id="eefe4-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="eefe4-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eefe4-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefe4-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eefe4-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eefe4-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="eefe4-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefe4-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eefe4-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eefe4-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="eefe4-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefe4-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eefe4-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eefe4-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="eefe4-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefe4-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eefe4-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eefe4-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="eefe4-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefe4-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eefe4-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eefe4-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="eefe4-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefe4-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eefe4-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eefe4-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="eefe4-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefe4-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eefe4-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eefe4-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="eefe4-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefe4-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eefe4-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eefe4-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eefe4-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="eefe4-142">Remarks</span></span>

<span data-ttu-id="eefe4-143">Cinco das propriedades necessárias são conhecidas como as propriedades de endereço base para destinatários:</span><span class="sxs-lookup"><span data-stu-id="eefe4-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="eefe4-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="eefe4-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="eefe4-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="eefe4-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="eefe4-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="eefe4-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="eefe4-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="eefe4-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="eefe4-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="eefe4-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="eefe4-149">Essas propriedades são consideradas especiais porque muitos outros grupos de propriedades semelhantes são criados sobre esse grupo base.</span><span class="sxs-lookup"><span data-stu-id="eefe4-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="eefe4-150">Os outros grupos são usados para descrever um destinatário em várias funções, como o remetente original ou delegado da mensagem.</span><span class="sxs-lookup"><span data-stu-id="eefe4-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="eefe4-151">Para obter mais informações sobre essas propriedades e como usá-las, confira [tipos de endereço MAPI](mapi-address-types.md).</span><span class="sxs-lookup"><span data-stu-id="eefe4-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="eefe4-152">Os usuários de mensagens podem exibir uma coleção de suas propriedades ao suportar a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="eefe4-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="eefe4-153">**PR_DETAILS_TABLE** é uma tabela de exibição que descreve o layout de uma caixa de diálogo de detalhes ou uma página de propriedades com guias que exibe informações sobre as propriedades do destinatário.</span><span class="sxs-lookup"><span data-stu-id="eefe4-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="eefe4-154">MAPI cria caixas de diálogo detalhes quando um cliente chama o método [IAddrBook::D etails](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="eefe4-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="eefe4-155">Os objetos do usuário de mensagens podem ter outras propriedades opcionais associadas a eles.</span><span class="sxs-lookup"><span data-stu-id="eefe4-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="eefe4-156">O MAPI define muitas propriedades que fornecem informações de endereçamento adicionais sobre um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="eefe4-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="eefe4-157">Todas essas propriedades são cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="eefe4-157">All of these properties are character strings.</span></span> <span data-ttu-id="eefe4-158">A lista a seguir mostra as propriedades mais comumente usadas:</span><span class="sxs-lookup"><span data-stu-id="eefe4-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="eefe4-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefe4-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="eefe4-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefe4-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="eefe4-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefe4-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="eefe4-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefe4-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="eefe4-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefe4-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="eefe4-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefe4-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="eefe4-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefe4-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="eefe4-166">Para obter uma lista completa das propriedades, consulte [mapeamento de nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md).</span><span class="sxs-lookup"><span data-stu-id="eefe4-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eefe4-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="eefe4-167">See also</span></span>



[<span data-ttu-id="eefe4-168">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="eefe4-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

