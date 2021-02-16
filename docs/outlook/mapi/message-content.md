---
title: Conteúdo da Mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c4d2439c06da292c9cc72c1506a1ae4d10c6704f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435457"
---
# <a name="message-content"></a><span data-ttu-id="d0462-103">Conteúdo da Mensagem</span><span class="sxs-lookup"><span data-stu-id="d0462-103">Message Content</span></span>

  
  
<span data-ttu-id="d0462-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0462-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0462-105">Há duas codificações possíveis para o conteúdo da mensagem: uma usando MIME, a outra usando uuencode.</span><span class="sxs-lookup"><span data-stu-id="d0462-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="d0462-106">MIME é a codificação preferida.</span><span class="sxs-lookup"><span data-stu-id="d0462-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="d0462-107">Além disso, o MAPI define uma propriedade por destinatário, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), que rege se as informações TNEF devem ou não ser incluídas em uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="d0462-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="d0462-108">Portanto, há um total de quatro maneiras de codificar o conteúdo da mensagem:</span><span class="sxs-lookup"><span data-stu-id="d0462-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="d0462-109">MIME com TNEF</span><span class="sxs-lookup"><span data-stu-id="d0462-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="d0462-110">MIME sem TNEF</span><span class="sxs-lookup"><span data-stu-id="d0462-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="d0462-111">uuencode com TNEF</span><span class="sxs-lookup"><span data-stu-id="d0462-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="d0462-112">uuencode sem TNEF</span><span class="sxs-lookup"><span data-stu-id="d0462-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="d0462-113">Não é especificado como escolher MIME ou uuencode para mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="d0462-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="d0462-114">As propriedades a seguir são excluídas do TNEF: **\* PR_SENDER_**, **PR_ATTACH_DATA_ \***, **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="d0462-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="d0462-115">Todas as outras propriedades de mensagens transmitíveis são incluídas no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="d0462-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="d0462-116">As sugestões a seguir destinam-se a fornecer uma lista de parâmetros aos quais a implementação pode decidir como dar suporte:</span><span class="sxs-lookup"><span data-stu-id="d0462-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="d0462-117">Se deve codificar usando MIME ou uuencode para mensagens de saída: booleano.</span><span class="sxs-lookup"><span data-stu-id="d0462-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="d0462-118">Conjunto de caracteres a ser usado para mensagens de saída: cadeia de caracteres (copiada diretamente para o parâmetro charset) ou enumeração (convertida internamente em cadeia de caracteres charset).</span><span class="sxs-lookup"><span data-stu-id="d0462-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

