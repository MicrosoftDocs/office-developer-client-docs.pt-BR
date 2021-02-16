---
title: Suporte às responsabilidades do Gateway de Texto Formatado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d5c3480018be399a85ee0bfda7ce1ff9b701cecc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419426"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a><span data-ttu-id="242b1-103">Suporte a texto formatado: responsabilidades do gateway</span><span class="sxs-lookup"><span data-stu-id="242b1-103">Supporting Formatted Text: Gateway Responsibilities</span></span>

  
  
<span data-ttu-id="242b1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="242b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="242b1-105">**Para lidar com o Formato Rich Text para mensagens de saída, gateways**</span><span class="sxs-lookup"><span data-stu-id="242b1-105">**To handle Rich Text Format for outgoing messages, gateways**</span></span>
  
1. <span data-ttu-id="242b1-106">Recupere somente a propriedade de PR_RTF_COMPRESSED **(** [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="242b1-106">Retrieve only a message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property from the message store.</span></span> <span data-ttu-id="242b1-107">A principal vantagem na recuperação apenas da propriedade **PR_RTF_COMPRESSED** é que o texto da mensagem não precisa ser enviado entre máquinas se o gateway e o armazenamento de mensagens existirem em máquinas diferentes.</span><span class="sxs-lookup"><span data-stu-id="242b1-107">The main advantage in retrieving only the **PR_RTF_COMPRESSED** property is that the message text does not need to be sent between machines if the gateway and the message store exist on different machines.</span></span> 
    
2. <span data-ttu-id="242b1-108">Gere o texto da mensagem do texto formatado chamando a função de biblioteca RTF **HrTextFromCompressedRTFStream** ou, se a mensagem estiver armazenada localmente, **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="242b1-108">Generate the message text from the formatted text either by calling the RTF library function **HrTextFromCompressedRTFStream** or, if the message is stored locally, **RTFSync**.</span></span> <span data-ttu-id="242b1-109">O RTF_SYNC_RTF_CHANGED sinalizador deve ser definido na chamada para **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="242b1-109">The RTF_SYNC_RTF_CHANGED flag should be set in the call to **RTFSync**.</span></span> <span data-ttu-id="242b1-110">Para obter mais informações, consulte [RTFSync](rtfsync.md).</span><span class="sxs-lookup"><span data-stu-id="242b1-110">For more information, see [RTFSync](rtfsync.md).</span></span>
    
3. <span data-ttu-id="242b1-111">Faça modificações irreversíveis no texto da mensagem, como soltar caracteres sem suporte.</span><span class="sxs-lookup"><span data-stu-id="242b1-111">Make any irreversible modifications to the message text, such as dropping unsupported characters.</span></span> 
    
4. <span data-ttu-id="242b1-112">Verifique se **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) e todas as propriedades Auxilliary RTF estão definidas ou ausentes.</span><span class="sxs-lookup"><span data-stu-id="242b1-112">Ensure that both **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) and all of the RTF auxilliary properties are either set or absent.</span></span>
    
5. <span data-ttu-id="242b1-113">Se alguma modificação tiver sido feita, chame **RTFSync** com os sinalizadores RTF_SYNC_RTF_CHANGED e RTF_SYNC_BODY_CHANGED definidos.</span><span class="sxs-lookup"><span data-stu-id="242b1-113">If any modifications were made, call **RTFSync** with both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags set.</span></span> <span data-ttu-id="242b1-114">**RTFSync** recalculará as propriedades de auxilliary RTF do texto modificado.</span><span class="sxs-lookup"><span data-stu-id="242b1-114">**RTFSync** will recalculate the RTF auxilliary properties from the modified text.</span></span> 
    
6. <span data-ttu-id="242b1-115">Faça qualquer modificação reversa ao texto da mensagem, como inserir os espaço reservados de anexo e executar conversões de página de código não estruturada.</span><span class="sxs-lookup"><span data-stu-id="242b1-115">Make any reversable modifications to the message text, such as inserting attachment placeholders and performing nondestructive code page conversions.</span></span>
    
7. <span data-ttu-id="242b1-116">Envie a mensagem.</span><span class="sxs-lookup"><span data-stu-id="242b1-116">Send the message.</span></span>
    
 <span data-ttu-id="242b1-117">**Para lidar com o Formato Rich Text para mensagens de entrada, gateways**</span><span class="sxs-lookup"><span data-stu-id="242b1-117">**To handle Rich Text Format for incoming messages, gateways**</span></span>
  
1. <span data-ttu-id="242b1-118">Reverte todas as modificações de texto da mensagem que foram feitas diretamente antes de a mensagem ser enviada.</span><span class="sxs-lookup"><span data-stu-id="242b1-118">Reverse any message text modifications that were made directly before the message was sent.</span></span> 
    
2. <span data-ttu-id="242b1-119">Chame **RTFSync** se a mensagem **contiver** as propriedades PR_RTF_COMPRESSED **e PR_BODY** ([PidTagBody).](pidtagbody-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="242b1-119">Call **RTFSync** if the message contains both the **PR_RTF_COMPRESSED** and **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) properties.</span></span> 
    
3. <span data-ttu-id="242b1-120">Atualize a mensagem no armazenamento de mensagens com a **PR_RTF_COMPRESSED** se ela contiver; atualizar com a **PR_BODY** somente se **PR_RTF_COMPRESSED** estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="242b1-120">Update the message in the message store with the **PR_RTF_COMPRESSED** property if the message contains it; update with the **PR_BODY** property only if **PR_RTF_COMPRESSED** is absent.</span></span> 
    
4. <span data-ttu-id="242b1-121">Descarte **PR_BODY** se a mensagem contiver essa propriedade e **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="242b1-121">Discard **PR_BODY** if the message contains both this property and **PR_RTF_COMPRESSED**.</span></span>
    
<span data-ttu-id="242b1-122">Os gateways **chamam RTFSync** para evitar a transmissão do texto da mensagem e do texto formatado se o armazenamento de mensagens estiver em um computador diferente.</span><span class="sxs-lookup"><span data-stu-id="242b1-122">Gateways call **RTFSync** to avoid transmitting both the message text and formatted text if the message store is on a different machine.</span></span> <span data-ttu-id="242b1-123">Se o gateway for local, ele poderá definir as duas propriedades e permitir que o armazenamento de mensagens realize a sincronização.</span><span class="sxs-lookup"><span data-stu-id="242b1-123">If the gateway is local, it can set both properties and allow the message store to perform the synchronization.</span></span> 
  

