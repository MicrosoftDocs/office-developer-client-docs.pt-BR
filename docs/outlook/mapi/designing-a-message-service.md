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
ms.openlocfilehash: 19a8a939685c440901f3f57d72baf673a579e590
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316720"
---
# <a name="designing-a-message-service"></a><span data-ttu-id="c94d0-103">Projetar um serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="c94d0-103">Designing a message service</span></span>

<span data-ttu-id="c94d0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c94d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c94d0-105">Antes de começar a escrever código para dar suporte ao serviço de mensagens, é importante criar um design.</span><span class="sxs-lookup"><span data-stu-id="c94d0-105">Before you begin to write code to support your message service, it is important to create a design.</span></span> <span data-ttu-id="c94d0-106">Resolva os seguintes problemas no seu processo de design:</span><span class="sxs-lookup"><span data-stu-id="c94d0-106">Resolve the following issues in your design process:</span></span>
  
1. <span data-ttu-id="c94d0-107">Determinar quantos provedores de serviços devem ser incluídos no serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c94d0-107">Determine how many service providers should be included in the message service.</span></span> <span data-ttu-id="c94d0-108">Inclua somente provedores de serviços relacionados (ou seja, provedores que funcionam com o mesmo sistema de mensagens) em seu serviço.</span><span class="sxs-lookup"><span data-stu-id="c94d0-108">Include only related service providers (that is, providers that work with the same messaging system) in your service.</span></span> <span data-ttu-id="c94d0-109">Os provedores de serviços não relacionados não pertencem ao mesmo serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c94d0-109">Unrelated service providers do not belong in the same message service.</span></span> <span data-ttu-id="c94d0-110">Use o perfil para integrar provedores de serviço não relacionados e serviços de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c94d0-110">Use the profile for integrating unrelated service providers and message services.</span></span>
    
2. <span data-ttu-id="c94d0-111">Determine que tipo de provedores de serviço deve ser incluído no serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c94d0-111">Determine what type of service providers should be included in the message service.</span></span> <span data-ttu-id="c94d0-112">A maioria dos serviços do messge inclui um provedor de cada tipo comum.</span><span class="sxs-lookup"><span data-stu-id="c94d0-112">Most messge services include one provider of each of the common types.</span></span> <span data-ttu-id="c94d0-113">Ou seja, o serviço de mensagens típico tem um provedor de catálogo de endereços, um provedor de armazenamento de mensagens e um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="c94d0-113">That is, the typical message service has one address book provider, one message store provider, and one transport provider.</span></span>
    
3. <span data-ttu-id="c94d0-114">Determinar quantas DLLs devem conter o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c94d0-114">Determine how many DLLs should contain the message service.</span></span> <span data-ttu-id="c94d0-115">O número de DLLs que um serviço de mensagens usa depende do seguinte:</span><span class="sxs-lookup"><span data-stu-id="c94d0-115">The number of DLLs that a message service uses depends on the following:</span></span>
    
   - <span data-ttu-id="c94d0-116">O grau de complexidade que você como o escritor do serviço de mensagens está disposto a lidar.</span><span class="sxs-lookup"><span data-stu-id="c94d0-116">The degree of complexity that you as the writer of the message service are willing to handle.</span></span>
    
   - <span data-ttu-id="c94d0-117">O tipo de provedores de serviço no serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c94d0-117">The type of service providers in the message service.</span></span>
    
   - <span data-ttu-id="c94d0-118">A relação que o serviço de mensagens pode ter com outro serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c94d0-118">The relationship that the message service might have with another message service.</span></span>
    
   <span data-ttu-id="c94d0-119">Como o MAPI armazena somente um ponto de entrada para cada tipo de provedor, não inclua vários provedores do mesmo tipo em uma única DLL.</span><span class="sxs-lookup"><span data-stu-id="c94d0-119">Because MAPI stores only one entry point for each provider type, do not include multiple providers of the same type in a single DLL.</span></span> <span data-ttu-id="c94d0-120">Se fizer sentido incluir vários provedores de um tipo, implemente-os em DLLs separadas ou peça que compartilhem uma função de ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="c94d0-120">If it makes sense to include multiple providers of one type, either implement them in separate DLLs or have them share an entry point function.</span></span> <span data-ttu-id="c94d0-121">Outra opção é implementar serviços de mensagens relacionados ou serviços de mensagens que possam usar o mesmo código de instalação e configuração e a mesma função de ponto de entrada DLL, em uma DLL.</span><span class="sxs-lookup"><span data-stu-id="c94d0-121">Another option is to implement related message services, or message services that are able to use the same installation and configuration code and the same DLL entry point function, in one DLL.</span></span>
    
   <span data-ttu-id="c94d0-122">Se possível, mantenha-o simples e use uma DLL que contenha a implementação de todos os provedores de serviços no serviço de mensagens e todo o código para instalar e configurar o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c94d0-122">If possible, keep it simple and use one DLL that contains the implementation of all the service providers in the message service and all the code to install and configure the message service.</span></span> <span data-ttu-id="c94d0-123">Se isso não for possível, você poderá implementar uma DLL para o código de instalação e configuração e uma única DLL para todos os provedores de serviços ou uma DLL para cada provedor.</span><span class="sxs-lookup"><span data-stu-id="c94d0-123">If this is not possible, you can implement one DLL for the installation and configuration code and either a single DLL for all of the service providers or one DLL for each provider.</span></span>
    
4. <span data-ttu-id="c94d0-124">Determine o nome da DLL ou DLLs do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c94d0-124">Determine a name for the message service DLL or DLLs.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c94d0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c94d0-125">See also</span></span>

- [<span data-ttu-id="c94d0-126">Implementação do serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="c94d0-126">Message Service Implementation</span></span>](message-service-implementation.md)

