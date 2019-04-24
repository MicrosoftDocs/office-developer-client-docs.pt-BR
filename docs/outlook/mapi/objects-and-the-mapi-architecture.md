---
title: Objetos e a arquitetura MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4f8bc2a5268d220c17a59148f8b8ba1d320d225b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279782"
---
# <a name="objects-and-the-mapi-architecture"></a><span data-ttu-id="66eef-103">Objetos e a arquitetura MAPI</span><span class="sxs-lookup"><span data-stu-id="66eef-103">Objects and the MAPI architecture</span></span>

<span data-ttu-id="66eef-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66eef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66eef-105">Todos os objetos que o MAPI define se enquadram em uma ou mais camadas na arquitetura MAPI.</span><span class="sxs-lookup"><span data-stu-id="66eef-105">All of the objects that MAPI defines fall into one or more layers in the MAPI architecture.</span></span> <span data-ttu-id="66eef-106">A camada de interface de cliente contém todos os objetos que um aplicativo cliente, visualizador de formulários ou servidor de formulário pode implementar.</span><span class="sxs-lookup"><span data-stu-id="66eef-106">The client interface layer contains all the objects that a client application, form viewer, or form server can implement.</span></span> <span data-ttu-id="66eef-107">A camada de interface do provedor de serviços contém os objetos que um provedor de serviços de qualquer tipo pode implementar.</span><span class="sxs-lookup"><span data-stu-id="66eef-107">The service provider interface layer contains the objects that a service provider of any type can implement.</span></span> <span data-ttu-id="66eef-108">Esta camada inclui objetos implementados por catálogos de endereços, repositórios de mensagens, provedores de transporte e bibliotecas de formulários.</span><span class="sxs-lookup"><span data-stu-id="66eef-108">This layer includes objects implemented by address books, message stores, transport providers, and form libraries.</span></span> <span data-ttu-id="66eef-109">A camada que representa o subsistema MAPI está posicionada entre as camadas de interface de cliente e de provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="66eef-109">The layer that represents the MAPI subsystem is positioned between the client and service provider interface layers.</span></span> <span data-ttu-id="66eef-110">A camada MAPI contém todos os objetos que o MAPI implementa para clientes ou provedores de serviço a serem usados.</span><span class="sxs-lookup"><span data-stu-id="66eef-110">The MAPI layer contains all of the objects that MAPI implements for clients or service providers to use.</span></span> 
  
<span data-ttu-id="66eef-111">A ilustração a seguir mostra onde cada um dos objetos MAPI se ajusta à arquitetura MAPI.</span><span class="sxs-lookup"><span data-stu-id="66eef-111">The following illustration shows where each of the MAPI objects fits into the MAPI architecture.</span></span> <span data-ttu-id="66eef-112">Os objetos são representados com os nomes de suas interfaces derivadas.</span><span class="sxs-lookup"><span data-stu-id="66eef-112">The objects are represented with the names of their derived interfaces.</span></span> <span data-ttu-id="66eef-113">Por exemplo, um objeto de coletor de aviso é mostrado como [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md), a interface derivada de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) e que cada objeto de coletor de aviso é implementado.</span><span class="sxs-lookup"><span data-stu-id="66eef-113">For example, an advise sink object is shown as [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), the interface that derives from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) and that every advise sink object implements.</span></span> <span data-ttu-id="66eef-114">As interfaces que as camadas de ponte são usadas ou implementadas por vários componentes.</span><span class="sxs-lookup"><span data-stu-id="66eef-114">The interfaces that bridge layers are either used or implemented by multiple components.</span></span> <span data-ttu-id="66eef-115">Embora a camada MAPI pareça separar as camadas de cliente e provedor, indicando que toda a comunicação deve fluir por MAPI, esse não é o caso.</span><span class="sxs-lookup"><span data-stu-id="66eef-115">Although the MAPI layer appears to separate the client and provider layers, implying that all communication must flow through MAPI, this is not the case.</span></span> <span data-ttu-id="66eef-116">Os clientes podem e se comunicam diretamente com os objetos do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="66eef-116">Clients can and do communicate directly to service provider objects.</span></span> 
  
<span data-ttu-id="66eef-117">**Object layers in MAPI**</span><span class="sxs-lookup"><span data-stu-id="66eef-117">**Object layers in MAPI**</span></span>
  
<span data-ttu-id="66eef-118">![Camadas de objeto no MAPI] (media/amapi_38.gif "Camadas de objeto no MAPI")</span><span class="sxs-lookup"><span data-stu-id="66eef-118">![Object layers in MAPI](media/amapi_38.gif "Object layers in MAPI")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="66eef-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="66eef-119">See also</span></span>

- [<span data-ttu-id="66eef-120">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="66eef-120">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)
- [<span data-ttu-id="66eef-121">Visão geral de interface e objeto MAPI</span><span class="sxs-lookup"><span data-stu-id="66eef-121">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

