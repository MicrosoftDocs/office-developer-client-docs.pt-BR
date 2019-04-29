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
ms.openlocfilehash: bb6bc8b8d0199ab07d5dad353dbc25da240593e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419874"
---
# <a name="preparing-a-recipient"></a><span data-ttu-id="80a6f-103">Preparar um destinatário</span><span class="sxs-lookup"><span data-stu-id="80a6f-103">Preparing a Recipient</span></span>

  
  
<span data-ttu-id="80a6f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80a6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80a6f-105">Um aplicativo cliente prepara os destinatários convertendo seus identificadores de entrada de curto prazo para identificadores de entrada de longo prazo e possivelmente adicionando, alterando ou reordenando Propriedades.</span><span class="sxs-lookup"><span data-stu-id="80a6f-105">A client application prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span> <span data-ttu-id="80a6f-106">Você pode preparar destinatários que fazem parte de uma lista de destinatários para uma ou mais mensagens que não estão relacionadas a uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="80a6f-106">You can prepare recipients that are part of a recipient list for a message or recipients that are unrelated to a message.</span></span> <span data-ttu-id="80a6f-107">Normalmente, os clientes chamam [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) diretamente para converter identificadores de entrada de curto prazo em identificadores de entrada de longo prazo para destinatários incluídos na caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="80a6f-107">Typically, clients call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directly to translate short-term entry identifiers into long-term entry identifiers for recipients that are included in the common address dialog box.</span></span> <span data-ttu-id="80a6f-108">Para destinatários associados a uma mensagem de saída, a preparação do destinatário é tratada pelo processo de resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="80a6f-108">For recipients that are associated with an outgoing message, recipient preparation is handled by the name resolution process.</span></span> 
  
<span data-ttu-id="80a6f-109">Para preparar uma lista de destinatários, chame **IAddrBook::P reparerecips**.</span><span class="sxs-lookup"><span data-stu-id="80a6f-109">To prepare a list of recipients, call **IAddrBook::PrepareRecips**.</span></span> <span data-ttu-id="80a6f-110">**PrepareRecips** aceita uma estrutura [das ADRLIST](adrlist.md) e uma lista de marcas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="80a6f-110">**PrepareRecips** accepts an [ADRLIST](adrlist.md) structure and a list of property tags.</span></span> <span data-ttu-id="80a6f-111">A estrutura **das ADRLIST** contém os destinatários a serem preparados enquanto a lista de marcas de propriedade representa propriedades às quais cada destinatário deve suportar.</span><span class="sxs-lookup"><span data-stu-id="80a6f-111">The **ADRLIST** structure contains the recipients to be prepared while the property tag list represents properties that each recipient should support.</span></span> <span data-ttu-id="80a6f-112">**PrepareRecips** tenta colocar as propriedades incluídas na lista de marcas de propriedade no início da estrutura **das ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="80a6f-112">**PrepareRecips** attempts to place the properties that are included in the property tag list at the beginning of the **ADRLIST** structure.</span></span> <span data-ttu-id="80a6f-113">Se qualquer uma das propriedades na lista estiver ausente da estrutura **das ADRLIST** , o MAPI chamará o provedor de catálogo de endereços para fornecê-las.</span><span class="sxs-lookup"><span data-stu-id="80a6f-113">If any of the properties in the list are missing from the **ADRLIST** structure, MAPI calls the address book provider to supply them.</span></span> <span data-ttu-id="80a6f-114">Se você precisar verificar identificadores de entrada de longo prazo, passe NULL para o parâmetro _lpSPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="80a6f-114">If you only need to check for long-term entry identifiers, pass NULL for the  _lpSPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="80a6f-115">Por exemplo, suponha que você está trabalhando com cinco destinatários.</span><span class="sxs-lookup"><span data-stu-id="80a6f-115">For example, suppose you are working with five recipients.</span></span> <span data-ttu-id="80a6f-116">Todos os cinco destinatários aparecem na estrutura **das ADRLIST** com as seguintes propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="80a6f-116">All five recipients appear in the **ADRLIST** structure with the following properties in the following order:</span></span> 
  
1. <span data-ttu-id="80a6f-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80a6f-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
2. <span data-ttu-id="80a6f-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80a6f-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="80a6f-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80a6f-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
4. <span data-ttu-id="80a6f-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80a6f-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
5. <span data-ttu-id="80a6f-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80a6f-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
<span data-ttu-id="80a6f-122">Três outras propriedades estão incluídas na estrutura **das ADRLIST** para os primeiros dois destinatários.</span><span class="sxs-lookup"><span data-stu-id="80a6f-122">Three other properties are included in the **ADRLIST** structure for the first two recipients.</span></span> 
  
