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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342795"
---
# <a name="gateway-mapping-responsibilities"></a><span data-ttu-id="63d79-103">Responsabilidades de mapeamento do gateway</span><span class="sxs-lookup"><span data-stu-id="63d79-103">Gateway mapping responsibilities</span></span>

<span data-ttu-id="63d79-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63d79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63d79-105">Quando um gateway de reconhecimento MAPI recebe uma mensagem que contém propriedades nomeadas em um dos conjuntos de propriedades especiais designados para conter Propriedades do gateway-mapeáveis, o gateway deve mapear todas as propriedades para o protocolo do sistema de mensagens de destino.</span><span class="sxs-lookup"><span data-stu-id="63d79-105">When a MAPI-aware gateway receives a message containing named properties in one of the special property sets designated to contain gateway-mappable properties, the gateway should map all of the properties to the protocol of the destination messaging system.</span></span> <span data-ttu-id="63d79-106">Embora a MAPI recomende que os gateways manipulem todas as propriedades nomeadas nos conjuntos de propriedades especiais, os gateways são esperados para lidar apenas com dois: endereço de email e tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="63d79-106">Although MAPI recommends that gateways handle all named properties in the special property sets, gateways are expected to handle only two: email address and address type.</span></span> <span data-ttu-id="63d79-107">Como o endereço de email e as propriedades de tipo de endereço afetam diretamente a transmissão de mensagens, é fundamental que os gateways ofereçam suporte ao mapeamento dessas duas propriedades.</span><span class="sxs-lookup"><span data-stu-id="63d79-107">Because the email address and address type properties directly affect message transmission, it is critical that gateways support the mapping of these two properties.</span></span> <span data-ttu-id="63d79-108">Como as chaves de pesquisa consistem em um tipo de endereço e endereço de um usuário, elas também devem ser traduzidas, se possível.</span><span class="sxs-lookup"><span data-stu-id="63d79-108">Because search keys consist of a user's address type and address, they should also be translated if at all possible.</span></span>
  
<span data-ttu-id="63d79-109">Os identificadores de entrada não devem ser manipulados com frequência.</span><span class="sxs-lookup"><span data-stu-id="63d79-109">Entry identifiers are not expected to be handled frequently.</span></span> <span data-ttu-id="63d79-110">Para habilitar o mapeamento de um identificador de entrada que se origina em um sistema de mensagens para um identificador de entrada que pode ser usado por outro sistema de mensagens, o gateway deve ser capaz de usar o formato de ambos os sistemas.</span><span class="sxs-lookup"><span data-stu-id="63d79-110">To enable mapping of an entry identifier that originates in one messaging system to an entry identifier that is usable by another messaging system, the gateway must be able to use the format of both systems.</span></span> <span data-ttu-id="63d79-111">Como a maioria dos gateways não está ciente dos formatos de identificador de entrada, a conversão de identificadores de entrada é rara.</span><span class="sxs-lookup"><span data-stu-id="63d79-111">Because most gateways are not aware of entry identifier formats, the translation of entry identifiers is rare.</span></span>
  
<span data-ttu-id="63d79-112">Outra propriedade mapeável que não deve ser traduzida com frequência é o nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="63d79-112">Another mappable property that is not expected to be translated frequently is the display name.</span></span> <span data-ttu-id="63d79-113">Os gateways devem armazenar nomes de exibição e transmiti-los, mas não necessariamente traduzi-los.</span><span class="sxs-lookup"><span data-stu-id="63d79-113">Gateways should store display names and transmit them, but not necessarily translate them.</span></span> 
  

