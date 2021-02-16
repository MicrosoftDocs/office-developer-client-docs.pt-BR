---
title: MAPI Form Manager
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
# <a name="mapi-form-manager"></a><span data-ttu-id="cec91-103">MAPI Form Manager</span><span class="sxs-lookup"><span data-stu-id="cec91-103">MAPI Form Manager</span></span>

  
  
<span data-ttu-id="cec91-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cec91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cec91-105">Um gerenciador de formulário é um objeto que implementa a interface [IMAPIFormMgr.](imapiformmgriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="cec91-105">A form manager is an object that implements the [IMAPIFormMgr](imapiformmgriunknown.md) interface.</span></span> <span data-ttu-id="cec91-106">A maioria das organizações usará o gerenciador de formulário fornecido com MAPI, conhecido como gerenciador de formulário padrão.</span><span class="sxs-lookup"><span data-stu-id="cec91-106">Most organizations will use the form manager supplied with MAPI, referred to as the default form manager.</span></span> <span data-ttu-id="cec91-107">No entanto, uma organização pode substituir o gerenciador de formulário padrão por um gerenciador de formulário personalizado, se desejado.</span><span class="sxs-lookup"><span data-stu-id="cec91-107">However, an organization can replace the default form manager with a custom form manager if desired.</span></span> <span data-ttu-id="cec91-108">O gerenciador de formulários cuida da localização de formulários em bibliotecas de formulários, do carregamento de formulários em resposta às solicitações do usuário e da instalação de formulários na biblioteca de formulários local do usuário, na biblioteca de formulários de pasta ou na biblioteca de formulários pessoais.</span><span class="sxs-lookup"><span data-stu-id="cec91-108">The form manager takes care of locating forms within form libraries, loading forms in response to user requests, and installing forms into a user's local form library, folder form library, or personal form library.</span></span> 
  
<span data-ttu-id="cec91-109">Para que um usuário interaja com uma mensagem, uma instância do servidor de formulário para a classe de mensagem da mensagem deve ser criada e ativada para exibir a mensagem e executar a operação solicitada na mensagem.</span><span class="sxs-lookup"><span data-stu-id="cec91-109">For a user to interact with a message, an instance of the form server for the message's message class must be created and activated to display the message and carry out the requested operation on the message.</span></span> <span data-ttu-id="cec91-110">Conforme descrito no tópico [MapI Form Libraries](mapi-form-libraries.md), a implementação de um formulário pode existir em vários locais diferentes (bibliotecas de formulário) e não há garantia de que um formulário ou seu servidor estará disponível localmente ou em um estado de execução quando um usuário quiser interagir com ele.</span><span class="sxs-lookup"><span data-stu-id="cec91-110">As described in the topic [MAPI Form Libraries](mapi-form-libraries.md), a form's implementation can exist in several different locations (form libraries) and there is no guarantee that a form or its server will be locally available or in a running state when a user wants to interact with it.</span></span> <span data-ttu-id="cec91-111">O gerenciador de formulário cuida dos detalhes de localizar e ativar o formulário.</span><span class="sxs-lookup"><span data-stu-id="cec91-111">The form manager takes care of the details of locating and activating the form.</span></span>
  
<span data-ttu-id="cec91-112">Os clientes usam serviços fornecidos pelo gerenciador de formulários para encontrar e ativar formulários.</span><span class="sxs-lookup"><span data-stu-id="cec91-112">Clients use services provided by the form manager to find and activate forms.</span></span> <span data-ttu-id="cec91-113">A interface **IMAPIFormMgr** é implementada pelo gerenciador de formulário e é chamada pelos clientes para acessar seus serviços.</span><span class="sxs-lookup"><span data-stu-id="cec91-113">The **IMAPIFormMgr** interface is implemented by the form manager and is called by clients to access its services.</span></span> <span data-ttu-id="cec91-114">O gerenciador de formulários é um componente essencial porque oculta quase todos os detalhes de localizar e ativar formulários de clientes de mensagens.</span><span class="sxs-lookup"><span data-stu-id="cec91-114">The form manager is an essential component because it hides almost all the details of finding and activating forms from messaging clients.</span></span> 
  
<span data-ttu-id="cec91-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span><span class="sxs-lookup"><span data-stu-id="cec91-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span></span> <span data-ttu-id="cec91-116">O gerenciador de formulário padrão pesquisa as bibliotecas de formulário na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="cec91-116">The default form manager searches the form libraries in the following order:</span></span>
  
1. <span data-ttu-id="cec91-117">A biblioteca de formulário local do usuário.</span><span class="sxs-lookup"><span data-stu-id="cec91-117">The user's local form library.</span></span> <span data-ttu-id="cec91-118">Essa biblioteca de formulário é pesquisada primeiro porque fornece o acesso mais rápido à implementação de um formulário se a implementação estiver instalada na biblioteca de formulário local.</span><span class="sxs-lookup"><span data-stu-id="cec91-118">This form library is searched first because it provides the fastest access to a form's implementation if the implementation is installed in the local form library.</span></span>
    
2. <span data-ttu-id="cec91-119">A biblioteca de formulário de pasta do contêiner da mensagem — a pasta na qual a mensagem que está sendo carregada é armazenada.</span><span class="sxs-lookup"><span data-stu-id="cec91-119">The folder form library of the message's container — the folder in which the message being loaded is stored.</span></span>
    
3. <span data-ttu-id="cec91-120">A biblioteca de formulário pessoal do usuário.</span><span class="sxs-lookup"><span data-stu-id="cec91-120">The user's personal form library.</span></span>
    
<span data-ttu-id="cec91-121">Um gerenciador de formulário personalizado pode pesquisar as bibliotecas de formulário disponíveis em qualquer ordem ou pode implementar outras bibliotecas de formulário, como uma biblioteca de formulário em toda a organização.</span><span class="sxs-lookup"><span data-stu-id="cec91-121">A custom form manager can search the available form libraries in any order, or can implement other form libraries such as an organization-wide form library.</span></span> <span data-ttu-id="cec91-122">Para obter mais detalhes sobre bibliotecas de formulário, consulte [MAPI Form Libraries](mapi-form-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="cec91-122">For more details on form libraries, see [MAPI Form Libraries](mapi-form-libraries.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cec91-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="cec91-123">See also</span></span>



[<span data-ttu-id="cec91-124">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="cec91-124">MAPI Forms</span></span>](mapi-forms.md)

