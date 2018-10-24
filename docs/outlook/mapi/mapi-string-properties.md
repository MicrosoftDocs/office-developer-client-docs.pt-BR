---
title: Propriedades de cadeia de caracteres MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3e16a373ec35696f6d1a8ccc52263a1cf8570cfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572323"
---
# <a name="mapi-string-properties"></a><span data-ttu-id="389ce-103">Propriedades de cadeia de caracteres MAPI</span><span class="sxs-lookup"><span data-stu-id="389ce-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="389ce-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="389ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="389ce-105">MAPI fornece três tipos de propriedade diferentes para descrever as propriedades de cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="389ce-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="389ce-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="389ce-106">PT_TSTRING</span></span>
  
<span data-ttu-id="389ce-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="389ce-107">PT_STRING8</span></span>
  
<span data-ttu-id="389ce-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="389ce-108">PT_UNICODE</span></span>
  
<span data-ttu-id="389ce-109">Propriedades de cadeia de caracteres mais comumente são definidas como PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="389ce-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="389ce-110">O tipo de propriedade PT_TSTRING condicionalmente é compilado em um dos outros string propriedade tipos, dependendo dependendo se a macro UNICODE tiver sido definida.</span><span class="sxs-lookup"><span data-stu-id="389ce-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="389ce-111">PT_STRING8 descreve cadeias de caracteres terminada em nulo de 8 bits no formato ANSI; PT_UNICODE descreve as cadeias de caracteres do caractere de byte duplo terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="389ce-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="389ce-112">Como um cliente ou um provedor de serviço, ou cliente e provedor podem optar por oferecer suporte a cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="389ce-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="389ce-113">Não é necessário.</span><span class="sxs-lookup"><span data-stu-id="389ce-113">It is not required.</span></span> <span data-ttu-id="389ce-114">Um cliente que suporta apenas PT_STRING8 cadeias de caracteres pode operar com um provedor que ofereça suporte a Unicode e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="389ce-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="389ce-115">Para habilitar essa interoperabilidade, clientes e provedores de serviços passam um sinalizador, o sinalizador MAPI_UNICODE, para indicar que há suporte para nos métodos que envolvem a troca de cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="389ce-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="389ce-116">Por exemplo, suponha que um cliente dá suporte a Unicode e precisa recuperar o nome de exibição de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="389ce-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="389ce-117">Todas as propriedades PT_TSTRING do cliente são compiladas para digitar PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="389ce-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="389ce-118">Quando o cliente chama o método de [IMAPIProp::GetProps](imapiprop-getprops.md) da pasta para recuperar sua propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), passa o sinalizador MAPI_UNICODE para solicitar que a cadeia de caracteres de nome de exibição retornado no formato Unicode .</span><span class="sxs-lookup"><span data-stu-id="389ce-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="389ce-119">Clientes e provedores de serviços precisam estar ciente de que a especificação de um conjunto em uma chamada de método de caracteres é apenas uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="389ce-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="389ce-120">Suporte a um ou ambos os conjuntos de caracteres é até o implementador do objeto.</span><span class="sxs-lookup"><span data-stu-id="389ce-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="389ce-121">No entanto, os provedores de serviços são incentivados a oferecer suporte a ambos os conjuntos de caracteres porque ela permite que eles tenham mais difundida distribuição que os provedores que oferecem suporte a apenas um conjunto.</span><span class="sxs-lookup"><span data-stu-id="389ce-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="389ce-122">Propriedades de cadeia de caracteres podem crescer para ser muito grande, como podem propriedades binárias — digite de propriedades que usam a propriedade PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="389ce-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="389ce-123">Para facilitar a trabalhar com propriedades de grandes, MAPI permite que os provedores de serviço configuração dessas propriedades para impor limites de tamanho.</span><span class="sxs-lookup"><span data-stu-id="389ce-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="389ce-124">Esses limites podem variar, dependendo de:</span><span class="sxs-lookup"><span data-stu-id="389ce-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="389ce-125">Se as propriedades estão sendo lidos ou gravados.</span><span class="sxs-lookup"><span data-stu-id="389ce-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="389ce-126">Como o provedor de serviço implementa os métodos **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="389ce-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="389ce-127">Considerações de tempo de execução, como restrições de memória.</span><span class="sxs-lookup"><span data-stu-id="389ce-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="389ce-128">Problemas de conversão de conjunto de caracteres.</span><span class="sxs-lookup"><span data-stu-id="389ce-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="389ce-129">Limites de tamanho também podem ser colocados em cadeia de caracteres e conjunto de propriedades binárias quando eles são usados na coluna de uma tabela porque às vezes é impossível tornar todos um grande valor de propriedade visível.</span><span class="sxs-lookup"><span data-stu-id="389ce-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="389ce-130">Muitos provedores de serviço truncam grande cadeia de caracteres ou propriedades binárias que são usadas nas tabelas a 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="389ce-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="389ce-131">Quando um cliente chama um método do objeto **GetProps** ou **SetProps** para trabalhar com uma grande cadeia de caracteres ou uma propriedade binária e a chamada falhar devido ao tamanho da propriedade, o método retornará o valor de erro MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="389ce-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="389ce-132">Se for **GetProps** que está falhando para uma propriedade específica, o cliente pode recuperar chamando [IMAPIProp::OpenProperty](imapiprop-openproperty.md) e solicitando **IStream** para acesso especificando IID_IStream como o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="389ce-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="389ce-133">Usando **OpenProperty**, o cliente pode recuperar uma propriedade grande usando uma interface como **IStream** que é mais adequada para trabalhar com propriedades de grande porte.</span><span class="sxs-lookup"><span data-stu-id="389ce-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="389ce-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="389ce-134">See also</span></span>



[<span data-ttu-id="389ce-135">Visão geral da propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="389ce-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

