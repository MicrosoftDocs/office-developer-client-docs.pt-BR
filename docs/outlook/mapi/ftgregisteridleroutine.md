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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 0d3f24c41f2cfbd499d92e050c74da904dd4c377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766631"
---
# <a name="ftgregisteridleroutine"></a><span data-ttu-id="4a6d9-103">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="4a6d9-103">FtgRegisterIdleRoutine</span></span>

<span data-ttu-id="4a6d9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a6d9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a6d9-105">Adiciona uma rotina ociosa [FNIDLE](fnidle.md) baseada em função para o sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-105">Adds a [FNIDLE](fnidle.md) function-based idle routine to the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a6d9-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4a6d9-106">Header file:</span></span>  <br/> |<span data-ttu-id="4a6d9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4a6d9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4a6d9-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="4a6d9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4a6d9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4a6d9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4a6d9-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="4a6d9-110">Called by:</span></span>  <br/> |<span data-ttu-id="4a6d9-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="4a6d9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a><span data-ttu-id="4a6d9-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="4a6d9-112">Parameters</span></span>

<span data-ttu-id="4a6d9-113">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="4a6d9-113">_pfnIdle_</span></span>
  
> <span data-ttu-id="4a6d9-114">[in] Um ponteiro para a rotina ocioso.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-114">[in] A pointer to the idle routine.</span></span> 
    
<span data-ttu-id="4a6d9-115">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="4a6d9-115">_pvIdleParam_</span></span>
  
> <span data-ttu-id="4a6d9-116">[in] Um ponteiro para um bloco de memória que o mecanismo de ociosidade deve passar como um parâmetro para a rotina ociosa quando ele chama a ele.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-116">[in] A pointer to a block of memory that the idle engine should pass as a parameter to the idle routine when it calls it.</span></span> 
    
<span data-ttu-id="4a6d9-117">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="4a6d9-117">_priIdle_</span></span>
  
> <span data-ttu-id="4a6d9-118">[in] A prioridade inicial para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-118">[in] The initial priority for the idle routine.</span></span> <span data-ttu-id="4a6d9-119">Prioridades possíveis para rotinas definidos na implementação são maior ou menor do que zero, mas não a zero.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-119">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="4a6d9-120">A prioridade zero é reservada para um evento de usuário, como um clique do mouse ou de uma mensagem WM_PAINT.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-120">The zero priority is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="4a6d9-121">Prioridades maiores do que zero representam tarefas em segundo plano que têm uma prioridade maior que eventos do usuário e são enviadas como parte do loop de bomba de mensagem padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-121">Priorities greater than zero represent background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="4a6d9-122">Prioridades menor do que zero representa ociosa tarefas a serem executadas somente durante o tempo ocioso de bomba de mensagem.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-122">Priorities less than zero represent idle tasks that only run during message pump idle time.</span></span> <span data-ttu-id="4a6d9-123">Exemplos de prioridades são os seguintes: 1 para o envio de primeiro plano, 2 para inserção de energia-Editar caractere e 3 para baixar novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-123">Examples of priorities are as follows: 1 for foreground submission, 2 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="4a6d9-124">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="4a6d9-124">_csecIdle_</span></span>
  
> <span data-ttu-id="4a6d9-125">[in] O valor de tempo inicial, em centésimos de segundos, a serem usados em especificar parâmetros de rotina ociosos.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-125">[in] The initial time value, in hundredths of a second, to be used in specifying idle routine parameters.</span></span> <span data-ttu-id="4a6d9-126">O significado de valor de tempo inicial varia, dependendo do que é passado no parâmetro _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="4a6d9-126">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="4a6d9-127">O significado pode ser um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="4a6d9-127">The meaning can be one of the following:</span></span> 
    
  - <span data-ttu-id="4a6d9-128">O período mínimo de ociosidade do usuário que deve transcorrer antes de MAPI mecanismo ocioso chama a rotina ociosa pela primeira vez, se o sinalizador FIROWAIT for definido na _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-128">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="4a6d9-129">Após esse tempo, o mecanismo de ociosidade pode chamar a rotina ociosa sempre que for necessário.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-129">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="4a6d9-130">O intervalo mínimo entre as chamadas para a rotina ociosa, se o sinalizador FIROINTERVAL for definido na _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-130">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="4a6d9-131">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="4a6d9-131">_iroIdle_</span></span>
  
