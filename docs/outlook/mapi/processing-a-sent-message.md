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
ms.openlocfilehash: 0cea1a1008ecbff698b757d6c67af5c279954656
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770169"
---
# <a name="processing-a-sent-message"></a><span data-ttu-id="54dd7-103">Processar uma mensagem enviada</span><span class="sxs-lookup"><span data-stu-id="54dd7-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="54dd7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="54dd7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="54dd7-105">Mensagens, de saída após terem sido enviados, poderá ser deixada na caixa pasta, movida para uma pasta designada para armazenar mensagens enviadas ou excluídas de saída.</span><span class="sxs-lookup"><span data-stu-id="54dd7-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="54dd7-106">O tipo de processamento depende se você definiu a mensagem repositório de propriedades:</span><span class="sxs-lookup"><span data-stu-id="54dd7-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="54dd7-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="54dd7-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="54dd7-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="54dd7-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="54dd7-109">**PR_DELETE_AFTER_SUBMIT** é uma propriedade booleana, defina como TRUE se as mensagens devem ser excluídas depois que eles forem enviados e FALSE caso contrário.</span><span class="sxs-lookup"><span data-stu-id="54dd7-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="54dd7-110">**PR_SENTMAIL_ENTRYID** é o identificador de entrada de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="54dd7-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="54dd7-111">Quando essa propriedade é definida, você deve mover as mensagens enviadas para a pasta representada por esse identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="54dd7-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="54dd7-112">Normalmente, as mensagens salvas têm a identidade do repositório de mensagem do último ou provedor de enviá-los de transporte.</span><span class="sxs-lookup"><span data-stu-id="54dd7-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="54dd7-113">Uma delas ou a outra ou nenhuma dessas propriedades deve ser definido, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="54dd7-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="54dd7-114">No entanto, se você definir **PR_SENTMAIL_ENTRYID**, ele deve conter um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="54dd7-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="54dd7-115">A tabela a seguir descreve como essas propriedades afetam o que fazer com que as mensagens enviadas.</span><span class="sxs-lookup"><span data-stu-id="54dd7-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54dd7-116">Se nenhuma propriedade for definida:</span><span class="sxs-lookup"><span data-stu-id="54dd7-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="54dd7-117">Deixe a mensagem na pasta da qual ela foi enviada (normalmente a caixa de saída).</span><span class="sxs-lookup"><span data-stu-id="54dd7-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="54dd7-118">Se estiver definido **PR_SENTMAIL_ENTRYID** :</span><span class="sxs-lookup"><span data-stu-id="54dd7-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="54dd7-119">Move a mensagem para a pasta indicada.</span><span class="sxs-lookup"><span data-stu-id="54dd7-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="54dd7-120">Se estiver definido **PR_DELETE_AFTER_SUBMIT** :</span><span class="sxs-lookup"><span data-stu-id="54dd7-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="54dd7-121">Exclua a mensagem.</span><span class="sxs-lookup"><span data-stu-id="54dd7-121">Delete the message.</span></span>  <br/> |
   

