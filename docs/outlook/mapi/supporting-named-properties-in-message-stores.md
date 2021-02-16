---
title: Suporte a propriedades nomeadas em armazenamentos de mensagens
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
# <a name="supporting-named-properties-in-message-stores"></a><span data-ttu-id="f122a-103">Suporte a propriedades nomeadas em armazenamentos de mensagens</span><span class="sxs-lookup"><span data-stu-id="f122a-103">Supporting Named Properties in Message Stores</span></span>

  
  
<span data-ttu-id="f122a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f122a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f122a-105">Objetos message podem ter propriedades neles que não estão no conjunto de propriedades definido por MAPI.</span><span class="sxs-lookup"><span data-stu-id="f122a-105">Message objects can have properties in them that are not in the set of properties defined by MAPI.</span></span> <span data-ttu-id="f122a-106">Essas propriedades podem ser nomeadas ou não.</span><span class="sxs-lookup"><span data-stu-id="f122a-106">Such properties can be unnamed or named.</span></span> <span data-ttu-id="f122a-107">Propriedades não nomeadas devem residir em um intervalo de identificadores de propriedade definidos por MAPI.</span><span class="sxs-lookup"><span data-stu-id="f122a-107">Unnamed properties must reside in a range of property identifiers defined by MAPI.</span></span> <span data-ttu-id="f122a-108">Propriedades personalizadas nomeadas residem em um intervalo diferente de identificadores de propriedade definidos por MAPI.</span><span class="sxs-lookup"><span data-stu-id="f122a-108">Named custom properties reside in a different range of property identifiers defined by MAPI.</span></span> <span data-ttu-id="f122a-109">Eles geralmente são usados por tipos de mensagem personalizados.</span><span class="sxs-lookup"><span data-stu-id="f122a-109">They are typically used by custom message types.</span></span> <span data-ttu-id="f122a-110">Seu provedor de armazenamento de mensagens deve dar suporte a propriedades nomeadas se ela for usada como o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="f122a-110">Your message store provider must support named properties if it is to be used as the default message store.</span></span> <span data-ttu-id="f122a-111">O suporte a propriedades nomeadas significa implementar os métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e implementar uma ou mais assinaturas de mapeamento que identificam quais nomes vão com quais identificadores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f122a-111">Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers.</span></span> <span data-ttu-id="f122a-112">Para obter mais informações, consulte [Definindo novas propriedades MAPI](defining-new-mapi-properties.md) e [dando suporte a propriedades nomeadas.](supporting-named-properties.md)</span><span class="sxs-lookup"><span data-stu-id="f122a-112">For more information, see [Defining New MAPI Properties](defining-new-mapi-properties.md) and [Supporting Named Properties](supporting-named-properties.md).</span></span>
  
<span data-ttu-id="f122a-113">A maioria dos provedores de armazenamento de mensagens que suportam propriedades nomeadas usa uma única assinatura de mapeamento para todos os objetos no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f122a-113">Most message store providers that support named properties use a single mapping signature for all objects in the message store.</span></span> <span data-ttu-id="f122a-114">Isso tem dois benefícios.</span><span class="sxs-lookup"><span data-stu-id="f122a-114">This has two benefits.</span></span> <span data-ttu-id="f122a-115">Primeiro, é mais simples implementar assinaturas de mapeamento se houver apenas uma para acompanhar.</span><span class="sxs-lookup"><span data-stu-id="f122a-115">First, it is simpler to implement mapping signatures if there is only one to keep track of.</span></span> <span data-ttu-id="f122a-116">Segundo, se todos os objetos no armazenamento de mensagens usarem a mesma assinatura de mapeamento, os aplicativos cliente têm certeza de que todos os identificadores de propriedade em mensagens no armazenamento de mensagens realmente se referem à mesma propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="f122a-116">Second, if all objects in the message store use the same mapping signature, client applications are assured that all property identifiers on messages in the message store actually refer to the same named property.</span></span> <span data-ttu-id="f122a-117">Isso permite que aplicativos cliente exibem colunas para propriedades nomeadas em sua interface de exibição de pasta.</span><span class="sxs-lookup"><span data-stu-id="f122a-117">This enables client applications to display columns for named properties in their folder view interface.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f122a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="f122a-118">See also</span></span>



[<span data-ttu-id="f122a-119">Implementar mensagens em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="f122a-119">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

