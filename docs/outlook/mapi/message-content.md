---
title: Conteúdo da mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 85bd3f7db53f195295405fb0b02c25f084786a67
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586078"
---
# <a name="message-content"></a><span data-ttu-id="e167a-103">Conteúdo da mensagem</span><span class="sxs-lookup"><span data-stu-id="e167a-103">Message Content</span></span>

  
  
<span data-ttu-id="e167a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e167a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e167a-105">Há duas codificações possíveis para o conteúdo da mensagem: um usando MIME, o outro usando uuencode.</span><span class="sxs-lookup"><span data-stu-id="e167a-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="e167a-106">MIME é a codificação preferencial.</span><span class="sxs-lookup"><span data-stu-id="e167a-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="e167a-107">Além disso, o MAPI define uma propriedade por destinatário, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), que determina se ou não informações TNEF devem ser incluídas em uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="e167a-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="e167a-108">Portanto, há um total de quatro maneiras de codificação de conteúdo da mensagem:</span><span class="sxs-lookup"><span data-stu-id="e167a-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="e167a-109">MIME com TNEF</span><span class="sxs-lookup"><span data-stu-id="e167a-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="e167a-110">MIME sem TNEF</span><span class="sxs-lookup"><span data-stu-id="e167a-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="e167a-111">UUENCODE com TNEF</span><span class="sxs-lookup"><span data-stu-id="e167a-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="e167a-112">UUENCODE sem TNEF</span><span class="sxs-lookup"><span data-stu-id="e167a-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="e167a-113">Como escolher MIME ou uuencode para mensagens de saída não for especificado.</span><span class="sxs-lookup"><span data-stu-id="e167a-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="e167a-114">As seguintes propriedades são excluídas dos TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="e167a-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="e167a-115">Todas as outras propriedades de mensagem transmittable estão incluídas no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="e167a-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="e167a-116">As sugestões a seguir servem para fornecer uma lista de parâmetros que a implementação pode decidir como oferecer suporte a:</span><span class="sxs-lookup"><span data-stu-id="e167a-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="e167a-117">Se deseja codificar usando MIME ou uuencode para mensagens de saída: booleano.</span><span class="sxs-lookup"><span data-stu-id="e167a-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="e167a-118">Conjunto a ser usado para mensagens de saída de caracteres: cadeia de caracteres (copiado diretamente para o parâmetro charset) ou enumeração (traduzido internamente como cadeia de caracteres do conjunto de caracteres).</span><span class="sxs-lookup"><span data-stu-id="e167a-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

