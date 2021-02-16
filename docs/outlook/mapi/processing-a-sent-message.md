---
title: Processing a Sent Message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 880731bf204778cde21da6cd9024a3ca86c6f6a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434673"
---
# <a name="processing-a-sent-message"></a><span data-ttu-id="5781a-103">Processing a Sent Message</span><span class="sxs-lookup"><span data-stu-id="5781a-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="5781a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5781a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5781a-105">As mensagens de saída, depois de enviadas, podem ser deixadas na pasta Caixa de Saída, movidas para uma pasta designada para reter mensagens enviadas ou excluídas.</span><span class="sxs-lookup"><span data-stu-id="5781a-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="5781a-106">O tipo de processamento depende de você ter definido ou não as propriedades do armazenamento de mensagens:</span><span class="sxs-lookup"><span data-stu-id="5781a-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="5781a-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5781a-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="5781a-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5781a-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="5781a-109">**PR_DELETE_AFTER_SUBMIT** é uma propriedade Boolean, definida como TRUE se as mensagens devem ser excluídas depois que elas são enviadas e FALSE caso contrário.</span><span class="sxs-lookup"><span data-stu-id="5781a-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="5781a-110">**PR_SENTMAIL_ENTRYID** é o identificador de entrada de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="5781a-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="5781a-111">Quando essa propriedade estiver definida, você deverá mover mensagens enviadas para a pasta representada por esse identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="5781a-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="5781a-112">As mensagens salvas normalmente têm a identidade do último armazenamento de mensagens ou provedor de transporte para enviá-las.</span><span class="sxs-lookup"><span data-stu-id="5781a-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="5781a-113">Uma ou outra, ou nenhuma dessas propriedades deve ser definida, mas não ambas.</span><span class="sxs-lookup"><span data-stu-id="5781a-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="5781a-114">No entanto, se você definir **PR_SENTMAIL_ENTRYID**, ele deverá conter um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="5781a-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="5781a-115">A tabela a seguir descreve como essas propriedades afetam o que você faz com as mensagens enviadas.</span><span class="sxs-lookup"><span data-stu-id="5781a-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5781a-116">Se nenhuma das propriedades for definida:</span><span class="sxs-lookup"><span data-stu-id="5781a-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="5781a-117">Deixe a mensagem na pasta da qual ela foi enviada (normalmente a Caixa de Saída).</span><span class="sxs-lookup"><span data-stu-id="5781a-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="5781a-118">Se **PR_SENTMAIL_ENTRYID** estiver definido:</span><span class="sxs-lookup"><span data-stu-id="5781a-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="5781a-119">Mova a mensagem para a pasta indicada.</span><span class="sxs-lookup"><span data-stu-id="5781a-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="5781a-120">Se **PR_DELETE_AFTER_SUBMIT** estiver definido:</span><span class="sxs-lookup"><span data-stu-id="5781a-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="5781a-121">Exclua a mensagem.</span><span class="sxs-lookup"><span data-stu-id="5781a-121">Delete the message.</span></span>  <br/> |
   

