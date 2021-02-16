---
title: Manipulação de sessão MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 98c4bd0dba630db32fdb2309be3d29ebc13b1131
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422058"
---
# <a name="mapi-session-handling"></a><span data-ttu-id="fefd4-103">Manipulação de sessão MAPI</span><span class="sxs-lookup"><span data-stu-id="fefd4-103">MAPI Session Handling</span></span>

  
  
<span data-ttu-id="fefd4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fefd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fefd4-105">Antes de poder se comunicar com provedores de serviços e um sistema de mensagens subjacente, você deve estabelecer uma sessão.</span><span class="sxs-lookup"><span data-stu-id="fefd4-105">Before you can communicate with service providers and an underlying messaging system, you must establish a session.</span></span> <span data-ttu-id="fefd4-106">Uma sessão MAPI é um link de um cliente para outros componentes MAPI.</span><span class="sxs-lookup"><span data-stu-id="fefd4-106">A MAPI session is a link from a client to other MAPI components.</span></span> <span data-ttu-id="fefd4-107">Como resultado do início bem-sucedido de uma sessão, o MAPI retorna aos clientes um ponteiro para um objeto de sessão — um objeto que implementa a interface **IMAPISession.**</span><span class="sxs-lookup"><span data-stu-id="fefd4-107">As the result of successfully starting a session, MAPI returns to clients a pointer to a session object — an object that implements the **IMAPISession** interface.</span></span> <span data-ttu-id="fefd4-108">Para obter mais informações, [consulte IMAPISession : IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="fefd4-108">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="fefd4-109">Você pode usar os métodos da interface **IMAPISession** para acessar os objetos do livro de endereços e provedores de armazenamento de mensagens, acessar várias tabelas, exibir formulários, definir propriedades do provedor de transporte e executar a administração de perfil e serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="fefd4-109">You can use the methods of the **IMAPISession** interface to access the objects of address book and message store providers, access several tables, display forms, set transport provider properties, and perform profile and message service administration.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="fefd4-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="fefd4-110">In this section</span></span>

[<span data-ttu-id="fefd4-111">Iniciando uma sessão MAPI</span><span class="sxs-lookup"><span data-stu-id="fefd4-111">Starting a MAPI Session</span></span>](starting-a-mapi-session.md)
  
> <span data-ttu-id="fefd4-112">Descreve como iniciar uma sessão MAPI e inclui links para tópicos com informações mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="fefd4-112">Describes how to start a MAPI session and includes links to topics with more detailed information.</span></span>
    
[<span data-ttu-id="fefd4-113">Encerrando uma sessão MAPI</span><span class="sxs-lookup"><span data-stu-id="fefd4-113">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)
  
> <span data-ttu-id="fefd4-114">Descreve como encerrar uma sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="fefd4-114">Describes how to end a MAPI session.</span></span>
    
[<span data-ttu-id="fefd4-115">Acessando objetos usando a sessão</span><span class="sxs-lookup"><span data-stu-id="fefd4-115">Accessing Objects by Using the Session</span></span>](accessing-objects-by-using-the-session.md)
  
> <span data-ttu-id="fefd4-116">Descreve como usar um ponteiro de sessão para acessar objetos de sessão.</span><span class="sxs-lookup"><span data-stu-id="fefd4-116">Describes how to use a session pointer to access session objects.</span></span>
    
[<span data-ttu-id="fefd4-117">Recuperando a identidade principal e do provedor</span><span class="sxs-lookup"><span data-stu-id="fefd4-117">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
> <span data-ttu-id="fefd4-118">Descreve as propriedades usadas para recuperar a identidade principal e do provedor.</span><span class="sxs-lookup"><span data-stu-id="fefd4-118">Describes the properties used to retrieve primary and provider identity.</span></span>
    
[<span data-ttu-id="fefd4-119">Tabela de Status e Objetos de Status</span><span class="sxs-lookup"><span data-stu-id="fefd4-119">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)
  
> <span data-ttu-id="fefd4-120">Descreve como acessar informações da tabela de status.</span><span class="sxs-lookup"><span data-stu-id="fefd4-120">Describes how to access information from the status table.</span></span>
    

