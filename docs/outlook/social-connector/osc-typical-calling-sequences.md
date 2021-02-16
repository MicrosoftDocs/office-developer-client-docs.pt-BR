---
title: Sequências de chamadas típicas de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: Esta seção descreve as sequências de chamada típicas do Outlook Social Connector (OSC) de membros nas interfaces de extensibilidade do provedor OSC, que um provedor osC implementa.
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413609"
---
# <a name="osc-typical-calling-sequences"></a><span data-ttu-id="ef1b1-103">Sequências de chamadas típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="ef1b1-103">OSC typical calling sequences</span></span>

<span data-ttu-id="ef1b1-104">Esta seção descreve as sequências de chamada típicas do Outlook Social Connector (OSC) de membros nas interfaces de extensibilidade do provedor OSC, implementadas por um provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-104">This section describes the Outlook Social Connector (OSC) typical calling sequences of members in the OSC provider extensibility interfaces, which an OSC provider implements.</span></span> <span data-ttu-id="ef1b1-105">As sequências de chamada típicas ilustram como e quando o OSC usa essas interfaces e métodos para permitir que você determine melhor como implementar um determinado membro em uma interface de extensibilidade do provedor.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-105">The typical calling sequences illustrate how and when the OSC uses such interfaces and methods, to let you better determine how to implement a given member on a provider extensibility interface.</span></span> <span data-ttu-id="ef1b1-106">A sequência de chamada real pode variar dependendo dos recursos retornados pelo [método ISocialProvider::GetCapabilities.](isocialprovider-getcapabilities.md)</span><span class="sxs-lookup"><span data-stu-id="ef1b1-106">The actual calling sequence can vary depending on the capabilities returned by the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method.</span></span> <span data-ttu-id="ef1b1-107">Exemplos de recursos incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ef1b1-107">Examples of capabilities include the following:</span></span> 
  
- <span data-ttu-id="ef1b1-108">Suporte do provedor para obter, armazenamento em cache ou procurar dinamicamente amigos e atividades da rede social.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-108">Provider support for getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="ef1b1-109">A interface do usuário que o OSC deve exibir para logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-109">The user interface that the OSC should display for user logon.</span></span>
    
- <span data-ttu-id="ef1b1-110">O tipo de autenticação (por exemplo, autenticação baseada em formulários) que o OSC deve usar.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-110">The authentication type (for example, forms-based authentication) that the OSC should use.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="ef1b1-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ef1b1-111">In this section</span></span>

- <span data-ttu-id="ef1b1-112">[Autenticação](basic-authentication.md)Básica: descreve a sequência de chamada típica do OSC para dar suporte a um usuário do Office que está fazendo logon em uma rede social, se o provedor OSC suportar a autenticação básica.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-112">[Basic Authentication](basic-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports basic authentication.</span></span>
    
- <span data-ttu-id="ef1b1-113">[Autenticação baseada](forms-based-authentication.md)em formulários: descreve a sequência de chamada típica do OSC para dar suporte a um usuário do Office que está fazendo logon em uma rede social, se o provedor OSC suportar autenticação baseada em formulários.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-113">[Forms-Based Authentication](forms-based-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports forms-based authentication.</span></span>
    
- <span data-ttu-id="ef1b1-114">[Getting Activities](getting-activities.md): Descreve a sequência de chamada típica do OSC para sincronizar as atividades dos amigos do usuário do Office de uma rede social, se o provedor OSC de rede social suportar a sincronização de atividades.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-114">[Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.</span></span>
    
- <span data-ttu-id="ef1b1-115">[Obter informações](getting-friends-information.md)de amigos: descreve a sequência de chamada típica do OSC para sincronizar a lista de amigos do usuário do Office de uma rede social, se o provedor OSC de rede social suportar a sincronização em cache de contatos.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-115">[Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.</span></span>
    
## <a name="reference"></a><span data-ttu-id="ef1b1-116">Referências</span><span class="sxs-lookup"><span data-stu-id="ef1b1-116">Reference</span></span>

- [<span data-ttu-id="ef1b1-117">Referência do provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="ef1b1-117">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="ef1b1-118">Seções relacionadas</span><span class="sxs-lookup"><span data-stu-id="ef1b1-118">Related sections</span></span>

- [<span data-ttu-id="ef1b1-119">Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="ef1b1-119">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="ef1b1-120">Modelos de exemplo do OSC</span><span class="sxs-lookup"><span data-stu-id="ef1b1-120">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="ef1b1-121">Desenvolver um provedor com o esquema XML do OSC</span><span class="sxs-lookup"><span data-stu-id="ef1b1-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="ef1b1-122">Depurar um provedor</span><span class="sxs-lookup"><span data-stu-id="ef1b1-122">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="ef1b1-123">Implantar um provedor</span><span class="sxs-lookup"><span data-stu-id="ef1b1-123">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="ef1b1-124">Práticas recomendadas para o desenvolvimento de um provedor</span><span class="sxs-lookup"><span data-stu-id="ef1b1-124">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="ef1b1-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef1b1-125">See also</span></span>

- [<span data-ttu-id="ef1b1-126">XML para recursos</span><span class="sxs-lookup"><span data-stu-id="ef1b1-126">XML for Capabilities</span></span>](xml-for-capabilities.md)

