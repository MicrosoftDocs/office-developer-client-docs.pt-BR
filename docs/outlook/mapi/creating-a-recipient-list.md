---
title: Criar lista de destinatários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: fa23377a8b080ae9dac3e31dfa137ca03a242c74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766370"
---
# <a name="creating-a-recipient-list"></a><span data-ttu-id="99b21-103">Criar lista de destinatários</span><span class="sxs-lookup"><span data-stu-id="99b21-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="99b21-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99b21-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99b21-105">Uma lista de destinatários é uma estrutura [ADRLIST](adrlist.md) que contém uma matriz de estruturas de valor de propriedade de cada destinatário da mensagem — destino da mensagem.</span><span class="sxs-lookup"><span data-stu-id="99b21-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="99b21-106">Um destinatário pode representar um usuário humano, uma máquina ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="99b21-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="99b21-107">Todas as mensagens sejam enviadas exigem pelo menos um destinatário que tiver ficado durante o processo de resolução de nome — um processo para garantir que a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) é incluída na matriz de valores de propriedade do destinatário.</span><span class="sxs-lookup"><span data-stu-id="99b21-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="99b21-108">As propriedades de um destinatário são uma combinação de propriedades do catálogo de endereços e propriedades da mensagem.</span><span class="sxs-lookup"><span data-stu-id="99b21-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="99b21-109">Propriedades de destinatário podem aplicar a todas as mensagens para um destinatário específico ou apenas à mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="99b21-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="99b21-110">Ambos repositório de mensagens e provedores de transporte podem definir propriedades de destinatário.</span><span class="sxs-lookup"><span data-stu-id="99b21-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="99b21-111">Cada destinatário deve ter um conjunto básico de propriedades em sua matriz de valores de propriedade no momento em que a mensagem está pronta para ser enviada.</span><span class="sxs-lookup"><span data-stu-id="99b21-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="99b21-112">O conjunto necessário de propriedades de destinatário incluem:</span><span class="sxs-lookup"><span data-stu-id="99b21-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="99b21-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99b21-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="99b21-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99b21-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="99b21-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99b21-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="99b21-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="99b21-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="99b21-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99b21-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="99b21-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99b21-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="99b21-119">Essas propriedades são usadas para acessar o destinatário, enviar mensagens a ela e compará-lo com outras pessoas.</span><span class="sxs-lookup"><span data-stu-id="99b21-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="99b21-120">Nem todas essas propriedades precisam estar disponíveis imediatamente.</span><span class="sxs-lookup"><span data-stu-id="99b21-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="99b21-121">Você pode adicionar um destinatário inicialmente sem saber seu identificador de entrada, contar com o processo de resolução de nomes para atribuir essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="99b21-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="99b21-122">Em algum momento antes de enviar uma mensagem, chame [IAddrBook::ResolveName](iaddrbook-resolvename.md) para certificar-se de que todos os destinatários na sua lista de destinatários forem resolvidos.</span><span class="sxs-lookup"><span data-stu-id="99b21-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="99b21-123">Para obter mais informações, consulte a [resolução de um nome de destinatário](resolving-a-recipient-name.md).</span><span class="sxs-lookup"><span data-stu-id="99b21-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="99b21-124">Destinatários listas podem ser criadas a partir de mensagens a usuários ou entradas da lista de distribuição em um contêiner de catálogo de endereços ou algo isolado.</span><span class="sxs-lookup"><span data-stu-id="99b21-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="99b21-125">Algo isolado é destinatários que são criados como entradas temporárias a ser usado apenas para uma única mensagem:/ / Tools.ietf.org ou como entradas a ser adicionado a um catálogo de endereços pessoal.</span><span class="sxs-lookup"><span data-stu-id="99b21-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="99b21-126">O formato de um identificador de entrada únicos e endereço é definido por MAPI.</span><span class="sxs-lookup"><span data-stu-id="99b21-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="99b21-127">Para obter mais informações sobre esses formatos, consulte [Endereços únicos](one-off-addresses.md) e [Únicos identificadores de entrada](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="99b21-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="99b21-128">Você pode permitir que os usuários criem suas listas de destinatário:</span><span class="sxs-lookup"><span data-stu-id="99b21-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="99b21-129">Somente com entradas do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="99b21-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="99b21-130">Somente com entradas únicas.</span><span class="sxs-lookup"><span data-stu-id="99b21-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="99b21-131">Com uma combinação de destinatários do catálogo de endereços e algo isolado.</span><span class="sxs-lookup"><span data-stu-id="99b21-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="99b21-132">**Para criar uma lista de destinatários usando a caixa de diálogo endereço comuns**</span><span class="sxs-lookup"><span data-stu-id="99b21-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="99b21-133">Aloca uma estrutura [ADRPARM](adrparm.md) e um ponteiro para uma estrutura [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="99b21-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="99b21-134">Zero a memória na estrutura de **ADRPARM** e defina o ponteiro **ADRLIST** como NULL.</span><span class="sxs-lookup"><span data-stu-id="99b21-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="99b21-135">Chame [IAddrBook::Address](iaddrbook-address.md) para exibir a caixa de diálogo de endereço e popular a estrutura **ADRPARM** .</span><span class="sxs-lookup"><span data-stu-id="99b21-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="99b21-136">Chame [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passando o ponteiro **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="99b21-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="99b21-137">Essa estrutura irá conter as propriedades de cada um dos destinatários selecionados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="99b21-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="99b21-138">**Para criar uma lista de destinatários programaticamente**</span><span class="sxs-lookup"><span data-stu-id="99b21-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="99b21-139">Aloca uma estrutura **ADRLIST** que contém uma estrutura [ADRENTRY](adrentry.md) para cada um dos destinatários a serem incluídos na lista.</span><span class="sxs-lookup"><span data-stu-id="99b21-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="99b21-140">Verifique cada estrutura **ADRENTRY** grande o suficiente para armazenar cada uma das propriedades exigidas e **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="99b21-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="99b21-141">Para cada destinatário, defina a matriz de valores de propriedade para seu membro **aEntries** na estrutura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="99b21-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="99b21-142">Chame [IMessage::ModifyRecipients](imessage-modifyrecipients.md) com o sinalizador MODRECIP_ADD definido.</span><span class="sxs-lookup"><span data-stu-id="99b21-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    

