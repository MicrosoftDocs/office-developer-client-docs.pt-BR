---
title: Adicionando informações de renderização ao texto formatado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a67fc7cbb3be5c7a23cb85e60dc33d853614cda2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420609"
---
# <a name="adding-rendering-information-to-formatted-text"></a><span data-ttu-id="e6373-103">Adicionando informações de renderização ao texto formatado</span><span class="sxs-lookup"><span data-stu-id="e6373-103">Adding Rendering Information to Formatted Text</span></span>

  
  
<span data-ttu-id="e6373-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6373-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6373-105">Para indicar o local no texto formatado onde um anexo é renderizado, você deve inserir uma sequência de caracteres de espaço reservado na propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e6373-105">To indicate the location in formatted text where an attachment is rendered, you must insert a sequence of placeholder characters in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> <span data-ttu-id="e6373-106">A sequência de espaço reservado é feita com os seguintes caracteres:  `\objattph` .</span><span class="sxs-lookup"><span data-stu-id="e6373-106">The placeholder sequence is made up of the following characters:  `\objattph`.</span></span>
  
 <span data-ttu-id="e6373-107">**Para adicionar informações de renderização ao texto formatado da mensagem**</span><span class="sxs-lookup"><span data-stu-id="e6373-107">**To add rendering information to formatted message text**</span></span>
  
- <span data-ttu-id="e6373-108">Ao escrever o fluxo de texto  na propriedade PR_RTF_COMPRESSED da mensagem, insira a sequência de espaço reservado e um caractere de espaço na posição onde o anexo deve ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="e6373-108">When writing the stream of text to the message's **PR_RTF_COMPRESSED** property, insert the placeholder sequence and a space character at the position where the attachment should be rendered.</span></span> 
    
- <span data-ttu-id="e6373-109">Definir a **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de cada anexo para um valor numérico.</span><span class="sxs-lookup"><span data-stu-id="e6373-109">Set the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property of each attachment to a numeric value.</span></span> <span data-ttu-id="e6373-110">O valor mais baixo deve ser atribuído **à PR_RENDERING_POSITION** do primeiro anexo a ser exibido no texto formatado; o maior valor para o último anexo.</span><span class="sxs-lookup"><span data-stu-id="e6373-110">The lowest value should be assigned to the **PR_RENDERING_POSITION** property of the first attachment to appear in the formatted text; the highest value to the last attachment.</span></span> 
    

