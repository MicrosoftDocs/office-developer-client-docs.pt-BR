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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 1fbeccd805953322b579d1490b5e74e5132aa7ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766301"
---
# <a name="changeidleroutine"></a><span data-ttu-id="48a50-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="48a50-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="48a50-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48a50-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48a50-105">Altera algumas ou todas as características de uma rotina de ociosidade [FNIDLE](fnidle.md) com base.</span><span class="sxs-lookup"><span data-stu-id="48a50-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48a50-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="48a50-106">Header file:</span></span>  <br/> |<span data-ttu-id="48a50-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="48a50-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="48a50-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="48a50-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="48a50-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="48a50-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="48a50-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="48a50-110">Called by:</span></span>  <br/> |<span data-ttu-id="48a50-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="48a50-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="48a50-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="48a50-112">Parameters</span></span>

<span data-ttu-id="48a50-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="48a50-113">_ftg_</span></span>
  
> <span data-ttu-id="48a50-114">[in] Marca de função que identifica a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="48a50-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="48a50-115">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="48a50-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="48a50-116">[in] Ponteiro para a rotina ocioso.</span><span class="sxs-lookup"><span data-stu-id="48a50-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="48a50-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="48a50-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="48a50-118">[in] Ponteiro para um novo bloco de memória que a implementação chamando aloca para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="48a50-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="48a50-119">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="48a50-119">_priIdle_</span></span>
  
> <span data-ttu-id="48a50-120">[in] Valor que representa uma nova prioridade para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="48a50-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="48a50-121">Prioridades possíveis para rotinas definidos na implementação são maior ou menor do que zero, mas não a zero.</span><span class="sxs-lookup"><span data-stu-id="48a50-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="48a50-122">Um valor de zero é reservado para um evento de usuário, como um clique do mouse ou de uma mensagem WM_PAINT.</span><span class="sxs-lookup"><span data-stu-id="48a50-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="48a50-123">Valores maiores que zero representam as prioridades de tarefas em segundo plano que têm uma prioridade maior que eventos do usuário e são enviadas como parte do loop de bomba de mensagem padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="48a50-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="48a50-124">Valores inferiores a zero representam as prioridades de ociosidade tarefas a serem executadas somente durante o tempo ocioso da mensagem de retângulos.</span><span class="sxs-lookup"><span data-stu-id="48a50-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="48a50-125">Exemplos de prioridades são: 1 para o envio de primeiro plano, 1 para inserção de energia-Editar caractere e 3 para baixar novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="48a50-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="48a50-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="48a50-126">_csecIdle_</span></span>
  
> <span data-ttu-id="48a50-127">[in] Um novo tempo, em centésimos de segundos, para aplicar a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="48a50-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="48a50-128">O significado de valor de tempo inicial varia, dependendo do que é passado no parâmetro _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="48a50-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="48a50-129">Ele pode ser:</span><span class="sxs-lookup"><span data-stu-id="48a50-129">It can be:</span></span> 
    
  - <span data-ttu-id="48a50-130">O período mínimo de ociosidade do usuário que deve transcorrer antes de MAPI mecanismo ocioso chama a rotina ociosa pela primeira vez, se o sinalizador FIROWAIT for definido na _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="48a50-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="48a50-131">Após esse tempo, o mecanismo de ociosidade pode chamar a rotina ociosa sempre que for necessário.</span><span class="sxs-lookup"><span data-stu-id="48a50-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="48a50-132">O intervalo mínimo entre as chamadas para a rotina ociosa, se o sinalizador FIROINTERVAL for definido na _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="48a50-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="48a50-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="48a50-133">_iroIdle_</span></span>
  
