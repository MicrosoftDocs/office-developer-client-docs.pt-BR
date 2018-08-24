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
ms.openlocfilehash: a9bba55b585b09d6a5779ba41a283b20c645656f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576229"
---
# <a name="types-of-transport-providers"></a><span data-ttu-id="fc9ca-103">Tipos de provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="fc9ca-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="fc9ca-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc9ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc9ca-105">Todos os provedores de transporte oferecem suporte a uma variedade de recursos padrão, como:</span><span class="sxs-lookup"><span data-stu-id="fc9ca-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="fc9ca-106">Fornecimento de segurança adequadas para o sistema de mensagens subjacente.</span><span class="sxs-lookup"><span data-stu-id="fc9ca-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="fc9ca-107">Enviando e recebendo mensagens do sistema de mensagens subjacente.</span><span class="sxs-lookup"><span data-stu-id="fc9ca-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="fc9ca-108">Expondo os tipos de endereço os provedores de transporte oferecem suporte para que o spooler MAPI e aplicativos cliente podem usá-las apropriadamente.</span><span class="sxs-lookup"><span data-stu-id="fc9ca-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="fc9ca-109">Aceitando entrega a destinatários específicos.</span><span class="sxs-lookup"><span data-stu-id="fc9ca-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="fc9ca-110">Além disso, o MAPI suporta dois tipos de especializados de provedores de sistemas de mensagens específicos.</span><span class="sxs-lookup"><span data-stu-id="fc9ca-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="fc9ca-111">**Tipo de transporte**</span><span class="sxs-lookup"><span data-stu-id="fc9ca-111">**Transport type**</span></span>|<span data-ttu-id="fc9ca-112">**Funcionalidade adicionada**</span><span class="sxs-lookup"><span data-stu-id="fc9ca-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc9ca-113">Transporte remoto</span><span class="sxs-lookup"><span data-stu-id="fc9ca-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="fc9ca-114">Permite a interoperabilidade com clientes conectados remotamente.</span><span class="sxs-lookup"><span data-stu-id="fc9ca-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="fc9ca-115">Transporte TNEF</span><span class="sxs-lookup"><span data-stu-id="fc9ca-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="fc9ca-116">Permite que as propriedades MAPI seja preservado em sistemas que não têm suporte-los de mensagens.</span><span class="sxs-lookup"><span data-stu-id="fc9ca-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="fc9ca-117">TNEF transportes são usados para traduzir mensagens entre sistemas de mensagens que oferecem suporte a diferentes conjuntos de propriedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="fc9ca-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="fc9ca-118">Usam o TNEF transportes MAPI [ITnef: IUnknown](itnefiunknown.md) interface para converter todas as propriedades que o sistema de destino não pode representar diretamente em um fluxo de dados binários que pode ser anexado à mensagem.</span><span class="sxs-lookup"><span data-stu-id="fc9ca-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="fc9ca-119">Mais tarde, transporte de outro TNEF pode usar **ITnef** para decodificar o fluxo de dados e fazer as propriedades MAPI originais disponível para aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="fc9ca-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="fc9ca-120">Além disso, o suporte TNEF é necessário se o seu transporte precisa suportar classes de mensagem personalizada.</span><span class="sxs-lookup"><span data-stu-id="fc9ca-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="fc9ca-121">Para obter informações sobre como implementar transportes TNEF, consulte [desenvolvendo um provedor de transporte TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fc9ca-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="fc9ca-122">Se seu provedor de transporte não for um desses tipos, você precisará implementá-lo com as funções básicas de MAPI e funções de rede disponíveis em sua plataforma de destino.</span><span class="sxs-lookup"><span data-stu-id="fc9ca-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  

