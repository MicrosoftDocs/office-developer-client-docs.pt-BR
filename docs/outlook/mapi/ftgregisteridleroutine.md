---
title: FtgRegisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtgRegisterIdleRoutine
api_type:
- COM
ms.assetid: 8d9557ba-7919-42c6-9e2f-f10214437d53
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b45b80f09efbd4f05aabc2c868d5bd8eb5fa4cce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418518"
---
# <a name="ftgregisteridleroutine"></a><span data-ttu-id="f3b87-103">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f3b87-103">FtgRegisterIdleRoutine</span></span>

<span data-ttu-id="f3b87-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3b87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3b87-105">Adiciona uma rotina de ociosidade baseada na função [FNIDLE](fnidle.md) ao sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="f3b87-105">Adds a [FNIDLE](fnidle.md) function-based idle routine to the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3b87-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f3b87-106">Header file:</span></span>  <br/> |<span data-ttu-id="f3b87-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="f3b87-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f3b87-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f3b87-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f3b87-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f3b87-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f3b87-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="f3b87-110">Called by:</span></span>  <br/> |<span data-ttu-id="f3b87-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="f3b87-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a><span data-ttu-id="f3b87-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3b87-112">Parameters</span></span>

<span data-ttu-id="f3b87-113">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="f3b87-113">_pfnIdle_</span></span>
  
> <span data-ttu-id="f3b87-114">no Um ponteiro para a rotina de ociosidade.</span><span class="sxs-lookup"><span data-stu-id="f3b87-114">[in] A pointer to the idle routine.</span></span> 
    
<span data-ttu-id="f3b87-115">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="f3b87-115">_pvIdleParam_</span></span>
  
> <span data-ttu-id="f3b87-116">no Um ponteiro para um bloco de memória que o mecanismo de ociosidade deve passar como um parâmetro para a rotina ociosa quando ele chama.</span><span class="sxs-lookup"><span data-stu-id="f3b87-116">[in] A pointer to a block of memory that the idle engine should pass as a parameter to the idle routine when it calls it.</span></span> 
    
<span data-ttu-id="f3b87-117">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="f3b87-117">_priIdle_</span></span>
  
> <span data-ttu-id="f3b87-118">no A prioridade inicial para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="f3b87-118">[in] The initial priority for the idle routine.</span></span> <span data-ttu-id="f3b87-119">As prioridades possíveis para rotinas definidas pela implementação são maiores ou menores que zero, mas não zero.</span><span class="sxs-lookup"><span data-stu-id="f3b87-119">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="f3b87-120">A prioridade zero é reservada para um evento de usuário, como um clique do mouse ou uma mensagem WM_PAINT.</span><span class="sxs-lookup"><span data-stu-id="f3b87-120">The zero priority is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="f3b87-121">As prioridades maiores do que zero representam tarefas em segundo plano que têm uma prioridade maior do que os eventos do usuário e são despachadas como parte do loop de bomba de mensagem padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="f3b87-121">Priorities greater than zero represent background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="f3b87-122">Prioridades com menos de zero representam tarefas ociosas que só são executadas durante o tempo ocioso do bombeamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f3b87-122">Priorities less than zero represent idle tasks that only run during message pump idle time.</span></span> <span data-ttu-id="f3b87-123">Exemplos de prioridades são: 1 para envio de primeiro plano, 2 para inserção de caracteres de edição de energia e 3 para baixar novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="f3b87-123">Examples of priorities are as follows: 1 for foreground submission, 2 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="f3b87-124">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="f3b87-124">_csecIdle_</span></span>
  
> <span data-ttu-id="f3b87-125">no O valor inicial de tempo, em centésimos de segundo, a ser usado na especificação de parâmetros de rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="f3b87-125">[in] The initial time value, in hundredths of a second, to be used in specifying idle routine parameters.</span></span> <span data-ttu-id="f3b87-126">O significado do valor de tempo inicial varia, dependendo do que é passado no parâmetro _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="f3b87-126">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="f3b87-127">O significado pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="f3b87-127">The meaning can be one of the following:</span></span> 
    
  - <span data-ttu-id="f3b87-128">O período mínimo de inatividade do usuário que deve decorrer antes de o mecanismo de ociosidade de MAPI chamar a rotina de ociosidade pela primeira vez, se o sinalizador FIROWAIT estiver definido no _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="f3b87-128">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="f3b87-129">Após esse tempo, o mecanismo de ociosidade pode chamar a rotina de ociosidade com a frequência necessária.</span><span class="sxs-lookup"><span data-stu-id="f3b87-129">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="f3b87-130">O intervalo mínimo entre as chamadas para a rotina ociosa, se o sinalizador FIROINTERVAL estiver definido no _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="f3b87-130">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="f3b87-131">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="f3b87-131">_iroIdle_</span></span>
  
