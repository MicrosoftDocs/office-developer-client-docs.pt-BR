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
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325750"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="80326-103">Gravar texto formatado sem compactação</span><span class="sxs-lookup"><span data-stu-id="80326-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="80326-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80326-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80326-105">Ao se preparar para enviar uma mensagem com texto formatado, defina a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) da mensagem como texto compactado ou descompactado.</span><span class="sxs-lookup"><span data-stu-id="80326-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="80326-106">A gravação de texto compactado na propriedade **PR_RTF_COMPRESSED** é uma operação muito intensa da CPU e pode afetar seriamente o desempenho.</span><span class="sxs-lookup"><span data-stu-id="80326-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="80326-107">Para melhorar o desempenho do envio de mensagens formatadas, você pode:</span><span class="sxs-lookup"><span data-stu-id="80326-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="80326-108">Atualize a CPU, uma solução que nem sempre é plausível.</span><span class="sxs-lookup"><span data-stu-id="80326-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="80326-109">Ou</span><span class="sxs-lookup"><span data-stu-id="80326-109">Or -</span></span>
    
- <span data-ttu-id="80326-110">Escreva texto descompactado na propriedade **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="80326-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="80326-111">O procedimento para configurar **PR_RTF_COMPRESSED** com texto descompactado é o mesmo que para configurá-lo com texto compactado, com uma exceção.</span><span class="sxs-lookup"><span data-stu-id="80326-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="80326-112">Ao chamar [WrapCompressedRTFStream](wrapcompressedrtfstream.md), defina o sinalizador STORE_UNCOMPRESSED_RTF no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="80326-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="80326-113">A configuração do texto descompactado tem a desvantagem de que aumenta o tamanho das mensagens.</span><span class="sxs-lookup"><span data-stu-id="80326-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

