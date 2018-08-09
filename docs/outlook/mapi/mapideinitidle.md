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
ms.openlocfilehash: 4eaeb3338c95196ff346c5098e5d06371b00bc5a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767983"
---
# <a name="mapideinitidle"></a><span data-ttu-id="b1ab6-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="b1ab6-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="b1ab6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1ab6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1ab6-105">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="b1ab6-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1ab6-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b1ab6-106">Header file:</span></span>  <br/> |<span data-ttu-id="b1ab6-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b1ab6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b1ab6-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="b1ab6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b1ab6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b1ab6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b1ab6-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="b1ab6-110">Called by:</span></span>  <br/> |<span data-ttu-id="b1ab6-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="b1ab6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="b1ab6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1ab6-112">Parameters</span></span>

<span data-ttu-id="b1ab6-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b1ab6-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="b1ab6-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b1ab6-114">Return value</span></span>

<span data-ttu-id="b1ab6-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b1ab6-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1ab6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1ab6-116">Remarks</span></span>

<span data-ttu-id="b1ab6-117">Um aplicativo cliente ou um provedor de serviços deve chamar **MAPIDeInitIdle** quando ele não precisa mais o mecanismo de ociosidade, por exemplo, quando ele está prestes a parar o processamento.</span><span class="sxs-lookup"><span data-stu-id="b1ab6-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="b1ab6-118">Todas as chamadas para [MAPIInitIdle](mapiinitidle.md) devem ser iguais por uma chamada subsequente para **MAPIDeInitIdle**ou o mecanismo de ocioso é deixado em execução para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="b1ab6-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="b1ab6-119">As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com ociosas rotinas com base no protótipo de função [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="b1ab6-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="b1ab6-120">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="b1ab6-120">**Idle routine function**</span></span>|<span data-ttu-id="b1ab6-121">**Uso**</span><span class="sxs-lookup"><span data-stu-id="b1ab6-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1ab6-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b1ab6-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="b1ab6-123">Altera as características de uma rotina de ociosidade registrada.</span><span class="sxs-lookup"><span data-stu-id="b1ab6-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="b1ab6-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b1ab6-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="b1ab6-125">Remove uma rotina de ociosidade registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="b1ab6-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="b1ab6-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b1ab6-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="b1ab6-127">Desativa ou ativa novamente uma rotina de ociosidade registrada sem removê-lo a partir do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="b1ab6-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="b1ab6-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b1ab6-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="b1ab6-129">Adiciona uma rotina de ociosidade ao sistema de MAPI, com ou sem ativá-lo.</span><span class="sxs-lookup"><span data-stu-id="b1ab6-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="b1ab6-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="b1ab6-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="b1ab6-131">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="b1ab6-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="b1ab6-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="b1ab6-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="b1ab6-133">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="b1ab6-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="b1ab6-134">Quando todas as tarefas de primeiro plano para a plataforma ficam ociosas, o mecanismo de ociosidade de MAPI chama a rotina de ocioso de prioridade mais alta que está pronta para executar.</span><span class="sxs-lookup"><span data-stu-id="b1ab6-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="b1ab6-135">Não há nenhuma garantia de chamar ordem entre as rotinas de ociosidade da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="b1ab6-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
