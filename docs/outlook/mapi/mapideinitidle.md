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
# <a name="mapideinitidle"></a><span data-ttu-id="6259b-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="6259b-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="6259b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6259b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6259b-105">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="6259b-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6259b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6259b-106">Header file:</span></span>  <br/> |<span data-ttu-id="6259b-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="6259b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6259b-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="6259b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6259b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6259b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6259b-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="6259b-110">Called by:</span></span>  <br/> |<span data-ttu-id="6259b-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="6259b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="6259b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6259b-112">Parameters</span></span>

<span data-ttu-id="6259b-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6259b-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="6259b-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6259b-114">Return value</span></span>

<span data-ttu-id="6259b-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6259b-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6259b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6259b-116">Remarks</span></span>

<span data-ttu-id="6259b-117">Um aplicativo cliente ou provedor de serviços deve chamar **MAPIDeInitIdle** quando ele não precisar mais do mecanismo ocioso, por exemplo, quando estiver prestes a parar o processamento.</span><span class="sxs-lookup"><span data-stu-id="6259b-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="6259b-118">Cada chamada para [MAPIInitIdle](mapiinitidle.md) deve ser correspondida por uma chamada subsequente para **MAPIDeInitIdle**ou o mecanismo de ociosidade é deixado em execução para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="6259b-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="6259b-119">As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com rotinas ociosas com base no protótipo de função do [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="6259b-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="6259b-120">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="6259b-120">**Idle routine function**</span></span>|<span data-ttu-id="6259b-121">**Usage**</span><span class="sxs-lookup"><span data-stu-id="6259b-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6259b-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="6259b-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="6259b-123">Altera as características de uma rotina de ociosidade registrada.</span><span class="sxs-lookup"><span data-stu-id="6259b-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="6259b-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="6259b-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="6259b-125">Remove uma rotina de ociosidade registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="6259b-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="6259b-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="6259b-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="6259b-127">Desabilita ou habilita novamente uma rotina de ociosidade registrada sem removê-la do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="6259b-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="6259b-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="6259b-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="6259b-129">Adiciona uma rotina ociosa ao sistema MAPI, com ou sem ativá-la.</span><span class="sxs-lookup"><span data-stu-id="6259b-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="6259b-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="6259b-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="6259b-131">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="6259b-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="6259b-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="6259b-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="6259b-133">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="6259b-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="6259b-134">Quando todas as tarefas de primeiro plano para a plataforma ficarem ociosas, o mecanismo de ociosidade de MAPI chamará a rotina de ociosidade de prioridade mais alta que está pronta para ser executada.</span><span class="sxs-lookup"><span data-stu-id="6259b-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="6259b-135">Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="6259b-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

