---
title: Suporte a responsabilidades de gateway de texto formatado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d5c3480018be399a85ee0bfda7ce1ff9b701cecc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327416"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a><span data-ttu-id="56ef2-103">Suporte a texto formatado: responsabilidades do gateway</span><span class="sxs-lookup"><span data-stu-id="56ef2-103">Supporting Formatted Text: Gateway Responsibilities</span></span>

  
  
<span data-ttu-id="56ef2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56ef2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="56ef2-105">**Para lidar com o formato Rich Text para mensagens de saída, gateways**</span><span class="sxs-lookup"><span data-stu-id="56ef2-105">**To handle Rich Text Format for outgoing messages, gateways**</span></span>
  
1. <span data-ttu-id="56ef2-106">Recupere somente a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) de uma mensagem do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="56ef2-106">Retrieve only a message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property from the message store.</span></span> <span data-ttu-id="56ef2-107">A principal vantagem em recuperar apenas a propriedade **PR_RTF_COMPRESSED** é que o texto da mensagem não precisará ser enviado entre as máquinas se o gateway e o repositório de mensagens existirem em máquinas diferentes.</span><span class="sxs-lookup"><span data-stu-id="56ef2-107">The main advantage in retrieving only the **PR_RTF_COMPRESSED** property is that the message text does not need to be sent between machines if the gateway and the message store exist on different machines.</span></span> 
    
2. <span data-ttu-id="56ef2-108">Gere o texto da mensagem do texto formatado chamando a função de biblioteca RTF **HrTextFromCompressedRTFStream** ou, se a mensagem for armazenada localmente, **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="56ef2-108">Generate the message text from the formatted text either by calling the RTF library function **HrTextFromCompressedRTFStream** or, if the message is stored locally, **RTFSync**.</span></span> <span data-ttu-id="56ef2-109">O sinalizador RTF_SYNC_RTF_CHANGED deve ser definido na chamada a **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="56ef2-109">The RTF_SYNC_RTF_CHANGED flag should be set in the call to **RTFSync**.</span></span> <span data-ttu-id="56ef2-110">Para obter mais informações, consulte [RTFSync](rtfsync.md).</span><span class="sxs-lookup"><span data-stu-id="56ef2-110">For more information, see [RTFSync](rtfsync.md).</span></span>
    
3. <span data-ttu-id="56ef2-111">Faça quaisquer modificações irreversível no texto da mensagem, como descartar os caracteres sem suporte.</span><span class="sxs-lookup"><span data-stu-id="56ef2-111">Make any irreversible modifications to the message text, such as dropping unsupported characters.</span></span> 
    
4. <span data-ttu-id="56ef2-112">Certifique-se de que o **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) e todas as propriedades RTF auxilliary estão definidas ou ausentes.</span><span class="sxs-lookup"><span data-stu-id="56ef2-112">Ensure that both **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) and all of the RTF auxilliary properties are either set or absent.</span></span>
    
5. <span data-ttu-id="56ef2-113">Se alguma modificação tiver sido feita, chame **RTFSync** com os sinalizadores RTF_SYNC_RTF_CHANGED e RTF_SYNC_BODY_CHANGED definidos.</span><span class="sxs-lookup"><span data-stu-id="56ef2-113">If any modifications were made, call **RTFSync** with both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags set.</span></span> <span data-ttu-id="56ef2-114">**RTFSync** recalculará as propriedades auxilliary rtf do texto modificado.</span><span class="sxs-lookup"><span data-stu-id="56ef2-114">**RTFSync** will recalculate the RTF auxilliary properties from the modified text.</span></span> 
    
6. <span data-ttu-id="56ef2-115">Faça quaisquer modificações revertidas no texto da mensagem, como inserir espaços reservados de anexo e executar conversões de página de código não destrutivas.</span><span class="sxs-lookup"><span data-stu-id="56ef2-115">Make any reversable modifications to the message text, such as inserting attachment placeholders and performing nondestructive code page conversions.</span></span>
    
7. <span data-ttu-id="56ef2-116">Envie a mensagem.</span><span class="sxs-lookup"><span data-stu-id="56ef2-116">Send the message.</span></span>
    
 <span data-ttu-id="56ef2-117">**Para lidar com o formato Rich Text para mensagens de entrada, gateways**</span><span class="sxs-lookup"><span data-stu-id="56ef2-117">**To handle Rich Text Format for incoming messages, gateways**</span></span>
  
1. <span data-ttu-id="56ef2-118">Reverte quaisquer modificações de texto de mensagem feitas diretamente antes da mensagem ser enviada.</span><span class="sxs-lookup"><span data-stu-id="56ef2-118">Reverse any message text modifications that were made directly before the message was sent.</span></span> 
    
2. <span data-ttu-id="56ef2-119">Chame **RTFSync** se a mensagem contiver as propriedades **PR_RTF_COMPRESSED** e **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="56ef2-119">Call **RTFSync** if the message contains both the **PR_RTF_COMPRESSED** and **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) properties.</span></span> 
    
3. <span data-ttu-id="56ef2-120">Atualize a mensagem no repositório de mensagens com a propriedade **PR_RTF_COMPRESSED** se a mensagem contiver; atualização com a propriedade **PR_BODY** somente se **PR_RTF_COMPRESSED** estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="56ef2-120">Update the message in the message store with the **PR_RTF_COMPRESSED** property if the message contains it; update with the **PR_BODY** property only if **PR_RTF_COMPRESSED** is absent.</span></span> 
    
4. <span data-ttu-id="56ef2-121">DesCartar **PR_BODY** se a mensagem contiver essa propriedade e **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="56ef2-121">Discard **PR_BODY** if the message contains both this property and **PR_RTF_COMPRESSED**.</span></span>
    
<span data-ttu-id="56ef2-122">Os gateways chamam **RTFSync** para evitar a transmissão do texto da mensagem e o texto formatado se o repositório de mensagens estiver em um computador diferente.</span><span class="sxs-lookup"><span data-stu-id="56ef2-122">Gateways call **RTFSync** to avoid transmitting both the message text and formatted text if the message store is on a different machine.</span></span> <span data-ttu-id="56ef2-123">Se o gateway for local, ele poderá definir ambas as propriedades e permitir que o repositório de mensagens realize a sincronização.</span><span class="sxs-lookup"><span data-stu-id="56ef2-123">If the gateway is local, it can set both properties and allow the message store to perform the synchronization.</span></span> 
  

