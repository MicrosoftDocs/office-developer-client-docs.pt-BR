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
# <a name="types-of-transport-providers"></a><span data-ttu-id="37032-103">Tipos de provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="37032-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="37032-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37032-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37032-105">Todos os provedores de transporte suportam uma variedade de recursos padrão, como:</span><span class="sxs-lookup"><span data-stu-id="37032-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="37032-106">Fornecendo segurança adequada para o sistema de mensagens subjacente.</span><span class="sxs-lookup"><span data-stu-id="37032-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="37032-107">Enviar e receber mensagens do sistema de mensagens subjacente.</span><span class="sxs-lookup"><span data-stu-id="37032-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="37032-108">Expor os tipos de endereço aos quais os provedores de transporte suportam para que o spooler MAPI e os aplicativos cliente possam usá-los adequadamente.</span><span class="sxs-lookup"><span data-stu-id="37032-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="37032-109">Aceitar entrega para destinatários específicos.</span><span class="sxs-lookup"><span data-stu-id="37032-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="37032-110">Além disso, o MAPI oferece suporte a dois tipos especializados de provedores para sistemas de mensagens específicos.</span><span class="sxs-lookup"><span data-stu-id="37032-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="37032-111">**Tipo de transporte**</span><span class="sxs-lookup"><span data-stu-id="37032-111">**Transport type**</span></span>|<span data-ttu-id="37032-112">**Funcionalidade adicionada**</span><span class="sxs-lookup"><span data-stu-id="37032-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37032-113">Transporte Remoto</span><span class="sxs-lookup"><span data-stu-id="37032-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="37032-114">Habilita a interoperabilidade com clientes conectados remotamente.</span><span class="sxs-lookup"><span data-stu-id="37032-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="37032-115">Transporte TNEF</span><span class="sxs-lookup"><span data-stu-id="37032-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="37032-116">Permite que as propriedades MAPI sejam preservadas em sistemas de mensagens que não as suportam.</span><span class="sxs-lookup"><span data-stu-id="37032-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="37032-117">Os transporte TNEF são usados para traduzir mensagens entre sistemas de mensagens que suportam diferentes conjuntos de propriedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="37032-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="37032-118">Os transporte TNEF usam a interface [MAPI ITnef : IUnknown](itnefiunknown.md) para converter quaisquer propriedades que o sistema de destino não possa representar diretamente em um fluxo de dados binário que possa ser anexado à mensagem.</span><span class="sxs-lookup"><span data-stu-id="37032-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="37032-119">Posteriormente, outro transporte TNEF pode usar **ITnef** para decodificar o fluxo de dados e disponibilizar as propriedades MAPI originais para aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="37032-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="37032-120">Além disso, o suporte a TNEF será necessário se o transporte precisar dar suporte a classes de mensagens personalizadas.</span><span class="sxs-lookup"><span data-stu-id="37032-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="37032-121">Para obter informações sobre a implementação de transporte TNEF, consulte [Desenvolvendo um provedor TNEF-Enabled transporte de transporte.](developing-a-tnef-enabled-transport-provider.md)</span><span class="sxs-lookup"><span data-stu-id="37032-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="37032-122">Se seu provedor de transporte não for um desses tipos, você terá que implementá-lo com as funções MAPI básicas e as funções de rede disponíveis em sua plataforma de destino.</span><span class="sxs-lookup"><span data-stu-id="37032-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  

