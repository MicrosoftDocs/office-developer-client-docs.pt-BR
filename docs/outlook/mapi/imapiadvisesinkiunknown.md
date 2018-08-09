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
ms.openlocfilehash: c6e352288f0bf5b0a3f284441bffc522bf00b9f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766924"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="0793f-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0793f-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="0793f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0793f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0793f-105">Implementa um objeto de coletor de eventos advise para tratamento de notificação.</span><span class="sxs-lookup"><span data-stu-id="0793f-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="0793f-106">Um ponteiro para um objeto de coletor de eventos advise é passado em uma chamada ao método **Advise** de um provedor de serviços, o mecanismo usado para registrar a notificação.</span><span class="sxs-lookup"><span data-stu-id="0793f-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0793f-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0793f-107">Header file:</span></span>  <br/> |<span data-ttu-id="0793f-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0793f-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0793f-109">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="0793f-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="0793f-110">Objetos de coletor de eventos de aviso</span><span class="sxs-lookup"><span data-stu-id="0793f-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="0793f-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="0793f-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="0793f-112">Aplicativos cliente e MAPI</span><span class="sxs-lookup"><span data-stu-id="0793f-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="0793f-113">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="0793f-113">Called by:</span></span>  <br/> |<span data-ttu-id="0793f-114">Provedores de serviços e MAPI</span><span class="sxs-lookup"><span data-stu-id="0793f-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="0793f-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="0793f-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0793f-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="0793f-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="0793f-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="0793f-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="0793f-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="0793f-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0793f-119">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="0793f-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0793f-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="0793f-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="0793f-121">Responde a uma notificação, executando uma ou mais tarefas.</span><span class="sxs-lookup"><span data-stu-id="0793f-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="0793f-122">As tarefas realizadas dependem do tipo de evento e o objeto que gera a notificação.</span><span class="sxs-lookup"><span data-stu-id="0793f-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0793f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0793f-123">See also</span></span>



[<span data-ttu-id="0793f-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="0793f-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

