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
ms.openlocfilehash: 91c1d9293108b96fde43b769c97ec673f82a8cb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563027"
---
# <a name="gateway-mapping-responsibilities"></a><span data-ttu-id="e028c-103">Responsabilidades de mapeamento do gateway</span><span class="sxs-lookup"><span data-stu-id="e028c-103">Gateway mapping responsibilities</span></span>

<span data-ttu-id="e028c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e028c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e028c-105">Quando um gateway de reconhecimento de MAPI recebe uma mensagem contendo propriedades nomeadas em um dos conjuntos de propriedade especial é designados para conter as propriedades podem ser mapeados gateway, o gateway deve mapear todas as propriedades para o protocolo do destino do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e028c-105">When a MAPI-aware gateway receives a message containing named properties in one of the special property sets designated to contain gateway-mappable properties, the gateway should map all of the properties to the protocol of the destination messaging system.</span></span> <span data-ttu-id="e028c-106">Embora o MAPI recomenda que gateways manipular nomeadas todas as propriedades nos conjuntos de propriedade especial, gateways esperados para lidar com apenas dois: endereço e o tipo de endereço de email.</span><span class="sxs-lookup"><span data-stu-id="e028c-106">Although MAPI recommends that gateways handle all named properties in the special property sets, gateways are expected to handle only two: email address and address type.</span></span> <span data-ttu-id="e028c-107">Como as propriedades de tipo de endereço e o endereço de email diretamente afetam a transmissão de mensagens, é fundamental que os gateways suportam o mapeamento dessas duas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e028c-107">Because the email address and address type properties directly affect message transmission, it is critical that gateways support the mapping of these two properties.</span></span> <span data-ttu-id="e028c-108">Porque as chaves de pesquisa consistem em tipo de endereço e o endereço de um usuário, eles também devem ser traduzidos se possível.</span><span class="sxs-lookup"><span data-stu-id="e028c-108">Because search keys consist of a user's address type and address, they should also be translated if at all possible.</span></span>
  
<span data-ttu-id="e028c-109">Identificadores de entrada não deverão ser manipulados com frequência.</span><span class="sxs-lookup"><span data-stu-id="e028c-109">Entry identifiers are not expected to be handled frequently.</span></span> <span data-ttu-id="e028c-110">Para habilitar o mapeamento de um identificador de entrada que se origina de um sistema de mensagens a um identificador de entrada que pode ser usado por outro sistema de mensagens, o gateway deve ser capaz de usar o formato dos dois sistemas.</span><span class="sxs-lookup"><span data-stu-id="e028c-110">To enable mapping of an entry identifier that originates in one messaging system to an entry identifier that is usable by another messaging system, the gateway must be able to use the format of both systems.</span></span> <span data-ttu-id="e028c-111">Porque a maioria dos gateways não estão cientes dos formatos de identificador de entrada, a tradução dos identificadores de entrada é rara.</span><span class="sxs-lookup"><span data-stu-id="e028c-111">Because most gateways are not aware of entry identifier formats, the translation of entry identifiers is rare.</span></span>
  
<span data-ttu-id="e028c-112">Outra propriedade podem ser mapeada que não é esperada a serem convertidos frequentemente é o nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="e028c-112">Another mappable property that is not expected to be translated frequently is the display name.</span></span> <span data-ttu-id="e028c-113">Gateways devem armazenar nomes para exibição e transmiti-las, mas não necessariamente traduzi-los.</span><span class="sxs-lookup"><span data-stu-id="e028c-113">Gateways should store display names and transmit them, but not necessarily translate them.</span></span> 
  

