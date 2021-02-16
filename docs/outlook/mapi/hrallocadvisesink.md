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
ms.openlocfilehash: 7f9873fe8e1825c68d4540cc1d093171e9f95727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428897"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="73238-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="73238-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="73238-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73238-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73238-105">Cria um objeto sink de aviso, dado um contexto especificado pela implementação da chamada e uma função de retorno de chamada a ser disparada por uma notificação de evento.</span><span class="sxs-lookup"><span data-stu-id="73238-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73238-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="73238-106">Header file:</span></span>  <br/> |<span data-ttu-id="73238-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="73238-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="73238-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="73238-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="73238-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="73238-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="73238-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="73238-110">Called by:</span></span>  <br/> |<span data-ttu-id="73238-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="73238-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="73238-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73238-112">Parameters</span></span>

 <span data-ttu-id="73238-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="73238-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="73238-114">[in] Ponteiro para uma função de retorno de chamada com base no protótipo [NOTIFCALLBACK](notifcallback.md) que MAPI deve chamar quando um evento de notificação ocorre para o evento de aviso recém-criado.</span><span class="sxs-lookup"><span data-stu-id="73238-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="73238-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="73238-115">_lpvContext_</span></span>
  
> <span data-ttu-id="73238-116">[in] Ponteiro para dados do chamador passados para a função de retorno de chamada quando MAPI o chama.</span><span class="sxs-lookup"><span data-stu-id="73238-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="73238-117">Os dados do chamador podem representar um endereço significativo para o cliente ou provedor.</span><span class="sxs-lookup"><span data-stu-id="73238-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="73238-118">Normalmente, para código C++, o parâmetro  _lpvContext_ representa um ponteiro para o endereço de um objeto.</span><span class="sxs-lookup"><span data-stu-id="73238-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="73238-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="73238-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="73238-120">[out] Ponteiro para um ponteiro para um objeto de evento de aconselhá-lo.</span><span class="sxs-lookup"><span data-stu-id="73238-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="73238-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="73238-121">Return value</span></span>

<span data-ttu-id="73238-122">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="73238-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="73238-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="73238-123">Remarks</span></span>

<span data-ttu-id="73238-124">Para usar a função **HrAllocAdviseSink,** um aplicativo cliente ou provedor de serviços cria um objeto para receber notificações, cria uma função de retorno de chamada de notificação com base no protótipo da função [NOTIFCALLBACK](notifcallback.md) que vai com esse objeto e passa um ponteiro para o objeto na função **HrAllocAdviseSink** como o valor _lpvContext._</span><span class="sxs-lookup"><span data-stu-id="73238-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="73238-125">Fazer isso executa uma notificação; e como parte do processo de notificação, MAPI chama a função de retorno de chamada com o ponteiro do objeto como o contexto.</span><span class="sxs-lookup"><span data-stu-id="73238-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="73238-126">O MAPI implementa seu mecanismo de notificação de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="73238-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="73238-127">Em C++, o retorno de chamada de notificação pode ser um método de objeto.</span><span class="sxs-lookup"><span data-stu-id="73238-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="73238-128">Se o objeto que está gerando a notificação não estiver presente, o cliente ou provedor que está solicitando a notificação deve manter uma contagem de referência separada para esse objeto para o sink de aviso do objeto.</span><span class="sxs-lookup"><span data-stu-id="73238-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="73238-129">**HrAllocAdviseSink** deve ser usado com moderação; é mais seguro para os clientes criarem seus próprios aconselhá-los.</span><span class="sxs-lookup"><span data-stu-id="73238-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

