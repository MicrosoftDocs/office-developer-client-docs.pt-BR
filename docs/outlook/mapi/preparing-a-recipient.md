---
title: Preparar um destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b4ccfb8cf8201a17993932acc4c0104ace80b94d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588717"
---
# <a name="preparing-a-recipient"></a><span data-ttu-id="3f20a-103">Preparar um destinatário</span><span class="sxs-lookup"><span data-stu-id="3f20a-103">Preparing a Recipient</span></span>

  
  
<span data-ttu-id="3f20a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f20a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f20a-105">Um aplicativo cliente prepara destinatários, convertendo seus identificadores de entrada de curto prazo aos identificadores de entrada de longo prazo e, possivelmente, adicionar, alterar ou reordenar propriedades.</span><span class="sxs-lookup"><span data-stu-id="3f20a-105">A client application prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span> <span data-ttu-id="3f20a-106">Você pode preparar destinatários que fazem parte de uma lista de destinatários de uma mensagem ou destinatários que não estão relacionados a uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="3f20a-106">You can prepare recipients that are part of a recipient list for a message or recipients that are unrelated to a message.</span></span> <span data-ttu-id="3f20a-107">Normalmente, os clientes chame [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) diretamente para traduzir identificadores de entrada de curto prazo em longo prazo identificadores de entrada para destinatários incluídos na caixa de diálogo endereço comuns.</span><span class="sxs-lookup"><span data-stu-id="3f20a-107">Typically, clients call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directly to translate short-term entry identifiers into long-term entry identifiers for recipients that are included in the common address dialog box.</span></span> <span data-ttu-id="3f20a-108">Para que os destinatários que estão associados uma mensagem de saída, preparação do destinatário é tratada pelo processo de resolução de nome.</span><span class="sxs-lookup"><span data-stu-id="3f20a-108">For recipients that are associated with an outgoing message, recipient preparation is handled by the name resolution process.</span></span> 
  
<span data-ttu-id="3f20a-109">Para preparar uma lista de destinatários, chame **IAddrBook::PrepareRecips**.</span><span class="sxs-lookup"><span data-stu-id="3f20a-109">To prepare a list of recipients, call **IAddrBook::PrepareRecips**.</span></span> <span data-ttu-id="3f20a-110">**PrepareRecips** aceita uma estrutura [ADRLIST](adrlist.md) e uma lista das marcas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="3f20a-110">**PrepareRecips** accepts an [ADRLIST](adrlist.md) structure and a list of property tags.</span></span> <span data-ttu-id="3f20a-111">A estrutura **ADRLIST** contém os destinatários para estar preparado enquanto a lista de marcas de propriedade representa propriedades que deve oferecer suporte a cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="3f20a-111">The **ADRLIST** structure contains the recipients to be prepared while the property tag list represents properties that each recipient should support.</span></span> <span data-ttu-id="3f20a-112">**PrepareRecips** tenta colocar as propriedades que estão incluídas na lista de marca de propriedade, no início da estrutura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="3f20a-112">**PrepareRecips** attempts to place the properties that are included in the property tag list at the beginning of the **ADRLIST** structure.</span></span> <span data-ttu-id="3f20a-113">Se qualquer uma das propriedades na lista estão ausentes da estrutura de **ADRLIST** , MAPI chama o provedor de catálogo de endereços para fornecê-las.</span><span class="sxs-lookup"><span data-stu-id="3f20a-113">If any of the properties in the list are missing from the **ADRLIST** structure, MAPI calls the address book provider to supply them.</span></span> <span data-ttu-id="3f20a-114">Se você só precisa procurar a longo prazo identificadores de entrada, passe NULL para o parâmetro _lpSPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="3f20a-114">If you only need to check for long-term entry identifiers, pass NULL for the  _lpSPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="3f20a-115">Por exemplo, suponha que você estiver trabalhando com cinco destinatários.</span><span class="sxs-lookup"><span data-stu-id="3f20a-115">For example, suppose you are working with five recipients.</span></span> <span data-ttu-id="3f20a-116">Todos os destinatários de cinco aparecem na estrutura de **ADRLIST** com as seguintes propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="3f20a-116">All five recipients appear in the **ADRLIST** structure with the following properties in the following order:</span></span> 
  
1. <span data-ttu-id="3f20a-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f20a-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
2. <span data-ttu-id="3f20a-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f20a-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="3f20a-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f20a-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
4. <span data-ttu-id="3f20a-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f20a-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
5. <span data-ttu-id="3f20a-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f20a-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
<span data-ttu-id="3f20a-122">Três outras propriedades estão incluídas na estrutura de **ADRLIST** para os dois primeiros destinatários.</span><span class="sxs-lookup"><span data-stu-id="3f20a-122">Three other properties are included in the **ADRLIST** structure for the first two recipients.</span></span> 
  
