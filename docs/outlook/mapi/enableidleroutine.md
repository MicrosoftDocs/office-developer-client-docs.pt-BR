---
title: EnableIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EnableIdleRoutine
api_type:
- COM
ms.assetid: 332ea831-bdf9-4dbd-b9c7-a80f8ba11b3b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e04c872762665f4b3a22559dc2ed1504e7b8f9af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410218"
---
# <a name="enableidleroutine"></a><span data-ttu-id="2741d-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2741d-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="2741d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2741d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2741d-105">Habilita ou desabilita uma rotina ociosa baseada em [FNIDLE](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="2741d-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2741d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2741d-106">Header file:</span></span>  <br/> |<span data-ttu-id="2741d-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="2741d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2741d-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2741d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2741d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2741d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2741d-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="2741d-110">Called by:</span></span>  <br/> |<span data-ttu-id="2741d-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="2741d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="2741d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2741d-112">Parameters</span></span>

 <span data-ttu-id="2741d-113">_FTG_</span><span class="sxs-lookup"><span data-stu-id="2741d-113">_ftg_</span></span>
  
> <span data-ttu-id="2741d-114">no Marca de função que identifica a rotina ociosa a ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="2741d-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="2741d-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="2741d-115">_fEnable_</span></span>
  
> <span data-ttu-id="2741d-116">no Contém TRUE se o mecanismo ocioso deve habilitar a rotina ociosa ou FALSE se ela deve desabilitá-la.</span><span class="sxs-lookup"><span data-stu-id="2741d-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2741d-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2741d-117">Return value</span></span>

<span data-ttu-id="2741d-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2741d-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2741d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2741d-119">Remarks</span></span>

<span data-ttu-id="2741d-120">As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com rotinas ociosas com base no protótipo de função do [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="2741d-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="2741d-121">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="2741d-121">**Idle routine function**</span></span>|<span data-ttu-id="2741d-122">**Usage**</span><span class="sxs-lookup"><span data-stu-id="2741d-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2741d-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2741d-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="2741d-124">Altera as características de uma rotina de ociosidade registrada.</span><span class="sxs-lookup"><span data-stu-id="2741d-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="2741d-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2741d-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="2741d-126">Remove uma rotina de ociosidade registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="2741d-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="2741d-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="2741d-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="2741d-128">Desabilita ou habilita novamente uma rotina de ociosidade registrada sem removê-la do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="2741d-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="2741d-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2741d-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="2741d-130">Adiciona uma rotina ociosa ao sistema MAPI, com ou sem ativá-la.</span><span class="sxs-lookup"><span data-stu-id="2741d-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="2741d-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="2741d-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="2741d-132">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="2741d-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="2741d-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="2741d-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="2741d-134">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="2741d-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="2741d-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** aceitam como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="2741d-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="2741d-136">Quando todas as tarefas de primeiro plano para a plataforma ficarem ociosas, o mecanismo de ociosidade de MAPI chamará a rotina de ociosidade de prioridade mais alta que está pronta para ser executada.</span><span class="sxs-lookup"><span data-stu-id="2741d-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="2741d-137">Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="2741d-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

