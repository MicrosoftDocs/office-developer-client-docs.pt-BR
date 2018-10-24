---
title: Gravar texto formatado sem compactação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d34168743926681ee7169a593e302755b193aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577041"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="6d068-103">Gravar texto formatado sem compactação</span><span class="sxs-lookup"><span data-stu-id="6d068-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="6d068-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d068-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d068-105">Durante a preparação enviar uma mensagem com o texto formatado, tanto definir a propriedade de **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) da mensagem como texto compactado ou descompactado.</span><span class="sxs-lookup"><span data-stu-id="6d068-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="6d068-106">Gravar texto compactado na propriedade **PR_RTF_COMPRESSED** é uma operação intensiva na CPU exato e pode afetar significativamente o desempenho.</span><span class="sxs-lookup"><span data-stu-id="6d068-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="6d068-107">Para melhorar o desempenho do envio de mensagens formatadas, seja:</span><span class="sxs-lookup"><span data-stu-id="6d068-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="6d068-108">Atualize a CPU, uma solução que nem sempre é plausível.</span><span class="sxs-lookup"><span data-stu-id="6d068-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="6d068-109">Ou -</span><span class="sxs-lookup"><span data-stu-id="6d068-109">Or -</span></span>
    
- <span data-ttu-id="6d068-110">Escreva o texto descompactado na propriedade **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="6d068-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="6d068-111">O procedimento para definir **PR_RTF_COMPRESSED** com texto descompactado é a mesma que para defini-la com texto compactado, com uma exceção.</span><span class="sxs-lookup"><span data-stu-id="6d068-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="6d068-112">Ao chamar [WrapCompressedRTFStream](wrapcompressedrtfstream.md), defina o sinalizador STORE_UNCOMPRESSED_RTF no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="6d068-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="6d068-113">Definindo texto descompactado tem a desvantagem em que ela aumenta o tamanho das mensagens.</span><span class="sxs-lookup"><span data-stu-id="6d068-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