> <span data-ttu-id="4a6d9-132">[in] A bitmask dos sinalizadores usados para definir as opções iniciais para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-132">[in] The bitmask of flags used to set initial options for the idle routine.</span></span> <span data-ttu-id="4a6d9-133">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="4a6d9-133">The following flags can be set:</span></span>
    
  <span data-ttu-id="4a6d9-134">FIRONOADJUSTMENT</span><span class="sxs-lookup"><span data-stu-id="4a6d9-134">FIRONOADJUSTMENT</span></span>
    
  > <span data-ttu-id="4a6d9-135">Use esse sinalizador para especificar que o timer de ociosidade de rotina não deve ser ajustado para suspensão ou continuar.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-135">Use this flag to specify that the idle routine timer should not be adjusted for sleep or resume.</span></span> <span data-ttu-id="4a6d9-136">O comportamento padrão sem esse sinalizador é que o tempo de espera é excluído ao calcular o tempo decorrido.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-136">The default behavior without this flag is that sleep time is excluded when calculating the elapsed time.</span></span> <span data-ttu-id="4a6d9-137">Se FIRONOADJUSTMENT é passado, em seguida, o tempo de inatividade é incluído, ao calcular o tempo decorrido.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-137">If FIRONOADJUSTMENT is passed then the sleep time is included when calculating elapsed time.</span></span>
      
  <span data-ttu-id="4a6d9-138">FIRODISABLED</span><span class="sxs-lookup"><span data-stu-id="4a6d9-138">FIRODISABLED</span></span>
    
  > <span data-ttu-id="4a6d9-139">A rotina de ociosidade deve ser desabilitada quando registrado.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-139">The idle routine should be disabled when registered.</span></span> <span data-ttu-id="4a6d9-140">A ação padrão é permitir a rotina ociosa quando **FtgRegisterIdleRoutine** registra a ele.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-140">The default action is to enable the idle routine when **FtgRegisterIdleRoutine** registers it.</span></span> 
      
  <span data-ttu-id="4a6d9-141">FIROINTERVAL</span><span class="sxs-lookup"><span data-stu-id="4a6d9-141">FIROINTERVAL</span></span> 
    
  > <span data-ttu-id="4a6d9-142">O tempo especificado pelo parâmetro _csecIdle_ é o intervalo mínimo entre sucessivas chamadas para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-142">The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  <span data-ttu-id="4a6d9-143">FIROONCEONLY</span><span class="sxs-lookup"><span data-stu-id="4a6d9-143">FIROONCEONLY</span></span> 
    
  > <span data-ttu-id="4a6d9-144">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-144">Obsolete.</span></span> <span data-ttu-id="4a6d9-145">Não a use.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-145">Do not use.</span></span> 
      
  <span data-ttu-id="4a6d9-146">FIROPERBLOCK</span><span class="sxs-lookup"><span data-stu-id="4a6d9-146">FIROPERBLOCK</span></span> 
    
  > <span data-ttu-id="4a6d9-147">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-147">Obsolete.</span></span> <span data-ttu-id="4a6d9-148">Não a use.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-148">Do not use.</span></span> 
      
  <span data-ttu-id="4a6d9-149">FIROWAIT</span><span class="sxs-lookup"><span data-stu-id="4a6d9-149">FIROWAIT</span></span> 
    
  > <span data-ttu-id="4a6d9-150">O tempo especificado pelo parâmetro _csecIdle_ é o período mínimo de ociosidade do usuário que deve transcorrer antes que a rotina ociosa chamada pelo mecanismo de ociosidade de MAPI pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-150">The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="4a6d9-151">Após esse tempo, o mecanismo de ociosidade pode chamar a rotina ociosa sempre que for necessário.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-151">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4a6d9-152">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4a6d9-152">Return value</span></span>