1. <span data-ttu-id="80a6f-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80a6f-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span>
    
2. <span data-ttu-id="80a6f-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80a6f-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="80a6f-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80a6f-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span></span>
    
<span data-ttu-id="80a6f-126">Como todos os destinatários precisam ter suas primeiras três propriedades **PR_ADDRTYPE**, **PR_ENTRYID**e **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), crie uma matriz de marca de propriedade com essas propriedades e passe e a estrutura **das ADRLIST** como **PrepareRecips**.</span><span class="sxs-lookup"><span data-stu-id="80a6f-126">Because all of the recipients need to have as their first three properties **PR_ADDRTYPE**, **PR_ENTRYID**, and **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), create a property tag array with these properties and pass it and the **ADRLIST** structure to **PrepareRecips**.</span></span> <span data-ttu-id="80a6f-127">**PrepareRecips** chama o método **IMAPIProp::** GetProps de cada destinatário para recuperar o **PR_HOME_TELEPHONE_NUMBER** porque ele não faz parte da estrutura do **das ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="80a6f-127">**PrepareRecips** calls each recipient's **IMAPIProp::GetProps** method to retrieve **PR_HOME_TELEPHONE_NUMBER** because it is not currently part of the **ADRLIST** structure.</span></span> <span data-ttu-id="80a6f-128">Quando **PrepareRecips** retorna, a lista de destinatários representa uma lista mesclada de destinatários com as propriedades incluídas na estrutura **das ADRLIST** que aparecem primeiro para cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="80a6f-128">When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient.</span></span> 
  
<span data-ttu-id="80a6f-129">A lista de destinatários para os destinatários 1 e 2 inclui propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="80a6f-129">The recipient list for recipients 1 and 2 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="80a6f-130">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="80a6f-130">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="80a6f-131">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="80a6f-131">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="80a6f-132">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="80a6f-132">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="80a6f-133">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="80a6f-133">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="80a6f-134">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="80a6f-134">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="80a6f-135">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="80a6f-135">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="80a6f-136">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="80a6f-136">**PR_ADDRTYPE**</span></span>
    
8. <span data-ttu-id="80a6f-137">**PR_ACCOUNT**</span><span class="sxs-lookup"><span data-stu-id="80a6f-137">**PR_ACCOUNT**</span></span>
    
9. <span data-ttu-id="80a6f-138">**PR_GIVEN_NAME**</span><span class="sxs-lookup"><span data-stu-id="80a6f-138">**PR_GIVEN_NAME**</span></span>
    
10. <span data-ttu-id="80a6f-139">**PR_SURNAME**</span><span class="sxs-lookup"><span data-stu-id="80a6f-139">**PR_SURNAME**</span></span>
    
<span data-ttu-id="80a6f-140">A lista de destinatários para os destinatários 3, 4 e 5 inclui propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="80a6f-140">The recipient list for recipients 3, 4, and 5 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="80a6f-141">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="80a6f-141">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="80a6f-142">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="80a6f-142">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="80a6f-143">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="80a6f-143">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="80a6f-144">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="80a6f-144">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="80a6f-145">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="80a6f-145">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="80a6f-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="80a6f-146">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="80a6f-147">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="80a6f-147">**PR_ADDRTYPE**</span></span>
    
<span data-ttu-id="80a6f-148">Como alternativa para chamar **IAddrBook::P reparerecips** para trabalhar com propriedades, chame o método [IMAPIProp:](imapiprop-getprops.md) : GetProps de cada destinatário e, se necessário, o método [IMAPIProp::](imapiprop-setprops.md) SetProps.</span><span class="sxs-lookup"><span data-stu-id="80a6f-148">As an alternative to calling **IAddrBook::PrepareRecips** to work with properties, call each recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method and, if necessary, its [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="80a6f-149">Quando somente um destinatário está envolvido, qualquer técnica é satisfatória.</span><span class="sxs-lookup"><span data-stu-id="80a6f-149">When only one recipient is involved, either technique is satisfactory.</span></span> <span data-ttu-id="80a6f-150">No enTanto, quando vários destinatários estão envolvidos, chamar **PrepareRecips** em vez dos métodos **IMAPIProp** poupa tempo e, se você estiver operando remotamente, várias chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="80a6f-150">However, when multiple recipients are involved, calling **PrepareRecips** rather than the **IMAPIProp** methods saves time and, if you are operating remotely, many remote procedure calls.</span></span> <span data-ttu-id="80a6f-151">O **PrepareRecips** processa todos os destinatários em uma única chamada enquanto GetProps e SetProps fazem uma chamada para cada destinatário. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="80a6f-151">**PrepareRecips** processes all recipients in a single call whereas **GetProps** and **SetProps** make one call for each recipient.</span></span> 
  