> <span data-ttu-id="48a50-134">[in] Bitmask dos sinalizadores indicando novas opções para chamar a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="48a50-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="48a50-135">Exatamente um dos sinalizadores a seguir deve ser definido:</span><span class="sxs-lookup"><span data-stu-id="48a50-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="48a50-136">FIROINTERVAL: O tempo especificado pelo parâmetro _csecIdle_ é o intervalo mínimo entre sucessivas chamadas para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="48a50-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="48a50-137">FIROONCEONLY: obsoleto.</span><span class="sxs-lookup"><span data-stu-id="48a50-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="48a50-138">Não a use.</span><span class="sxs-lookup"><span data-stu-id="48a50-138">Do not use.</span></span> 
      
  - <span data-ttu-id="48a50-139">FIROPERBLOCK: obsoleto.</span><span class="sxs-lookup"><span data-stu-id="48a50-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="48a50-140">Não a use.</span><span class="sxs-lookup"><span data-stu-id="48a50-140">Do not use.</span></span> 
      
  - <span data-ttu-id="48a50-141">FIROWAIT: O tempo especificado pelo parâmetro _csecIdle_ é o período mínimo de ociosidade do usuário que deve transcorrer antes que a rotina ociosa chamada pelo mecanismo de ociosidade de MAPI pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="48a50-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="48a50-142">Após esse tempo, o mecanismo de ociosidade pode chamar a rotina ociosa sempre que for necessário.</span><span class="sxs-lookup"><span data-stu-id="48a50-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="48a50-143">_ircIdle_</span><span class="sxs-lookup"><span data-stu-id="48a50-143">_ircIdle_</span></span>
  
> <span data-ttu-id="48a50-144">[in] Bitmask dos sinalizadores usados para indicar as alterações sejam feitas para a rotina ociosa.</span><span class="sxs-lookup"><span data-stu-id="48a50-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="48a50-145">Sinalizadores a seguir podem ser definidos em qualquer combinação:</span><span class="sxs-lookup"><span data-stu-id="48a50-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="48a50-146">FIRCCSEC: Uma alteração para o tempo associado a rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _csecIdle_ .</span><span class="sxs-lookup"><span data-stu-id="48a50-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="48a50-147">FIRCIRO: Uma alteração para as opções para a rotina de ociosidade, ou seja, uma alteração indicada pelo valor passado no parâmetro _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="48a50-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="48a50-148">FIRCPFN: Uma alteração para o ponteiro de rotina ocioso, ou seja, uma alteração indicada pelo valor passado no parâmetro _pfnIdle_ .</span><span class="sxs-lookup"><span data-stu-id="48a50-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="48a50-149">FIRCPRI: Uma alteração para a prioridade de rotina de ociosidade, ou seja, uma alteração indicada pelo valor passado no parâmetro _priIdle_ .</span><span class="sxs-lookup"><span data-stu-id="48a50-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="48a50-150">FIRCPV: Uma alteração para o bloco de memória de rotina ocioso, ou seja, uma alteração indicada pelo valor passado no parâmetro _pvIdleParam_ .</span><span class="sxs-lookup"><span data-stu-id="48a50-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="48a50-151">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="48a50-151">Return value</span></span>

<span data-ttu-id="48a50-152">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="48a50-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="48a50-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="48a50-153">Remarks</span></span>

<span data-ttu-id="48a50-154">As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com ociosas rotinas com base no protótipo de função [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="48a50-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="48a50-155">**Função de rotina ociosa**</span><span class="sxs-lookup"><span data-stu-id="48a50-155">**Idle routine function**</span></span>|<span data-ttu-id="48a50-156">**Usage**</span><span class="sxs-lookup"><span data-stu-id="48a50-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48a50-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="48a50-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="48a50-158">Altera as características de uma rotina de ociosidade registrada.</span><span class="sxs-lookup"><span data-stu-id="48a50-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="48a50-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="48a50-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="48a50-160">Remove uma rotina de ociosidade registrada do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="48a50-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="48a50-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="48a50-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="48a50-162">Desativa ou ativa novamente uma rotina de ociosidade registrada sem removê-lo a partir do sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="48a50-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="48a50-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="48a50-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="48a50-164">Adiciona uma rotina de ociosidade ao sistema de MAPI, com ou sem ativá-lo.</span><span class="sxs-lookup"><span data-stu-id="48a50-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="48a50-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="48a50-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="48a50-166">Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="48a50-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="48a50-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="48a50-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="48a50-168">Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="48a50-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="48a50-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** tomar como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="48a50-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="48a50-170">Quando todas as tarefas de primeiro plano para a plataforma ficam ociosas, o mecanismo de ociosidade de MAPI chama a rotina de ocioso de prioridade mais alta que está pronta para executar.</span><span class="sxs-lookup"><span data-stu-id="48a50-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="48a50-171">Não há nenhuma garantia de chamar ordem entre as rotinas de ociosidade da mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="48a50-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

