---
title: Escrevendo texto formatado descompactado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426321"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="3822c-103">Escrevendo texto formatado descompactado</span><span class="sxs-lookup"><span data-stu-id="3822c-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="3822c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3822c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3822c-105">Ao se preparar para enviar uma mensagem com texto formatado, de definir a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)da mensagem como texto compactado ou descompactado.</span><span class="sxs-lookup"><span data-stu-id="3822c-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="3822c-106">Escrever texto compactado na propriedade **PR_RTF_COMPRESSED** é uma operação muito intensa da CPU e pode afetar significativamente o desempenho.</span><span class="sxs-lookup"><span data-stu-id="3822c-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="3822c-107">Para melhorar o desempenho do envio de mensagens formatadas:</span><span class="sxs-lookup"><span data-stu-id="3822c-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="3822c-108">Atualize a CPU, uma solução que nem sempre é um problema.</span><span class="sxs-lookup"><span data-stu-id="3822c-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="3822c-109">Ou -</span><span class="sxs-lookup"><span data-stu-id="3822c-109">Or -</span></span>
    
- <span data-ttu-id="3822c-110">Escreva texto descompactado na **PR_RTF_COMPRESSED** propriedade.</span><span class="sxs-lookup"><span data-stu-id="3822c-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="3822c-111">O procedimento para definir **PR_RTF_COMPRESSED** com texto descompactado é o mesmo para defini-lo com texto compactado, com uma exceção.</span><span class="sxs-lookup"><span data-stu-id="3822c-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="3822c-112">Ao chamar [WrapCompressedRTFStream](wrapcompressedrtfstream.md), defina o STORE_UNCOMPRESSED_RTF no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="3822c-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="3822c-113">Definir texto não compactado tem a desvantagem de aumentar o tamanho das mensagens.</span><span class="sxs-lookup"><span data-stu-id="3822c-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

