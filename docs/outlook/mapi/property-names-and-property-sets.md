---
title: Nomes de propriedade e conjuntos de propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fa9d6afcaf1b360f37e8c8873c9d1a823fcd4888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328543"
---
# <a name="property-names-and-property-sets"></a><span data-ttu-id="4514f-103">Nomes de propriedade e conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="4514f-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="4514f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4514f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4514f-105">O nome de cada propriedade nomeada tem duas partes:</span><span class="sxs-lookup"><span data-stu-id="4514f-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="4514f-106">Um identificador global exclusivo, ou GUID, que especifica um conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="4514f-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="4514f-107">Uma cadeia de caracteres Unicode ou um valor numérico de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4514f-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="4514f-108">Os nomes das propriedades nomeadas são descritos usando uma [estrutura MAPINAMEID.](mapinameid.md)</span><span class="sxs-lookup"><span data-stu-id="4514f-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="4514f-109">Essa estrutura contém um membro do conjunto de propriedades, um membro para especificar o nome em formato numérico ou de cadeia de caracteres e um membro para identificar qual formato é usado.</span><span class="sxs-lookup"><span data-stu-id="4514f-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="4514f-110">Como o conjunto de propriedades faz parte do nome da propriedade, ele não é opcional.</span><span class="sxs-lookup"><span data-stu-id="4514f-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="4514f-111">O MAPI definiu vários conjuntos de propriedades para uso por clientes e provedores de serviços, mas se um conjunto de propriedades existente for inadequado, um novo conjunto de propriedades poderá ser definido.</span><span class="sxs-lookup"><span data-stu-id="4514f-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="4514f-112">Os clientes e provedores de serviços podem definir seus próprios conjuntos de propriedades chamando a [função CoCreateGUID.](https://msdn.microsoft.com/library/ms688568.aspx)</span><span class="sxs-lookup"><span data-stu-id="4514f-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) function.</span></span> <span data-ttu-id="4514f-113">Normalmente, esses conjuntos de propriedades são criados para aplicativos cliente personalizados.</span><span class="sxs-lookup"><span data-stu-id="4514f-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="4514f-114">Os conjuntos de propriedades de MAPI são representados pelas seguintes constantes:</span><span class="sxs-lookup"><span data-stu-id="4514f-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="4514f-115">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="4514f-115">PS_MAPI</span></span>
  
<span data-ttu-id="4514f-116">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="4514f-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="4514f-117">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="4514f-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="4514f-118">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="4514f-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="4514f-119">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="4514f-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="4514f-120">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="4514f-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="4514f-121">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4514f-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="4514f-122">O PS_MAPI de propriedades é reservado; é usado por provedores de serviços para gerar nomes para propriedades com identificadores abaixo do intervalo de propriedades nomeado.</span><span class="sxs-lookup"><span data-stu-id="4514f-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="4514f-123">O PS_PUBLIC_STRINGS de propriedades é usado por clientes para propriedades nomeadas de mensagens IPM.</span><span class="sxs-lookup"><span data-stu-id="4514f-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="4514f-124">Como as propriedades nomeadas no conjunto de propriedades PS_PUBLIC_STRINGS aparecem na interface do usuário de um cliente, mensagens nãovisíveis, como aquelas que pertencem à classe de mensagem IPC, devem evitar a criação de propriedades nomeadas com esse conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="4514f-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="4514f-125">Em vez disso, eles devem criar propriedades no intervalo específico da classe de mensagem, 0x6800 por meio 0x7FFF.</span><span class="sxs-lookup"><span data-stu-id="4514f-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="4514f-126">A outra propriedade define propriedades nomeadas de espera que descrevem destinatários que normalmente são membros de uma lista de roteamento.</span><span class="sxs-lookup"><span data-stu-id="4514f-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="4514f-127">Contendo o mesmo tipo de informação que as propriedades associadas às propriedades da lista de destinatários, as propriedades nesses conjuntos de propriedades são compreendidas pelos gateways para exigir mapeamento para um sistema de mensagens de destino.</span><span class="sxs-lookup"><span data-stu-id="4514f-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="4514f-128">Como há cinco tipos de informações para descrever propriedades, MAPI definiu cinco conjuntos de propriedades diferentes.</span><span class="sxs-lookup"><span data-stu-id="4514f-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="4514f-129">Um cliente enviando uma mensagem que deve incluir um endereço e um tipo de endereço para seus membros da lista de roteamento atribui uma propriedade nomeada para cada membro nos conjuntos de propriedades PS_ROUTING_EMAIL_ADDRESSES e PS_ROUTING_ADDRTYPE roteamento.</span><span class="sxs-lookup"><span data-stu-id="4514f-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="4514f-130">Isso garante que o endereço e o tipo de endereço permaneçam viáveis quando enviados para um sistema de mensagens externo.</span><span class="sxs-lookup"><span data-stu-id="4514f-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4514f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4514f-131">See also</span></span>



[<span data-ttu-id="4514f-132">MAPI denominada propriedades</span><span class="sxs-lookup"><span data-stu-id="4514f-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

