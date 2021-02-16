---
title: DeregisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DeregisterIdleRoutine
api_type:
- COM
ms.assetid: a8ada6fe-9963-4c25-b4b4-db77f9517368
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 62231a900dbe01ebe1e848355226c0589072cd42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404558"
---
# <a name="deregisteridleroutine"></a><span data-ttu-id="2f4f5-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2f4f5-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="2f4f5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f4f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f4f5-105">Remove uma rotina [ociosa baseada em FNIDLE](fnidle.md) do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="2f4f5-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f4f5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2f4f5-106">Header file:</span></span>  <br/> |<span data-ttu-id="2f4f5-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2f4f5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2f4f5-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2f4f5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2f4f5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2f4f5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2f4f5-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="2f4f5-110">Called by:</span></span>  <br/> |<span data-ttu-id="2f4f5-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="2f4f5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="2f4f5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f4f5-112">Parameters</span></span>

 <span data-ttu-id="2f4f5-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="2f4f5-113">_ftg_</span></span>
  
> <span data-ttu-id="2f4f5-114">[in] Marca de função que identifica a rotina ociosa a ser removida.</span><span class="sxs-lookup"><span data-stu-id="2f4f5-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2f4f5-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2f4f5-115">Return value</span></span>

<span data-ttu-id="2f4f5-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2f4f5-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2f4f5-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f4f5-117">Remarks</span></span>

<span data-ttu-id="2f4f5-118">Qualquer tarefa em um aplicativo cliente ou provedor de serviços pode desregister qualquer rotina ociosa para a qual tenha um parâmetro  _ftg_ válido.</span><span class="sxs-lookup"><span data-stu-id="2f4f5-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="2f4f5-119">Em particular, uma rotina ociosa pode se desregister.</span><span class="sxs-lookup"><span data-stu-id="2f4f5-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="2f4f5-120">As funções a seguir lidam com o mecanismo ocioso MAPI e com rotinas ociosas com base no protótipo de [função FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="2f4f5-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="2f4f5-121">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="2f4f5-121">**Idle routine function**</span></span>|<span data-ttu-id="2f4f5-122">**Uso**</span><span class="sxs-lookup"><span data-stu-id="2f4f5-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f4f5-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2f4f5-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="2f4f5-124">Altera as características de uma rotina ociosa registrada.</span><span class="sxs-lookup"><span data-stu-id="2f4f5-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="2f4f5-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="2f4f5-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="2f4f5-126">Remove uma rotina ociosa registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="2f4f5-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="2f4f5-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2f4f5-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="2f4f5-128">Desabilita ou reabilitar uma rotina ociosa registrada sem removê-la do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="2f4f5-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="2f4f5-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2f4f5-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="2f4f5-130">Adiciona uma rotina ociosa ao sistema MAPI, com ou sem habilita-la.</span><span class="sxs-lookup"><span data-stu-id="2f4f5-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="2f4f5-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="2f4f5-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="2f4f5-132">Desliga o mecanismo ocioso MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="2f4f5-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="2f4f5-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="2f4f5-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="2f4f5-134">Inicializa o mecanismo ocioso MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="2f4f5-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="2f4f5-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine** e **EnableIdleRoutine** levam como parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="2f4f5-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="2f4f5-136">Quando todas as tarefas em primeiro plano da plataforma ficam ociosas, o mecanismo ocioso MAPI chama a rotina ociosa de prioridade mais alta que está pronta para ser executada.</span><span class="sxs-lookup"><span data-stu-id="2f4f5-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="2f4f5-137">Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="2f4f5-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="2f4f5-138">Depois que a rotina ociosa for desregisterada, o mecanismo ocioso não a chamará novamente.</span><span class="sxs-lookup"><span data-stu-id="2f4f5-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="2f4f5-139">Qualquer implementação que chame **DeregisterIdleRoutine** deve desalocar todos os blocos de memória para os quais ele passou ponteiros para o mecanismo ocioso usar em sua chamada original para a função **FtgRegisterIdleRoutine.**</span><span class="sxs-lookup"><span data-stu-id="2f4f5-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

