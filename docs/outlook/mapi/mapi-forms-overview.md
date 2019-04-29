---
title: Visão geral de formulários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4e7d48f6f6a47ce28aa0e1291ccef209b998c18e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432517"
---
# <a name="mapi-forms-overview"></a><span data-ttu-id="9014b-103">Visão geral de formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="9014b-103">MAPI forms overview</span></span>
  
<span data-ttu-id="9014b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9014b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9014b-105">Um formulário MAPI é um visualizador de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="9014b-105">A MAPI form is a viewer for a message.</span></span> <span data-ttu-id="9014b-106">Cada mensagem tem uma classe de mensagem que determina o formulário específico que é usado como seu visualizador.</span><span class="sxs-lookup"><span data-stu-id="9014b-106">Every message has a message class that dictates the particular form that is used as its viewer.</span></span> <span data-ttu-id="9014b-107">O MAPI define várias classes de mensagens e implementou os formulários para exibir mensagens dessas classes.</span><span class="sxs-lookup"><span data-stu-id="9014b-107">MAPI defines several message classes and has implemented the forms for viewing messages of these classes.</span></span> <span data-ttu-id="9014b-108">Os desenvolvedores de software cliente podem criar novas classes de mensagens e formulários personalizados para exibir mensagens criadas usando as novas classes.</span><span class="sxs-lookup"><span data-stu-id="9014b-108">Client software developers can create new message classes and custom forms for viewing messages created by using the new classes.</span></span>
  
<span data-ttu-id="9014b-109">Todos os formulários personalizados implementam um conjunto de comandos de menu padrão, como **abrir**, **criar**, **excluir**e **responder**e um conjunto de comandos específicos para o formulário específico.</span><span class="sxs-lookup"><span data-stu-id="9014b-109">Every custom form implements a set of standard menu commands, such as **Open**, **Create**, **Delete**, and **Reply**, and a set of commands that are specific to the particular form.</span></span> <span data-ttu-id="9014b-110">Alguns dos comandos de formulário estão integrados à interface do usuário do aplicativo cliente quando o formulário está ativo; outros comandos de formulário substituem completamente os comandos do cliente.</span><span class="sxs-lookup"><span data-stu-id="9014b-110">Some of the form commands are integrated with the user interface of the client application when the form is active; other form commands completely replace the client commands.</span></span> 
  
<span data-ttu-id="9014b-111">A ilustração a seguir mostra a relação entre os componentes MAPI envolvidos no uso de formulários.</span><span class="sxs-lookup"><span data-stu-id="9014b-111">The following illustration shows the relationship between the MAPI components involved in using forms.</span></span> 
  
<span data-ttu-id="9014b-112">**MAPI form architecture**</span><span class="sxs-lookup"><span data-stu-id="9014b-112">**MAPI form architecture**</span></span>
  
<span data-ttu-id="9014b-113">![Arquitetura de formulários MAPI] (media/forms01.gif "Arquitetura de formulários MAPI")</span><span class="sxs-lookup"><span data-stu-id="9014b-113">![MAPI form architecture](media/forms01.gif "MAPI form architecture")</span></span>
  
<span data-ttu-id="9014b-114">No diagrama, observe que o gerente de formulário desempenha uma função semelhante a outros provedores de serviço MAPI, embora não seja um provedor de serviços propriamente dito.</span><span class="sxs-lookup"><span data-stu-id="9014b-114">In the diagram, notice that the form manager plays a role that is similar to other MAPI service providers, although it is not a service provider itself.</span></span> <span data-ttu-id="9014b-115">O Gerenciador de formulários é uma DLL substituível que implementa algumas das interfaces MAPI.</span><span class="sxs-lookup"><span data-stu-id="9014b-115">The form manager is a replaceable DLL that implements some of the MAPI interfaces.</span></span> <span data-ttu-id="9014b-116">Embora os desenvolvedores possam implementar seus próprios gerentes de formulário, a maioria dos ambientes usará o Gerenciador de formulários fornecido pela Microsoft devido à complexidade do gerente de formulários.</span><span class="sxs-lookup"><span data-stu-id="9014b-116">Although developers can implement their own form manager, most environments will use the form manager provided by Microsoft due to the form manager's complexity.</span></span>
  
