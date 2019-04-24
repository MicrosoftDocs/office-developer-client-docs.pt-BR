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
ms.openlocfilehash: d83b98b4f06c648676852673a694a63b78f568b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345861"
---
# <a name="mapi-named-properties"></a><span data-ttu-id="1af38-103">MAPI denominada propriedades</span><span class="sxs-lookup"><span data-stu-id="1af38-103">MAPI Named Properties</span></span>
 
<span data-ttu-id="1af38-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1af38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1af38-105">O MAPI fornece um recurso para atribuir nomes às propriedades, para mapear esses nomes para identificadores exclusivos e para tornar este mapeamento persistente.</span><span class="sxs-lookup"><span data-stu-id="1af38-105">MAPI provides a facility for assigning names to properties, for mapping these names to unique identifiers, and for making this mapping persistent.</span></span> <span data-ttu-id="1af38-106">Nome persistente para mapeamento de identificador garante que os nomes de propriedade permaneçam válidos entre as sessões.</span><span class="sxs-lookup"><span data-stu-id="1af38-106">Persistent name to identifier mapping ensures that property names remain valid across sessions.</span></span>
  
<span data-ttu-id="1af38-107">Para definir uma propriedade nomeada, um cliente ou provedor de serviços constitui um nome e o armazena em uma estrutura [MAPINAMEID](mapinameid.md) .</span><span class="sxs-lookup"><span data-stu-id="1af38-107">To define a named property, a client or service provider makes up a name and stores it in a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="1af38-108">Como os nomes são compostos de um identificador global exclusivo de 32 bits, ou GUID, e uma cadeia de caracteres Unicode ou valor numérico, os criadores de propriedades nomeadas podem criar nomes significativos sem temer a duplicação.</span><span class="sxs-lookup"><span data-stu-id="1af38-108">Because names are made up of a 32-bit globally unique identifier, or GUID, and either a Unicode character string or numeric value, creators of named properties can create meaningful names without fear of duplication.</span></span> <span data-ttu-id="1af38-109">Os nomes são exclusivos e podem ser usados sem considerar o valor de seus identificadores.</span><span class="sxs-lookup"><span data-stu-id="1af38-109">Names are unique and they can be used without regard to the value of their identifiers.</span></span> 
  
<span data-ttu-id="1af38-110">Para dar suporte a propriedades nomeadas, um provedor de serviços implementa dois métodos — [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) – para traduzir entre nomes e identificadores e permitir seu [IMAPIProp:: GetProps](imapiprop-getprops.md) [ IMAPIProp::](imapiprop-setprops.md) SetProps métodos para recuperar e modificar propriedades com identificadores no intervalo de propriedades nomeado.</span><span class="sxs-lookup"><span data-stu-id="1af38-110">To support named properties, a service provider implements two methods — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — to translate between names and identifiers and to allow its [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) methods to retrieve and modify properties with identifiers in the named property range.</span></span> <span data-ttu-id="1af38-111">O intervalo de identificadores de propriedade nomeados está entre 0x8000 e 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="1af38-111">The range for named property identifiers is between 0x8000 and 0xFFFE.</span></span> 
  
<span data-ttu-id="1af38-112">Qualquer objeto que implemente a interface **IMAPIProp** pode dar suporte a propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="1af38-112">Any object that implements the **IMAPIProp** interface can support named properties.</span></span> <span data-ttu-id="1af38-113">Provedores de catálogo de endereços que permitem que entradas de outros provedores sejam copiadas em seus contêineres e provedores de repositórios de mensagens que podem ser usados para criar tipos de mensagem arbitrários são necessários para fornecer esse suporte.</span><span class="sxs-lookup"><span data-stu-id="1af38-113">Address book providers that allow entries from other providers to be copied into their containers and message store providers that can be used to create arbitrary message types are required to supply this support.</span></span> <span data-ttu-id="1af38-114">É uma opção para todos os outros provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="1af38-114">It is an option for all other service providers.</span></span> <span data-ttu-id="1af38-115">Os provedores que não dão suporte a propriedades nomeadas retornam MAPI_E_NO_SUPPORT dos métodos **GetIDsFromNames** e **GetNamesFromIDs** e se recusam a definir qualquer propriedade com identificadores de 0x8000 ou superior, retornando MAPI_E_UNEXPECTED no \*\* SPropProblemarray\*\*.</span><span class="sxs-lookup"><span data-stu-id="1af38-115">Providers that do not support named properties return MAPI_E_NO_SUPPORT from the **GetIDsFromNames** and **GetNamesFromIDs** methods and refuse to set any properties with identifiers of 0x8000 or greater, returning MAPI_E_UNEXPECTED in the **SPropProblemarray**.</span></span>
  
<span data-ttu-id="1af38-116">A criação de nomes para propriedades é uma maneira de os clientes definirem novas propriedades para classes de mensagem personalizadas ou existentes.</span><span class="sxs-lookup"><span data-stu-id="1af38-116">Creating names for properties is one way for clients to define new properties for existing or custom message classes.</span></span> <span data-ttu-id="1af38-117">Os provedores de serviços podem usar propriedades nomeadas para expor recursos exclusivos de seus sistemas de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1af38-117">Service providers can use named properties to expose unique features of their messaging systems.</span></span> <span data-ttu-id="1af38-118">Mas outro uso para propriedades nomeadas é fornecer uma maneira alternativa de se referir a propriedades com identificadores abaixo de 0x8000.</span><span class="sxs-lookup"><span data-stu-id="1af38-118">Yet another use for named properties is to provide an alternate way of referring to properties with identifiers below 0x8000.</span></span> 
  
<span data-ttu-id="1af38-119">Por exemplo, um cliente poderia usar código semelhante ao código a seguir para recuperar os nomes de todas as propriedades nomeadas de um objeto:</span><span class="sxs-lookup"><span data-stu-id="1af38-119">For example, a client could use code similar to the following code to retrieve the names for all of an object's named properties:</span></span>
  
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

<span data-ttu-id="1af38-120">Para solicitar todos os nomes do conjunto de propriedades PS_PUBLIC_STRINGS, um cliente substituiria nulo no parâmetro set de propriedade para PS_PUBLIC_STRINGS da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1af38-120">To request all names from the PS_PUBLIC_STRINGS property set, a client would replace the NULL in the property set parameter to PS_PUBLIC_STRINGS as follows:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="1af38-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1af38-121">See also</span></span>

- [<span data-ttu-id="1af38-122">Visão geral da propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="1af38-122">MAPI Property Overview</span></span>](mapi-property-overview.md)

