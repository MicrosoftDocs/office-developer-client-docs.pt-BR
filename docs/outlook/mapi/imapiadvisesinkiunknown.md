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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: c6e352288f0bf5b0a3f284441bffc522bf00b9f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766924"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="abc60-103">IMAPIAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="abc60-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="abc60-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="abc60-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="abc60-105">Implementa um objeto de coletor de eventos advise para tratamento de notificação.</span><span class="sxs-lookup"><span data-stu-id="abc60-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="abc60-106">Um ponteiro para um objeto de coletor de eventos advise é passado em uma chamada ao método **Advise** de um provedor de serviços, o mecanismo usado para registrar a notificação.</span><span class="sxs-lookup"><span data-stu-id="abc60-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="abc60-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="abc60-107">Header file:</span></span>  <br/> |<span data-ttu-id="abc60-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="abc60-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="abc60-109">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="abc60-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="abc60-110">Objetos de coletor de eventos de aviso</span><span class="sxs-lookup"><span data-stu-id="abc60-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="abc60-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="abc60-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="abc60-112">Aplicativos cliente e MAPI</span><span class="sxs-lookup"><span data-stu-id="abc60-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="abc60-113">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="abc60-113">Called by:</span></span>  <br/> |<span data-ttu-id="abc60-114">Provedores de serviços e MAPI</span><span class="sxs-lookup"><span data-stu-id="abc60-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="abc60-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="abc60-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="abc60-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="abc60-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="abc60-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="abc60-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="abc60-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="abc60-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="abc60-119">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="abc60-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="abc60-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="abc60-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="abc60-121">Responde a uma notificação, executando uma ou mais tarefas.</span><span class="sxs-lookup"><span data-stu-id="abc60-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="abc60-122">As tarefas realizadas dependem do tipo de evento e o objeto que gera a notificação.</span><span class="sxs-lookup"><span data-stu-id="abc60-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="abc60-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="abc60-123">See also</span></span>



[<span data-ttu-id="abc60-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="abc60-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

