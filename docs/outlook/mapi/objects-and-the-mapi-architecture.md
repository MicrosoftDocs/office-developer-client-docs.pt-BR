---
title: Objetos e a arquitetura do MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0e89c2ad37b700a977962e5e0ff0ca30b9d910e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768180"
---
# <a name="objects-and-the-mapi-architecture"></a><span data-ttu-id="9f3d5-103">Objetos e a arquitetura do MAPI</span><span class="sxs-lookup"><span data-stu-id="9f3d5-103">Objects and the MAPI architecture</span></span>

<span data-ttu-id="9f3d5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f3d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f3d5-105">Todos os objetos que MAPI define se encaixam em uma ou mais camadas da arquitetura de MAPI.</span><span class="sxs-lookup"><span data-stu-id="9f3d5-105">All of the objects that MAPI defines fall into one or more layers in the MAPI architecture.</span></span> <span data-ttu-id="9f3d5-106">A camada da interface de cliente contém todos os objetos que um aplicativo cliente, o Visualizador do formulário ou o servidor de formulário pode implementar.</span><span class="sxs-lookup"><span data-stu-id="9f3d5-106">The client interface layer contains all the objects that a client application, form viewer, or form server can implement.</span></span> <span data-ttu-id="9f3d5-107">A camada de interface do provedor de serviço contém os objetos que pode ser implementar um provedor de serviços de qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="9f3d5-107">The service provider interface layer contains the objects that a service provider of any type can implement.</span></span> <span data-ttu-id="9f3d5-108">Essa camada inclui objetos implementados por catálogos de endereços, repositórios de mensagem, provedores de transporte e bibliotecas de formulários.</span><span class="sxs-lookup"><span data-stu-id="9f3d5-108">This layer includes objects implemented by address books, message stores, transport providers, and form libraries.</span></span> <span data-ttu-id="9f3d5-109">A camada que representa o subsistema de MAPI está posicionada entre as camadas de interface de provedor de cliente e de serviço.</span><span class="sxs-lookup"><span data-stu-id="9f3d5-109">The layer that represents the MAPI subsystem is positioned between the client and service provider interface layers.</span></span> <span data-ttu-id="9f3d5-110">A camada MAPI contém todos os objetos que implementa o MAPI para clientes ou provedores de serviço para usar.</span><span class="sxs-lookup"><span data-stu-id="9f3d5-110">The MAPI layer contains all of the objects that MAPI implements for clients or service providers to use.</span></span> 
  
<span data-ttu-id="9f3d5-111">A ilustração a seguir mostra onde cada um dos objetos MAPI se encaixa a arquitetura MAPI.</span><span class="sxs-lookup"><span data-stu-id="9f3d5-111">The following illustration shows where each of the MAPI objects fits into the MAPI architecture.</span></span> <span data-ttu-id="9f3d5-112">Os objetos são representados com os nomes de suas interfaces derivadas.</span><span class="sxs-lookup"><span data-stu-id="9f3d5-112">The objects are represented with the names of their derived interfaces.</span></span> <span data-ttu-id="9f3d5-113">Por exemplo, um objeto de coletor de eventos advise é mostrado como [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md), a interface que derive da [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) e que cada objeto de coletor de eventos advise implementa.</span><span class="sxs-lookup"><span data-stu-id="9f3d5-113">For example, an advise sink object is shown as [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), the interface that derives from [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) and that every advise sink object implements.</span></span> <span data-ttu-id="9f3d5-114">As interfaces que ponte camadas são usadas ou implementadas por vários componentes.</span><span class="sxs-lookup"><span data-stu-id="9f3d5-114">The interfaces that bridge layers are either used or implemented by multiple components.</span></span> <span data-ttu-id="9f3d5-115">Embora a camada MAPI aparece para separar as camadas de cliente e o provedor, indicando que todas as comunicações devem fluir por MAPI, isso não é o caso.</span><span class="sxs-lookup"><span data-stu-id="9f3d5-115">Although the MAPI layer appears to separate the client and provider layers, implying that all communication must flow through MAPI, this is not the case.</span></span> <span data-ttu-id="9f3d5-116">Os clientes possam e se comunicar diretamente com objetos do provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="9f3d5-116">Clients can and do communicate directly to service provider objects.</span></span> 
  
<span data-ttu-id="9f3d5-117">**Object layers in MAPI**</span><span class="sxs-lookup"><span data-stu-id="9f3d5-117">**Object layers in MAPI**</span></span>
  
<span data-ttu-id="9f3d5-118">![Camadas de objeto no MAPI] (media/amapi_38.gif "Camadas de objeto no MAPI")</span><span class="sxs-lookup"><span data-stu-id="9f3d5-118">![Object layers in MAPI](media/amapi_38.gif "Object layers in MAPI")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9f3d5-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f3d5-119">See also</span></span>

- [<span data-ttu-id="9f3d5-120">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f3d5-120">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)
- [<span data-ttu-id="9f3d5-121">Objeto MAPI e visão geral da Interface</span><span class="sxs-lookup"><span data-stu-id="9f3d5-121">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

