---
title: Sequências de chamadas típicas de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: Esta seção descreve as sequências de chamada típica Outlook Social Connector (OSC) de membros em interfaces de extensibilidade do provedor de OSC, que implementa um provedor OSC.
ms.openlocfilehash: 4a79e27fadb78933f41f26818cfab8b7f4a5aae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770943"
---
# <a name="osc-typical-calling-sequences"></a><span data-ttu-id="40c10-103">Sequências de chamadas típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="40c10-103">OSC typical calling sequences</span></span>

<span data-ttu-id="40c10-104">Esta seção descreve as sequências de chamada típica Outlook Social Connector (OSC) de membros em interfaces de extensibilidade do provedor de OSC, que implementa um provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="40c10-104">This section describes the Outlook Social Connector (OSC) typical calling sequences of members in the OSC provider extensibility interfaces, which an OSC provider implements.</span></span> <span data-ttu-id="40c10-105">As sequências de chamada típicas ilustram como e quando o OSC usa tais interfaces e métodos, para permitir a melhor determinam como implementar um determinado membro em uma interface de extensibilidade do provedor.</span><span class="sxs-lookup"><span data-stu-id="40c10-105">The typical calling sequences illustrate how and when the OSC uses such interfaces and methods, to let you better determine how to implement a given member on a provider extensibility interface.</span></span> <span data-ttu-id="40c10-106">A sequência de chamada real pode variar dependendo dos recursos retornados pelo método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="40c10-106">The actual calling sequence can vary depending on the capabilities returned by the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method.</span></span> <span data-ttu-id="40c10-107">Exemplos de recursos incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="40c10-107">Examples of capabilities include the following:</span></span> 
  
- <span data-ttu-id="40c10-108">Provedor de suporte para obtenção, cache ou procurando dinamicamente amigos e atividades da rede social.</span><span class="sxs-lookup"><span data-stu-id="40c10-108">Provider support for getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="40c10-109">Interface do usuário que o OSC deve ser exibida para logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="40c10-109">The user interface that the OSC should display for user logon.</span></span>
    
- <span data-ttu-id="40c10-110">O tipo de autenticação (por exemplo, autenticação baseada em formulários) que o OSC deve usar.</span><span class="sxs-lookup"><span data-stu-id="40c10-110">The authentication type (for example, forms-based authentication) that the OSC should use.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="40c10-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="40c10-111">In this section</span></span>

- <span data-ttu-id="40c10-112">[A autenticação básica](basic-authentication.md): descreve a sequência de chamada típica do OSC para dar suporte a um usuário do Office que está conectado a uma rede social, se o provedor do OSC suportar a autenticação básica.</span><span class="sxs-lookup"><span data-stu-id="40c10-112">[Basic Authentication](basic-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports basic authentication.</span></span>
    
- <span data-ttu-id="40c10-113">[Autenticação baseada em formulários](forms-based-authentication.md): descreve a sequência de chamada típica do OSC para dar suporte a um usuário do Office que está conectado a uma rede social, se o provedor do OSC oferece suporte a autenticação baseada em formulários.</span><span class="sxs-lookup"><span data-stu-id="40c10-113">[Forms-Based Authentication](forms-based-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports forms-based authentication.</span></span>
    
- <span data-ttu-id="40c10-114">[Obtendo atividades](getting-activities.md): descreve a sequência de chamada típica do OSC sincronize as atividades de amigos do usuário do Office a partir de uma rede social, se o provedor do OSC de redes sociais oferece suporte à sincronização de atividades.</span><span class="sxs-lookup"><span data-stu-id="40c10-114">[Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.</span></span>
    
- <span data-ttu-id="40c10-115">[Obtendo informações de amigos](getting-friends-information.md): descreve a sequência de chamada típica do OSC sincronize a lista de amigos do usuário do Office a partir de uma rede social, se o provedor OSC de redes sociais oferece suporte a cache de sincronização de contatos.</span><span class="sxs-lookup"><span data-stu-id="40c10-115">[Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.</span></span>
    
## <a name="reference"></a><span data-ttu-id="40c10-116">Referência</span><span class="sxs-lookup"><span data-stu-id="40c10-116">Reference</span></span>

- [<span data-ttu-id="40c10-117">Referência do provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="40c10-117">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="40c10-118">Se��es relacionadas</span><span class="sxs-lookup"><span data-stu-id="40c10-118">Related sections</span></span>

- [<span data-ttu-id="40c10-119">Introdução ao desenvolvimento de um Outlook Social Connector Provider</span><span class="sxs-lookup"><span data-stu-id="40c10-119">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="40c10-120">Modelos de amostra do OSC</span><span class="sxs-lookup"><span data-stu-id="40c10-120">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="40c10-121">Desenvolvendo um provedor com o esquema OSC XML</span><span class="sxs-lookup"><span data-stu-id="40c10-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="40c10-122">Depurando um provedor</span><span class="sxs-lookup"><span data-stu-id="40c10-122">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="40c10-123">Implantando um provedor</span><span class="sxs-lookup"><span data-stu-id="40c10-123">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="40c10-124">Práticas recomendadas para o desenvolvimento de um provedor</span><span class="sxs-lookup"><span data-stu-id="40c10-124">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="40c10-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="40c10-125">See also</span></span>

- [<span data-ttu-id="40c10-126">XML para recursos</span><span class="sxs-lookup"><span data-stu-id="40c10-126">XML for Capabilities</span></span>](xml-for-capabilities.md)

