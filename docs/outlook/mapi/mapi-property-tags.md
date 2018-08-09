---
title: Marcas de propriedade MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8dc37f1b594eeaa199b48f5946d10e60427d4988
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767926"
---
# <a name="mapi-property-tags"></a><span data-ttu-id="8cdb5-103">Marcas de propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="8cdb5-103">MAPI property tags</span></span>
  
<span data-ttu-id="8cdb5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8cdb5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8cdb5-105">Uma marca de propriedade é um número de 32 bits que contém um identificador exclusivo de propriedade em bits 31 até 16 e um tipo de propriedade em bits 0 a 15, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="8cdb5-105">A property tag is a 32-bit number that contains a unique property identifier in bits 16 through 31 and a property type in bits 0 through 15 as shown in the following illustration.</span></span> 
  
<span data-ttu-id="8cdb5-106">**Property tag elements**</span><span class="sxs-lookup"><span data-stu-id="8cdb5-106">**Property tag elements**</span></span>
  
<span data-ttu-id="8cdb5-107">![Elementos de marca de propriedade] (media/amapi_10.gif "Elementos de marca de propriedade")</span><span class="sxs-lookup"><span data-stu-id="8cdb5-107">![Property tag elements](media/amapi_10.gif "Property tag elements")</span></span>
  
<span data-ttu-id="8cdb5-108">Marcas de propriedade são usadas para identificar as propriedades MAPI e cada propriedade deve ter um, independentemente se a propriedade é definida por um provedor de serviços, um cliente ou MAPI.</span><span class="sxs-lookup"><span data-stu-id="8cdb5-108">Property tags are used to identify MAPI properties and every property must have one, regardless of whether the property is defined by MAPI, a client, or a service provider.</span></span> <span data-ttu-id="8cdb5-109">MAPI define um conjunto de constantes da propriedade tag para suas propriedades no arquivo de cabeçalho Mapitags.h; Essas propriedades são referidas como "propriedades definidas pelo MAPI".</span><span class="sxs-lookup"><span data-stu-id="8cdb5-109">MAPI defines a set of property tag constants for its properties in the Mapitags.h header file; these properties are referred to as the "MAPI-defined properties".</span></span> 
  
<span data-ttu-id="8cdb5-110">As constantes da propriedade tag siga uma convenção de nomenclatura para consistência e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="8cdb5-110">The property tag constants follow a naming convention for consistency and ease of use.</span></span> <span data-ttu-id="8cdb5-111">Há duas partes com o nome da marca de cada propriedade: um ou mais cadeias de caracteres que descrevem o conteúdo da propriedade e um prefixo PR_.</span><span class="sxs-lookup"><span data-stu-id="8cdb5-111">There are two parts to the name of each property tag: a PR_ prefix and one or more character strings that describe the contents of the property.</span></span> <span data-ttu-id="8cdb5-112">Várias cadeias de caracteres são separadas por sublinhados.</span><span class="sxs-lookup"><span data-stu-id="8cdb5-112">Multiple character strings are separated by underscores.</span></span> <span data-ttu-id="8cdb5-113">Por exemplo, a marca de propriedade para o tipo de endereço de um destinatário de mensagem é **PR\_ADDRTYPE** ([PidTagOrgAddrtype](http://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) e o identificador de entrada para a pasta designado para receber uma cópia de todas as mensagens de saída é **PR_IPM_SENTMAIL_ ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8cdb5-113">For example, the property tag for the address type of a message recipient is **PR\_ADDRTYPE** ([PidTagOrgAddrtype](http://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) and the entry identifier for the folder designated to receive a copy of every outbound message is **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
  
<span data-ttu-id="8cdb5-114">Algumas macros estão disponíveis para ajudar a trabalhar com marcas de propriedade, entre eles [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md)e [PROP_TAG](prop_tag.md).</span><span class="sxs-lookup"><span data-stu-id="8cdb5-114">A few macros are available to help work with property tags, among them [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md), and [PROP_TAG](prop_tag.md).</span></span> <span data-ttu-id="8cdb5-115">**PROP\_tipo** extrai o tipo de propriedade da marca a propriedade; **PROP\_ID** extrai o identificador.</span><span class="sxs-lookup"><span data-stu-id="8cdb5-115">**PROP\_TYPE** extracts the property type from the property tag; **PROP\_ID** extracts the identifier.</span></span> <span data-ttu-id="8cdb5-116">**PROP_TAG** constrói uma marca de propriedade de um tipo de propriedade e o identificador.</span><span class="sxs-lookup"><span data-stu-id="8cdb5-116">**PROP_TAG** builds a property tag from a property type and identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8cdb5-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cdb5-117">See also</span></span>

- [<span data-ttu-id="8cdb5-118">Visão geral da propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="8cdb5-118">MAPI Property Overview</span></span>](mapi-property-overview.md)

