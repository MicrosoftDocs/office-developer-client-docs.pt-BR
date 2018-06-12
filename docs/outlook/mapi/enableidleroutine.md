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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 00b5c123e588636654fb4287cc7b45500d47d89c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766493"
---
# <a name="enableidleroutine"></a><span data-ttu-id="131ae-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="131ae-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="131ae-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="131ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="131ae-105">Habilita ou desabilita uma rotina de ociosidade [FNIDLE](fnidle.md) com base.</span><span class="sxs-lookup"><span data-stu-id="131ae-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="131ae-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="131ae-106">Header file:</span></span>  <br/> |<span data-ttu-id="131ae-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="131ae-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="131ae-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="131ae-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="131ae-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="131ae-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="131ae-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="131ae-110">Called by:</span></span>  <br/> |<span data-ttu-id="131ae-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="131ae-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="131ae-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="131ae-112">Parameters</span></span>

 <span data-ttu-id="131ae-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="131ae-113">_ftg_</span></span>
  
> <span data-ttu-id="131ae-114">[in] Marca de função que identifica a rotina ociosa para ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="131ae-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="131ae-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="131ae-115">_fEnable_</span></span>
  
> <span data-ttu-id="131ae-116">[in] Contém TRUE se o mecanismo de ociosidade deve habilitar a rotina ociosa ou FALSE se ele deve desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="131ae-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="131ae-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="131ae-117">Return value</span></span>

<span data-ttu-id="131ae-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="131ae-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="131ae-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="131ae-119">Remarks</span></span>

<span data-ttu-id="131ae-120">As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com ociosas rotinas com base no protótipo de função [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="131ae-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="131ae-121">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="131ae-121">**Idle routine function**</span></span>|<span data-ttu-id="131ae-122">**Usage**</span><span class="sxs-lookup"><span data-stu-id="131ae-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="131ae-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="131ae-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="131ae-124">Altera as características de uma rotina de ociosidade registrada.</span><span class="sxs-lookup"><span data-stu-id="131ae-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="131ae-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="131ae-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="131ae-126">Remove uma rotina de ociosidade registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="131ae-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="131ae-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="131ae-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="131ae-128">Desativa ou ativa novamente uma rotina de ociosidade registrada sem removê-lo a partir do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="131ae-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="131ae-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="131ae-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="131ae-130">Adiciona uma rotina de ociosidade ao sistema de MAPI, com ou sem ativá-lo.</span><span class="sxs-lookup"><span data-stu-id="131ae-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="131ae-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="131ae-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="131ae-132">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="131ae-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="131ae-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="131ae-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="131ae-134">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="131ae-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="131ae-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** tomar como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="131ae-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="131ae-136">Quando todas as tarefas de primeiro plano para a plataforma ficam ociosas, o mecanismo de ociosidade de MAPI chama a rotina de ocioso de prioridade mais alta que está pronta para executar.</span><span class="sxs-lookup"><span data-stu-id="131ae-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="131ae-137">Não há nenhuma garantia de chamar ordem entre as rotinas de ociosidade da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="131ae-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

