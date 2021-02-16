---
title: ChangeIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ChangeIdleRoutine
api_type:
- HeaderDef
ms.assetid: 0a24fe3b-a1ef-4748-b3b3-3bf747473c9d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cfec9356a866c79b687497c3af007c046a20a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418264"
---
# <a name="changeidleroutine"></a><span data-ttu-id="c9cb1-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c9cb1-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="c9cb1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9cb1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9cb1-105">Altera algumas ou todas as características de uma rotina ociosa baseada em [FNIDLE.](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="c9cb1-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9cb1-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c9cb1-106">Header file:</span></span>  <br/> |<span data-ttu-id="c9cb1-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c9cb1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c9cb1-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c9cb1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c9cb1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c9cb1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c9cb1-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="c9cb1-110">Called by:</span></span>  <br/> |<span data-ttu-id="c9cb1-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="c9cb1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID ChangeIdleRoutine(
  FTG ftg,
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle,
  USHORT ircIdle
);
```

## <a name="parameters"></a><span data-ttu-id="c9cb1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9cb1-112">Parameters</span></span>

<span data-ttu-id="c9cb1-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="c9cb1-113">_ftg_</span></span>
  
> <span data-ttu-id="c9cb1-114">[in] Marca de função que identifica a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="c9cb1-115">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="c9cb1-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="c9cb1-116">[in] Ponteiro para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="c9cb1-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="c9cb1-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="c9cb1-118">[in] Ponteiro para um novo bloco de memória que a implementação de chamada aloca para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="c9cb1-119">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="c9cb1-119">_priIdle_</span></span>
  
> <span data-ttu-id="c9cb1-120">[in] Valor que representa uma nova prioridade para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="c9cb1-121">As prioridades possíveis para rotinas definidas pela implementação são maiores ou menores do que zero, mas não zero.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="c9cb1-122">Um valor zero é reservado para um evento de usuário, como um clique do mouse ou uma WM_PAINT mensagem.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="c9cb1-123">Valores maiores do que zero representam prioridades para tarefas em segundo plano que têm uma prioridade mais alta do que os eventos do usuário e são enviados como parte do loop padrão de mensagem do Windows.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="c9cb1-124">Valores menores que zero representam prioridades para tarefas ociosas que só são executadas durante o tempo ocioso de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="c9cb1-125">Exemplos de prioridades são: 1 para envio em primeiro plano, 1 para inserção de caracteres de edição de energia e 3 para baixar novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="c9cb1-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="c9cb1-126">_csecIdle_</span></span>
  
> <span data-ttu-id="c9cb1-127">[in] Um novo tempo, em centésimos de um segundo, a ser aplicado à rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="c9cb1-128">O significado do valor de hora inicial varia, dependendo do que é passado no _parâmetro iroIdle._</span><span class="sxs-lookup"><span data-stu-id="c9cb1-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="c9cb1-129">Pode ser:</span><span class="sxs-lookup"><span data-stu-id="c9cb1-129">It can be:</span></span> 
    
  - <span data-ttu-id="c9cb1-130">O período mínimo de inação do usuário que deve passar antes que o mecanismo ocioso mapi chamar a rotina ociosa pela primeira vez, se o sinalizador FIROWAIT estiver definido em  _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="c9cb1-131">Depois que esse tempo passar, o mecanismo ocioso poderá chamar a rotina ociosa com a frequência necessária.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="c9cb1-132">O intervalo mínimo entre chamadas para a rotina ociosa, se o sinalizador FIROINTERVAL for definido em  _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="c9cb1-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="c9cb1-133">_iroIdle_</span></span>
  
> <span data-ttu-id="c9cb1-134">[in] Bitmask de sinalizadores indicando novas opções para chamar a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="c9cb1-135">Exatamente um dos seguintes sinalizadores deve ser definido:</span><span class="sxs-lookup"><span data-stu-id="c9cb1-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="c9cb1-136">FIROINTERVAL: o tempo especificado pelo parâmetro  _csecIdle_ é o intervalo mínimo entre chamadas sucessivas para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="c9cb1-137">FIROONCEONLY: Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="c9cb1-138">Não usar.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-138">Do not use.</span></span> 
      
  - <span data-ttu-id="c9cb1-139">FIROPERBLOCK: obsoleto.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="c9cb1-140">Não usar.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-140">Do not use.</span></span> 
      
  - <span data-ttu-id="c9cb1-141">FIROWAIT: o tempo especificado pelo parâmetro  _csecIdle_ é o período mínimo de inação do usuário que deve passar antes que o mecanismo ocioso mapi chamar a rotina ociosa pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="c9cb1-142">Depois que esse tempo passar, o mecanismo ocioso poderá chamar a rotina ociosa com a frequência necessária.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="c9cb1-143">_ircIdle_</span><span class="sxs-lookup"><span data-stu-id="c9cb1-143">_ircIdle_</span></span>
  
> <span data-ttu-id="c9cb1-144">[in] Bitmask de sinalizadores usados para indicar as alterações a serem feitas na rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="c9cb1-145">Os sinalizadores a seguir podem ser definidos em qualquer combinação:</span><span class="sxs-lookup"><span data-stu-id="c9cb1-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="c9cb1-146">FIRCCSEC: Uma alteração no tempo associado à rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _csecIdle._</span><span class="sxs-lookup"><span data-stu-id="c9cb1-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="c9cb1-147">FIRCIRO: Uma alteração nas opções para a rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _iroIdle._</span><span class="sxs-lookup"><span data-stu-id="c9cb1-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="c9cb1-148">FIRCPFN: Uma alteração no ponteiro de rotina ociosa, ou seja, uma alteração indicada pelo valor passado no _parâmetro pfnIdle._</span><span class="sxs-lookup"><span data-stu-id="c9cb1-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="c9cb1-149">FIRCPRI: Uma alteração na prioridade da rotina ociosa, ou seja, uma alteração indicada pelo valor passado no _parâmetro priIdle._</span><span class="sxs-lookup"><span data-stu-id="c9cb1-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="c9cb1-150">FIRCPV: Uma alteração no bloco de memória da rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _pvIdleParam._</span><span class="sxs-lookup"><span data-stu-id="c9cb1-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c9cb1-151">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c9cb1-151">Return value</span></span>

<span data-ttu-id="c9cb1-152">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c9cb1-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9cb1-153">Remarks</span></span>

<span data-ttu-id="c9cb1-154">As funções a seguir lidam com o mecanismo ocioso MAPI e com rotinas ociosas com base no protótipo de [função FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="c9cb1-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="c9cb1-155">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="c9cb1-155">**Idle routine function**</span></span>|<span data-ttu-id="c9cb1-156">**Uso**</span><span class="sxs-lookup"><span data-stu-id="c9cb1-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c9cb1-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="c9cb1-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="c9cb1-158">Altera as características de uma rotina ociosa registrada.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="c9cb1-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c9cb1-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="c9cb1-160">Remove uma rotina ociosa registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="c9cb1-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c9cb1-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="c9cb1-162">Desabilita ou reabilitar uma rotina ociosa registrada sem removê-la do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="c9cb1-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c9cb1-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="c9cb1-164">Adiciona uma rotina ociosa ao sistema MAPI, com ou sem habilita-la.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="c9cb1-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="c9cb1-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="c9cb1-166">Desliga o mecanismo ocioso MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="c9cb1-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="c9cb1-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="c9cb1-168">Inicializa o mecanismo ocioso MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="c9cb1-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine** e **EnableIdleRoutine** levam como parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="c9cb1-170">Quando todas as tarefas em primeiro plano da plataforma ficam ociosas, o mecanismo ocioso MAPI chama a rotina ociosa de prioridade mais alta que está pronta para ser executada.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="c9cb1-171">Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="c9cb1-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

