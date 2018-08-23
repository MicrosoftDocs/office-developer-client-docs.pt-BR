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
ms.openlocfilehash: 33f4634623662b7bc09e0830e8bd0b51adc7799d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583495"
---
# <a name="mapideinitidle"></a><span data-ttu-id="f75fc-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="f75fc-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="f75fc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f75fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f75fc-105">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="f75fc-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f75fc-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f75fc-106">Header file:</span></span>  <br/> |<span data-ttu-id="f75fc-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f75fc-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f75fc-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="f75fc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f75fc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f75fc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f75fc-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="f75fc-110">Called by:</span></span>  <br/> |<span data-ttu-id="f75fc-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="f75fc-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="f75fc-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f75fc-112">Parameters</span></span>

<span data-ttu-id="f75fc-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f75fc-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="f75fc-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f75fc-114">Return value</span></span>

<span data-ttu-id="f75fc-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f75fc-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f75fc-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f75fc-116">Remarks</span></span>

<span data-ttu-id="f75fc-117">Um aplicativo cliente ou um provedor de serviços deve chamar **MAPIDeInitIdle** quando ele não precisa mais o mecanismo de ociosidade, por exemplo, quando ele está prestes a parar o processamento.</span><span class="sxs-lookup"><span data-stu-id="f75fc-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="f75fc-118">Todas as chamadas para [MAPIInitIdle](mapiinitidle.md) devem ser iguais por uma chamada subsequente para **MAPIDeInitIdle**ou o mecanismo de ocioso é deixado em execução para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="f75fc-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="f75fc-119">As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com ociosas rotinas com base no protótipo de função [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="f75fc-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="f75fc-120">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="f75fc-120">**Idle routine function**</span></span>|<span data-ttu-id="f75fc-121">**Uso**</span><span class="sxs-lookup"><span data-stu-id="f75fc-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f75fc-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f75fc-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="f75fc-123">Altera as características de uma rotina de ociosidade registrada.</span><span class="sxs-lookup"><span data-stu-id="f75fc-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="f75fc-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f75fc-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="f75fc-125">Remove uma rotina de ociosidade registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="f75fc-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="f75fc-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f75fc-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="f75fc-127">Desativa ou ativa novamente uma rotina de ociosidade registrada sem removê-lo a partir do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="f75fc-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="f75fc-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f75fc-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="f75fc-129">Adiciona uma rotina de ociosidade ao sistema de MAPI, com ou sem ativá-lo.</span><span class="sxs-lookup"><span data-stu-id="f75fc-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="f75fc-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="f75fc-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="f75fc-131">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="f75fc-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="f75fc-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="f75fc-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="f75fc-133">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="f75fc-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="f75fc-134">Quando todas as tarefas de primeiro plano para a plataforma ficam ociosas, o mecanismo de ociosidade de MAPI chama a rotina de ocioso de prioridade mais alta que está pronta para executar.</span><span class="sxs-lookup"><span data-stu-id="f75fc-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="f75fc-135">Não há nenhuma garantia de chamar ordem entre as rotinas de ociosidade da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="f75fc-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

