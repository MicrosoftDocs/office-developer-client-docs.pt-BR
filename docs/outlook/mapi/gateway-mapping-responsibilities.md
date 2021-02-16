---
title: Responsabilidades de mapeamento do gateway
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 214d24bb0b0af525d5e2588c556c37cf720364a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422751"
---
# <a name="gateway-mapping-responsibilities"></a><span data-ttu-id="9f6ea-103">Responsabilidades de mapeamento do gateway</span><span class="sxs-lookup"><span data-stu-id="9f6ea-103">Gateway mapping responsibilities</span></span>

<span data-ttu-id="9f6ea-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f6ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f6ea-105">Quando um gateway que reconhece MAPI recebe uma mensagem contendo propriedades nomeadas em um dos conjuntos de propriedades especiais designados para conter propriedades mapeáveis de gateway, o gateway deve mapear todas as propriedades para o protocolo do sistema de mensagens de destino.</span><span class="sxs-lookup"><span data-stu-id="9f6ea-105">When a MAPI-aware gateway receives a message containing named properties in one of the special property sets designated to contain gateway-mappable properties, the gateway should map all of the properties to the protocol of the destination messaging system.</span></span> <span data-ttu-id="9f6ea-106">Embora o MAPI recomende que os gateways manipularem todas as propriedades nomeadas nos conjuntos de propriedades especiais, espera-se que os gateways manipularão apenas dois: endereço de email e tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="9f6ea-106">Although MAPI recommends that gateways handle all named properties in the special property sets, gateways are expected to handle only two: email address and address type.</span></span> <span data-ttu-id="9f6ea-107">Como as propriedades do endereço de email e do tipo de endereço afetam diretamente a transmissão de mensagens, é fundamental que os gateways deem suporte ao mapeamento dessas duas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9f6ea-107">Because the email address and address type properties directly affect message transmission, it is critical that gateways support the mapping of these two properties.</span></span> <span data-ttu-id="9f6ea-108">Como as chaves de pesquisa consistem no tipo de endereço e no endereço de um usuário, elas também devem ser traduzidas, se possível.</span><span class="sxs-lookup"><span data-stu-id="9f6ea-108">Because search keys consist of a user's address type and address, they should also be translated if at all possible.</span></span>
  
<span data-ttu-id="9f6ea-109">Não se espera que os identificadores de entrada sejam manipulados com frequência.</span><span class="sxs-lookup"><span data-stu-id="9f6ea-109">Entry identifiers are not expected to be handled frequently.</span></span> <span data-ttu-id="9f6ea-110">Para habilitar o mapeamento de um identificador de entrada originado em um sistema de mensagens para um identificador de entrada que possa ser usado por outro sistema de mensagens, o gateway deve ser capaz de usar o formato dos dois sistemas.</span><span class="sxs-lookup"><span data-stu-id="9f6ea-110">To enable mapping of an entry identifier that originates in one messaging system to an entry identifier that is usable by another messaging system, the gateway must be able to use the format of both systems.</span></span> <span data-ttu-id="9f6ea-111">Como a maioria dos gateways não reconhece formatos de identificador de entrada, a tradução dos identificadores de entrada é rara.</span><span class="sxs-lookup"><span data-stu-id="9f6ea-111">Because most gateways are not aware of entry identifier formats, the translation of entry identifiers is rare.</span></span>
  
<span data-ttu-id="9f6ea-112">Outra propriedade mappable que não se espera que seja traduzida com frequência é o nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="9f6ea-112">Another mappable property that is not expected to be translated frequently is the display name.</span></span> <span data-ttu-id="9f6ea-113">Gateways devem armazenar nomes de exibição e transmiti-los, mas não necessariamente traduzi-los.</span><span class="sxs-lookup"><span data-stu-id="9f6ea-113">Gateways should store display names and transmit them, but not necessarily translate them.</span></span> 
  

