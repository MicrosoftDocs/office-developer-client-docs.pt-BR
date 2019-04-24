---
title: Preparando-se para liberar um provedor do OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: Esta seção sugere testes que você pode fazer antes de liberar seu provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327150"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="faf46-103">Preparando-se para liberar um provedor do OSC</span><span class="sxs-lookup"><span data-stu-id="faf46-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="faf46-104">Esta seção sugere testes que você pode fazer antes de liberar seu provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="faf46-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="faf46-105">Você pode começar a fazer referência aos tópicos desta seção e a executar alguns desses testes durante suas fases de desenvolvimento e teste, mas você deve ter concluído esses testes no momento da liberação.</span><span class="sxs-lookup"><span data-stu-id="faf46-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="faf46-106">Esses testes verificam a funcionalidade básica da sua implementação das interfaces do provedor OSC com relação aos recursos que você especificar para o provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="faf46-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="faf46-107">Além disso, mesmo que o OSC seja um recurso compartilhado por vários aplicativos cliente do Office, esses testes usam o Outlook como cliente para testar a funcionalidade fundamental.</span><span class="sxs-lookup"><span data-stu-id="faf46-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="faf46-108">Você deve determinar se outros testes são necessários para os recursos específicos do provedor.</span><span class="sxs-lookup"><span data-stu-id="faf46-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="faf46-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="faf46-109">In this section</span></span>

- <span data-ttu-id="faf46-110">[Testing Deployment](testing-deployment.md): descreve os cenários em que você deve testar a instalação e desinstalação de um provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="faf46-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="faf46-111">[Recursos de teste, autenticação e configuração](testing-capabilities-authentication-and-configuration.md): descreve os testes para obter recursos e cenários sobre como configurar uma conta e autenticar um usuário para uma rede social.</span><span class="sxs-lookup"><span data-stu-id="faf46-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="faf46-112">[Teste a seguir e pare as pessoas a seguir](testing-following-and-stop-following-persons.md): descreve cenários para testar a capacidade do provedor do OSC de adicionar uma pessoa como amigo ou remover um amigo da rede social.</span><span class="sxs-lookup"><span data-stu-id="faf46-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="faf46-113">[TestAndo amigos](testing-friends.md): descreve testes e cenários para verificar se o provedor do OSC retorna adequadamente dados de amigos e não amigos, quando aplicável, dependendo do modo de sincronização que o provedor suporta.</span><span class="sxs-lookup"><span data-stu-id="faf46-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="faf46-114">[Atividades de teste](testing-activities.md): descreve testes e cenários para verificar se o provedor do OSC retorna adequadamente as atividades de amigos e não amigos, quando aplicável, dependendo do modo de sincronização que o provedor suporta.</span><span class="sxs-lookup"><span data-stu-id="faf46-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="faf46-115">Referências</span><span class="sxs-lookup"><span data-stu-id="faf46-115">Reference</span></span>

- [<span data-ttu-id="faf46-116">Referência do provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="faf46-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="faf46-117">Seções relacionadas</span><span class="sxs-lookup"><span data-stu-id="faf46-117">Related sections</span></span>

- [<span data-ttu-id="faf46-118">Modelos de exemplo do OSC</span><span class="sxs-lookup"><span data-stu-id="faf46-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="faf46-119">Sequências de chamada típicas do OSC</span><span class="sxs-lookup"><span data-stu-id="faf46-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="faf46-120">Desenvolver um provedor com o esquema XML do OSC</span><span class="sxs-lookup"><span data-stu-id="faf46-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="faf46-121">Depurar um provedor</span><span class="sxs-lookup"><span data-stu-id="faf46-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="faf46-122">Implantar um provedor</span><span class="sxs-lookup"><span data-stu-id="faf46-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

