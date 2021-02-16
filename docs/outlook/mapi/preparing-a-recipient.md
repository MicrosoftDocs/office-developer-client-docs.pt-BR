---
title: Preparando um destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bb6bc8b8d0199ab07d5dad353dbc25da240593e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419874"
---
# <a name="preparing-a-recipient"></a><span data-ttu-id="1de02-103">Preparando um destinatário</span><span class="sxs-lookup"><span data-stu-id="1de02-103">Preparing a Recipient</span></span>

  
  
<span data-ttu-id="1de02-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1de02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1de02-105">Um aplicativo cliente prepara destinatários convertendo seus identificadores de entrada de curto prazo em identificadores de entrada de longo prazo e possivelmente adicionando, alterando ou reordenando propriedades.</span><span class="sxs-lookup"><span data-stu-id="1de02-105">A client application prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span> <span data-ttu-id="1de02-106">Você pode preparar destinatários que fazem parte de uma lista de destinatários para uma mensagem ou destinatários que não estão relacionados a uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="1de02-106">You can prepare recipients that are part of a recipient list for a message or recipients that are unrelated to a message.</span></span> <span data-ttu-id="1de02-107">Normalmente, os clientes chamam [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) diretamente para converter identificadores de entrada de curto prazo em identificadores de entrada de longo prazo para destinatários incluídos na caixa de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="1de02-107">Typically, clients call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directly to translate short-term entry identifiers into long-term entry identifiers for recipients that are included in the common address dialog box.</span></span> <span data-ttu-id="1de02-108">Para destinatários associados a uma mensagem de saída, a preparação do destinatário é manipulada pelo processo de resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="1de02-108">For recipients that are associated with an outgoing message, recipient preparation is handled by the name resolution process.</span></span> 
  
<span data-ttu-id="1de02-109">Para preparar uma lista de destinatários, chame **IAddrBook::P repareRecips**.</span><span class="sxs-lookup"><span data-stu-id="1de02-109">To prepare a list of recipients, call **IAddrBook::PrepareRecips**.</span></span> <span data-ttu-id="1de02-110">**PrepareRecips** aceita uma estrutura [ADRLIST](adrlist.md) e uma lista de marcas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="1de02-110">**PrepareRecips** accepts an [ADRLIST](adrlist.md) structure and a list of property tags.</span></span> <span data-ttu-id="1de02-111">A **estrutura ADRLIST** contém os destinatários a serem preparados, enquanto a lista de marca de propriedade representa as propriedades que cada destinatário deve suportar.</span><span class="sxs-lookup"><span data-stu-id="1de02-111">The **ADRLIST** structure contains the recipients to be prepared while the property tag list represents properties that each recipient should support.</span></span> <span data-ttu-id="1de02-112">**PrepareRecips** tenta colocar as propriedades incluídas na lista de marca de propriedade no início da estrutura **ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="1de02-112">**PrepareRecips** attempts to place the properties that are included in the property tag list at the beginning of the **ADRLIST** structure.</span></span> <span data-ttu-id="1de02-113">Se alguma das propriedades na lista estiver ausente da estrutura **ADRLIST,** o MAPI chamará o provedor de agendas para fornerí-las.</span><span class="sxs-lookup"><span data-stu-id="1de02-113">If any of the properties in the list are missing from the **ADRLIST** structure, MAPI calls the address book provider to supply them.</span></span> <span data-ttu-id="1de02-114">Se você só precisar verificar se há identificadores de entrada de longo prazo, passe NULL para _o parâmetro lpSPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="1de02-114">If you only need to check for long-term entry identifiers, pass NULL for the  _lpSPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="1de02-115">Por exemplo, suponha que você está trabalhando com cinco destinatários.</span><span class="sxs-lookup"><span data-stu-id="1de02-115">For example, suppose you are working with five recipients.</span></span> <span data-ttu-id="1de02-116">Todos os cinco destinatários aparecem na estrutura **ADRLIST** com as seguintes propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="1de02-116">All five recipients appear in the **ADRLIST** structure with the following properties in the following order:</span></span> 
  
1. <span data-ttu-id="1de02-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1de02-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
2. <span data-ttu-id="1de02-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1de02-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="1de02-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1de02-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
4. <span data-ttu-id="1de02-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1de02-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
5. <span data-ttu-id="1de02-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1de02-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
<span data-ttu-id="1de02-122">Três outras propriedades estão incluídas na **estrutura ADRLIST** para os dois primeiros destinatários.</span><span class="sxs-lookup"><span data-stu-id="1de02-122">Three other properties are included in the **ADRLIST** structure for the first two recipients.</span></span> 
  
