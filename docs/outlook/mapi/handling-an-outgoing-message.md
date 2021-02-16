---
title: Manipular uma mensagem de saída
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 07785ac82c41108b4333b3c370e3d2f5bfd1426a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407624"
---
# <a name="handling-an-outgoing-message"></a><span data-ttu-id="23781-103">Manipular uma mensagem de saída</span><span class="sxs-lookup"><span data-stu-id="23781-103">Handling an outgoing message</span></span>

<span data-ttu-id="23781-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23781-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23781-105">Uma mensagem de saída é uma mensagem que pode ser enviada para um ou mais destinatários em um ou mais sistemas de mensagens ou ser postada em uma pasta em um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="23781-105">An outgoing message is a message that can be sent to one or more recipients across one or more messaging systems or be posted to a folder in a message store.</span></span>
  
## <a name="create-and-send-an-outgoing-message"></a><span data-ttu-id="23781-106">Criar e enviar uma mensagem de saída</span><span class="sxs-lookup"><span data-stu-id="23781-106">Create and send an outgoing message</span></span>
  
1. <span data-ttu-id="23781-107">Abra o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="23781-107">Open the default message store.</span></span> <span data-ttu-id="23781-108">Para obter mais informações, consulte [Abrindo um armazenamento de mensagens](opening-a-message-store.md) e abrindo o armazenamento de mensagens [padrão.](opening-the-default-message-store.md)</span><span class="sxs-lookup"><span data-stu-id="23781-108">For more information, see [Opening a Message Store](opening-a-message-store.md) and [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="23781-109">Abra a pasta Caixa de Saída.</span><span class="sxs-lookup"><span data-stu-id="23781-109">Open the Outbox folder.</span></span> <span data-ttu-id="23781-110">Para obter mais informações, consulte [Abrindo uma pasta do armazenamento de mensagens.](opening-a-message-store-folder.md)</span><span class="sxs-lookup"><span data-stu-id="23781-110">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="23781-111">Chame o método **IMAPIFolder::CreateMessage** da pasta outbox para criar a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="23781-111">Call the Outbox folder's **IMAPIFolder::CreateMessage** method to create the new message.</span></span> <span data-ttu-id="23781-112">Para obter mais informações, [consulte IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span><span class="sxs-lookup"><span data-stu-id="23781-112">For more information, see [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span></span>
    
4. <span data-ttu-id="23781-113">Crie uma lista de destinatários com um ou mais destinatários resolvidos.</span><span class="sxs-lookup"><span data-stu-id="23781-113">Create a recipient list with one or more resolved recipients.</span></span> <span data-ttu-id="23781-114">Para obter mais informações, consulte [Criando uma lista de destinatários.](creating-a-recipient-list.md)</span><span class="sxs-lookup"><span data-stu-id="23781-114">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
5. <span data-ttu-id="23781-115">Opcionalmente, adicione um assunto.</span><span class="sxs-lookup"><span data-stu-id="23781-115">Optionally, add a subject.</span></span> <span data-ttu-id="23781-116">Para obter mais informações, consulte [Criando um assunto de mensagem.](creating-a-message-subject.md)</span><span class="sxs-lookup"><span data-stu-id="23781-116">For more information, see [Creating a Message Subject](creating-a-message-subject.md).</span></span>
    
6. <span data-ttu-id="23781-117">Adicione o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="23781-117">Add the message text.</span></span> <span data-ttu-id="23781-118">Para obter mais informações, consulte [Criando texto da mensagem.](creating-message-text.md)</span><span class="sxs-lookup"><span data-stu-id="23781-118">For more information, see [Creating Message Text](creating-message-text.md).</span></span>
    
7. <span data-ttu-id="23781-119">Se o texto da mensagem estiver formatado, adicione informações de renderização.</span><span class="sxs-lookup"><span data-stu-id="23781-119">If the message text is formatted, add rendering information.</span></span> <span data-ttu-id="23781-120">Para obter mais informações, consulte [Adicionando informações de renderização ao texto formatado.](adding-rendering-information-to-formatted-text.md)</span><span class="sxs-lookup"><span data-stu-id="23781-120">For more information, see [Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md).</span></span>
    
8. <span data-ttu-id="23781-121">Opcionalmente, adicione um ou mais anexos.</span><span class="sxs-lookup"><span data-stu-id="23781-121">Optionally, add one or more attachments.</span></span> <span data-ttu-id="23781-122">Para obter mais informações, consulte [Criando um anexo de mensagem.](creating-a-message-attachment.md)</span><span class="sxs-lookup"><span data-stu-id="23781-122">For more information, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
9. <span data-ttu-id="23781-123">Definir outras propriedades de mensagem conforme desejado e salvar e enviar a mensagem chamando **IMessage::SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="23781-123">Set other message properties as desired and then save and send the message by calling **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="23781-124">Para obter mais informações, consulte [IMessage::SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="23781-124">For more information, see [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span>
    
10. <span data-ttu-id="23781-125">Exclua a mensagem enviada se a propriedade **PR \_ DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) estiver definida como TRUE ou movê-la para a pasta identificada pela propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="23781-125">Delete the sent message if the **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property is set to TRUE or move it to the folder identified by the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="23781-126">Para obter mais informações, [consulte Processing a Sent Message](processing-a-sent-message.md).</span><span class="sxs-lookup"><span data-stu-id="23781-126">For more information, see [Processing a Sent Message](processing-a-sent-message.md).</span></span>
    
<span data-ttu-id="23781-127">Se você quiser salvar intermitentemente a mensagem antes de enviá-la, chame o método [IMAPIProp::SaveChanges da](imapiprop-savechanges.md) mensagem.</span><span class="sxs-lookup"><span data-stu-id="23781-127">If you want to intermittantly save the message before sending it, call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="23781-128">Para obter mais informações, consulte, [Salvar uma mensagem](saving-a-message.md) ou enviar uma [mensagem.](sending-a-message.md)</span><span class="sxs-lookup"><span data-stu-id="23781-128">For more information, see, [Saving a Message](saving-a-message.md) or [Sending a Message](sending-a-message.md).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="23781-129">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="23781-129">In this section</span></span>

- <span data-ttu-id="23781-130">[Criando uma lista de](creating-a-recipient-list.md)destinatários: descreve como criar uma lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="23781-130">[Creating a Recipient List](creating-a-recipient-list.md): Describes how to create a recipient list.</span></span>
    
- <span data-ttu-id="23781-131">[Criando um assunto de](creating-a-message-subject.md)mensagem: descreve como criar um assunto opcional para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="23781-131">[Creating a Message Subject](creating-a-message-subject.md): Describes how to create an optional subject for a message.</span></span>
    
- <span data-ttu-id="23781-132">[Criando texto da](creating-message-text.md)mensagem: descreve como criar o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="23781-132">[Creating Message Text](creating-message-text.md): Describes how to create message text.</span></span>
    
- <span data-ttu-id="23781-133">[Adicionando informações de renderização ao texto formatado:](adding-rendering-information-to-formatted-text.md)descreve onde em texto formatado um anexo deve ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="23781-133">[Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md): Describes where in formatted text an attachment is to be rendered.</span></span>
    
- <span data-ttu-id="23781-134">[Criando um anexo de](creating-a-message-attachment.md)mensagem: descreve como criar anexos.</span><span class="sxs-lookup"><span data-stu-id="23781-134">[Creating a Message Attachment](creating-a-message-attachment.md): Describes how to create attachments.</span></span>
    
- <span data-ttu-id="23781-135">[Salvar uma mensagem:](saving-a-message.md)descreve como os clientes salvam mensagens.</span><span class="sxs-lookup"><span data-stu-id="23781-135">[Saving a Message](saving-a-message.md): Describes how clients save messages.</span></span>
    
- <span data-ttu-id="23781-136">[Enviar uma mensagem:](sending-a-message.md)descreve como enviar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="23781-136">[Sending a Message](sending-a-message.md): Describes how to send a message.</span></span>
    
- <span data-ttu-id="23781-137">[Processing a Sent Message](processing-a-sent-message.md): Describes how to sent messages can be processed.</span><span class="sxs-lookup"><span data-stu-id="23781-137">[Processing a Sent Message](processing-a-sent-message.md): Describes how to sent messages can be processed.</span></span>
    

