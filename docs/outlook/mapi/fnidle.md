---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 534f4da15bba5f38bec4cde91206694f8691cbc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412377"
---
# <a name="fnidle"></a><span data-ttu-id="5ee0b-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="5ee0b-103">FNIDLE</span></span>
 
<span data-ttu-id="5ee0b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ee0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ee0b-105">Define uma rotina ociosa que o mecanismo ocioso MAPI chama periodicamente de acordo com a prioridade.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ee0b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5ee0b-106">Header file:</span></span>  <br/> |<span data-ttu-id="5ee0b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5ee0b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5ee0b-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="5ee0b-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="5ee0b-109">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="5ee0b-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="5ee0b-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="5ee0b-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="5ee0b-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="5ee0b-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="5ee0b-112">Tipo de ponteiro correspondente:</span><span class="sxs-lookup"><span data-stu-id="5ee0b-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="5ee0b-113">PFNIDLE</span><span class="sxs-lookup"><span data-stu-id="5ee0b-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="5ee0b-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ee0b-114">Parameters</span></span>

 <span data-ttu-id="5ee0b-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="5ee0b-115">_lpvContext_</span></span>
  
> <span data-ttu-id="5ee0b-116">[in] Ponteiro para um bloco de memória que o MAPI passa para a rotina ociosa sempre que o chama.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="5ee0b-117">Esse ponteiro é passado para o mecanismo ocioso MAPI no parâmetro  _pvIdleParam_ pelo [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span><span class="sxs-lookup"><span data-stu-id="5ee0b-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="5ee0b-118">Os dados no bloco de memória podem fornecer contexto para a chamada para a rotina ociosa, como qual objeto operar ou o estado atual de uma operação demorada.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5ee0b-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5ee0b-119">Return value</span></span>

<span data-ttu-id="5ee0b-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="5ee0b-120">FALSE</span></span> 
  
> <span data-ttu-id="5ee0b-121">Uma rotina ociosa com o **protótipo FNIDLE** sempre deve retornar FALSE.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5ee0b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ee0b-122">Remarks</span></span>

<span data-ttu-id="5ee0b-123">A funcionalidade específica da rotina ociosa é determinada pela implementação do aplicativo cliente ou do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="5ee0b-124">O cliente ou provedor deve limitar o tempo de execução de cada estado de uma rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="5ee0b-125">Cada estado deve executar uma quantidade mínima de processamento, atualizar o estado atual nos dados de contexto apontados por  _lpvContext_ e retornar ao mecanismo ocioso MAPI.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="5ee0b-126">O cliente ou provedor deve chamar a função [MAPIInitIdle](mapiinitidle.md) antes de registrar sua própria rotina ociosa com uma chamada para a função [FtgRegisterIdleRoutine.](ftgregisteridleroutine.md)</span><span class="sxs-lookup"><span data-stu-id="5ee0b-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="5ee0b-127">As funções a seguir lidam com o mecanismo ocioso MAPI e com rotinas ociosas com base no protótipo de função FNIDLE:</span><span class="sxs-lookup"><span data-stu-id="5ee0b-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="5ee0b-128">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="5ee0b-128">**Idle routine function**</span></span>|<span data-ttu-id="5ee0b-129">**Uso**</span><span class="sxs-lookup"><span data-stu-id="5ee0b-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5ee0b-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5ee0b-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="5ee0b-131">Altera as características de uma rotina ociosa registrada.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="5ee0b-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5ee0b-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="5ee0b-133">Remove uma rotina ociosa registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="5ee0b-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5ee0b-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="5ee0b-135">Desabilita ou reabilitar uma rotina ociosa registrada sem removê-la do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="5ee0b-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5ee0b-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="5ee0b-137">Adiciona uma rotina ociosa ao sistema MAPI, com ou sem habilita-la.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="5ee0b-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="5ee0b-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="5ee0b-139">Desliga o mecanismo ocioso MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="5ee0b-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="5ee0b-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="5ee0b-141">Inicializa o mecanismo ocioso MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="5ee0b-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine** e **EnableIdleRoutine** levam como parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="5ee0b-143">Quando todas as tarefas em primeiro plano da plataforma ficam ociosas, o mecanismo ocioso MAPI chama a rotina ociosa de prioridade mais alta que está pronta para ser executada.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="5ee0b-144">Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="5ee0b-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

