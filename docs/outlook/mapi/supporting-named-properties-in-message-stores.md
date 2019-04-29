---
title: Suporte a propriedades nomeadas em repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1c73bb5-b44a-4ec6-89e4-0e2228572b2d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7e33c49d1ed211abf70e04a8bd3c06ca62e88572
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434918"
---
# <a name="supporting-named-properties-in-message-stores"></a><span data-ttu-id="f6a3e-103">Suporte a propriedades nomeadas em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="f6a3e-103">Supporting Named Properties in Message Stores</span></span>

  
  
<span data-ttu-id="f6a3e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6a3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6a3e-105">Os objetos Message podem ter propriedades no conjunto de propriedades definidas por MAPI.</span><span class="sxs-lookup"><span data-stu-id="f6a3e-105">Message objects can have properties in them that are not in the set of properties defined by MAPI.</span></span> <span data-ttu-id="f6a3e-106">Essas propriedades podem ser não nomeadas ou nomeadas.</span><span class="sxs-lookup"><span data-stu-id="f6a3e-106">Such properties can be unnamed or named.</span></span> <span data-ttu-id="f6a3e-107">As propriedades sem nome devem residir em um intervalo de identificadores de propriedade definido por MAPI.</span><span class="sxs-lookup"><span data-stu-id="f6a3e-107">Unnamed properties must reside in a range of property identifiers defined by MAPI.</span></span> <span data-ttu-id="f6a3e-108">As propriedades personalizadas nomeadas residem em um intervalo diferente de identificadores de propriedade definidos por MAPI.</span><span class="sxs-lookup"><span data-stu-id="f6a3e-108">Named custom properties reside in a different range of property identifiers defined by MAPI.</span></span> <span data-ttu-id="f6a3e-109">Normalmente, eles são usados por tipos de mensagem personalizados.</span><span class="sxs-lookup"><span data-stu-id="f6a3e-109">They are typically used by custom message types.</span></span> <span data-ttu-id="f6a3e-110">Seu provedor de repositório de mensagens deve oferecer suporte a propriedades nomeadas se for usado como o repositório de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="f6a3e-110">Your message store provider must support named properties if it is to be used as the default message store.</span></span> <span data-ttu-id="f6a3e-111">O suporte a propriedades nomeadas significa implementar os métodos [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) e implementar uma ou mais assinaturas de mapeamento que identifiquem quais nomes são usados em quais identificadores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f6a3e-111">Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers.</span></span> <span data-ttu-id="f6a3e-112">Para obter mais informações, consulte [definindo novas propriedades MAPI](defining-new-mapi-properties.md) e [propriedades nomeadas de suporte](supporting-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f6a3e-112">For more information, see [Defining New MAPI Properties](defining-new-mapi-properties.md) and [Supporting Named Properties](supporting-named-properties.md).</span></span>
  
<span data-ttu-id="f6a3e-113">A maioria dos provedores de repositórios de mensagens que oferecem suporte a propriedades nomeadas usam uma única assinatura de mapeamento para todos os objetos no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f6a3e-113">Most message store providers that support named properties use a single mapping signature for all objects in the message store.</span></span> <span data-ttu-id="f6a3e-114">Isso tem dois benefícios.</span><span class="sxs-lookup"><span data-stu-id="f6a3e-114">This has two benefits.</span></span> <span data-ttu-id="f6a3e-115">Primeiro, é mais simples implementar assinaturas de mapeamento se houver apenas uma para acompanhar.</span><span class="sxs-lookup"><span data-stu-id="f6a3e-115">First, it is simpler to implement mapping signatures if there is only one to keep track of.</span></span> <span data-ttu-id="f6a3e-116">Em segundo lugar, se todos os objetos no repositório de mensagens usarem a mesma assinatura de mapeamento, os aplicativos cliente serão garantidos que todos os identificadores de propriedade nas mensagens no repositório de mensagens realmente se referem à mesma propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="f6a3e-116">Second, if all objects in the message store use the same mapping signature, client applications are assured that all property identifiers on messages in the message store actually refer to the same named property.</span></span> <span data-ttu-id="f6a3e-117">Isso permite que os aplicativos cliente exibam colunas para propriedades nomeadas na interface de exibição de pastas.</span><span class="sxs-lookup"><span data-stu-id="f6a3e-117">This enables client applications to display columns for named properties in their folder view interface.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f6a3e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6a3e-118">See also</span></span>



[<span data-ttu-id="f6a3e-119">Implementar mensagens em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="f6a3e-119">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

