---
title: Texto formatado Gateway responsabilidades de suporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d369093589ffad03bf087b02905c443cf6f46c34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564266"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a><span data-ttu-id="7f8e3-103">Suporte a texto formatado: responsabilidades do gateway</span><span class="sxs-lookup"><span data-stu-id="7f8e3-103">Supporting Formatted Text: Gateway Responsibilities</span></span>

  
  
<span data-ttu-id="7f8e3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f8e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="7f8e3-105">**Lidar com formato Rich Text para mensagens de saída, gateways**</span><span class="sxs-lookup"><span data-stu-id="7f8e3-105">**To handle Rich Text Format for outgoing messages, gateways**</span></span>
  
1. <span data-ttu-id="7f8e3-106">Recupere somente as propriedades da mensagem **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) a partir do armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="7f8e3-106">Retrieve only a message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property from the message store.</span></span> <span data-ttu-id="7f8e3-107">A principal vantagem em recuperar apenas a propriedade **PR_RTF_COMPRESSED** é que o texto da mensagem não precisa ser enviadas entre máquinas se o gateway e o armazenamento de mensagens existirem em máquinas diferentes.</span><span class="sxs-lookup"><span data-stu-id="7f8e3-107">The main advantage in retrieving only the **PR_RTF_COMPRESSED** property is that the message text does not need to be sent between machines if the gateway and the message store exist on different machines.</span></span> 
    
2. <span data-ttu-id="7f8e3-108">Gerar o texto da mensagem de texto formatado ou chamando-se a função de biblioteca RTF **HrTextFromCompressedRTFStream** ou, se a mensagem é armazenada localmente, **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="7f8e3-108">Generate the message text from the formatted text either by calling the RTF library function **HrTextFromCompressedRTFStream** or, if the message is stored locally, **RTFSync**.</span></span> <span data-ttu-id="7f8e3-109">O sinalizador RTF_SYNC_RTF_CHANGED deve ser definido na chamada a **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="7f8e3-109">The RTF_SYNC_RTF_CHANGED flag should be set in the call to **RTFSync**.</span></span> <span data-ttu-id="7f8e3-110">Para obter mais informações, consulte [RTFSync](rtfsync.md).</span><span class="sxs-lookup"><span data-stu-id="7f8e3-110">For more information, see [RTFSync](rtfsync.md).</span></span>
    
3. <span data-ttu-id="7f8e3-111">Fazer quaisquer modificações irreversíveis o texto da mensagem, como o descarte de caracteres não suportados.</span><span class="sxs-lookup"><span data-stu-id="7f8e3-111">Make any irreversible modifications to the message text, such as dropping unsupported characters.</span></span> 
    
4. <span data-ttu-id="7f8e3-112">Certifique-se de que **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) e todas as propriedades de auxilliary RTF são definidos ou ausente.</span><span class="sxs-lookup"><span data-stu-id="7f8e3-112">Ensure that both **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) and all of the RTF auxilliary properties are either set or absent.</span></span>
    
5. <span data-ttu-id="7f8e3-113">Se quaisquer modificações foram feitas, chame **RTFSync** com o conjunto de sinalizadores de RTF_SYNC_RTF_CHANGED e RTF_SYNC_BODY_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="7f8e3-113">If any modifications were made, call **RTFSync** with both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags set.</span></span> <span data-ttu-id="7f8e3-114">**RTFSync** recalcule as propriedades de auxilliary RTF do texto modificado.</span><span class="sxs-lookup"><span data-stu-id="7f8e3-114">**RTFSync** will recalculate the RTF auxilliary properties from the modified text.</span></span> 
    
6. <span data-ttu-id="7f8e3-115">Fazer quaisquer modificações reversable o texto da mensagem, como a inserção de espaços reservados de anexo e executar conversões de página de código não destrutiva.</span><span class="sxs-lookup"><span data-stu-id="7f8e3-115">Make any reversable modifications to the message text, such as inserting attachment placeholders and performing nondestructive code page conversions.</span></span>
    
7. <span data-ttu-id="7f8e3-116">Envie a mensagem.</span><span class="sxs-lookup"><span data-stu-id="7f8e3-116">Send the message.</span></span>
    
 <span data-ttu-id="7f8e3-117">**Lidar com formato Rich Text para mensagens de entrada, gateways**</span><span class="sxs-lookup"><span data-stu-id="7f8e3-117">**To handle Rich Text Format for incoming messages, gateways**</span></span>
  
1. <span data-ttu-id="7f8e3-118">Reverte quaisquer modificações de texto de mensagem que foram feitas diretamente antes que a mensagem foi enviada.</span><span class="sxs-lookup"><span data-stu-id="7f8e3-118">Reverse any message text modifications that were made directly before the message was sent.</span></span> 
    
2. <span data-ttu-id="7f8e3-119">Se a mensagem contém propriedades de **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) e o **PR_RTF_COMPRESSED** , chame **RTFSync** .</span><span class="sxs-lookup"><span data-stu-id="7f8e3-119">Call **RTFSync** if the message contains both the **PR_RTF_COMPRESSED** and **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) properties.</span></span> 
    
3. <span data-ttu-id="7f8e3-120">Atualize a mensagem no repositório de mensagem com a propriedade **PR_RTF_COMPRESSED** se a mensagem contivê-lo; Atualizar com a propriedade **PR_BODY** somente se **PR_RTF_COMPRESSED** não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="7f8e3-120">Update the message in the message store with the **PR_RTF_COMPRESSED** property if the message contains it; update with the **PR_BODY** property only if **PR_RTF_COMPRESSED** is absent.</span></span> 
    
4. <span data-ttu-id="7f8e3-121">Descarte **PR_BODY** se a mensagem contiver essa propriedade e a **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="7f8e3-121">Discard **PR_BODY** if the message contains both this property and **PR_RTF_COMPRESSED**.</span></span>
    
<span data-ttu-id="7f8e3-122">Gateways chame **RTFSync** para evitar a transmissão de texto da mensagem e o texto formatado se o armazenamento de mensagens estiver em uma máquina diferente.</span><span class="sxs-lookup"><span data-stu-id="7f8e3-122">Gateways call **RTFSync** to avoid transmitting both the message text and formatted text if the message store is on a different machine.</span></span> <span data-ttu-id="7f8e3-123">Se o gateway for local, ele pode definir ambas as propriedades e permitir o armazenamento de mensagens realizar essa sincronização.</span><span class="sxs-lookup"><span data-stu-id="7f8e3-123">If the gateway is local, it can set both properties and allow the message store to perform the synchronization.</span></span> 
  

