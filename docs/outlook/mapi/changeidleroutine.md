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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334430"
---
# <a name="changeidleroutine"></a><span data-ttu-id="31775-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="31775-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="31775-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31775-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31775-105">Altera algumas ou todas as características de uma rotina ociosa baseada em [FNIDLE](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="31775-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31775-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="31775-106">Header file:</span></span>  <br/> |<span data-ttu-id="31775-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="31775-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="31775-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="31775-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="31775-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="31775-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="31775-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="31775-110">Called by:</span></span>  <br/> |<span data-ttu-id="31775-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="31775-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="31775-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31775-112">Parameters</span></span>

<span data-ttu-id="31775-113">_FTG_</span><span class="sxs-lookup"><span data-stu-id="31775-113">_ftg_</span></span>
  
> <span data-ttu-id="31775-114">no Marca de função que identifica a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="31775-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="31775-115">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="31775-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="31775-116">no Ponteiro para a rotina Idle.</span><span class="sxs-lookup"><span data-stu-id="31775-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="31775-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="31775-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="31775-118">no Ponteiro para um novo bloco de memória que a implementação de chamada aloca para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="31775-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="31775-119">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="31775-119">_priIdle_</span></span>
  
> <span data-ttu-id="31775-120">no O valor que representa uma nova prioridade para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="31775-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="31775-121">As prioridades possíveis para rotinas definidas pela implementação são maiores ou menores que zero, mas não zero.</span><span class="sxs-lookup"><span data-stu-id="31775-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="31775-122">Um valor igual A zero é reservado para um evento de usuário, como um clique do mouse ou uma mensagem de WM_PAINT.</span><span class="sxs-lookup"><span data-stu-id="31775-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="31775-123">Valores maiores do que zero representam prioridades para tarefas em segundo plano que têm uma prioridade maior do que os eventos de usuário e são despachados como parte do loop de bomba de mensagem do Windows padrão.</span><span class="sxs-lookup"><span data-stu-id="31775-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="31775-124">Valores menores que zero representam prioridades para tarefas ociosas que só são executadas durante o tempo ocioso de bomba de mensagem.</span><span class="sxs-lookup"><span data-stu-id="31775-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="31775-125">Os exemplos de prioridades são: 1 para envio de primeiro plano, 1 para a inserção de caracteres de edição de energia e 3 para baixar novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="31775-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="31775-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="31775-126">_csecIdle_</span></span>
  
> <span data-ttu-id="31775-127">no Um novo tempo, em centésimos de segundo, a ser aplicado à rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="31775-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="31775-128">O significado do valor de tempo inicial varia, dependendo do que é passado no parâmetro _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="31775-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="31775-129">Pode ser:</span><span class="sxs-lookup"><span data-stu-id="31775-129">It can be:</span></span> 
    
  - <span data-ttu-id="31775-130">O período mínimo de inatividade do usuário que deve decorrer antes de o mecanismo de ociosidade de MAPI chamar a rotina de ociosidade pela primeira vez, se o sinalizador FIROWAIT estiver definido no _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="31775-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="31775-131">Após esse tempo, o mecanismo de ociosidade pode chamar a rotina de ociosidade com a frequência necessária.</span><span class="sxs-lookup"><span data-stu-id="31775-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="31775-132">O intervalo mínimo entre as chamadas para a rotina ociosa, se o sinalizador FIROINTERVAL estiver definido no _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="31775-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="31775-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="31775-133">_iroIdle_</span></span>
  
> <span data-ttu-id="31775-134">no Bitmask de sinalizadores que indicam novas opções para chamar a rotina de ociosidade.</span><span class="sxs-lookup"><span data-stu-id="31775-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="31775-135">É necessário definir exatamente um dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="31775-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="31775-136">FIROINTERVAL: o tempo especificado pelo parâmetro _csecIdle_ é o intervalo mínimo entre chamadas sucessivas para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="31775-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="31775-137">FIROONCEONLY: obsoleto.</span><span class="sxs-lookup"><span data-stu-id="31775-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="31775-138">Não usar.</span><span class="sxs-lookup"><span data-stu-id="31775-138">Do not use.</span></span> 
      
  - <span data-ttu-id="31775-139">FIROPERBLOCK: obsoleto.</span><span class="sxs-lookup"><span data-stu-id="31775-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="31775-140">Não usar.</span><span class="sxs-lookup"><span data-stu-id="31775-140">Do not use.</span></span> 
      
  - <span data-ttu-id="31775-141">FIROWAIT: o tempo especificado pelo parâmetro _csecIdle_ é o período mínimo de inatividade do usuário que deve decorrer antes de o mecanismo de ociosidade de MAPI chamar a rotina de ociosidade pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="31775-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="31775-142">Após esse tempo, o mecanismo de ociosidade pode chamar a rotina de ociosidade com a frequência necessária.</span><span class="sxs-lookup"><span data-stu-id="31775-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="31775-143">_ircIdle_</span><span class="sxs-lookup"><span data-stu-id="31775-143">_ircIdle_</span></span>
  
> <span data-ttu-id="31775-144">no Bitmask dos sinalizadores usados para indicar que as alterações serão feitas na rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="31775-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="31775-145">Os seguintes sinalizadores podem ser definidos em qualquer combinação:</span><span class="sxs-lookup"><span data-stu-id="31775-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="31775-146">FIRCCSEC: uma alteração no tempo associado à rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _csecIdle_ .</span><span class="sxs-lookup"><span data-stu-id="31775-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="31775-147">FIRCIRO: uma alteração nas opções para a rotina de ociosidade, ou seja, uma alteração indicada pelo valor passado no parâmetro _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="31775-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="31775-148">FIRCPFN: uma alteração no ponteiro de rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _pfnIdle_ .</span><span class="sxs-lookup"><span data-stu-id="31775-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="31775-149">FIRCPRI: uma alteração na prioridade da rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _priIdle_ .</span><span class="sxs-lookup"><span data-stu-id="31775-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="31775-150">FIRCPV: uma alteração no bloco de memória da rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _pvIdleParam_ .</span><span class="sxs-lookup"><span data-stu-id="31775-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="31775-151">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="31775-151">Return value</span></span>

<span data-ttu-id="31775-152">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="31775-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31775-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="31775-153">Remarks</span></span>

<span data-ttu-id="31775-154">As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com rotinas ociosas com base no protótipo de função do [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="31775-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="31775-155">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="31775-155">**Idle routine function**</span></span>|<span data-ttu-id="31775-156">**Usage**</span><span class="sxs-lookup"><span data-stu-id="31775-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31775-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="31775-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="31775-158">Altera as características de uma rotina de ociosidade registrada.</span><span class="sxs-lookup"><span data-stu-id="31775-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="31775-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="31775-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="31775-160">Remove uma rotina de ociosidade registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="31775-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="31775-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="31775-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="31775-162">Desabilita ou habilita novamente uma rotina de ociosidade registrada sem removê-la do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="31775-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="31775-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="31775-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="31775-164">Adiciona uma rotina ociosa ao sistema MAPI, com ou sem ativá-la.</span><span class="sxs-lookup"><span data-stu-id="31775-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="31775-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="31775-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="31775-166">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="31775-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="31775-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="31775-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="31775-168">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="31775-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="31775-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** aceitam como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="31775-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="31775-170">Quando todas as tarefas de primeiro plano para a plataforma ficarem ociosas, o mecanismo de ociosidade de MAPI chamará a rotina de ociosidade de prioridade mais alta que está pronta para ser executada.</span><span class="sxs-lookup"><span data-stu-id="31775-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="31775-171">Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="31775-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

