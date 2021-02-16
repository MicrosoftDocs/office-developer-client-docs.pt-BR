---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409563"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="2f3da-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2f3da-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="2f3da-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f3da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f3da-105">Implementa um objeto sink de aviso para manipular a notificação.</span><span class="sxs-lookup"><span data-stu-id="2f3da-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="2f3da-106">Um ponteiro para um objeto sink de aviso é passado em uma chamada para o método **Advise** de um provedor de serviços, o mecanismo usado para registrar para notificação.</span><span class="sxs-lookup"><span data-stu-id="2f3da-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f3da-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2f3da-107">Header file:</span></span>  <br/> |<span data-ttu-id="2f3da-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2f3da-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2f3da-109">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="2f3da-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="2f3da-110">Avisar objetos sink</span><span class="sxs-lookup"><span data-stu-id="2f3da-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="2f3da-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2f3da-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="2f3da-112">Aplicativos cliente e MAPI</span><span class="sxs-lookup"><span data-stu-id="2f3da-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="2f3da-113">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="2f3da-113">Called by:</span></span>  <br/> |<span data-ttu-id="2f3da-114">Provedores de serviços e MAPI</span><span class="sxs-lookup"><span data-stu-id="2f3da-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="2f3da-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="2f3da-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2f3da-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="2f3da-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="2f3da-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="2f3da-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="2f3da-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="2f3da-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2f3da-119">Vtable order</span><span class="sxs-lookup"><span data-stu-id="2f3da-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2f3da-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="2f3da-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="2f3da-121">Responde a uma notificação executando uma ou mais tarefas.</span><span class="sxs-lookup"><span data-stu-id="2f3da-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="2f3da-122">As tarefas executadas dependem do tipo de evento e do objeto que gera a notificação.</span><span class="sxs-lookup"><span data-stu-id="2f3da-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f3da-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f3da-123">See also</span></span>



[<span data-ttu-id="2f3da-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="2f3da-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

