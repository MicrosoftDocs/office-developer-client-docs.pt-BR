---
title: MAPIInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIInitIdle
api_type:
- COM
ms.assetid: b6de7c6a-f2e7-4248-adea-d354924a8bbf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b07c40882c0b9974c71eeb03123e7025b948a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432440"
---
# <a name="mapiinitidle"></a><span data-ttu-id="2e956-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="2e956-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="2e956-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e956-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e956-105">Inicializa o mecanismo ocioso MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="2e956-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e956-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2e956-106">Header file:</span></span>  <br/> |<span data-ttu-id="2e956-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2e956-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2e956-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2e956-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2e956-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2e956-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2e956-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="2e956-110">Called by:</span></span>  <br/> |<span data-ttu-id="2e956-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="2e956-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="2e956-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e956-112">Parameters</span></span>

 <span data-ttu-id="2e956-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="2e956-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="2e956-114">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2e956-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2e956-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2e956-115">Return value</span></span>

<span data-ttu-id="2e956-116">A **função MAPIInitIdle** retornará zero se a inicialização for bem-sucedida e 1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="2e956-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="2e956-117">Se **MAPIInitIdle** for chamado várias vezes, todas as chamadas adicionais serão bem-sucedidas, mas serão ignoradas, exceto para incrementar a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="2e956-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2e956-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e956-118">Remarks</span></span>

<span data-ttu-id="2e956-119">Um aplicativo cliente ou provedor de serviços deve chamar **MAPIInitIdle** antes de chamar qualquer outra função de mecanismo ocioso.</span><span class="sxs-lookup"><span data-stu-id="2e956-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="2e956-120">Cada chamada para **MAPIInitIdle** deve ser a mesma de uma chamada subsequente para [MAPIDeInitIdle](mapideinitidle.md)ou o mecanismo ocioso é deixado em execução para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="2e956-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="2e956-121">As funções a seguir lidam com o mecanismo ocioso MAPI e com rotinas ociosas com base no protótipo de [função FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="2e956-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="2e956-122">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="2e956-122">**Idle routine function**</span></span>|<span data-ttu-id="2e956-123">**Uso**</span><span class="sxs-lookup"><span data-stu-id="2e956-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e956-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2e956-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="2e956-125">Altera as características de uma rotina ociosa registrada.</span><span class="sxs-lookup"><span data-stu-id="2e956-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="2e956-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2e956-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="2e956-127">Remove uma rotina ociosa registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="2e956-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="2e956-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2e956-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="2e956-129">Desabilita ou reabilitar uma rotina ociosa registrada sem removê-la do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="2e956-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="2e956-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2e956-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="2e956-131">Adiciona uma rotina ociosa ao sistema MAPI, com ou sem habilita-la.</span><span class="sxs-lookup"><span data-stu-id="2e956-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="2e956-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="2e956-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="2e956-133">Desliga o mecanismo ocioso MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="2e956-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="2e956-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="2e956-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="2e956-135">Inicializa o mecanismo ocioso MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="2e956-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="2e956-136">Quando todas as tarefas em primeiro plano da plataforma ficam ociosas, o mecanismo ocioso MAPI chama a rotina ociosa de prioridade mais alta que está pronta para ser executada.</span><span class="sxs-lookup"><span data-stu-id="2e956-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="2e956-137">Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="2e956-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