1. <span data-ttu-id="1de02-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1de02-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span>
    
2. <span data-ttu-id="1de02-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1de02-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="1de02-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1de02-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span></span>
    
<span data-ttu-id="1de02-126">Como todos os destinatários precisam ter como suas três primeiras propriedades **PR_ADDRTYPE**, **PR_ENTRYID** e **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), crie uma matriz de marca de propriedade com essas propriedades e passe-a e a estrutura **ADRLIST** para **PrepareRecips**.</span><span class="sxs-lookup"><span data-stu-id="1de02-126">Because all of the recipients need to have as their first three properties **PR_ADDRTYPE**, **PR_ENTRYID**, and **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), create a property tag array with these properties and pass it and the **ADRLIST** structure to **PrepareRecips**.</span></span> <span data-ttu-id="1de02-127">**PrepareRecips** chama o método **IMAPIProp::GetProps**  de cada destinatário para recuperar PR_HOME_TELEPHONE_NUMBER porque ele não faz parte da estrutura **ADRLIST** no momento.</span><span class="sxs-lookup"><span data-stu-id="1de02-127">**PrepareRecips** calls each recipient's **IMAPIProp::GetProps** method to retrieve **PR_HOME_TELEPHONE_NUMBER** because it is not currently part of the **ADRLIST** structure.</span></span> <span data-ttu-id="1de02-128">Quando **PrepareRecips** retorna, a lista de destinatários representa uma lista mesclada de destinatários com as propriedades incluídas na estrutura **ADRLIST** que aparecem primeiro para cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="1de02-128">When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient.</span></span> 
  
<span data-ttu-id="1de02-129">A lista de destinatários dos destinatários 1 e 2 inclui propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="1de02-129">The recipient list for recipients 1 and 2 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="1de02-130">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="1de02-130">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="1de02-131">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="1de02-131">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="1de02-132">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="1de02-132">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="1de02-133">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="1de02-133">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="1de02-134">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="1de02-134">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="1de02-135">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="1de02-135">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="1de02-136">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="1de02-136">**PR_ADDRTYPE**</span></span>
    
8. <span data-ttu-id="1de02-137">**PR_ACCOUNT**</span><span class="sxs-lookup"><span data-stu-id="1de02-137">**PR_ACCOUNT**</span></span>
    
9. <span data-ttu-id="1de02-138">**PR_GIVEN_NAME**</span><span class="sxs-lookup"><span data-stu-id="1de02-138">**PR_GIVEN_NAME**</span></span>
    
10. <span data-ttu-id="1de02-139">**PR_SURNAME**</span><span class="sxs-lookup"><span data-stu-id="1de02-139">**PR_SURNAME**</span></span>
    
<span data-ttu-id="1de02-140">A lista de destinatários dos destinatários 3, 4 e 5 inclui propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="1de02-140">The recipient list for recipients 3, 4, and 5 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="1de02-141">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="1de02-141">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="1de02-142">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="1de02-142">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="1de02-143">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="1de02-143">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="1de02-144">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="1de02-144">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="1de02-145">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="1de02-145">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="1de02-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="1de02-146">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="1de02-147">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="1de02-147">**PR_ADDRTYPE**</span></span>
    
<span data-ttu-id="1de02-148">Como alternativa à chamada **de IAddrBook::P repareRecips** para trabalhar com propriedades, chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) de cada destinatário e, se necessário, seu método [IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="1de02-148">As an alternative to calling **IAddrBook::PrepareRecips** to work with properties, call each recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method and, if necessary, its [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="1de02-149">Quando apenas um destinatário está envolvido, qualquer técnica é satisfatória.</span><span class="sxs-lookup"><span data-stu-id="1de02-149">When only one recipient is involved, either technique is satisfactory.</span></span> <span data-ttu-id="1de02-150">No entanto, quando vários destinatários estão envolvidos, chamar **PrepareRecips** em vez dos métodos **IMAPIProp** economiza tempo e, se você estiver operando remotamente, muitas chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="1de02-150">However, when multiple recipients are involved, calling **PrepareRecips** rather than the **IMAPIProp** methods saves time and, if you are operating remotely, many remote procedure calls.</span></span> <span data-ttu-id="1de02-151">**PrepareRecips** processa todos os destinatários em uma única chamada, enquanto **GetProps** e **SetProps** fazem uma chamada para cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="1de02-151">**PrepareRecips** processes all recipients in a single call whereas **GetProps** and **SetProps** make one call for each recipient.</span></span> 
  

