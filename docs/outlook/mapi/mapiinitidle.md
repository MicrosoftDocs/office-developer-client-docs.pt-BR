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
ms.openlocfilehash: e4f4cdd1d0ed2e03d49f471e6e91464b7973c920
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767993"
---
# <a name="mapiinitidle"></a><span data-ttu-id="4405f-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="4405f-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="4405f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4405f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4405f-105">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="4405f-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4405f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4405f-106">Header file:</span></span>  <br/> |<span data-ttu-id="4405f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4405f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4405f-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="4405f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4405f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4405f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4405f-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="4405f-110">Called by:</span></span>  <br/> |<span data-ttu-id="4405f-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="4405f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="4405f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4405f-112">Parameters</span></span>

 <span data-ttu-id="4405f-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="4405f-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="4405f-114">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4405f-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4405f-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4405f-115">Return value</span></span>

<span data-ttu-id="4405f-116">A função **MAPIInitIdle** retorna zero se a inicialização é bem-sucedida e 1, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="4405f-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="4405f-117">Se **MAPIInitIdle** for chamado várias vezes, todas as chamadas adicionais êxito, mas são ignoradas, exceto to incrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="4405f-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4405f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4405f-118">Remarks</span></span>

<span data-ttu-id="4405f-119">Um aplicativo cliente ou um provedor de serviços deve chamar **MAPIInitIdle** antes de chamar qualquer outra função de mecanismo ocioso.</span><span class="sxs-lookup"><span data-stu-id="4405f-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="4405f-120">Todas as chamadas para **MAPIInitIdle** devem ser iguais por uma chamada subsequente para [MAPIDeInitIdle](mapideinitidle.md)ou o mecanismo de ocioso é deixado em execução para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="4405f-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="4405f-121">As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com ociosas rotinas com base no protótipo de função [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="4405f-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="4405f-122">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="4405f-122">**Idle routine function**</span></span>|<span data-ttu-id="4405f-123">**Uso**</span><span class="sxs-lookup"><span data-stu-id="4405f-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4405f-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="4405f-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="4405f-125">Altera as características de uma rotina de ociosidade registrada.</span><span class="sxs-lookup"><span data-stu-id="4405f-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="4405f-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="4405f-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="4405f-127">Remove uma rotina de ociosidade registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="4405f-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="4405f-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="4405f-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="4405f-129">Desativa ou ativa novamente uma rotina de ociosidade registrada sem removê-lo a partir do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="4405f-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="4405f-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="4405f-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="4405f-131">Adiciona uma rotina de ociosidade ao sistema de MAPI, com ou sem ativá-lo.</span><span class="sxs-lookup"><span data-stu-id="4405f-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="4405f-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="4405f-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="4405f-133">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="4405f-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="4405f-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="4405f-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="4405f-135">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="4405f-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="4405f-136">Quando todas as tarefas de primeiro plano para a plataforma ficam ociosas, o mecanismo de ociosidade de MAPI chama a rotina de ocioso de prioridade mais alta que está pronta para executar.</span><span class="sxs-lookup"><span data-stu-id="4405f-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="4405f-137">Não há nenhuma garantia de chamar ordem entre as rotinas de ociosidade da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="4405f-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