> <span data-ttu-id="f3b87-132">no A bitmask dos sinalizadores usados para definir as opções iniciais da rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="f3b87-132">[in] The bitmask of flags used to set initial options for the idle routine.</span></span> <span data-ttu-id="f3b87-133">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="f3b87-133">The following flags can be set:</span></span>
    
  <span data-ttu-id="f3b87-134">FIRONOADJUSTMENT</span><span class="sxs-lookup"><span data-stu-id="f3b87-134">FIRONOADJUSTMENT</span></span>
    
  > <span data-ttu-id="f3b87-135">Use este sinalizador para especificar que o timer de rotina ociosa não deve ser ajustado para Sleep ou resume.</span><span class="sxs-lookup"><span data-stu-id="f3b87-135">Use this flag to specify that the idle routine timer should not be adjusted for sleep or resume.</span></span> <span data-ttu-id="f3b87-136">O comportamento padrão sem esse sinalizador é que o tempo de suspensão é excluído ao calcular o tempo decorrido.</span><span class="sxs-lookup"><span data-stu-id="f3b87-136">The default behavior without this flag is that sleep time is excluded when calculating the elapsed time.</span></span> <span data-ttu-id="f3b87-137">Se FIRONOADJUSTMENT for passado, o tempo de espera será incluído no cálculo do tempo decorrido.</span><span class="sxs-lookup"><span data-stu-id="f3b87-137">If FIRONOADJUSTMENT is passed then the sleep time is included when calculating elapsed time.</span></span>
      
  <span data-ttu-id="f3b87-138">FIRODISABLED</span><span class="sxs-lookup"><span data-stu-id="f3b87-138">FIRODISABLED</span></span>
    
  > <span data-ttu-id="f3b87-139">A rotina ociosa deve ser desabilitada quando for registrada.</span><span class="sxs-lookup"><span data-stu-id="f3b87-139">The idle routine should be disabled when registered.</span></span> <span data-ttu-id="f3b87-140">A ação padrão é habilitar a rotina de ociosidade quando o **FtgRegisterIdleRoutine** o registra.</span><span class="sxs-lookup"><span data-stu-id="f3b87-140">The default action is to enable the idle routine when **FtgRegisterIdleRoutine** registers it.</span></span> 
      
  <span data-ttu-id="f3b87-141">FIROINTERVAL</span><span class="sxs-lookup"><span data-stu-id="f3b87-141">FIROINTERVAL</span></span> 
    
  > <span data-ttu-id="f3b87-142">O tempo especificado pelo parâmetro _csecIdle_ é o intervalo mínimo entre chamadas sucessivas para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="f3b87-142">The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  <span data-ttu-id="f3b87-143">FIROONCEONLY</span><span class="sxs-lookup"><span data-stu-id="f3b87-143">FIROONCEONLY</span></span> 
    
  > <span data-ttu-id="f3b87-144">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="f3b87-144">Obsolete.</span></span> <span data-ttu-id="f3b87-145">Não usar.</span><span class="sxs-lookup"><span data-stu-id="f3b87-145">Do not use.</span></span> 
      
  <span data-ttu-id="f3b87-146">FIROPERBLOCK</span><span class="sxs-lookup"><span data-stu-id="f3b87-146">FIROPERBLOCK</span></span> 
    
  > <span data-ttu-id="f3b87-147">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="f3b87-147">Obsolete.</span></span> <span data-ttu-id="f3b87-148">Não usar.</span><span class="sxs-lookup"><span data-stu-id="f3b87-148">Do not use.</span></span> 
      
  <span data-ttu-id="f3b87-149">FIROWAIT</span><span class="sxs-lookup"><span data-stu-id="f3b87-149">FIROWAIT</span></span> 
    
  > <span data-ttu-id="f3b87-150">O tempo especificado pelo parâmetro _csecIdle_ é o período mínimo de inatividade do usuário que deve decorrer antes de o mecanismo de ociosidade de MAPI chamar a rotina de ociosidade pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="f3b87-150">The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="f3b87-151">Após esse tempo, o mecanismo de ociosidade pode chamar a rotina de ociosidade com a frequência necessária.</span><span class="sxs-lookup"><span data-stu-id="f3b87-151">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f3b87-152">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f3b87-152">Return value</span></span>

