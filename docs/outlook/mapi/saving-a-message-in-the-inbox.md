---
title: Salvar uma mensagem na Caixa de Entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 672a9df55ce711b88451a517a2813c9ad8c599ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407890"
---
# <a name="saving-a-message-in-the-inbox"></a><span data-ttu-id="c8f46-103">Salvar uma mensagem na Caixa de Entrada</span><span class="sxs-lookup"><span data-stu-id="c8f46-103">Saving a Message in the Inbox</span></span>

  
  
<span data-ttu-id="c8f46-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8f46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="c8f46-105">**Para armazenar uma mensagem na Caixa de Entrada sem destinatários**</span><span class="sxs-lookup"><span data-stu-id="c8f46-105">**To store a message in the Inbox without any recipients**</span></span>
  
1. <span data-ttu-id="c8f46-106">Chame [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar o identificador de entrada da Caixa de Entrada.</span><span class="sxs-lookup"><span data-stu-id="c8f46-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="c8f46-107">Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir a Caixa de Entrada e recuperar um ponteiro para ela.</span><span class="sxs-lookup"><span data-stu-id="c8f46-107">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and retrieve a pointer to it.</span></span> 
    
3. <span data-ttu-id="c8f46-108">Chame o método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) da Caixa de Entrada para criar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="c8f46-108">Call the Inbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message.</span></span> 
    
4. <span data-ttu-id="c8f46-109">Chame o método [IMAPIProp::SetProps](imapiprop-setprops.md) da mensagem para adicionar as propriedades **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) e **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c8f46-109">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to add the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) and **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) properties.</span></span> 
    
5. <span data-ttu-id="c8f46-110">Criar cada anexo, definir suas propriedades e salvá-lo.</span><span class="sxs-lookup"><span data-stu-id="c8f46-110">Create each attachment, set its properties, and save it.</span></span> <span data-ttu-id="c8f46-111">Para obter informações detalhadas sobre como adicionar anexos a mensagens, consulte [Criando um anexo de mensagem.](creating-a-message-attachment.md)</span><span class="sxs-lookup"><span data-stu-id="c8f46-111">For detailed information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="c8f46-112">Chame **IMessage::SaveChanges** para salvar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="c8f46-112">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="c8f46-113">Neste ponto, ele aparecerá no índice da Caixa de Entrada.</span><span class="sxs-lookup"><span data-stu-id="c8f46-113">At this point it will appear in the contents table of the Inbox.</span></span> 
    
<span data-ttu-id="c8f46-114">Se você quiser salvar uma mensagem intermitentemente antes de aparecer na tabela de conteúdo da Caixa de Entrada, crie-a em uma pasta oculta, como a pasta raiz da subárvore do IPM, e mova-a para a Caixa de Entrada.</span><span class="sxs-lookup"><span data-stu-id="c8f46-114">If you want to save a message intermittantly before having it appear in the contents table of the Inbox, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the Inbox.</span></span> 
  

