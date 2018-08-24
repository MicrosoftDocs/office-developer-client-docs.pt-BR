---
title: Processar uma mensagem enviada
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bd86e5d06e868ebc540d8eb779c059089045cd8a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574178"
---
# <a name="processing-a-sent-message"></a><span data-ttu-id="82e12-103">Processar uma mensagem enviada</span><span class="sxs-lookup"><span data-stu-id="82e12-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="82e12-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82e12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82e12-105">Mensagens, de saída após terem sido enviados, poderá ser deixada na caixa pasta, movida para uma pasta designada para armazenar mensagens enviadas ou excluídas de saída.</span><span class="sxs-lookup"><span data-stu-id="82e12-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="82e12-106">O tipo de processamento depende se você definiu a mensagem repositório de propriedades:</span><span class="sxs-lookup"><span data-stu-id="82e12-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="82e12-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82e12-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="82e12-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82e12-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="82e12-109">**PR_DELETE_AFTER_SUBMIT** é uma propriedade booleana, defina como TRUE se as mensagens devem ser excluídas depois que eles forem enviados e FALSE caso contrário.</span><span class="sxs-lookup"><span data-stu-id="82e12-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="82e12-110">**PR_SENTMAIL_ENTRYID** é o identificador de entrada de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="82e12-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="82e12-111">Quando essa propriedade é definida, você deve mover as mensagens enviadas para a pasta representada por esse identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="82e12-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="82e12-112">Normalmente, as mensagens salvas têm a identidade do repositório de mensagem do último ou provedor de enviá-los de transporte.</span><span class="sxs-lookup"><span data-stu-id="82e12-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="82e12-113">Uma delas ou a outra ou nenhuma dessas propriedades deve ser definido, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="82e12-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="82e12-114">No entanto, se você definir **PR_SENTMAIL_ENTRYID**, ele deve conter um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="82e12-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="82e12-115">A tabela a seguir descreve como essas propriedades afetam o que fazer com que as mensagens enviadas.</span><span class="sxs-lookup"><span data-stu-id="82e12-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="82e12-116">Se nenhuma propriedade for definida:</span><span class="sxs-lookup"><span data-stu-id="82e12-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="82e12-117">Deixe a mensagem na pasta da qual ela foi enviada (normalmente a caixa de saída).</span><span class="sxs-lookup"><span data-stu-id="82e12-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="82e12-118">Se estiver definido **PR_SENTMAIL_ENTRYID** :</span><span class="sxs-lookup"><span data-stu-id="82e12-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="82e12-119">Move a mensagem para a pasta indicada.</span><span class="sxs-lookup"><span data-stu-id="82e12-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="82e12-120">Se estiver definido **PR_DELETE_AFTER_SUBMIT** :</span><span class="sxs-lookup"><span data-stu-id="82e12-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="82e12-121">Exclua a mensagem.</span><span class="sxs-lookup"><span data-stu-id="82e12-121">Delete the message.</span></span>  <br/> |
   

