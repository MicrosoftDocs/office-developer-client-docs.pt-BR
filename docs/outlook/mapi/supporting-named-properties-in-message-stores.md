---
title: Suporte a propriedades nomeadas em repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1c73bb5-b44a-4ec6-89e4-0e2228572b2d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 235683d8565732034f868dd71e4f2047ffe76f09
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569838"
---
# <a name="supporting-named-properties-in-message-stores"></a><span data-ttu-id="0d76b-103">Suporte a propriedades nomeadas em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="0d76b-103">Supporting Named Properties in Message Stores</span></span>

  
  
<span data-ttu-id="0d76b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d76b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d76b-105">Objetos de mensagem podem ter propriedades neles que não estão no conjunto de propriedades definidas pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="0d76b-105">Message objects can have properties in them that are not in the set of properties defined by MAPI.</span></span> <span data-ttu-id="0d76b-106">Tais propriedades podem ser não nomeadas ou nomeadas.</span><span class="sxs-lookup"><span data-stu-id="0d76b-106">Such properties can be unnamed or named.</span></span> <span data-ttu-id="0d76b-107">Propriedades sem nome devem residir em um intervalo de identificadores de propriedade definida pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="0d76b-107">Unnamed properties must reside in a range of property identifiers defined by MAPI.</span></span> <span data-ttu-id="0d76b-108">Propriedades personalizadas nomeadas residirem em um intervalo diferente dos identificadores de propriedade definida pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="0d76b-108">Named custom properties reside in a different range of property identifiers defined by MAPI.</span></span> <span data-ttu-id="0d76b-109">Eles geralmente são usados por tipos de mensagem personalizada.</span><span class="sxs-lookup"><span data-stu-id="0d76b-109">They are typically used by custom message types.</span></span> <span data-ttu-id="0d76b-110">Seu provedor de armazenamento de mensagem deve oferecer suporte a propriedades nomeadas caso deva ser usado como o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="0d76b-110">Your message store provider must support named properties if it is to be used as the default message store.</span></span> <span data-ttu-id="0d76b-111">Suporte a propriedades nomeadas significa Implementando os métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e a implementação de uma ou mais assinaturas de mapeamento que identificam quais nomes vá com quais identificadores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="0d76b-111">Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers.</span></span> <span data-ttu-id="0d76b-112">Para obter mais informações, consulte [Definindo novas propriedades MAPI](defining-new-mapi-properties.md) e [Suporte a propriedades chamado](supporting-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="0d76b-112">For more information, see [Defining New MAPI Properties](defining-new-mapi-properties.md) and [Supporting Named Properties](supporting-named-properties.md).</span></span>
  
<span data-ttu-id="0d76b-113">A maioria das mensagens armazenar provedores que suportam chamados de assinatura de um único mapeamento de uso de propriedades para todos os objetos no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0d76b-113">Most message store providers that support named properties use a single mapping signature for all objects in the message store.</span></span> <span data-ttu-id="0d76b-114">Isso tem duas vantagens.</span><span class="sxs-lookup"><span data-stu-id="0d76b-114">This has two benefits.</span></span> <span data-ttu-id="0d76b-115">Primeiro, é mais simples implementar assinaturas de mapeamento, se houver apenas um para acompanhar.</span><span class="sxs-lookup"><span data-stu-id="0d76b-115">First, it is simpler to implement mapping signatures if there is only one to keep track of.</span></span> <span data-ttu-id="0d76b-116">Em segundo lugar, se todos os objetos no repositório de mensagem usam a mesma assinatura de mapeamento, aplicativos de cliente são certeza de que todos os identificadores de propriedade em mensagens no repositório de mensagem realmente se referem a mesma propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="0d76b-116">Second, if all objects in the message store use the same mapping signature, client applications are assured that all property identifiers on messages in the message store actually refer to the same named property.</span></span> <span data-ttu-id="0d76b-117">Isso permite que aplicativos de cliente exibir colunas para propriedades nomeadas em sua interface de visualização de pasta.</span><span class="sxs-lookup"><span data-stu-id="0d76b-117">This enables client applications to display columns for named properties in their folder view interface.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0d76b-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d76b-118">See also</span></span>



[<span data-ttu-id="0d76b-119">Implementar mensagens em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="0d76b-119">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