<span data-ttu-id="f3b87-153">A função **FtgRegisterIdleRoutine** retorna uma marca de função identificando a rotina de ociosidade que foi adicionada ao sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="f3b87-153">The **FtgRegisterIdleRoutine** function returns a function tag identifying the idle routine that was added to the MAPI system.</span></span> <span data-ttu-id="f3b87-154">Se o **FtgRegisterIdleRoutine** não puder registrar a rotina de ociosidade para o aplicativo cliente ou provedor de serviços, por exemplo, por causa de problemas de memória, ele retornará NULL.</span><span class="sxs-lookup"><span data-stu-id="f3b87-154">If **FtgRegisterIdleRoutine** cannot register the idle routine for the client application or service provider, for example because of memory problems, it returns NULL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f3b87-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3b87-155">Remarks</span></span>

<span data-ttu-id="f3b87-156">As funções a seguir lidam com o mecanismo de ociosidade de MAPI e com rotinas ociosas com base no protótipo de função [FNIDLE](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="f3b87-156">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype.</span></span> 
  
|<span data-ttu-id="f3b87-157">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="f3b87-157">**Idle routine function**</span></span>|<span data-ttu-id="f3b87-158">**Usage**</span><span class="sxs-lookup"><span data-stu-id="f3b87-158">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3b87-159">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f3b87-159">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="f3b87-160">Altera as características de uma rotina de ociosidade registrada.</span><span class="sxs-lookup"><span data-stu-id="f3b87-160">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="f3b87-161">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f3b87-161">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="f3b87-162">Remove uma rotina de ociosidade registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="f3b87-162">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="f3b87-163">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f3b87-163">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="f3b87-164">Desabilita ou habilita novamente uma rotina de ociosidade registrada sem removê-la do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="f3b87-164">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="f3b87-165">**FtgRegisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="f3b87-165">**FtgRegisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="f3b87-166">Adiciona uma rotina ociosa ao sistema MAPI, com ou sem ativá-la.</span><span class="sxs-lookup"><span data-stu-id="f3b87-166">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="f3b87-167">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="f3b87-167">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="f3b87-168">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="f3b87-168">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="f3b87-169">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="f3b87-169">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="f3b87-170">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="f3b87-170">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="f3b87-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** aceitam como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="f3b87-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="f3b87-172">Quando todas as tarefas de primeiro plano para a plataforma ficarem ociosas, o mecanismo de ociosidade de MAPI chamará a rotina de ociosidade de prioridade mais alta que está pronta para ser executada.</span><span class="sxs-lookup"><span data-stu-id="f3b87-172">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="f3b87-173">Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="f3b87-173">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="f3b87-174">Veja a seguir um exemplo de como usar o sinalizador FIRONOADJUSTMENT no parâmetro _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="f3b87-174">The following is an example of using the FIRONOADJUSTMENT flag in the  _iroIdle_ parameter.</span></span> 
  
1. <span data-ttu-id="f3b87-175">Registrar uma rotina ociosa com atraso de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="f3b87-175">Register an idle routine with a 5 minute delay.</span></span>
    
2. <span data-ttu-id="f3b87-176">Hibernar/dormir o computador após 1 minuto (4 minutos restantes no temporizador).</span><span class="sxs-lookup"><span data-stu-id="f3b87-176">Hibernate/Sleep the computer after 1 minute (4 minutes left on the timer).</span></span>
    
3. <span data-ttu-id="f3b87-177">ReTome o computador 10 minutos mais tarde.</span><span class="sxs-lookup"><span data-stu-id="f3b87-177">Resume the computer 10 minutes later.</span></span>
    
<span data-ttu-id="f3b87-178">O comportamento padrão, sem o FIRONOADJUSTMENT, é que você ainda precisa aguardar mais 4 minutos para que a rotina seja executada.</span><span class="sxs-lookup"><span data-stu-id="f3b87-178">The default behavior, without FIRONOADJUSTMENT, is that you still have to wait 4 more minutes for your routine to run.</span></span> <span data-ttu-id="f3b87-179">Ou seja, o cronômetro foi ajustado para permitir por quanto tempo o computador estava em suspensão.</span><span class="sxs-lookup"><span data-stu-id="f3b87-179">That is, your timer was adjusted to allow for how long the computer was asleep.</span></span> <span data-ttu-id="f3b87-180">No enTanto, se você passar FIRONOADJUSTMENT sua rotina de ociosidade será executada imediatamente porque decorrido mais de cinco minutos de tempo real.</span><span class="sxs-lookup"><span data-stu-id="f3b87-180">However, if you pass FIRONOADJUSTMENT your idle routine will run immediately because more than 5 minutes of real time have elapsed.</span></span>
  

