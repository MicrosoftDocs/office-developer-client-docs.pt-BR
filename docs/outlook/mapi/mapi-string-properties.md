---
title: Propriedades da cadeia de caracteres MAPI
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
# <a name="mapi-string-properties"></a><span data-ttu-id="93ff6-103">Propriedades da cadeia de caracteres MAPI</span><span class="sxs-lookup"><span data-stu-id="93ff6-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="93ff6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93ff6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93ff6-105">MAPI fornece três tipos de propriedades diferentes para descrever Propriedades de cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="93ff6-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="93ff6-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="93ff6-106">PT_TSTRING</span></span>
  
<span data-ttu-id="93ff6-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="93ff6-107">PT_STRING8</span></span>
  
<span data-ttu-id="93ff6-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="93ff6-108">PT_UNICODE</span></span>
  
<span data-ttu-id="93ff6-109">As propriedades de cadeia de caracteres são mais comumente definidas como PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="93ff6-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="93ff6-110">O tipo de propriedade PT_TSTRING, condicionalmente, compila-se para um dos outros tipos de propriedade de cadeia de caracteres, dependendo de a macro UNICODE ter sido definida.</span><span class="sxs-lookup"><span data-stu-id="93ff6-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="93ff6-111">PT_STRING8 descreve as cadeias de caracteres de 8 bits terminadas por nulo no formato ANSI; PT_UNICODE descreve as cadeias de caracteres de caractere nulo de byte duplo terminadas.</span><span class="sxs-lookup"><span data-stu-id="93ff6-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="93ff6-112">Um cliente ou um provedor de serviços ou o cliente e o provedor podem optar por oferecer suporte a cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="93ff6-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="93ff6-113">Não é necessário.</span><span class="sxs-lookup"><span data-stu-id="93ff6-113">It is not required.</span></span> <span data-ttu-id="93ff6-114">Um cliente que oferece suporte somente a cadeias de caracteres do PT_STRING8 pode operar com um provedor que oferece suporte a Unicode e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="93ff6-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="93ff6-115">Para habilitar essa interoperabilidade, os clientes e provedores de serviço passam um sinalizador, o sinalizador MAPI_UNICODE, para indicar que há suporte para Unicode em métodos que envolvem a troca de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="93ff6-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="93ff6-116">Por exemplo, suponha que um cliente dê suporte a Unicode e precise recuperar o nome de exibição de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="93ff6-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="93ff6-117">Todas as propriedades de PT_TSTRING do cliente são compiladas para o tipo PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="93ff6-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="93ff6-118">Quando o cliente chama o método [IMAPIProp::](imapiprop-getprops.md) GetProps da pasta para recuperar sua propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), ele passa o sinalizador MAPI_UNICODE para solicitar que a cadeia de caracteres do nome para exibição seja retornada no formato Unicode .</span><span class="sxs-lookup"><span data-stu-id="93ff6-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="93ff6-119">Os clientes e provedores de serviços devem estar cientes de que a especificação de um conjunto de caracteres em uma chamada de método é apenas uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="93ff6-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="93ff6-120">O suporte a um ou a ambos os conjuntos de caracteres é até o implementador do objeto.</span><span class="sxs-lookup"><span data-stu-id="93ff6-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="93ff6-121">No enTanto, os provedores de serviços são incentivados a oferecer suporte a ambos os conjuntos de caracteres, pois eles podem obter uma distribuição mais abrangente do que os provedores que dão suporte a apenas um conjunto.</span><span class="sxs-lookup"><span data-stu-id="93ff6-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="93ff6-122">As propriedades de cadeia de caracteres podem aumentar para serem muito grandes como propriedades binárias, propriedades que usam o tipo de propriedade PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="93ff6-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="93ff6-123">Para facilitar o trabalho com propriedades grandes, o MAPI permite que os provedores de serviços configurem essas propriedades para impor limites de tamanho.</span><span class="sxs-lookup"><span data-stu-id="93ff6-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="93ff6-124">Esses limites podem variar, dependendo de:</span><span class="sxs-lookup"><span data-stu-id="93ff6-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="93ff6-125">Se as propriedades estão sendo lidas ou gravadas.</span><span class="sxs-lookup"><span data-stu-id="93ff6-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="93ff6-126">Como o provedor de serviços implementa os métodos **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="93ff6-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="93ff6-127">Considerações de tempo de execução, como restrições de memória.</span><span class="sxs-lookup"><span data-stu-id="93ff6-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="93ff6-128">Problemas de conversão de conjunto de caracteres.</span><span class="sxs-lookup"><span data-stu-id="93ff6-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="93ff6-129">Os limites de tamanho também podem ser colocados em Propriedades de cadeia de caracteres e binárias quando são usados no conjunto de colunas de uma tabela porque às vezes é impossível tornar todos os valores de propriedade grandes visíveis.</span><span class="sxs-lookup"><span data-stu-id="93ff6-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="93ff6-130">Muitos provedores de serviços truncam Propriedades de cadeia de caracteres grandes ou binárias que são usadas em tabelas para 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="93ff6-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="93ff6-131">Quando um cliente chama o método getProps ou setProps de um objeto para trabalhar com uma cadeia de caracteres grande ou uma propriedade binária e a chamada falha devido ao tamanho da propriedade, o método retorna o valor de erro MAPI_E_NOT_ENOUGH_MEMORY. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93ff6-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="93ff6-132">Se for getProps com falha para uma propriedade específica, o cliente poderá se recuperar chamando [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) e solicitando o \*\*\*\* **IStream** para acesso, especificando IID_IStream como o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="93ff6-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="93ff6-133">Usando **OpenProperty**, o cliente pode recuperar uma propriedade grande usando uma interface como **IStream** que é mais adequada para trabalhar com propriedades grandes.</span><span class="sxs-lookup"><span data-stu-id="93ff6-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="93ff6-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="93ff6-134">See also</span></span>



[<span data-ttu-id="93ff6-135">Visão geral da propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="93ff6-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

