---
title: Projetar um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b572ebcec0a33d2134f4cf19b88e3132cbd47117
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581997"
---
# <a name="designing-a-message-service"></a><span data-ttu-id="71d5a-103">Projetar um serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="71d5a-103">Designing a message service</span></span>

<span data-ttu-id="71d5a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71d5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71d5a-105">Antes de começar a escrever código para suportar o seu serviço de mensagem, é importante criar um design.</span><span class="sxs-lookup"><span data-stu-id="71d5a-105">Before you begin to write code to support your message service, it is important to create a design.</span></span> <span data-ttu-id="71d5a-106">Resolva os seguintes problemas em seu processo de design:</span><span class="sxs-lookup"><span data-stu-id="71d5a-106">Resolve the following issues in your design process:</span></span>
  
1. <span data-ttu-id="71d5a-107">Determine quantos provedores de serviço devem ser incluídos no serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="71d5a-107">Determine how many service providers should be included in the message service.</span></span> <span data-ttu-id="71d5a-108">Inclua apenas a provedores de serviço relacionado (ou seja, provedores que funcionam com o mesmo sistema de mensagens) em seu serviço.</span><span class="sxs-lookup"><span data-stu-id="71d5a-108">Include only related service providers (that is, providers that work with the same messaging system) in your service.</span></span> <span data-ttu-id="71d5a-109">O mesmo serviço de mensagem não pertencem a provedores de serviços não relacionados.</span><span class="sxs-lookup"><span data-stu-id="71d5a-109">Unrelated service providers do not belong in the same message service.</span></span> <span data-ttu-id="71d5a-110">Use o perfil para a integração de serviços de mensagem e provedores de serviços não relacionados.</span><span class="sxs-lookup"><span data-stu-id="71d5a-110">Use the profile for integrating unrelated service providers and message services.</span></span>
    
2. <span data-ttu-id="71d5a-111">Determine que tipo de provedores de serviço deve ser incluído no serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="71d5a-111">Determine what type of service providers should be included in the message service.</span></span> <span data-ttu-id="71d5a-112">A maioria dos serviços de messge incluir um provedor de cada um dos tipos comuns.</span><span class="sxs-lookup"><span data-stu-id="71d5a-112">Most messge services include one provider of each of the common types.</span></span> <span data-ttu-id="71d5a-113">Ou seja, o serviço de mensagem típica tem o provedor de catálogo de endereços de um provedor de armazenamento de uma mensagem e provedor de transporte de um.</span><span class="sxs-lookup"><span data-stu-id="71d5a-113">That is, the typical message service has one address book provider, one message store provider, and one transport provider.</span></span>
    
3. <span data-ttu-id="71d5a-114">Determinar quantos DLLs deve conter o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="71d5a-114">Determine how many DLLs should contain the message service.</span></span> <span data-ttu-id="71d5a-115">O número de DLLs que usa um serviço de mensagem depende dos seguintes fatores:</span><span class="sxs-lookup"><span data-stu-id="71d5a-115">The number of DLLs that a message service uses depends on the following:</span></span>
    
   - <span data-ttu-id="71d5a-116">O grau de complexidade que você, como o autor do serviço de mensagem está dispostos a lidar com.</span><span class="sxs-lookup"><span data-stu-id="71d5a-116">The degree of complexity that you as the writer of the message service are willing to handle.</span></span>
    
   - <span data-ttu-id="71d5a-117">O tipo de provedores de serviço no serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="71d5a-117">The type of service providers in the message service.</span></span>
    
   - <span data-ttu-id="71d5a-118">A relação entre o serviço de mensagem pode ter com outro serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="71d5a-118">The relationship that the message service might have with another message service.</span></span>
    
   <span data-ttu-id="71d5a-119">Como o MAPI armazena o ponto de entrada apenas um para cada tipo de provedor, não inclua vários provedores do mesmo tipo em uma única DLL.</span><span class="sxs-lookup"><span data-stu-id="71d5a-119">Because MAPI stores only one entry point for each provider type, do not include multiple providers of the same type in a single DLL.</span></span> <span data-ttu-id="71d5a-120">Se fizer sentido para incluir vários provedores de um tipo, implementá-las em DLLs separadas ou compartilhando uma função de ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="71d5a-120">If it makes sense to include multiple providers of one type, either implement them in separate DLLs or have them share an entry point function.</span></span> <span data-ttu-id="71d5a-121">Outra opção é a implementação de serviços de mensagem relacionadas ou serviços de mensagem que são capazes de usar a mesma instalação e o ponto de código de configuração e a mesma entrada DLL função, em uma DLL.</span><span class="sxs-lookup"><span data-stu-id="71d5a-121">Another option is to implement related message services, or message services that are able to use the same installation and configuration code and the same DLL entry point function, in one DLL.</span></span>
    
   <span data-ttu-id="71d5a-122">Se possível, mantenha a simplicidade e usar uma DLL que contém a implementação de todos os provedores de serviço no serviço de mensagem e todo o código para instalar e configurar o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="71d5a-122">If possible, keep it simple and use one DLL that contains the implementation of all the service providers in the message service and all the code to install and configure the message service.</span></span> <span data-ttu-id="71d5a-123">Se isso não for possível, você pode implementar uma DLL para o código de instalação e configuração e a uma única DLL para todos os provedores de serviço ou uma DLL para cada provedor.</span><span class="sxs-lookup"><span data-stu-id="71d5a-123">If this is not possible, you can implement one DLL for the installation and configuration code and either a single DLL for all of the service providers or one DLL for each provider.</span></span>
    
4. <span data-ttu-id="71d5a-124">Determine um nome para o serviço de mensagem DLL ou DLLs.</span><span class="sxs-lookup"><span data-stu-id="71d5a-124">Determine a name for the message service DLL or DLLs.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="71d5a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="71d5a-125">See also</span></span>

- [<span data-ttu-id="71d5a-126">Implementação do serviço de mensagem</span><span class="sxs-lookup"><span data-stu-id="71d5a-126">Message Service Implementation</span></span>](message-service-implementation.md)

