---
title: MAPIDeInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIDeInitIdle
api_type:
- COM
ms.assetid: f7b04486-bc48-4ba4-9f35-f021e06124bf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 74bba3ea9982838f0d010bbf106c1132df1c2c25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408205"
---
# <a name="mapideinitidle"></a><span data-ttu-id="54c53-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="54c53-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="54c53-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54c53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54c53-105">Desliga o mecanismo ocioso MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="54c53-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54c53-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="54c53-106">Header file:</span></span>  <br/> |<span data-ttu-id="54c53-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="54c53-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="54c53-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="54c53-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="54c53-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="54c53-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="54c53-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="54c53-110">Called by:</span></span>  <br/> |<span data-ttu-id="54c53-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="54c53-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="54c53-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54c53-112">Parameters</span></span>

<span data-ttu-id="54c53-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="54c53-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="54c53-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="54c53-114">Return value</span></span>

<span data-ttu-id="54c53-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="54c53-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54c53-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="54c53-116">Remarks</span></span>

<span data-ttu-id="54c53-117">Um aplicativo cliente ou provedor de serviços deve chamar **MAPIDeInitIdle** quando não precisar mais do mecanismo ocioso, por exemplo, quando estiver prestes a parar o processamento.</span><span class="sxs-lookup"><span data-stu-id="54c53-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="54c53-118">Cada chamada para [MAPIInitIdle](mapiinitidle.md) deve ser a mesma de uma chamada subsequente para **MAPIDeInitIdle** ou o mecanismo ocioso é deixado em execução para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="54c53-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="54c53-119">As funções a seguir lidam com o mecanismo ocioso MAPI e com rotinas ociosas com base no protótipo de [função FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="54c53-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="54c53-120">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="54c53-120">**Idle routine function**</span></span>|<span data-ttu-id="54c53-121">**Uso**</span><span class="sxs-lookup"><span data-stu-id="54c53-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54c53-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="54c53-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="54c53-123">Altera as características de uma rotina ociosa registrada.</span><span class="sxs-lookup"><span data-stu-id="54c53-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="54c53-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="54c53-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="54c53-125">Remove uma rotina ociosa registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="54c53-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="54c53-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="54c53-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="54c53-127">Desabilita ou reabilitar uma rotina ociosa registrada sem removê-la do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="54c53-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="54c53-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="54c53-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="54c53-129">Adiciona uma rotina ociosa ao sistema MAPI, com ou sem habilita-la.</span><span class="sxs-lookup"><span data-stu-id="54c53-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="54c53-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="54c53-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="54c53-131">Desliga o mecanismo ocioso MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="54c53-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="54c53-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="54c53-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="54c53-133">Inicializa o mecanismo ocioso MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="54c53-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="54c53-134">Quando todas as tarefas em primeiro plano para a plataforma ficam ociosas, o mecanismo ocioso MAPI chama a rotina ociosa de prioridade mais alta que está pronta para ser executada.</span><span class="sxs-lookup"><span data-stu-id="54c53-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="54c53-135">Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="54c53-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

