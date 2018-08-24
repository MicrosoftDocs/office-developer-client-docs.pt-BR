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
ms.openlocfilehash: cbad4b903592f83fc7d72fde21f149c9835f2e23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575634"
---
# <a name="fnidle"></a><span data-ttu-id="28c9a-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="28c9a-103">FNIDLE</span></span>
 
<span data-ttu-id="28c9a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28c9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28c9a-105">Define uma rotina de ociosidade chamada pelo mecanismo de ociosidade de MAPI periodicamente de acordo com a prioridade.</span><span class="sxs-lookup"><span data-stu-id="28c9a-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28c9a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="28c9a-106">Header file:</span></span>  <br/> |<span data-ttu-id="28c9a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="28c9a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="28c9a-108">Função definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="28c9a-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="28c9a-109">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="28c9a-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="28c9a-110">Função definido chamada pelo:</span><span class="sxs-lookup"><span data-stu-id="28c9a-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="28c9a-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="28c9a-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="28c9a-112">Tipo de ponteiro correspondente:</span><span class="sxs-lookup"><span data-stu-id="28c9a-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="28c9a-113">PFNIDLE</span><span class="sxs-lookup"><span data-stu-id="28c9a-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="28c9a-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28c9a-114">Parameters</span></span>

 <span data-ttu-id="28c9a-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="28c9a-115">_lpvContext_</span></span>
  
> <span data-ttu-id="28c9a-116">[in] Ponteiro para um bloco de memória que MAPI passa para a rotina ociosa horário ele chama a ele.</span><span class="sxs-lookup"><span data-stu-id="28c9a-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="28c9a-117">Esse ponteiro é passado para o mecanismo de ociosidade de MAPI no parâmetro _pvIdleParam_ por [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span><span class="sxs-lookup"><span data-stu-id="28c9a-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="28c9a-118">Os dados no bloco de memória poderá fornecer contexto para a chamada para a rotina ociosa, como o objeto a ser operado, ou o estado atual de uma operação demorada.</span><span class="sxs-lookup"><span data-stu-id="28c9a-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="28c9a-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="28c9a-119">Return value</span></span>

<span data-ttu-id="28c9a-120">FALSO</span><span class="sxs-lookup"><span data-stu-id="28c9a-120">FALSE</span></span> 
  
> <span data-ttu-id="28c9a-121">Uma rotina de ociosidade com o protótipo **FNIDLE** deve sempre retornam FALSE.</span><span class="sxs-lookup"><span data-stu-id="28c9a-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="28c9a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="28c9a-122">Remarks</span></span>

<span data-ttu-id="28c9a-123">A funcionalidade específica de rotina ociosa é determinada Implementando o aplicativo cliente ou provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="28c9a-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="28c9a-124">O cliente ou o provedor deverá limitar o tempo de execução de cada estado de uma rotina de ocioso.</span><span class="sxs-lookup"><span data-stu-id="28c9a-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="28c9a-125">Cada estado deve realizar uma quantidade mínima de processamento, atualize o estado atual nos dados de contexto apontados pela _lpvContext_e retornar ao mecanismo de ociosidade de MAPI.</span><span class="sxs-lookup"><span data-stu-id="28c9a-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="28c9a-126">O cliente ou o provedor deve chamar a função MAPI [MAPIInitIdle](mapiinitidle.md) para que ele possa registrar sua própria rotina ociosa com uma chamada para a função [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) .</span><span class="sxs-lookup"><span data-stu-id="28c9a-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="28c9a-127">As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com ociosas rotinas com base no protótipo de função FNIDLE:</span><span class="sxs-lookup"><span data-stu-id="28c9a-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="28c9a-128">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="28c9a-128">**Idle routine function**</span></span>|<span data-ttu-id="28c9a-129">**Uso**</span><span class="sxs-lookup"><span data-stu-id="28c9a-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28c9a-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="28c9a-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="28c9a-131">Altera as características de uma rotina de ociosidade registrada.</span><span class="sxs-lookup"><span data-stu-id="28c9a-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="28c9a-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="28c9a-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="28c9a-133">Remove uma rotina de ociosidade registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="28c9a-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="28c9a-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="28c9a-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="28c9a-135">Desativa ou ativa novamente uma rotina de ociosidade registrada sem removê-lo a partir do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="28c9a-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="28c9a-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="28c9a-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="28c9a-137">Adiciona uma rotina de ociosidade ao sistema de MAPI, com ou sem ativá-lo.</span><span class="sxs-lookup"><span data-stu-id="28c9a-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="28c9a-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="28c9a-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="28c9a-139">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="28c9a-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="28c9a-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="28c9a-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="28c9a-141">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="28c9a-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="28c9a-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** tomar como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="28c9a-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="28c9a-143">Quando todas as tarefas de primeiro plano para a plataforma ficam ociosas, o mecanismo de ociosidade de MAPI chama a rotina de ocioso de prioridade mais alta que está pronta para executar.</span><span class="sxs-lookup"><span data-stu-id="28c9a-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="28c9a-144">Não há nenhuma garantia de chamar ordem entre as rotinas de ociosidade da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="28c9a-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

