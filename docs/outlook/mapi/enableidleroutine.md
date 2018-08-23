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
ms.openlocfilehash: c53bd63e60281e999d0d379913b3609e9472a40e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579274"
---
# <a name="enableidleroutine"></a><span data-ttu-id="2dd48-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2dd48-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="2dd48-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2dd48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2dd48-105">Habilita ou desabilita uma rotina de ociosidade [FNIDLE](fnidle.md) com base.</span><span class="sxs-lookup"><span data-stu-id="2dd48-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2dd48-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2dd48-106">Header file:</span></span>  <br/> |<span data-ttu-id="2dd48-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2dd48-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2dd48-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="2dd48-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2dd48-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2dd48-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2dd48-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="2dd48-110">Called by:</span></span>  <br/> |<span data-ttu-id="2dd48-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="2dd48-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="2dd48-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2dd48-112">Parameters</span></span>

 <span data-ttu-id="2dd48-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="2dd48-113">_ftg_</span></span>
  
> <span data-ttu-id="2dd48-114">[in] Marca de função que identifica a rotina ociosa para ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="2dd48-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="2dd48-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="2dd48-115">_fEnable_</span></span>
  
> <span data-ttu-id="2dd48-116">[in] Contém TRUE se o mecanismo de ociosidade deve habilitar a rotina ociosa ou FALSE se ele deve desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="2dd48-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2dd48-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2dd48-117">Return value</span></span>

<span data-ttu-id="2dd48-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2dd48-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2dd48-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2dd48-119">Remarks</span></span>

<span data-ttu-id="2dd48-120">As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com ociosas rotinas com base no protótipo de função [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="2dd48-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="2dd48-121">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="2dd48-121">**Idle routine function**</span></span>|<span data-ttu-id="2dd48-122">**Uso**</span><span class="sxs-lookup"><span data-stu-id="2dd48-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2dd48-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2dd48-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="2dd48-124">Altera as características de uma rotina de ociosidade registrada.</span><span class="sxs-lookup"><span data-stu-id="2dd48-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="2dd48-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2dd48-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="2dd48-126">Remove uma rotina de ociosidade registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="2dd48-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="2dd48-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="2dd48-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="2dd48-128">Desativa ou ativa novamente uma rotina de ociosidade registrada sem removê-lo a partir do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="2dd48-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="2dd48-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2dd48-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="2dd48-130">Adiciona uma rotina de ociosidade ao sistema de MAPI, com ou sem ativá-lo.</span><span class="sxs-lookup"><span data-stu-id="2dd48-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="2dd48-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="2dd48-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="2dd48-132">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="2dd48-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="2dd48-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="2dd48-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="2dd48-134">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="2dd48-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="2dd48-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** tomar como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="2dd48-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="2dd48-136">Quando todas as tarefas de primeiro plano para a plataforma ficam ociosas, o mecanismo de ociosidade de MAPI chama a rotina de ocioso de prioridade mais alta que está pronta para executar.</span><span class="sxs-lookup"><span data-stu-id="2dd48-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="2dd48-137">Não há nenhuma garantia de chamar ordem entre as rotinas de ociosidade da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="2dd48-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

