---
title: Tipos de provedores de transporte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ca224658552af105d95794b4dd01d2ac76fe084f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406161"
---
# <a name="types-of-transport-providers"></a><span data-ttu-id="6ec11-103">Tipos de provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="6ec11-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="6ec11-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ec11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ec11-105">Todos os provedores de transporte dão suporte a uma variedade de recursos padrão, como:</span><span class="sxs-lookup"><span data-stu-id="6ec11-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="6ec11-106">Fornecer segurança adequada para o sistema de mensagens subjacente.</span><span class="sxs-lookup"><span data-stu-id="6ec11-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="6ec11-107">Envio e recebimento de mensagens do sistema de mensagens subjacente.</span><span class="sxs-lookup"><span data-stu-id="6ec11-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="6ec11-108">Expondo os tipos de endereço que os provedores de transporte dão suporte para que o spooler MAPI e os aplicativos cliente possam usá-los adequadamente.</span><span class="sxs-lookup"><span data-stu-id="6ec11-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="6ec11-109">Aceitar a entrega para destinatários específicos.</span><span class="sxs-lookup"><span data-stu-id="6ec11-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="6ec11-110">Além disso, o MAPI dá suporte a dois tipos especializados de provedores para sistemas de mensagens específicos.</span><span class="sxs-lookup"><span data-stu-id="6ec11-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="6ec11-111">**Tipo de transporte**</span><span class="sxs-lookup"><span data-stu-id="6ec11-111">**Transport type**</span></span>|<span data-ttu-id="6ec11-112">**Funcionalidade adicionada**</span><span class="sxs-lookup"><span data-stu-id="6ec11-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ec11-113">Transporte remoto</span><span class="sxs-lookup"><span data-stu-id="6ec11-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="6ec11-114">Permite a interoperabilidade com clientes conectados remotamente.</span><span class="sxs-lookup"><span data-stu-id="6ec11-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="6ec11-115">Transporte TNEF</span><span class="sxs-lookup"><span data-stu-id="6ec11-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="6ec11-116">Permite que as propriedades MAPI sejam preservadas em sistemas de mensagens que não dão suporte a eles.</span><span class="sxs-lookup"><span data-stu-id="6ec11-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="6ec11-117">Os transportes TNEF são usados para converter mensagens entre sistemas de mensagens que oferecem suporte a diferentes conjuntos de propriedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="6ec11-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="6ec11-118">Transportes TNEF use a interface MAPI [ITnef: IUnknown](itnefiunknown.md) para converter qualquer propriedade que o sistema de destino não possa representar diretamente para um fluxo de dados binários que possa ser anexado à mensagem.</span><span class="sxs-lookup"><span data-stu-id="6ec11-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="6ec11-119">Mais tarde, outro transporte TNEF pode usar o **ITnef** para decodificar o fluxo de dados e tornar as propriedades MAPI originais disponíveis para aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="6ec11-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="6ec11-120">Além disso, o suporte a TNEF será necessário se o transporte precisar oferecer suporte a classes de mensagens personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6ec11-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="6ec11-121">Para obter informações sobre a implementação de transportes TNEF, consulte [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6ec11-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="6ec11-122">Se o seu provedor de transporte não for um desses tipos, você terá que implementá-lo com as funções básicas de MAPI e de rede disponíveis na sua plataforma de destino.</span><span class="sxs-lookup"><span data-stu-id="6ec11-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  

