---
title: HrAllocAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5a5e736e8be1120f5fb90048f01fdc8a44479060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766764"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="01a17-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="01a17-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="01a17-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01a17-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01a17-105">Cria um objeto de coletor de eventos advise, recebe um contexto especificado por uma função de retorno de chamada seja disparado por uma notificação de evento e a implementação de chamada.</span><span class="sxs-lookup"><span data-stu-id="01a17-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01a17-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="01a17-106">Header file:</span></span>  <br/> |<span data-ttu-id="01a17-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="01a17-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="01a17-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="01a17-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="01a17-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="01a17-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="01a17-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="01a17-110">Called by:</span></span>  <br/> |<span data-ttu-id="01a17-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="01a17-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="01a17-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01a17-112">Parameters</span></span>

 <span data-ttu-id="01a17-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="01a17-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="01a17-114">[in] Ponteiro para uma função de retorno de chamada com base em protótipo [NOTIFCALLBACK](notifcallback.md) que MAPI é chamar quando ocorre um evento de notificação do recém-criado coletor de eventos de aviso.</span><span class="sxs-lookup"><span data-stu-id="01a17-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="01a17-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="01a17-115">_lpvContext_</span></span>
  
> <span data-ttu-id="01a17-116">[in] Ponteiro para dados do chamador passado para a função de retorno de chamada quando chamadas de MAPI-lo.</span><span class="sxs-lookup"><span data-stu-id="01a17-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="01a17-117">Os dados do chamador podem representar um endereço de significância para o cliente ou o provedor.</span><span class="sxs-lookup"><span data-stu-id="01a17-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="01a17-118">Geralmente, para código C++, o parâmetro _lpvContext_ representa um ponteiro para o endereço de um objeto.</span><span class="sxs-lookup"><span data-stu-id="01a17-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="01a17-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="01a17-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="01a17-120">[out] Ponteiro para um ponteiro para um objeto de coletor de eventos advise.</span><span class="sxs-lookup"><span data-stu-id="01a17-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="01a17-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="01a17-121">Return value</span></span>

<span data-ttu-id="01a17-122">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="01a17-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01a17-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="01a17-123">Remarks</span></span>

<span data-ttu-id="01a17-124">Para usar a função **HrAllocAdviseSink** , um aplicativo cliente ou um provedor de serviço cria um objeto para receber notificações, cria uma função de retorno de chamada de notificação com base no protótipo de função [NOTIFCALLBACK](notifcallback.md) que vai com esse objeto, e passa um ponteiro para o objeto na função **HrAllocAdviseSink** como o valor de _lpvContext_ .</span><span class="sxs-lookup"><span data-stu-id="01a17-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="01a17-125">Isso realiza uma notificação; e como parte do processo de notificação, MAPI chama a função de retorno de chamada com o ponteiro de objeto, como o contexto.</span><span class="sxs-lookup"><span data-stu-id="01a17-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="01a17-126">MAPI implementa seu mecanismo de notificação de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="01a17-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="01a17-127">Em C++, o retorno de chamada de notificação pode ser um método do objeto.</span><span class="sxs-lookup"><span data-stu-id="01a17-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="01a17-128">Se o objeto gerar a notificação não estiver presente, o cliente ou solicitar a notificação de provedor deve manter uma contagem de referência separada para aquele objeto para o objeto coletor de eventos de aviso.</span><span class="sxs-lookup"><span data-stu-id="01a17-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="01a17-129">**HrAllocAdviseSink** deve ser usado com moderação; é mais segura para os clientes criar seus próprios PIAs advise.</span><span class="sxs-lookup"><span data-stu-id="01a17-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

