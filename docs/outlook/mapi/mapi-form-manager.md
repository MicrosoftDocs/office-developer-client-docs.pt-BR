---
title: Gerenciador de formulário MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d12d879ea5a82c5e0e3978d90694b3851aaac5cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767852"
---
# <a name="mapi-form-manager"></a><span data-ttu-id="ecf80-103">Gerenciador de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="ecf80-103">MAPI Form Manager</span></span>

  
  
<span data-ttu-id="ecf80-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ecf80-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ecf80-105">Um gerente de formulário é um objeto que implementa a interface [IMAPIFormMgr](imapiformmgriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="ecf80-105">A form manager is an object that implements the [IMAPIFormMgr](imapiformmgriunknown.md) interface.</span></span> <span data-ttu-id="ecf80-106">A maioria das organizações usará o Gerenciador de formulário fornecido com MAPI, conhecido como o Gerenciador de formulário padrão.</span><span class="sxs-lookup"><span data-stu-id="ecf80-106">Most organizations will use the form manager supplied with MAPI, referred to as the default form manager.</span></span> <span data-ttu-id="ecf80-107">No entanto, uma organização pode substituir o Gerenciador de formulário padrão por um gerente de formulário personalizado, se desejado.</span><span class="sxs-lookup"><span data-stu-id="ecf80-107">However, an organization can replace the default form manager with a custom form manager if desired.</span></span> <span data-ttu-id="ecf80-108">O gerente do formulário cuida de localizar os formulários dentro de bibliotecas de formulários, carregando formulários em resposta às solicitações dos usuários e instalando formulários para a biblioteca de formulários particulares, biblioteca de formulários de pasta ou biblioteca de formulários local para um usuário.</span><span class="sxs-lookup"><span data-stu-id="ecf80-108">The form manager takes care of locating forms within form libraries, loading forms in response to user requests, and installing forms into a user's local form library, folder form library, or personal form library.</span></span> 
  
<span data-ttu-id="ecf80-109">Para um usuário interagir com uma mensagem, uma instância do servidor de formulário para a classe de mensagem da mensagem deve ser criada e ativada para exibir a mensagem e realizar a operação solicitada na mensagem.</span><span class="sxs-lookup"><span data-stu-id="ecf80-109">For a user to interact with a message, an instance of the form server for the message's message class must be created and activated to display the message and carry out the requested operation on the message.</span></span> <span data-ttu-id="ecf80-110">Conforme descrito no tópico [MAPI bibliotecas de formulários](mapi-form-libraries.md), a implementação de um formulário pode existir em vários locais diferentes (bibliotecas de formulários) e não há nenhuma garantia de que um formulário ou o seu servidor será disponível localmente ou em uma execução de estado quando um usuário deseja interagir com ele.</span><span class="sxs-lookup"><span data-stu-id="ecf80-110">As described in the topic [MAPI Form Libraries](mapi-form-libraries.md), a form's implementation can exist in several different locations (form libraries) and there is no guarantee that a form or its server will be locally available or in a running state when a user wants to interact with it.</span></span> <span data-ttu-id="ecf80-111">O gerente do formulário cuida dos detalhes de localização e ativando o formulário.</span><span class="sxs-lookup"><span data-stu-id="ecf80-111">The form manager takes care of the details of locating and activating the form.</span></span>
  
<span data-ttu-id="ecf80-112">Clientes usam os serviços fornecidos pelo gerente de formulário para localizar e ativar formulários.</span><span class="sxs-lookup"><span data-stu-id="ecf80-112">Clients use services provided by the form manager to find and activate forms.</span></span> <span data-ttu-id="ecf80-113">A interface **IMAPIFormMgr** é implementada pelo gerente de formulário e é chamada pelos clientes para acessar seus serviços.</span><span class="sxs-lookup"><span data-stu-id="ecf80-113">The **IMAPIFormMgr** interface is implemented by the form manager and is called by clients to access its services.</span></span> <span data-ttu-id="ecf80-114">O Gerenciador de formulário é um componente essencial porque ele oculta quase todos os detalhes de localização e ativando formulários de clientes de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ecf80-114">The form manager is an essential component because it hides almost all the details of finding and activating forms from messaging clients.</span></span> 
  
<span data-ttu-id="ecf80-115">Ao carregar os servidores de formulário, o gerente do formulário padrão carrega o formulário da biblioteca de formulários primeira em que se encontra uma implementação para a classe de mensagem do formulário.</span><span class="sxs-lookup"><span data-stu-id="ecf80-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span></span> <span data-ttu-id="ecf80-116">O Gerenciador de formulário padrão pesquisará as bibliotecas de formulários na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="ecf80-116">The default form manager searches the form libraries in the following order:</span></span>
  
1. <span data-ttu-id="ecf80-117">Biblioteca de formulários locais do usuário.</span><span class="sxs-lookup"><span data-stu-id="ecf80-117">The user's local form library.</span></span> <span data-ttu-id="ecf80-118">Esta biblioteca de formulários é pesquisada primeiro porque ele fornece o acesso mais rápido a implementação de um formulário, se a implementação estiver instalada na biblioteca de formulários local.</span><span class="sxs-lookup"><span data-stu-id="ecf80-118">This form library is searched first because it provides the fastest access to a form's implementation if the implementation is installed in the local form library.</span></span>
    
2. <span data-ttu-id="ecf80-119">A biblioteca de formulários de pasta do contêiner da mensagem — a pasta na qual a mensagem está sendo carregada é armazenada.</span><span class="sxs-lookup"><span data-stu-id="ecf80-119">The folder form library of the message's container — the folder in which the message being loaded is stored.</span></span>
    
3. <span data-ttu-id="ecf80-120">Biblioteca de formulários particular do usuário.</span><span class="sxs-lookup"><span data-stu-id="ecf80-120">The user's personal form library.</span></span>
    
<span data-ttu-id="ecf80-121">Um gerente de formulário personalizado pode pesquisar as bibliotecas de formulário disponível em qualquer ordem, ou pode implementar outras bibliotecas de formulários, como uma biblioteca de formulários de toda a organização.</span><span class="sxs-lookup"><span data-stu-id="ecf80-121">A custom form manager can search the available form libraries in any order, or can implement other form libraries such as an organization-wide form library.</span></span> <span data-ttu-id="ecf80-122">Para obter mais detalhes sobre as bibliotecas de formulários, consulte [Bibliotecas de formulários de MAPI](mapi-form-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="ecf80-122">For more details on form libraries, see [MAPI Form Libraries](mapi-form-libraries.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ecf80-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecf80-123">See also</span></span>



[<span data-ttu-id="ecf80-124">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="ecf80-124">MAPI Forms</span></span>](mapi-forms.md)

