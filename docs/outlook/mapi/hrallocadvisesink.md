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
# <a name="hrallocadvisesink"></a><span data-ttu-id="d08a3-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d08a3-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="d08a3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d08a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d08a3-105">Cria um objeto de coletor de aviso, dado um contexto especificado pela implementação de chamada e uma função de retorno de chamada a ser disparada por uma notificação de evento.</span><span class="sxs-lookup"><span data-stu-id="d08a3-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d08a3-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d08a3-106">Header file:</span></span>  <br/> |<span data-ttu-id="d08a3-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="d08a3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d08a3-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d08a3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d08a3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d08a3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d08a3-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="d08a3-110">Called by:</span></span>  <br/> |<span data-ttu-id="d08a3-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="d08a3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="d08a3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d08a3-112">Parameters</span></span>

 <span data-ttu-id="d08a3-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="d08a3-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="d08a3-114">no Ponteiro para uma função de retorno de chamada com base no protótipo [NOTIFCALLBACK](notifcallback.md) que o MAPI deve chamar quando ocorre um evento de notificação para o coletor de aviso recém-criado.</span><span class="sxs-lookup"><span data-stu-id="d08a3-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="d08a3-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="d08a3-115">_lpvContext_</span></span>
  
> <span data-ttu-id="d08a3-116">no Ponteiro para dados do chamador passados para a função de retorno de chamada quando o MAPI o chama.</span><span class="sxs-lookup"><span data-stu-id="d08a3-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="d08a3-117">Os dados do chamador podem representar um endereço de importância para o cliente ou provedor.</span><span class="sxs-lookup"><span data-stu-id="d08a3-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="d08a3-118">Normalmente, para o código C++, o parâmetro _lpvContext_ representa um ponteiro para o endereço de um objeto.</span><span class="sxs-lookup"><span data-stu-id="d08a3-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="d08a3-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="d08a3-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="d08a3-120">bota Ponteiro para um ponteiro para um objeto de coletor de aviso.</span><span class="sxs-lookup"><span data-stu-id="d08a3-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d08a3-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d08a3-121">Return value</span></span>

<span data-ttu-id="d08a3-122">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d08a3-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d08a3-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d08a3-123">Remarks</span></span>

<span data-ttu-id="d08a3-124">Para usar a função **HrAllocAdviseSink** , um aplicativo cliente ou provedor de serviços cria um objeto para receber notificações, cria uma função de retorno de chamada de notificação com base no protótipo da função [NOTIFCALLBACK](notifcallback.md) que acompanha esse objeto, e passa um ponteiro para o objeto na função **HrAllocAdviseSink** como o valor _lpvContext_ .</span><span class="sxs-lookup"><span data-stu-id="d08a3-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="d08a3-125">Fazer isso executará uma notificação; e como parte do processo de notificação, MAPI chama a função de retorno de chamada com o ponteiro do objeto como o contexto.</span><span class="sxs-lookup"><span data-stu-id="d08a3-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="d08a3-126">O MAPI implementa o mecanismo de notificação de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="d08a3-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="d08a3-127">No C++, o retorno de chamada de notificação pode ser um método de objeto.</span><span class="sxs-lookup"><span data-stu-id="d08a3-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="d08a3-128">Se o objeto que gera a notificação não estiver presente, o cliente ou provedor que solicitar a notificação deverá manter uma contagem de referência separada para esse objeto para o coletor de aviso do objeto.</span><span class="sxs-lookup"><span data-stu-id="d08a3-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="d08a3-129">**HrAllocAdviseSink** deve ser usado com moderação; é mais seguro que os clientes criem seus próprios coletores de aviso.</span><span class="sxs-lookup"><span data-stu-id="d08a3-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

