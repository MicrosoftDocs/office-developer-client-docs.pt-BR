---
title: Fornecer relatórios de leitura e não leitura para provedores de repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 96546d3d766af398ff7acb50f4fc3a479b5668b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432335"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a><span data-ttu-id="11522-103">Fornecer relatórios de leitura e não leitura para provedores de repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="11522-103">Providing Read and Nonread Reports for Message Store Providers</span></span>

  
  
<span data-ttu-id="11522-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11522-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11522-105">Se um provedor de repositório de mensagens puder receber mensagens, será necessário suportar relatórios de leitura e relatórios não lidos de mensagens recebidas pelo provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="11522-105">If a message store provider can receive messages, it is required to support read reports and nonread reports of messages received by the message store provider.</span></span> <span data-ttu-id="11522-106">Se uma mensagem recebida contiver a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) e se o valor dessa propriedade for true, o repositório de mensagens deverá enviar uma mensagem de notificação ao remetente quando o usuário abrir a mensagem, indicando que a mensagem foi lida.</span><span class="sxs-lookup"><span data-stu-id="11522-106">If a received message contains the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and that property's value is TRUE, the message store should send a notification message to the sender when the user opens the message, indicating that the message has been read.</span></span> <span data-ttu-id="11522-107">Da mesma forma, se o usuário excluir a mensagem antes de abri-la, o repositório de mensagens deverá emitir uma resposta para o remetente, indicando que a mensagem não foi lida.</span><span class="sxs-lookup"><span data-stu-id="11522-107">Similarly, if the user deletes the message before opening it, the message store should issue a reply to the sender indicating that the message was not read.</span></span>
  
<span data-ttu-id="11522-108">A emissão desses relatórios é uma questão de criação de um objeto [IMessage: IMAPIProp](imessageimapiprop.md) , o preenchimento das propriedades relevantes na mensagem e o envio ao spooler MAPI como se a mensagem tivesse sido originada com o usuário.</span><span class="sxs-lookup"><span data-stu-id="11522-108">Issuing these reports is a matter of creating an [IMessage : IMAPIProp](imessageimapiprop.md) object, filling out the relevant properties on the message, and submitting it to the MAPI spooler as if the message had originated with the user.</span></span> <span data-ttu-id="11522-109">O método [IMAPISupport:: ReadReceipt](imapisupport-readreceipt.md) pode ser usado para isso.</span><span class="sxs-lookup"><span data-stu-id="11522-109">The [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method can be used for this.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="11522-110">Cuidado especial deve ser feito quando um repositório de mensagens faz cópias de uma mensagem não lida com os relatórios de leitura ou não leitura pendentes.</span><span class="sxs-lookup"><span data-stu-id="11522-110">Special care must be taken when a message store makes copies of an unread message with pending read or nonread reports.</span></span> <span data-ttu-id="11522-111">Esses relatórios não devem ser gerados quando os usuários lêem qualquer cópia de uma mensagem para a qual os relatórios foram solicitados.</span><span class="sxs-lookup"><span data-stu-id="11522-111">Such reports should not be generated when users read any copies of a message for which reports have been requested.</span></span> <span data-ttu-id="11522-112">Ao fazer uma cópia dessa mensagem, o provedor do repositório de mensagens deve incluir os sinalizadores CLEAR_RN_PENDING e CLEAR_NRN_PENDING em suas chamadas para [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) e [IMessage:: SetReadFlag](imessage-setreadflag.md).</span><span class="sxs-lookup"><span data-stu-id="11522-112">When making a copy of such a message, the message store provider should include the CLEAR_RN_PENDING and CLEAR_NRN_PENDING flags in its calls to [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) and [IMessage::SetReadFlag](imessage-setreadflag.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="11522-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="11522-113">See also</span></span>



[<span data-ttu-id="11522-114">Recursos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="11522-114">Message Store Features</span></span>](message-store-features.md)