<span data-ttu-id="4a6d9-153">A função de **FtgRegisterIdleRoutine** retornará uma marca de função que identifica a rotina ociosa que foi adicionada ao sistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-153">The **FtgRegisterIdleRoutine** function returns a function tag identifying the idle routine that was added to the MAPI system.</span></span> <span data-ttu-id="4a6d9-154">Se **FtgRegisterIdleRoutine** não é possível registrar a rotina ociosa para o aplicativo cliente ou o provedor de serviço, por exemplo devido a problemas de memória, ele retornará NULL.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-154">If **FtgRegisterIdleRoutine** cannot register the idle routine for the client application or service provider, for example because of memory problems, it returns NULL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4a6d9-155">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="4a6d9-155">Remarks</span></span>

<span data-ttu-id="4a6d9-156">As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com ociosas rotinas com base no protótipo de função [FNIDLE](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="4a6d9-156">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype.</span></span> 
  
|<span data-ttu-id="4a6d9-157">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-157">**Idle routine function**</span></span>|<span data-ttu-id="4a6d9-158">**Usage**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-158">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a6d9-159">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="4a6d9-159">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="4a6d9-160">Altera as características de uma rotina de ociosidade registrada.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-160">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="4a6d9-161">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="4a6d9-161">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="4a6d9-162">Remove uma rotina de ociosidade registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-162">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="4a6d9-163">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="4a6d9-163">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="4a6d9-164">Desativa ou ativa novamente uma rotina de ociosidade registrada sem removê-lo a partir do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-164">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="4a6d9-165">**FtgRegisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-165">**FtgRegisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="4a6d9-166">Adiciona uma rotina de ociosidade ao sistema de MAPI, com ou sem ativá-lo.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-166">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="4a6d9-167">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="4a6d9-167">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="4a6d9-168">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-168">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="4a6d9-169">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="4a6d9-169">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="4a6d9-170">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-170">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="4a6d9-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** tomar como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="4a6d9-172">Quando todas as tarefas de primeiro plano para a plataforma ficam ociosas, o mecanismo de ociosidade de MAPI chama a rotina de ocioso de prioridade mais alta que está pronta para executar.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-172">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="4a6d9-173">Não há nenhuma garantia de chamar ordem entre as rotinas de ociosidade da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-173">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="4a6d9-174">O exemplo a seguir é um exemplo de como usar o sinalizador FIRONOADJUSTMENT no parâmetro _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="4a6d9-174">The following is an example of using the FIRONOADJUSTMENT flag in the  _iroIdle_ parameter.</span></span> 
  
1. <span data-ttu-id="4a6d9-175">Registre uma rotina de ociosidade com um atraso de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-175">Register an idle routine with a 5 minute delay.</span></span>
    
2. <span data-ttu-id="4a6d9-176">Hibernação/suspensão o computador após 1 minuto (4 minutos deixado no cronômetro).</span><span class="sxs-lookup"><span data-stu-id="4a6d9-176">Hibernate/Sleep the computer after 1 minute (4 minutes left on the timer).</span></span>
    
3. <span data-ttu-id="4a6d9-177">Reinicie o computador 10 minutos mais tarde.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-177">Resume the computer 10 minutes later.</span></span>
    
<span data-ttu-id="4a6d9-178">O comportamento padrão, sem FIRONOADJUSTMENT, é que você ainda terá que aguardar 4 minutos mais para sua rotina executar.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-178">The default behavior, without FIRONOADJUSTMENT, is that you still have to wait 4 more minutes for your routine to run.</span></span> <span data-ttu-id="4a6d9-179">Ou seja, seu timer foi ajustada para permitir quanto tempo o computador estava suspenso.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-179">That is, your timer was adjusted to allow for how long the computer was asleep.</span></span> <span data-ttu-id="4a6d9-180">No entanto, se você passar FIRONOADJUSTMENT sua rotina ociosa será executado imediatamente porque decorridos mais de 5 minutos de tempo real.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-180">However, if you pass FIRONOADJUSTMENT your idle routine will run immediately because more than 5 minutes of real time have elapsed.</span></span>
  

