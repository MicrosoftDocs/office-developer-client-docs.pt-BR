---
title: Tabelas de destinatários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cc7635c474b99898d59589f33fcf06cf24697378
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770214"
---
# <a name="recipient-tables"></a><span data-ttu-id="b5846-103">Tabelas de destinatários</span><span class="sxs-lookup"><span data-stu-id="b5846-103">Recipient Tables</span></span>

  
  
<span data-ttu-id="b5846-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b5846-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b5846-105">Tabela de destinatário contém informações sobre todos os destinatários de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="b5846-105">The recipient table contains information about all the recipients for a message.</span></span> <span data-ttu-id="b5846-106">Tabelas de destinatários de implementar provedores de armazenamento de mensagens e aplicativos cliente usá-los.</span><span class="sxs-lookup"><span data-stu-id="b5846-106">Message store providers implement recipient tables and client applications use them.</span></span> <span data-ttu-id="b5846-107">Clientes acessar uma tabela de destinatário fazendo uma chamada ao método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) ou se o provedor de armazenamento de mensagem lhe fornecer apoio, para o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="b5846-107">Clients access a recipient table by making a call to the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, or if the message store provider supports it, to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="b5846-108">Os clientes acessar tabelas de destinatários com **OpenProperty** especificando **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) para a marca de propriedade e IID_IMAPITable para o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="b5846-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> <span data-ttu-id="b5846-109">Podem ser feitas alterações em uma tabela de destinatário, chamando o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="b5846-109">Changes to a recipient table can be made by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
<span data-ttu-id="b5846-110">Tabelas de destinatários têm outra coluna definir dependendo se a mensagem foi enviada.</span><span class="sxs-lookup"><span data-stu-id="b5846-110">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="b5846-111">As seguintes propriedades compõem a coluna necessária definida nas tabelas de destinatário:</span><span class="sxs-lookup"><span data-stu-id="b5846-111">The following properties make up the required column set in recipient tables:</span></span>
  
- <span data-ttu-id="b5846-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b5846-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="b5846-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b5846-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="b5846-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b5846-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="b5846-115">As propriedades opcionais são:</span><span class="sxs-lookup"><span data-stu-id="b5846-115">The optional properties are:</span></span>
  
- <span data-ttu-id="b5846-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b5846-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="b5846-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b5846-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="b5846-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b5846-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="b5846-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b5846-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
<span data-ttu-id="b5846-120">Mensagens enviadas devem incluir essas propriedades adicionais em seu conjunto de coluna necessária:</span><span class="sxs-lookup"><span data-stu-id="b5846-120">Submitted messages should include these additional properties in their required column set:</span></span>
  
- <span data-ttu-id="b5846-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b5846-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="b5846-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b5846-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="b5846-123">Dependendo da implementação de um provedor, colunas adicionais, como **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) e [ENTRYID](entryid.md), podem ser na tabela.</span><span class="sxs-lookup"><span data-stu-id="b5846-123">Depending on a provider's implementation, additional columns, such as **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and [ENTRYID](entryid.md), might be in the table.</span></span>
  
<span data-ttu-id="b5846-124">Provedor de armazenamento de qualquer mensagem que ofereça suporte a transmissão de mensagens — conforme indicado pelo sendo definido na propriedade de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do provedor definido o bit STORE_SUBMIT_OK — deve oferecer suporte a um determinado conjunto de restrições na implementação de um destinatário de tabela.</span><span class="sxs-lookup"><span data-stu-id="b5846-124">Any message store provider that supports message transmission — as indicated by the STORE_SUBMIT_OK bit being set in the provider's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property — should offer support for a particular set of restrictions in a recipient table implementation.</span></span> <span data-ttu-id="b5846-125">**E**, **ou**, existir e restrições de propriedade estão entre os tipos de restrições que deveriam estar disponíveis para os usuários da tabela de destinatário.</span><span class="sxs-lookup"><span data-stu-id="b5846-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span></span> <span data-ttu-id="b5846-126">Somente os operadores iguais e não iguais precisam oferecer suporte a restrição de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b5846-126">Only the equal and not equal operators need to be supported on the property restriction.</span></span> <span data-ttu-id="b5846-127">Essas restrições devem trabalhar com as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="b5846-127">These restrictions must work with the following properties:</span></span>
  
- <span data-ttu-id="b5846-128">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="b5846-128">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="b5846-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b5846-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="b5846-130">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="b5846-130">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="b5846-131">**PR_RESPONSIBILITY**</span><span class="sxs-lookup"><span data-stu-id="b5846-131">**PR_RESPONSIBILITY**</span></span>
    
- <span data-ttu-id="b5846-132">**PR_SPOOLER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="b5846-132">**PR_SPOOLER_STATUS**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5846-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5846-133">See also</span></span>



[<span data-ttu-id="b5846-134">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="b5846-134">MAPI Tables</span></span>](mapi-tables.md)

