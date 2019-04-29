---
title: Criar uma lista de destinatários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e3aa1f2b2e1e7c6d8a9be3fff451002952930ffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428211"
---
# <a name="creating-a-recipient-list"></a><span data-ttu-id="40435-103">Criar uma lista de destinatários</span><span class="sxs-lookup"><span data-stu-id="40435-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="40435-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40435-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40435-105">Uma lista de destinatários é uma estrutura [das ADRLIST](adrlist.md) que contém uma matriz de estruturas de valor de propriedade para cada destinatário de mensagem — destino para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="40435-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="40435-106">Um destinatário pode representar um usuário humano, uma máquina ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="40435-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="40435-107">Todas as mensagens a serem enviadas exigem pelo menos um destinatário com o processo de resolução de nome — um processo para garantir que a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) seja incluída na matriz de valor de Propriedade do destinatário.</span><span class="sxs-lookup"><span data-stu-id="40435-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="40435-108">As propriedades de um destinatário são uma combinação de propriedades de catálogo de endereços e propriedades de mensagem.</span><span class="sxs-lookup"><span data-stu-id="40435-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="40435-109">As propriedades de destinatário podem ser aplicadas a todas as mensagens de um determinado destinatário ou apenas à mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="40435-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="40435-110">O armazenamento de mensagens e os provedores de transporte podem definir as propriedades do destinatário.</span><span class="sxs-lookup"><span data-stu-id="40435-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="40435-111">Cada destinatário deve ter um conjunto principal de propriedades em sua matriz de valor de propriedade, quando a mensagem estiver pronta para ser enviada.</span><span class="sxs-lookup"><span data-stu-id="40435-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="40435-112">O conjunto necessário de propriedades de destinatários inclui:</span><span class="sxs-lookup"><span data-stu-id="40435-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="40435-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40435-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="40435-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40435-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="40435-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40435-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="40435-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="40435-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="40435-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40435-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="40435-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40435-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="40435-119">Essas propriedades são usadas para acessar o destinatário, enviar mensagens a ele e compará-las a outras pessoas.</span><span class="sxs-lookup"><span data-stu-id="40435-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="40435-120">Nem todas essas propriedades precisam estar disponíveis imediatamente.</span><span class="sxs-lookup"><span data-stu-id="40435-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="40435-121">Você pode adicionar um destinatário inicialmente sem saber seu identificador de entrada, contando com o processo de resolução de nomes para atribuir essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="40435-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="40435-122">Em algum momento antes de enviar uma mensagem, chame [IAddrBook:: ResolveName](iaddrbook-resolvename.md) para garantir que todos os destinatários na lista de destinatários sejam resolvidos.</span><span class="sxs-lookup"><span data-stu-id="40435-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="40435-123">Para obter mais informações, consulte [resolvendo o nome de um destinatário](resolving-a-recipient-name.md).</span><span class="sxs-lookup"><span data-stu-id="40435-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="40435-124">As listas de destinatários podem ser criadas a partir de usuários de mensagens ou entradas de lista de distribuição em um contêiner de catálogo de endereços ou em um.</span><span class="sxs-lookup"><span data-stu-id="40435-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="40435-125">Uma delas são destinatários criados como entradas temporárias para serem usados apenas para endereçar uma única mensagem ou como entradas a serem adicionadas a um catálogo de endereços pessoal.</span><span class="sxs-lookup"><span data-stu-id="40435-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="40435-126">O formato para um identificador de entrada one-off e um endereço é definido por MAPI.</span><span class="sxs-lookup"><span data-stu-id="40435-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="40435-127">Para obter mais informações sobre esses formatos, confira [endereços únicos](one-off-addresses.md) e [identificadores de entrada one-off](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="40435-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="40435-128">Você pode permitir que os usuários criem suas listas de destinatários:</span><span class="sxs-lookup"><span data-stu-id="40435-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="40435-129">Somente com entradas do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="40435-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="40435-130">Somente com entradas one-off.</span><span class="sxs-lookup"><span data-stu-id="40435-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="40435-131">Com uma combinação de destinatários do catálogo de endereços e uma única.</span><span class="sxs-lookup"><span data-stu-id="40435-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="40435-132">**Para criar uma lista de destinatários usando a caixa de diálogo endereço comum**</span><span class="sxs-lookup"><span data-stu-id="40435-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="40435-133">Alocar uma estrutura [ADRPARM](adrparm.md) e um ponteiro para uma estrutura [das ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="40435-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="40435-134">Zero a memória na estrutura **ADRPARM** e definir o ponteiro **das ADRLIST** como nulo.</span><span class="sxs-lookup"><span data-stu-id="40435-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="40435-135">Chamar [IAddrBook:: endereço](iaddrbook-address.md) para exibir a caixa de diálogo de endereço e preencher a estrutura **ADRPARM** .</span><span class="sxs-lookup"><span data-stu-id="40435-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="40435-136">Chamar [IMessage:: ModifyRecipients](imessage-modifyrecipients.md), passando o ponteiro do **das ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="40435-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="40435-137">Essa estrutura conterá as propriedades de cada um dos destinatários selecionados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="40435-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="40435-138">**Para criar uma lista de destinatários por programação**</span><span class="sxs-lookup"><span data-stu-id="40435-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="40435-139">Aloque uma estrutura **das ADRLIST** que contenha uma estrutura [ADRENTRY](adrentry.md) para cada um dos destinatários a serem incluídos na lista.</span><span class="sxs-lookup"><span data-stu-id="40435-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="40435-140">Torne cada estrutura **ADRENTRY** grande o suficiente para reter cada uma das propriedades obrigatórias e **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="40435-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="40435-141">Para cada destinatário, defina a matriz de valor da propriedade para seu membro **aEntries** na estrutura **das ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="40435-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="40435-142">Chamar [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) com o sinalizador MODRECIP_ADD definido.</span><span class="sxs-lookup"><span data-stu-id="40435-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    

