---
title: Fornecer relatórios de leitura e não leitura para provedores do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8e2552cbeaf528de634c39a5ebd175a2615782b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594436"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a><span data-ttu-id="e4282-103">Fornecer relatórios de leitura e não leitura para provedores do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="e4282-103">Providing Read and Nonread Reports for Message Store Providers</span></span>

  
  
<span data-ttu-id="e4282-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4282-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4282-105">Se um provedor de armazenamento de mensagem pode receber mensagens, ela é necessária para oferecer suporte a relatórios de leitura e nonread relatórios de mensagens recebidas pelo provedor de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e4282-105">If a message store provider can receive messages, it is required to support read reports and nonread reports of messages received by the message store provider.</span></span> <span data-ttu-id="e4282-106">Se uma mensagem recebida contém a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) e o valor da propriedade é TRUE, o armazenamento de mensagens deve enviar uma mensagem de notificação para o remetente quando o usuário abre a mensagem, indicando que a mensagem foi lido.</span><span class="sxs-lookup"><span data-stu-id="e4282-106">If a received message contains the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and that property's value is TRUE, the message store should send a notification message to the sender when the user opens the message, indicating that the message has been read.</span></span> <span data-ttu-id="e4282-107">Da mesma forma, se o usuário excluir a mensagem antes de abri-lo, o armazenamento de mensagens deve emitir uma resposta ao remetente, indicando que a mensagem não foi lido.</span><span class="sxs-lookup"><span data-stu-id="e4282-107">Similarly, if the user deletes the message before opening it, the message store should issue a reply to the sender indicating that the message was not read.</span></span>
  
<span data-ttu-id="e4282-108">Emitir esses relatórios é uma questão de criação de um [IMessage: IMAPIProp](imessageimapiprop.md) objeto, preenchendo as propriedades relevantes na mensagem e enviá-lo para o spooler MAPI como se a mensagem tinha originada com o usuário.</span><span class="sxs-lookup"><span data-stu-id="e4282-108">Issuing these reports is a matter of creating an [IMessage : IMAPIProp](imessageimapiprop.md) object, filling out the relevant properties on the message, and submitting it to the MAPI spooler as if the message had originated with the user.</span></span> <span data-ttu-id="e4282-109">O método [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) pode ser usado para que isso.</span><span class="sxs-lookup"><span data-stu-id="e4282-109">The [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method can be used for this.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e4282-110">Especial deve ter cuidado quando um armazenamento de mensagens faz cópias de uma mensagem não lida com pendentes lidas ou nonread relatórios.</span><span class="sxs-lookup"><span data-stu-id="e4282-110">Special care must be taken when a message store makes copies of an unread message with pending read or nonread reports.</span></span> <span data-ttu-id="e4282-111">Esses relatórios não deverão ser gerados quando os usuários ler alguma cópia de uma mensagem para o qual os relatórios tiverem sido solicitados.</span><span class="sxs-lookup"><span data-stu-id="e4282-111">Such reports should not be generated when users read any copies of a message for which reports have been requested.</span></span> <span data-ttu-id="e4282-112">Quando você faz uma cópia de uma mensagem, o provedor de armazenamento de mensagem deve incluir os sinalizadores CLEAR_RN_PENDING e CLEAR_NRN_PENDING em suas chamadas para [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) e [IMessage::SetReadFlag](imessage-setreadflag.md).</span><span class="sxs-lookup"><span data-stu-id="e4282-112">When making a copy of such a message, the message store provider should include the CLEAR_RN_PENDING and CLEAR_NRN_PENDING flags in its calls to [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) and [IMessage::SetReadFlag](imessage-setreadflag.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e4282-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4282-113">See also</span></span>



[<span data-ttu-id="e4282-114">Recursos de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="e4282-114">Message Store Features</span></span>](message-store-features.md)

