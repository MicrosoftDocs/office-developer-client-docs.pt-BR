---
title: Gerenciador de formulários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3059183103ca2552505486b5ec54366729ae4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430193"
---
# <a name="mapi-form-manager"></a><span data-ttu-id="7ddae-103">Gerenciador de formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="7ddae-103">MAPI Form Manager</span></span>

  
  
<span data-ttu-id="7ddae-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ddae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ddae-105">Um gerente de formulários é um objeto que implementa a interface [IMAPIFormMgr](imapiformmgriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="7ddae-105">A form manager is an object that implements the [IMAPIFormMgr](imapiformmgriunknown.md) interface.</span></span> <span data-ttu-id="7ddae-106">A maioria das organizações usará o Gerenciador de formulários fornecido com MAPI, chamado de Gerenciador de formulários padrão.</span><span class="sxs-lookup"><span data-stu-id="7ddae-106">Most organizations will use the form manager supplied with MAPI, referred to as the default form manager.</span></span> <span data-ttu-id="7ddae-107">No enTanto, uma organização pode substituir o Gerenciador de formulários padrão por um gerente de formulário personalizado, se desejado.</span><span class="sxs-lookup"><span data-stu-id="7ddae-107">However, an organization can replace the default form manager with a custom form manager if desired.</span></span> <span data-ttu-id="7ddae-108">O gerente de formulários cuida da localização de formulários nas bibliotecas de formulários, carregando formulários em resposta às solicitações do usuário e instalando formulários na biblioteca de formulários local, na biblioteca de formulários de pastas ou na biblioteca de formulários pessoais de um usuário.</span><span class="sxs-lookup"><span data-stu-id="7ddae-108">The form manager takes care of locating forms within form libraries, loading forms in response to user requests, and installing forms into a user's local form library, folder form library, or personal form library.</span></span> 
  
<span data-ttu-id="7ddae-109">Para que um usuário interaja com uma mensagem, uma instância do servidor de formulário da classe Message da mensagem deve ser criada e ativada para exibir a mensagem e realizar a operação solicitada na mensagem.</span><span class="sxs-lookup"><span data-stu-id="7ddae-109">For a user to interact with a message, an instance of the form server for the message's message class must be created and activated to display the message and carry out the requested operation on the message.</span></span> <span data-ttu-id="7ddae-110">Conforme descrito no tópico [bibliotecas de formulários MAPI](mapi-form-libraries.md), a implementação de um formulário pode existir em vários locais diferentes (bibliotecas de formulários) e não há garantia de que um formulário ou seu servidor estará localmente disponível ou em um estado de execução quando um usuário quiser interagir com ele.</span><span class="sxs-lookup"><span data-stu-id="7ddae-110">As described in the topic [MAPI Form Libraries](mapi-form-libraries.md), a form's implementation can exist in several different locations (form libraries) and there is no guarantee that a form or its server will be locally available or in a running state when a user wants to interact with it.</span></span> <span data-ttu-id="7ddae-111">O gerente de formulários cuida dos detalhes da localização e ativação do formulário.</span><span class="sxs-lookup"><span data-stu-id="7ddae-111">The form manager takes care of the details of locating and activating the form.</span></span>
  
<span data-ttu-id="7ddae-112">Os clientes usam os serviços fornecidos pelo gerente de formulários para localizar e ativar formulários.</span><span class="sxs-lookup"><span data-stu-id="7ddae-112">Clients use services provided by the form manager to find and activate forms.</span></span> <span data-ttu-id="7ddae-113">A interface **IMAPIFormMgr** é implementada pelo Gerenciador de formulários e é chamada por clientes para acessar seus serviços.</span><span class="sxs-lookup"><span data-stu-id="7ddae-113">The **IMAPIFormMgr** interface is implemented by the form manager and is called by clients to access its services.</span></span> <span data-ttu-id="7ddae-114">O Gerenciador de formulários é um componente essencial porque oculta quase todos os detalhes de encontrar e ativar formulários de clientes de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7ddae-114">The form manager is an essential component because it hides almost all the details of finding and activating forms from messaging clients.</span></span> 
  
<span data-ttu-id="7ddae-115">Ao carregar servidores de formulário, o Gerenciador de formulários padrão carrega o formulário a partir da primeira biblioteca de formulários na qual uma implementação da classe de mensagem do formulário é encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ddae-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span></span> <span data-ttu-id="7ddae-116">O Gerenciador de formulários padrão pesquisa as bibliotecas de formulários na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="7ddae-116">The default form manager searches the form libraries in the following order:</span></span>
  
1. <span data-ttu-id="7ddae-117">A biblioteca de formulários local do usuário.</span><span class="sxs-lookup"><span data-stu-id="7ddae-117">The user's local form library.</span></span> <span data-ttu-id="7ddae-118">Esta biblioteca de formulários é pesquisada primeiro porque fornece o acesso mais rápido à implementação de um formulário se a implementação estiver instalada na biblioteca de formulários local.</span><span class="sxs-lookup"><span data-stu-id="7ddae-118">This form library is searched first because it provides the fastest access to a form's implementation if the implementation is installed in the local form library.</span></span>
    
2. <span data-ttu-id="7ddae-119">A biblioteca de formulários de pasta do contêiner da mensagem — a pasta na qual a mensagem que está sendo carregada está armazenada.</span><span class="sxs-lookup"><span data-stu-id="7ddae-119">The folder form library of the message's container — the folder in which the message being loaded is stored.</span></span>
    
3. <span data-ttu-id="7ddae-120">A biblioteca de formulários pessoais do usuário.</span><span class="sxs-lookup"><span data-stu-id="7ddae-120">The user's personal form library.</span></span>
    
<span data-ttu-id="7ddae-121">Um gerente de formulário personalizado pode pesquisar as bibliotecas de formulários disponíveis em qualquer ordem, ou pode implementar outras bibliotecas de formulários, como uma biblioteca de formulários em toda a organização.</span><span class="sxs-lookup"><span data-stu-id="7ddae-121">A custom form manager can search the available form libraries in any order, or can implement other form libraries such as an organization-wide form library.</span></span> <span data-ttu-id="7ddae-122">Para obter mais detalhes sobre bibliotecas de formulários, consulte [bibliotecas de formulários MAPI](mapi-form-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="7ddae-122">For more details on form libraries, see [MAPI Form Libraries](mapi-form-libraries.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7ddae-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ddae-123">See also</span></span>



[<span data-ttu-id="7ddae-124">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="7ddae-124">MAPI Forms</span></span>](mapi-forms.md)

