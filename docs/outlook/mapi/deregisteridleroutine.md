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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 85161fb87e798bbb03b267f9760870da1246e48d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766401"
---
# <a name="deregisteridleroutine"></a><span data-ttu-id="112bb-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="112bb-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="112bb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="112bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="112bb-105">Remove um [FNIDLE](fnidle.md) com base em rotina ociosa do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="112bb-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="112bb-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="112bb-106">Header file:</span></span>  <br/> |<span data-ttu-id="112bb-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="112bb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="112bb-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="112bb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="112bb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="112bb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="112bb-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="112bb-110">Called by:</span></span>  <br/> |<span data-ttu-id="112bb-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="112bb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="112bb-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="112bb-112">Parameters</span></span>

 <span data-ttu-id="112bb-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="112bb-113">_ftg_</span></span>
  
> <span data-ttu-id="112bb-114">[in] Marca de função que identifica a rotina ociosa a ser removido.</span><span class="sxs-lookup"><span data-stu-id="112bb-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="112bb-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="112bb-115">Return value</span></span>

<span data-ttu-id="112bb-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="112bb-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="112bb-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="112bb-117">Remarks</span></span>

<span data-ttu-id="112bb-118">Qualquer tarefa em um aplicativo cliente ou de um provedor de serviços pode cancelar o registro de qualquer rotina ociosa para o qual ele tem um parâmetro válido _ftg_ .</span><span class="sxs-lookup"><span data-stu-id="112bb-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="112bb-119">Em particular, uma rotina de ociosidade pode cancelar o registro em si.</span><span class="sxs-lookup"><span data-stu-id="112bb-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="112bb-120">As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com ociosas rotinas com base no protótipo de função [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="112bb-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="112bb-121">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="112bb-121">**Idle routine function**</span></span>|<span data-ttu-id="112bb-122">**Usage**</span><span class="sxs-lookup"><span data-stu-id="112bb-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="112bb-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="112bb-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="112bb-124">Altera as características de uma rotina de ociosidade registrada.</span><span class="sxs-lookup"><span data-stu-id="112bb-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="112bb-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="112bb-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="112bb-126">Remove uma rotina de ociosidade registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="112bb-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="112bb-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="112bb-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="112bb-128">Desativa ou ativa novamente uma rotina de ociosidade registrada sem removê-lo a partir do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="112bb-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="112bb-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="112bb-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="112bb-130">Adiciona uma rotina de ociosidade ao sistema de MAPI, com ou sem ativá-lo.</span><span class="sxs-lookup"><span data-stu-id="112bb-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="112bb-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="112bb-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="112bb-132">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="112bb-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="112bb-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="112bb-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="112bb-134">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="112bb-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="112bb-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** tomar como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="112bb-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="112bb-136">Quando todas as tarefas de primeiro plano para a plataforma ficam ociosas, o mecanismo de ociosidade de MAPI chama a rotina de ocioso de prioridade mais alta que está pronta para executar.</span><span class="sxs-lookup"><span data-stu-id="112bb-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="112bb-137">Não há nenhuma garantia de chamar ordem entre as rotinas de ociosidade da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="112bb-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="112bb-138">Depois que a rotina ociosa é o registro cancelada, o mecanismo de ociosidade não chamá-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="112bb-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="112bb-139">Qualquer implementação que chama **DeregisterIdleRoutine** deve desalocar qualquer blocos de memória ao qual ele passado ponteiros para o mecanismo de ociosidade usar em sua chamada original para a função **FtgRegisterIdleRoutine** .</span><span class="sxs-lookup"><span data-stu-id="112bb-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

