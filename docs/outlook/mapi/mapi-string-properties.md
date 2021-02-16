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
ms.openlocfilehash: 9720b649eadecc73d84d98926674a1786796ba70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431390"
---
# <a name="mapi-string-properties"></a><span data-ttu-id="557d1-103">Propriedades de cadeia de caracteres MAPI</span><span class="sxs-lookup"><span data-stu-id="557d1-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="557d1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="557d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="557d1-105">MAPI provides three different property types to describe string properties:</span><span class="sxs-lookup"><span data-stu-id="557d1-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="557d1-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="557d1-106">PT_TSTRING</span></span>
  
<span data-ttu-id="557d1-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="557d1-107">PT_STRING8</span></span>
  
<span data-ttu-id="557d1-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="557d1-108">PT_UNICODE</span></span>
  
<span data-ttu-id="557d1-109">Propriedades de cadeia de caracteres são mais comumente definidas como PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="557d1-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="557d1-110">O PT_TSTRING tipo de propriedade é compilado condicionalmente para um dos outros tipos de propriedade de cadeia de caracteres, dependendo se a macro UNICODE foi definida.</span><span class="sxs-lookup"><span data-stu-id="557d1-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="557d1-111">PT_STRING8 descreve cadeias de caracteres terminadas por caractere nulo de 8 bits no formato ANSI; PT_UNICODE descreve cadeias de caracteres terminadas por byte nulo.</span><span class="sxs-lookup"><span data-stu-id="557d1-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="557d1-112">Um cliente ou um provedor de serviços, ou o cliente e o provedor podem optar por dar suporte a cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="557d1-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="557d1-113">Não é necessário.</span><span class="sxs-lookup"><span data-stu-id="557d1-113">It is not required.</span></span> <span data-ttu-id="557d1-114">Um cliente que dá suporte apenas PT_STRING8 cadeias de caracteres pode operar com um provedor que oferece suporte a Unicode e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="557d1-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="557d1-115">Para habilitar essa interoperabilidade, os clientes e provedores de serviços passam um sinalizador, o sinalizador MAPI_UNICODE, para indicar que Unicode é suportado em métodos que envolvem a troca de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="557d1-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="557d1-116">Por exemplo, suponha que um cliente suporte Unicode e precise recuperar o nome de exibição de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="557d1-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="557d1-117">Todas as propriedades de PT_TSTRING cliente são compiladas para digitar PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="557d1-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="557d1-118">Quando o cliente chama o método [IMAPIProp::GetProps](imapiprop-getprops.md) da pasta **para** recuperar sua propriedade PR_DISPLAY_NAME ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), ele passa o sinalizador MAPI_UNICODE para solicitar que a cadeia de caracteres de nome de exibição seja retornada no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="557d1-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="557d1-119">Os clientes e provedores de serviços precisam estar cientes de que especificar um conjunto de caracteres em uma chamada de método é apenas uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="557d1-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="557d1-120">O suporte a um ou a ambos os conjuntos de caracteres é de acordo com o implementador do objeto.</span><span class="sxs-lookup"><span data-stu-id="557d1-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="557d1-121">No entanto, os provedores de serviços são incentivados a dar suporte a ambos os conjuntos de caracteres porque permite que eles alcancem uma distribuição mais difundida do que os provedores que suportam apenas um conjunto.</span><span class="sxs-lookup"><span data-stu-id="557d1-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="557d1-122">As propriedades de cadeia de caracteres podem crescer para serem muito grandes, assim como propriedades binárias — propriedades que usam o tipo de propriedade PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="557d1-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="557d1-123">Para facilitar o trabalho com propriedades grandes, o MAPI permite aos provedores de serviços definir essas propriedades para impor limites de tamanho.</span><span class="sxs-lookup"><span data-stu-id="557d1-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="557d1-124">Esses limites podem variar, dependendo de:</span><span class="sxs-lookup"><span data-stu-id="557d1-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="557d1-125">Se as propriedades estão sendo lidas ou escritas.</span><span class="sxs-lookup"><span data-stu-id="557d1-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="557d1-126">Como o provedor de serviços implementa os **métodos IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="557d1-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="557d1-127">Considerações sobre tempo de execução, como restrições de memória.</span><span class="sxs-lookup"><span data-stu-id="557d1-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="557d1-128">Problemas de tradução do conjunto de caracteres.</span><span class="sxs-lookup"><span data-stu-id="557d1-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="557d1-129">Os limites de tamanho também podem ser colocados em propriedades binárias e de cadeia de caracteres quando são usados no conjunto de colunas de uma tabela porque às vezes é impossível tornar visível todo o valor de uma propriedade grande.</span><span class="sxs-lookup"><span data-stu-id="557d1-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="557d1-130">Muitos provedores de serviços truncam uma cadeia de caracteres grande ou propriedades binárias que são usadas em tabelas para 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="557d1-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="557d1-131">Quando um cliente chama o método **GetProps** ou **SetProps** de um objeto para trabalhar com uma propriedade binária ou cadeia de caracteres grande e a chamada falha devido ao tamanho da propriedade, o método retorna o valor de erro MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="557d1-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="557d1-132">Se for **GetProps** que está falhando em uma propriedade específica, o cliente poderá recuperar chamando [IMAPIProp::OpenProperty](imapiprop-openproperty.md) e solicitando o **IStream** para acesso especificando IID_IStream como o identificador da interface.</span><span class="sxs-lookup"><span data-stu-id="557d1-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="557d1-133">Usando **OpenProperty**, o cliente pode recuperar uma propriedade grande usando uma interface como **IStream** que é mais adequada para trabalhar com propriedades grandes.</span><span class="sxs-lookup"><span data-stu-id="557d1-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="557d1-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="557d1-134">See also</span></span>



[<span data-ttu-id="557d1-135">Visão geral da propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="557d1-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