<span data-ttu-id="9014b-117">A lista a seguir descreve os componentes no diagrama e sua relação com outros componentes:</span><span class="sxs-lookup"><span data-stu-id="9014b-117">The following list describes the components in the diagram and their relationship to other components:</span></span>
  
- <span data-ttu-id="9014b-118">Cliente de mensagens: um aplicativo que pode usar objetos Form.</span><span class="sxs-lookup"><span data-stu-id="9014b-118">Messaging client: An application that can use form objects.</span></span> <span data-ttu-id="9014b-119">O cliente de mensagens usa as interfaces de formulário MAPI para se comunicar com o Gerenciador de formulários para carregar mensagens em objetos de formulário.</span><span class="sxs-lookup"><span data-stu-id="9014b-119">The messaging client uses the MAPI form interfaces to communicate with the form manager to load messages into form objects.</span></span>
    
- <span data-ttu-id="9014b-120">Interfaces de formulário MAPI: um padrão definido para comunicação entre componentes MAPI relacionados a formulários.</span><span class="sxs-lookup"><span data-stu-id="9014b-120">MAPI form interfaces: A defined standard for communication between MAPI components that are related to forms.</span></span>
    
- <span data-ttu-id="9014b-121">Gerenciador de formulários: a DLL que os clientes de mensagens usam para lidar com a instalação de formulários em bibliotecas de formulários, carregamento de servidores de formulários e comunicação inicial entre clientes de mensagens e servidores de formulário.</span><span class="sxs-lookup"><span data-stu-id="9014b-121">Form manager: The DLL that messaging clients use to handle installation of forms in form libraries, loading of form servers, and initial communication between messaging clients and form servers.</span></span>
    
- <span data-ttu-id="9014b-122">Bibliotecas de formulários: armazenamento permanente para os arquivos executáveis associados aos servidores de formulários.</span><span class="sxs-lookup"><span data-stu-id="9014b-122">Form libraries: Permanent storage for the executable files associated with form servers.</span></span>
    
- <span data-ttu-id="9014b-123">Servidores de formulário: arquivos executáveis que implementam um formulário.</span><span class="sxs-lookup"><span data-stu-id="9014b-123">Form servers: Executable files that implement a form.</span></span> <span data-ttu-id="9014b-124">Os servidores de formulário criam objetos de formulário e interfaces de usuário para lidar com mensagens específicas.</span><span class="sxs-lookup"><span data-stu-id="9014b-124">Form servers create form objects and user interfaces to deal with specific messages.</span></span> <span data-ttu-id="9014b-125">Esse executável também é um servidor OLE e obedece às convenções de OLE usuais.</span><span class="sxs-lookup"><span data-stu-id="9014b-125">This executable is also an OLE server and adheres to the usual OLE conventions.</span></span>
    
- <span data-ttu-id="9014b-126">Objetos Form: objetos de tempo de execução criados por servidores de formulário que correspondem a mensagens específicas.</span><span class="sxs-lookup"><span data-stu-id="9014b-126">Form objects: Run-time objects created by form servers that correspond to specific messages.</span></span> <span data-ttu-id="9014b-127">Os objetos Form são executados no mesmo contexto de processo que seu servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="9014b-127">Form objects run in the same process context as their form server.</span></span>
    
<span data-ttu-id="9014b-128">Para obter mais informações sobre os componentes de formulário MAPI, consulte [MAPI Forms](mapi-forms.md).</span><span class="sxs-lookup"><span data-stu-id="9014b-128">For more information about MAPI form components, see [MAPI Forms](mapi-forms.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9014b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="9014b-129">See also</span></span>

- [<span data-ttu-id="9014b-130">Recursos e arquitetura MAPI</span><span class="sxs-lookup"><span data-stu-id="9014b-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

