---
title: Tabelas de Destinatários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8950623308e85de1d239deb322f65ee867a33ca0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437284"
---
# <a name="recipient-tables"></a><span data-ttu-id="d499c-103">Tabelas de Destinatários</span><span class="sxs-lookup"><span data-stu-id="d499c-103">Recipient Tables</span></span>

  
  
<span data-ttu-id="d499c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d499c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d499c-105">A tabela de destinatários contém informações sobre todos os destinatários de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="d499c-105">The recipient table contains information about all the recipients for a message.</span></span> <span data-ttu-id="d499c-106">Os provedores de armazenamento de mensagens implementam tabelas de destinatários e os aplicativos cliente as usam.</span><span class="sxs-lookup"><span data-stu-id="d499c-106">Message store providers implement recipient tables and client applications use them.</span></span> <span data-ttu-id="d499c-107">Os clientes acessam uma tabela de destinatários fazendo uma chamada para o método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) ou, se o provedor de armazenamento de mensagens a suportar, para o método [IMAPIProp::OpenProperty.](imapiprop-openproperty.md)</span><span class="sxs-lookup"><span data-stu-id="d499c-107">Clients access a recipient table by making a call to the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, or if the message store provider supports it, to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="d499c-108">Os clientes acessam tabelas de destinatários com **OpenProperty** especificando PR_MESSAGE_RECIPIENTS ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) para **a** marca de propriedade e IID_IMAPITable para o identificador da interface.</span><span class="sxs-lookup"><span data-stu-id="d499c-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> <span data-ttu-id="d499c-109">As alterações em uma tabela de destinatários podem ser feitas chamando-se o [método IMessage::ModifyRecipients.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="d499c-109">Changes to a recipient table can be made by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
<span data-ttu-id="d499c-110">As tabelas de destinatários têm um conjunto de colunas diferente, dependendo se a mensagem foi enviada.</span><span class="sxs-lookup"><span data-stu-id="d499c-110">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="d499c-111">As propriedades a seguir compom o conjunto de colunas necessário nas tabelas de destinatários:</span><span class="sxs-lookup"><span data-stu-id="d499c-111">The following properties make up the required column set in recipient tables:</span></span>
  
- <span data-ttu-id="d499c-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d499c-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="d499c-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d499c-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="d499c-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d499c-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="d499c-115">As propriedades opcionais são:</span><span class="sxs-lookup"><span data-stu-id="d499c-115">The optional properties are:</span></span>
  
- <span data-ttu-id="d499c-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d499c-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="d499c-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d499c-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="d499c-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d499c-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="d499c-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d499c-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
<span data-ttu-id="d499c-120">As mensagens enviadas devem incluir essas propriedades adicionais no conjunto de colunas necessário:</span><span class="sxs-lookup"><span data-stu-id="d499c-120">Submitted messages should include these additional properties in their required column set:</span></span>
  
- <span data-ttu-id="d499c-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d499c-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="d499c-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d499c-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="d499c-123">Dependendo da implementação de um provedor, colunas adicionais, como **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) e [ENTRYID](entryid.md), podem estar na tabela.</span><span class="sxs-lookup"><span data-stu-id="d499c-123">Depending on a provider's implementation, additional columns, such as **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and [ENTRYID](entryid.md), might be in the table.</span></span>
  
<span data-ttu-id="d499c-124">Qualquer provedor de repositório de mensagens que ofereça suporte à transmissão de mensagens — conforme indicado pelo bit STORE_SUBMIT_OK sendo definido na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do provedor — deve oferecer suporte para um conjunto específico de restrições em uma implementação de tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="d499c-124">Any message store provider that supports message transmission — as indicated by the STORE_SUBMIT_OK bit being set in the provider's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property — should offer support for a particular set of restrictions in a recipient table implementation.</span></span> <span data-ttu-id="d499c-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span><span class="sxs-lookup"><span data-stu-id="d499c-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span></span> <span data-ttu-id="d499c-126">Somente os operadores iguais e não iguais precisam ter suporte na restrição de propriedade.</span><span class="sxs-lookup"><span data-stu-id="d499c-126">Only the equal and not equal operators need to be supported on the property restriction.</span></span> <span data-ttu-id="d499c-127">Essas restrições devem funcionar com as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="d499c-127">These restrictions must work with the following properties:</span></span>
  
- <span data-ttu-id="d499c-128">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="d499c-128">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="d499c-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d499c-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="d499c-130">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="d499c-130">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="d499c-131">**PR_RESPONSIBILITY**</span><span class="sxs-lookup"><span data-stu-id="d499c-131">**PR_RESPONSIBILITY**</span></span>
    
- <span data-ttu-id="d499c-132">**PR_SPOOLER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="d499c-132">**PR_SPOOLER_STATUS**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d499c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d499c-133">See also</span></span>



[<span data-ttu-id="d499c-134">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="d499c-134">MAPI Tables</span></span>](mapi-tables.md)

