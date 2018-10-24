---
title: Nomes de propriedades e conjuntos de propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fa9d6afcaf1b360f37e8c8873c9d1a823fcd4888
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391651"
---
# <a name="property-names-and-property-sets"></a><span data-ttu-id="2d5cd-103">Nomes de propriedades e conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="2d5cd-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="2d5cd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d5cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d5cd-105">O nome de cada propriedade nomeada tem duas partes:</span><span class="sxs-lookup"><span data-stu-id="2d5cd-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="2d5cd-106">Um identificador global exclusivo ou GUID, que especifica um conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="2d5cd-107">Uma cadeia de caracteres Unicode ou o valor numérico de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="2d5cd-108">Nomes de propriedades nomeadas são descritos usando uma estrutura [MAPINAMEID](mapinameid.md) .</span><span class="sxs-lookup"><span data-stu-id="2d5cd-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="2d5cd-109">Essa estrutura contém um membro do conjunto de propriedade, um membro para especificar o nome no formato numérico ou cadeia de caracteres e para identificar qual formato é usado.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="2d5cd-110">Como o conjunto de propriedades é parte do nome da propriedade, não é opcional.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="2d5cd-111">MAPI definiu vários conjuntos de propriedade para uso por clientes e provedores de serviço, mas se um conjunto existente de propriedade for inadequado, um novo conjunto de propriedades pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="2d5cd-112">Clientes e provedores de serviços podem definir seus próprios conjuntos de propriedade chamando [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) função.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) function.</span></span> <span data-ttu-id="2d5cd-113">Normalmente, esses conjuntos de propriedade são criados para os aplicativos cliente personalizados.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="2d5cd-114">Conjuntos de propriedades do MAPI são representados por constantes a seguir:</span><span class="sxs-lookup"><span data-stu-id="2d5cd-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="2d5cd-115">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="2d5cd-115">PS_MAPI</span></span>
  
<span data-ttu-id="2d5cd-116">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="2d5cd-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="2d5cd-117">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="2d5cd-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="2d5cd-118">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="2d5cd-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="2d5cd-119">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="2d5cd-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="2d5cd-120">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="2d5cd-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="2d5cd-121">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2d5cd-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="2d5cd-122">O conjunto de propriedades PS_MAPI está reservado; ele é usado pelos provedores de serviços para gerar nomes de propriedades com identificadores abaixo do intervalo de propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="2d5cd-123">O conjunto de propriedades PS_PUBLIC_STRINGS é usado pelos clientes para propriedades nomeadas das mensagens IPM.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="2d5cd-124">Como propriedades nomeadas no conjunto de propriedades PS_PUBLIC_STRINGS aparecem na interface de usuário do cliente, mensagens arquvo, tais como aqueles que pertencem à classe de mensagem CPI devem evitar a criação de chamada propriedades com este conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="2d5cd-125">Em vez disso, eles devem criar propriedades no intervalo de específicas de classe de mensagem, 0x6800 por meio de 0x7FFF.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="2d5cd-126">Os outros conjuntos de propriedade espera propriedades nomeadas descrevendo os destinatários que geralmente são membros de uma lista de roteamento.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="2d5cd-127">Propriedades nesses conjuntos de propriedade que contém o mesmo tipo de informações como as propriedades que estão associadas com propriedades da lista de destinatários, são compreendidas por gateways para exigir o mapeamento para um sistema de mensagens de destino.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="2d5cd-128">Como há cinco tipos de informações para descrição das propriedades, MAPI definiu cinco conjuntos de propriedade diferentes.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="2d5cd-129">Um cliente enviando uma mensagem que deve incluir um endereço e o tipo de endereço para seus membros da lista roteamento atribui uma propriedade nomeada para cada membro na PS_ROUTING_EMAIL_ADDRESSES e a propriedade PS_ROUTING_ADDRTYPE define.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="2d5cd-130">Isso garante que o endereço e o tipo de endereço permaneçam viáveis quando enviado para um sistema de mensagens externo.</span><span class="sxs-lookup"><span data-stu-id="2d5cd-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2d5cd-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d5cd-131">See also</span></span>



[<span data-ttu-id="2d5cd-132">MAPI denominada propriedades</span><span class="sxs-lookup"><span data-stu-id="2d5cd-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

