---
title: MAPI denominada propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5a6ba7af5e497ba59b43e9b80cfc9595961ed10e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579540"
---
# <a name="mapi-named-properties"></a><span data-ttu-id="2b0f4-103">MAPI denominada propriedades</span><span class="sxs-lookup"><span data-stu-id="2b0f4-103">MAPI Named Properties</span></span>
 
<span data-ttu-id="2b0f4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b0f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b0f4-105">MAPI fornece uma facilidade para atribuir nomes às propriedades, para mapear esses nomes para identificadores exclusivos e para tornar esse mapeamento persistente.</span><span class="sxs-lookup"><span data-stu-id="2b0f4-105">MAPI provides a facility for assigning names to properties, for mapping these names to unique identifiers, and for making this mapping persistent.</span></span> <span data-ttu-id="2b0f4-106">Nome persistente para mapeamento do identificador garante que os nomes de propriedade permaneçam válidos nas sessões.</span><span class="sxs-lookup"><span data-stu-id="2b0f4-106">Persistent name to identifier mapping ensures that property names remain valid across sessions.</span></span>
  
<span data-ttu-id="2b0f4-107">Para definir uma propriedade nomeada, um provedor de cliente ou serviço constitui um nome e o armazena em uma estrutura [MAPINAMEID](mapinameid.md) .</span><span class="sxs-lookup"><span data-stu-id="2b0f4-107">To define a named property, a client or service provider makes up a name and stores it in a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="2b0f4-108">Porque nomes são compostos de um identificador globalmente exclusivo de 32 bits, ou GUID e qualquer um Unicode caractere cadeia de caracteres ou um valor numérico, os criadores de propriedades nomeadas podem criar nomes significativos sem medo de duplicação.</span><span class="sxs-lookup"><span data-stu-id="2b0f4-108">Because names are made up of a 32-bit globally unique identifier, or GUID, and either a Unicode character string or numeric value, creators of named properties can create meaningful names without fear of duplication.</span></span> <span data-ttu-id="2b0f4-109">Nomes são exclusivos e eles podem ser usados sem relação com o valor dos seus identificadores.</span><span class="sxs-lookup"><span data-stu-id="2b0f4-109">Names are unique and they can be used without regard to the value of their identifiers.</span></span> 
  
<span data-ttu-id="2b0f4-110">Para oferecer suporte a propriedades nomeadas, um provedor de serviço implementa dois métodos — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — convertem entre nomes e os identificadores e permitir seu [IMAPIProp::GetProps](imapiprop-getprops.md) [ IMAPIProp::SetProps](imapiprop-setprops.md) métodos para recuperar e modificar as propriedades com identificadores no intervalo nomeado de propriedade.</span><span class="sxs-lookup"><span data-stu-id="2b0f4-110">To support named properties, a service provider implements two methods — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — to translate between names and identifiers and to allow its [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) methods to retrieve and modify properties with identifiers in the named property range.</span></span> <span data-ttu-id="2b0f4-111">O intervalo para identificadores de propriedade nomeada é entre 0x8000 e 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="2b0f4-111">The range for named property identifiers is between 0x8000 and 0xFFFE.</span></span> 
  
<span data-ttu-id="2b0f4-112">Qualquer objeto que implementa a interface **IMAPIProp** pode oferecer suporte a propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="2b0f4-112">Any object that implements the **IMAPIProp** interface can support named properties.</span></span> <span data-ttu-id="2b0f4-113">Provedores de catálogo de endereços que permitem que as entradas de outros provedores a serem copiados para seus contêineres e mensagem armazenam provedores que podem ser usados para criar tipos de mensagem arbitrária são necessários para fornecer esse suporte.</span><span class="sxs-lookup"><span data-stu-id="2b0f4-113">Address book providers that allow entries from other providers to be copied into their containers and message store providers that can be used to create arbitrary message types are required to supply this support.</span></span> <span data-ttu-id="2b0f4-114">É uma opção para todos os outros provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="2b0f4-114">It is an option for all other service providers.</span></span> <span data-ttu-id="2b0f4-115">Provedores que não oferecem suporte a propriedades nomeadas retornam MAPI_E_NO_SUPPORT dos métodos **GetIDsFromNames** e **GetNamesFromIDs** e se recusar a definir todas as propriedades com identificadores de 0x8000 ou posterior, retornando MAPI_E_UNEXPECTED no \*\* SPropProblemarray\*\*.</span><span class="sxs-lookup"><span data-stu-id="2b0f4-115">Providers that do not support named properties return MAPI_E_NO_SUPPORT from the **GetIDsFromNames** and **GetNamesFromIDs** methods and refuse to set any properties with identifiers of 0x8000 or greater, returning MAPI_E_UNEXPECTED in the **SPropProblemarray**.</span></span>
  
<span data-ttu-id="2b0f4-116">A criação de nomes de propriedades é uma maneira para que os clientes definir novas propriedades para classes de mensagem existente ou personalizado.</span><span class="sxs-lookup"><span data-stu-id="2b0f4-116">Creating names for properties is one way for clients to define new properties for existing or custom message classes.</span></span> <span data-ttu-id="2b0f4-117">Provedores de serviço podem usar propriedades nomeadas expor recursos exclusivos de seus sistemas de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2b0f4-117">Service providers can use named properties to expose unique features of their messaging systems.</span></span> <span data-ttu-id="2b0f4-118">Ainda é outro uso de propriedades nomeadas oferecer uma maneira alternativa de se referir a propriedades com identificadores abaixo 0x8000.</span><span class="sxs-lookup"><span data-stu-id="2b0f4-118">Yet another use for named properties is to provide an alternate way of referring to properties with identifiers below 0x8000.</span></span> 
  
<span data-ttu-id="2b0f4-119">Por exemplo, um cliente poderia usar código semelhante ao seguinte código para recuperar os nomes de todas as propriedades de um objeto nomeado:</span><span class="sxs-lookup"><span data-stu-id="2b0f4-119">For example, a client could use code similar to the following code to retrieve the names for all of an object's named properties:</span></span>
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = NULL;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

<span data-ttu-id="2b0f4-120">Para solicitar todos os nomes de conjunto de propriedades PS_PUBLIC_STRINGS, um cliente substituiria o NULL no parâmetro propriedade set para PS_PUBLIC_STRINGS da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2b0f4-120">To request all names from the PS_PUBLIC_STRINGS property set, a client would replace the NULL in the property set parameter to PS_PUBLIC_STRINGS as follows:</span></span> 
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = &PS_PUBLIC_STRINGS;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

## <a name="see-also"></a><span data-ttu-id="2b0f4-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b0f4-121">See also</span></span>

- [<span data-ttu-id="2b0f4-122">Visão geral da propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="2b0f4-122">MAPI Property Overview</span></span>](mapi-property-overview.md)

