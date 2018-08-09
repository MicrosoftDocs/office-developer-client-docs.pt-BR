---
title: Tratamento de sessão MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cdf3052175870287ff1a66d3745e90f8b8fff256
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767948"
---
# <a name="mapi-session-handling"></a><span data-ttu-id="a80b2-103">Tratamento de sessão MAPI</span><span class="sxs-lookup"><span data-stu-id="a80b2-103">MAPI Session Handling</span></span>

  
  
<span data-ttu-id="a80b2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a80b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a80b2-105">Antes de você poderá se comunicar com provedores de serviço e um sistema de mensagens subjacente, você precisa estabelecer uma sessão.</span><span class="sxs-lookup"><span data-stu-id="a80b2-105">Before you can communicate with service providers and an underlying messaging system, you must establish a session.</span></span> <span data-ttu-id="a80b2-106">Uma sessão MAPI é um vínculo de um cliente para outros componentes MAPI.</span><span class="sxs-lookup"><span data-stu-id="a80b2-106">A MAPI session is a link from a client to other MAPI components.</span></span> <span data-ttu-id="a80b2-107">Como resultado de iniciando com êxito uma sessão, MAPI retorna aos clientes um ponteiro para um objeto de sessão — um objeto que implementa a interface **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="a80b2-107">As the result of successfully starting a session, MAPI returns to clients a pointer to a session object — an object that implements the **IMAPISession** interface.</span></span> <span data-ttu-id="a80b2-108">Para obter mais informações, consulte [IMAPISession: IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="a80b2-108">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="a80b2-109">Você pode usar os métodos da interface **IMAPISession** para acessar os objetos de provedores de armazenamento de mensagens e catálogo de endereço, acessar várias tabelas, formulários de exibição, definir propriedades de provedor de transporte e executar a administração de serviço de perfil e mensagem.</span><span class="sxs-lookup"><span data-stu-id="a80b2-109">You can use the methods of the **IMAPISession** interface to access the objects of address book and message store providers, access several tables, display forms, set transport provider properties, and perform profile and message service administration.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="a80b2-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a80b2-110">In this section</span></span>

[<span data-ttu-id="a80b2-111">Iniciar sessão MAPI</span><span class="sxs-lookup"><span data-stu-id="a80b2-111">Starting a MAPI Session</span></span>](starting-a-mapi-session.md)
  
> <span data-ttu-id="a80b2-112">Descreve como iniciar uma sessão MAPI e inclui links para tópicos com informações mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="a80b2-112">Describes how to start a MAPI session and includes links to topics with more detailed information.</span></span>
    
[<span data-ttu-id="a80b2-113">Finalizar uma sessão MAPI</span><span class="sxs-lookup"><span data-stu-id="a80b2-113">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)
  
> <span data-ttu-id="a80b2-114">Descreve como encerrar uma sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="a80b2-114">Describes how to end a MAPI session.</span></span>
    
[<span data-ttu-id="a80b2-115">Acessar objetos usando a sessão</span><span class="sxs-lookup"><span data-stu-id="a80b2-115">Accessing Objects by Using the Session</span></span>](accessing-objects-by-using-the-session.md)
  
> <span data-ttu-id="a80b2-116">Descreve como usar um ponteiro de sessão para acessar objetos de sessão.</span><span class="sxs-lookup"><span data-stu-id="a80b2-116">Describes how to use a session pointer to access session objects.</span></span>
    
[<span data-ttu-id="a80b2-117">Recuperar identidade principal e do provedor</span><span class="sxs-lookup"><span data-stu-id="a80b2-117">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
> <span data-ttu-id="a80b2-118">Descreve as propriedades usadas para recuperar primário e a identidade do provedor.</span><span class="sxs-lookup"><span data-stu-id="a80b2-118">Describes the properties used to retrieve primary and provider identity.</span></span>
    
[<span data-ttu-id="a80b2-119">Tabela de status e objetos de status</span><span class="sxs-lookup"><span data-stu-id="a80b2-119">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)
  
> <span data-ttu-id="a80b2-120">Descreve como acessar as informações da tabela de status.</span><span class="sxs-lookup"><span data-stu-id="a80b2-120">Describes how to access information from the status table.</span></span>
    