1. <span data-ttu-id="3f20a-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f20a-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span>
    
2. <span data-ttu-id="3f20a-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f20a-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="3f20a-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f20a-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span></span>
    
<span data-ttu-id="3f20a-126">Como todos os destinatários precisam ter como suas três primeiras propriedades **PR_ADDRTYPE**, **PR_ENTRYID**e **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), crie uma matriz de marca de propriedade com essas propriedades e passe ela e a estrutura **ADRLIST** para **PrepareRecips**.</span><span class="sxs-lookup"><span data-stu-id="3f20a-126">Because all of the recipients need to have as their first three properties **PR_ADDRTYPE**, **PR_ENTRYID**, and **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), create a property tag array with these properties and pass it and the **ADRLIST** structure to **PrepareRecips**.</span></span> <span data-ttu-id="3f20a-127">**PrepareRecips** chama o método de **IMAPIProp::GetProps** de cada destinatário para recuperar **PR_HOME_TELEPHONE_NUMBER** porque atualmente não faz parte da estrutura de **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="3f20a-127">**PrepareRecips** calls each recipient's **IMAPIProp::GetProps** method to retrieve **PR_HOME_TELEPHONE_NUMBER** because it is not currently part of the **ADRLIST** structure.</span></span> <span data-ttu-id="3f20a-128">Quando **PrepareRecips** retorna, a lista de destinatários representa uma lista mesclada de destinatários com as propriedades incluídas na estrutura de **ADRLIST** aparecendo primeiro para cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="3f20a-128">When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient.</span></span> 
  
<span data-ttu-id="3f20a-129">A lista de destinatários para destinatários 1 e 2 inclui propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="3f20a-129">The recipient list for recipients 1 and 2 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="3f20a-130">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="3f20a-130">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="3f20a-131">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="3f20a-131">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="3f20a-132">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="3f20a-132">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="3f20a-133">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="3f20a-133">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="3f20a-134">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="3f20a-134">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="3f20a-135">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="3f20a-135">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="3f20a-136">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="3f20a-136">**PR_ADDRTYPE**</span></span>
    
8. <span data-ttu-id="3f20a-137">**PR_ACCOUNT**</span><span class="sxs-lookup"><span data-stu-id="3f20a-137">**PR_ACCOUNT**</span></span>
    
9. <span data-ttu-id="3f20a-138">**PR_GIVEN_NAME**</span><span class="sxs-lookup"><span data-stu-id="3f20a-138">**PR_GIVEN_NAME**</span></span>
    
10. <span data-ttu-id="3f20a-139">**PR_SURNAME**</span><span class="sxs-lookup"><span data-stu-id="3f20a-139">**PR_SURNAME**</span></span>
    
<span data-ttu-id="3f20a-140">A lista de destinatários para destinatários 3, 4 e 5 inclui propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="3f20a-140">The recipient list for recipients 3, 4, and 5 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="3f20a-141">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="3f20a-141">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="3f20a-142">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="3f20a-142">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="3f20a-143">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="3f20a-143">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="3f20a-144">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="3f20a-144">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="3f20a-145">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="3f20a-145">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="3f20a-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="3f20a-146">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="3f20a-147">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="3f20a-147">**PR_ADDRTYPE**</span></span>
    
<span data-ttu-id="3f20a-148">Como alternativa para chamar **IAddrBook::PrepareRecips** para trabalhar com propriedades, chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) de cada destinatário e, se necessário, seu método [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="3f20a-148">As an alternative to calling **IAddrBook::PrepareRecips** to work with properties, call each recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method and, if necessary, its [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="3f20a-149">Quando somente um destinatário está envolvido, qualquer técnica é satisfatória.</span><span class="sxs-lookup"><span data-stu-id="3f20a-149">When only one recipient is involved, either technique is satisfactory.</span></span> <span data-ttu-id="3f20a-150">No entanto, quando vários destinatários estão envolvidos, chamar **PrepareRecips** ao invés os métodos **IMAPIProp** poupa tempo e, caso esteja operando remotamente, número de chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="3f20a-150">However, when multiple recipients are involved, calling **PrepareRecips** rather than the **IMAPIProp** methods saves time and, if you are operating remotely, many remote procedure calls.</span></span> <span data-ttu-id="3f20a-151">**PrepareRecips** processa todos os destinatários em uma única chamada enquanto **GetProps** e **SetProps** fazem uma chamada para cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="3f20a-151">**PrepareRecips** processes all recipients in a single call whereas **GetProps** and **SetProps** make one call for each recipient.</span></span> 
  

