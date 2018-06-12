---
title: Adicionar informações de processamento de texto formatado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b912d81c1413fb40b6ddccc2f54bc393a6b67857
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766134"
---
# <a name="adding-rendering-information-to-formatted-text"></a><span data-ttu-id="99247-103">Adicionar informações de processamento de texto formatado</span><span class="sxs-lookup"><span data-stu-id="99247-103">Adding Rendering Information to Formatted Text</span></span>

  
  
<span data-ttu-id="99247-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99247-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99247-105">Para indicar o local no texto formatado em que um anexo é processado, você deve inserir uma sequência de caracteres de espaço reservado na propriedade de **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="99247-105">To indicate the location in formatted text where an attachment is rendered, you must insert a sequence of placeholder characters in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> <span data-ttu-id="99247-106">A sequência de espaço reservado é composta pelos seguintes caracteres: `\objattph`.</span><span class="sxs-lookup"><span data-stu-id="99247-106">The placeholder sequence is made up of the following characters:  `\objattph`.</span></span>
  
 <span data-ttu-id="99247-107">**Para adicionar informações de renderização ao texto da mensagem formatada**</span><span class="sxs-lookup"><span data-stu-id="99247-107">**To add rendering information to formatted message text**</span></span>
  
- <span data-ttu-id="99247-108">Ao escrever o fluxo de texto à propriedade **PR_RTF_COMPRESSED** da mensagem, insira a sequência de espaço reservado e um caractere de espaço na posição onde o anexo deve ser processado.</span><span class="sxs-lookup"><span data-stu-id="99247-108">When writing the stream of text to the message's **PR_RTF_COMPRESSED** property, insert the placeholder sequence and a space character at the position where the attachment should be rendered.</span></span> 
    
- <span data-ttu-id="99247-109">Defina a propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de cada anexo para um valor numérico.</span><span class="sxs-lookup"><span data-stu-id="99247-109">Set the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property of each attachment to a numeric value.</span></span> <span data-ttu-id="99247-110">O menor valor deve ser atribuído à propriedade **PR_RENDERING_POSITION** do primeiro anexo seja exibido em texto formatado; o valor mais alto para o último anexo.</span><span class="sxs-lookup"><span data-stu-id="99247-110">The lowest value should be assigned to the **PR_RENDERING_POSITION** property of the first attachment to appear in the formatted text; the highest value to the last attachment.</span></span> 
    

