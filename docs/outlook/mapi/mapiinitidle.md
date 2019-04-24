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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346652"
---
# <a name="mapiinitidle"></a><span data-ttu-id="5693e-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="5693e-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="5693e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5693e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5693e-105">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="5693e-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5693e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5693e-106">Header file:</span></span>  <br/> |<span data-ttu-id="5693e-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="5693e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5693e-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5693e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5693e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5693e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5693e-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="5693e-110">Called by:</span></span>  <br/> |<span data-ttu-id="5693e-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="5693e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="5693e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5693e-112">Parameters</span></span>

 <span data-ttu-id="5693e-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="5693e-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="5693e-114">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5693e-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5693e-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5693e-115">Return value</span></span>

<span data-ttu-id="5693e-116">A função **MAPIInitIdle** retornará zero se a inicialização for bem-sucedida e 1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="5693e-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="5693e-117">Se **MAPIInitIdle** é chamado várias vezes, todas as chamadas adicionais são bem-sucedidas, mas são ignoradas, exceto para incrementar a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="5693e-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5693e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5693e-118">Remarks</span></span>

<span data-ttu-id="5693e-119">Um aplicativo cliente ou provedor de serviços deve chamar **MAPIInitIdle** antes de chamar qualquer outra função de mecanismo ociosa.</span><span class="sxs-lookup"><span data-stu-id="5693e-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="5693e-120">Cada chamada para **MAPIInitIdle** deve ser correspondida por uma chamada subsequente para [MAPIDeInitIdle](mapideinitidle.md)ou o mecanismo de ociosidade é deixado em execução para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="5693e-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="5693e-121">As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com rotinas ociosas com base no protótipo de função do [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="5693e-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="5693e-122">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="5693e-122">**Idle routine function**</span></span>|<span data-ttu-id="5693e-123">**Usage**</span><span class="sxs-lookup"><span data-stu-id="5693e-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5693e-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5693e-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="5693e-125">Altera as características de uma rotina de ociosidade registrada.</span><span class="sxs-lookup"><span data-stu-id="5693e-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="5693e-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5693e-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="5693e-127">Remove uma rotina de ociosidade registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="5693e-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="5693e-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5693e-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="5693e-129">Desabilita ou habilita novamente uma rotina de ociosidade registrada sem removê-la do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="5693e-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="5693e-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5693e-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="5693e-131">Adiciona uma rotina ociosa ao sistema MAPI, com ou sem ativá-la.</span><span class="sxs-lookup"><span data-stu-id="5693e-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="5693e-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="5693e-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="5693e-133">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="5693e-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="5693e-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="5693e-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="5693e-135">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="5693e-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="5693e-136">Quando todas as tarefas de primeiro plano para a plataforma ficarem ociosas, o mecanismo de ociosidade de MAPI chamará a rotina de ociosidade de prioridade mais alta que está pronta para ser executada.</span><span class="sxs-lookup"><span data-stu-id="5693e-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="5693e-137">Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="5693e-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

