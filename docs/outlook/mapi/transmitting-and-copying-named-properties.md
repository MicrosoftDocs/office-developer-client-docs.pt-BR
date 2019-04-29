---
title: Transmitir e copiar propriedades nomeadas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6534e7344a62717e406c112249d26407b0852d93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437774"
---
# <a name="transmitting-and-copying-named-properties"></a><span data-ttu-id="ee8bb-103">Transmitir e copiar propriedades nomeadas</span><span class="sxs-lookup"><span data-stu-id="ee8bb-103">Transmitting and Copying Named Properties</span></span>

  
  
<span data-ttu-id="ee8bb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee8bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee8bb-105">Sempre que uma propriedade nomeada é enviada, movida ou copiada, o nome permanece constante, mas o identificador deve ser alterado para aderir ao mapeamento do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="ee8bb-105">Whenever a named property is sent, moved, or copied, the name remains constant but the identifier must change to adhere to the mapping of the destination object.</span></span> <span data-ttu-id="ee8bb-106">A única exceção a essa regra é quando a origem e o destino têm a mesma assinatura de mapeamento, tornando o remapeamento desnecessário.</span><span class="sxs-lookup"><span data-stu-id="ee8bb-106">The only exception to this rule is when the source and destination have the same mapping signature, making remapping unnecessary.</span></span>
  
<span data-ttu-id="ee8bb-107">É responsabilidade do provedor de transporte remapear os nomes das propriedades nomeadas transmitidas para os identificadores apropriados que funcionam no destino.</span><span class="sxs-lookup"><span data-stu-id="ee8bb-107">It is the responsibility of the transport provider to remap the names of transmitted named properties to appropriate identifiers that work at the destination.</span></span> <span data-ttu-id="ee8bb-108">O provedor de transporte de envio não pode saber qual é o mapeamento correto no destino; Ele deve transmitir os nomes e confiar no provedor de transporte de recebimento para mapeá-los para os identificadores que funcionam.</span><span class="sxs-lookup"><span data-stu-id="ee8bb-108">The sending transport provider cannot know what the correct mapping is at the destination; it must transmit the names and rely on the receiving transport provider to map them to identifiers that work.</span></span> <span data-ttu-id="ee8bb-109">A implementação de MAPI do TNEF manipula o remapeamento de propriedades nomeadas para provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="ee8bb-109">The MAPI implementation of TNEF handles the remapping of named properties for transport providers.</span></span> <span data-ttu-id="ee8bb-110">Os provedores de transporte podem manipular o remapeamento manualmente ou usar a implementação TNEF.</span><span class="sxs-lookup"><span data-stu-id="ee8bb-110">Transport providers can either handle the remapping manually or use the TNEF implementation.</span></span> 
  
<span data-ttu-id="ee8bb-111">Um remapeamento semelhante de propriedades nomeadas deve ocorrer quando essas propriedades são copiadas entre repositórios de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ee8bb-111">A similar remapping of named properties must occur when these properties are copied between message stores.</span></span> <span data-ttu-id="ee8bb-112">No enTanto, como os provedores de repositórios de mensagens podem recuperar o nome para o mapeamento de identificadores do destino, eles podem remapear as propriedades imediatamente e não precisam depender do repositório de mensagens de destino.</span><span class="sxs-lookup"><span data-stu-id="ee8bb-112">However, because message store providers can retrieve the name to identifier mapping of the destination, they can remap the properties right away and not have to rely on the destination message store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee8bb-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee8bb-113">See also</span></span>



[<span data-ttu-id="ee8bb-114">MAPI denominada propriedades</span><span class="sxs-lookup"><span data-stu-id="ee8bb-114">MAPI Named Properties</span></span>](mapi-named-properties.md)

