---
title: Preparando-se para o lançamento de um provedor OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: Esta seção sugere os testes, que você pode fazer antes de liberar seu provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 5caf4144a8daed31d30c9ecbcf9cf21c2300ed8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770830"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="30216-103">Preparando-se para o lançamento de um provedor OSC</span><span class="sxs-lookup"><span data-stu-id="30216-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="30216-104">Esta seção sugere os testes, que você pode fazer antes de liberar seu provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="30216-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="30216-105">Você pode iniciar consultando os tópicos desta seção e realizar alguns desses testes durante seu desenvolvimento e as fases de teste, mas você deve concluir estes testes quando que você solta.</span><span class="sxs-lookup"><span data-stu-id="30216-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="30216-106">Esses testes verificam a funcionalidade básica da sua implementação das interfaces do provedor do OSC com relação aos recursos que você especificar para o provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="30216-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="30216-107">Além disso, mesmo que o OSC é um recurso compartilhado por vários aplicativos de cliente do Office, esses testes usam o Outlook como o cliente para testar a funcionalidade fundamental.</span><span class="sxs-lookup"><span data-stu-id="30216-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="30216-108">Você deve determinar se outros testes são necessários para recursos específicos para o seu provedor.</span><span class="sxs-lookup"><span data-stu-id="30216-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="30216-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="30216-109">In this section</span></span>

- <span data-ttu-id="30216-110">[Implantação de teste](testing-deployment.md): descreve os cenários, você deve ser testado em torno de instalação e desinstalação de um provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="30216-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="30216-111">[Recursos de teste, a autenticação e a configuração](testing-capabilities-authentication-and-configuration.md): descreve os testes para obtenção de recursos e cenários em torno Configurando uma conta e autenticação de um usuário para uma rede social.</span><span class="sxs-lookup"><span data-stu-id="30216-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="30216-112">[Stop-seguir pessoas e testando seguir](testing-following-and-stop-following-persons.md): descreve os cenários para testar a capacidade do provedor OSC para adicionar uma pessoa como um amigo, ou para remover um amigo da rede social.</span><span class="sxs-lookup"><span data-stu-id="30216-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="30216-113">[Testando amigos](testing-friends.md): descreve os testes e cenários para verificar que o provedor do OSC apropriadamente retorna dados de amigos e não-amigos, onde aplicável, dependendo do modo de sincronização que o provedor oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="30216-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="30216-114">[Atividades de teste](testing-activities.md): descreve os testes e cenários para verificar que o provedor do OSC apropriadamente retorna atividades de amigos e não-amigos, onde aplicável, dependendo do modo de sincronização que o provedor oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="30216-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="30216-115">Referência</span><span class="sxs-lookup"><span data-stu-id="30216-115">Reference</span></span>

- [<span data-ttu-id="30216-116">Referência do provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="30216-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="30216-117">Se��es relacionadas</span><span class="sxs-lookup"><span data-stu-id="30216-117">Related sections</span></span>

- [<span data-ttu-id="30216-118">Modelos de amostra do OSC</span><span class="sxs-lookup"><span data-stu-id="30216-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="30216-119">Sequências de chamadas comuns do OSC</span><span class="sxs-lookup"><span data-stu-id="30216-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="30216-120">Desenvolvendo um provedor com o esquema OSC XML</span><span class="sxs-lookup"><span data-stu-id="30216-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="30216-121">Depurando um provedor</span><span class="sxs-lookup"><span data-stu-id="30216-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="30216-122">Implantando um provedor</span><span class="sxs-lookup"><span data-stu-id="30216-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

