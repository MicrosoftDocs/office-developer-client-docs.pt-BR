---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6464f16d9ad73b332ff20dc007ef162b9525c6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411173"
---
# <a name="mapiinitialize"></a><span data-ttu-id="84e5c-103">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="84e5c-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="84e5c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84e5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84e5c-105">Incrementa a contagem de referência do subsistema MAPI e inicializa dados globais para a DLL MAPI.</span><span class="sxs-lookup"><span data-stu-id="84e5c-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84e5c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="84e5c-106">Header file:</span></span>  <br/> |<span data-ttu-id="84e5c-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="84e5c-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="84e5c-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="84e5c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="84e5c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="84e5c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="84e5c-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="84e5c-110">Called by:</span></span>  <br/> |<span data-ttu-id="84e5c-111">Aplicativos do cliente</span><span class="sxs-lookup"><span data-stu-id="84e5c-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="84e5c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84e5c-112">Parameters</span></span>

 <span data-ttu-id="84e5c-113">_lpMapiInit_</span><span class="sxs-lookup"><span data-stu-id="84e5c-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="84e5c-114">[in] Ponteiro para uma [MAPIINIT_0](mapiinit_0.md) estrutura.</span><span class="sxs-lookup"><span data-stu-id="84e5c-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="84e5c-115">O  _parâmetro lpMapiInit_ pode ser definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="84e5c-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="84e5c-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="84e5c-116">Return value</span></span>

<span data-ttu-id="84e5c-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="84e5c-117">S_OK</span></span> 
  
> <span data-ttu-id="84e5c-118">O subsistema MAPI foi inicializado com êxito.</span><span class="sxs-lookup"><span data-stu-id="84e5c-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="84e5c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="84e5c-119">Remarks</span></span>

<span data-ttu-id="84e5c-120">A **função MAPIInitialize** incrementa a contagem de referência MAPI para o subsistema MAPI, e a função [MAPIUninitialize](mapiuninitialize.md) diminui a contagem de referência interna.</span><span class="sxs-lookup"><span data-stu-id="84e5c-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="84e5c-121">Assim, o número de chamadas para uma função deve ser igual ao número de chamadas para a outra.</span><span class="sxs-lookup"><span data-stu-id="84e5c-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="84e5c-122">**MAPIInitialize** retornará S_OK se o MAPI não tiver sido inicializado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="84e5c-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="84e5c-123">Um cliente ou provedor de serviços deve chamar **MAPIInitialize** antes de fazer qualquer outra chamada MAPI.</span><span class="sxs-lookup"><span data-stu-id="84e5c-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="84e5c-124">Se isso não fizer, as chamadas do cliente ou do provedor de serviços retornarão o MAPI_E_NOT_INITIALIZED valor.</span><span class="sxs-lookup"><span data-stu-id="84e5c-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="84e5c-125">Ao chamar **MAPIInitialize** de um aplicativo multithreaded, de definir [](mapiinit_0.md) o parâmetro _lpMapiInit_ como uma estrutura MAPIINIT_0 que é declarada da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="84e5c-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="84e5c-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span><span class="sxs-lookup"><span data-stu-id="84e5c-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="84e5c-127">e chame:</span><span class="sxs-lookup"><span data-stu-id="84e5c-127">and call:</span></span> 
  
 <span data-ttu-id="84e5c-128">**MAPIInitialize** ( &amp; MAPIINIT);</span><span class="sxs-lookup"><span data-stu-id="84e5c-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="84e5c-129">Quando essa estrutura é declarada, o MAPI cria um thread separado para manipular a janela de notificação, que continua até que a contagem de referência de inicialização cai para zero.</span><span class="sxs-lookup"><span data-stu-id="84e5c-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="84e5c-130">Um serviço do Windows deve definir o membro **lags** da estrutura **MAPIINIT_0** apontado por  _lpMapiInit_ como MAPI_NT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="84e5c-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="84e5c-131">Você não pode chamar **MAPIInitialize** ou **MAPIUninitialize** de dentro de uma função **DllMain** Win32 ou qualquer outra função que crie ou termine threads.</span><span class="sxs-lookup"><span data-stu-id="84e5c-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="84e5c-132">Para obter mais informações, [consulte Usando objetos Thread-Safe dados.](using-thread-safe-objects.md)</span><span class="sxs-lookup"><span data-stu-id="84e5c-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="84e5c-133">**MAPIInitialize** não retorna nenhuma informação de erro estendida.</span><span class="sxs-lookup"><span data-stu-id="84e5c-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="84e5c-134">Ao contrário da maioria das outras chamadas MAPI, os significados de seus valores de retorno são estritamente definidos para corresponder à etapa específica da inicialização que falhou:</span><span class="sxs-lookup"><span data-stu-id="84e5c-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="84e5c-135">Verifica parâmetros e sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="84e5c-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="84e5c-136">MAPI_E_INVALID_PARAMETER ou MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="84e5c-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="84e5c-137">O chamador passou um parâmetro ou sinalizador inválido.</span><span class="sxs-lookup"><span data-stu-id="84e5c-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="84e5c-138">Inicializa as chaves do Registro exigidas pelo MAPI e confirma o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="84e5c-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="84e5c-139">Essa etapa só acontece se o processo do cliente estiver sendo executado como um serviço no Windows e define o sinalizador MAPI_NT SERVICE na **estrutura MAPIINIT_0** configuração.</span><span class="sxs-lookup"><span data-stu-id="84e5c-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="84e5c-140">MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="84e5c-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="84e5c-141">O processo de chamada é um serviço do Windows e as chaves do Registro exigidas pelo MAPI não puderam ser inicializadas.</span><span class="sxs-lookup"><span data-stu-id="84e5c-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="84e5c-142">Informações adicionais podem estar disponíveis no log de eventos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="84e5c-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="84e5c-143">Verifique a compatibilidade de MAPI com OLE e inicialize o OLE.</span><span class="sxs-lookup"><span data-stu-id="84e5c-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="84e5c-144">Verifica se há compatibilidade entre as versões atuais do OLE e MAPI.</span><span class="sxs-lookup"><span data-stu-id="84e5c-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="84e5c-145">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="84e5c-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="84e5c-146">A versão do OLE instalada na estação de trabalho não é compatível com esta versão do MAPI.</span><span class="sxs-lookup"><span data-stu-id="84e5c-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="84e5c-147">Inicializa o OLE.</span><span class="sxs-lookup"><span data-stu-id="84e5c-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="84e5c-148">Somente durante esta etapa, essa função pode retornar um código de erro não listado aqui.</span><span class="sxs-lookup"><span data-stu-id="84e5c-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="84e5c-149">Qualquer erro  _não_ listado aqui deve ser assumido como vindo da função OLE **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="84e5c-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="84e5c-150">Inicializa variáveis globais por processo.</span><span class="sxs-lookup"><span data-stu-id="84e5c-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="84e5c-151">MAPI_E_SESSION_LIMIT.</span><span class="sxs-lookup"><span data-stu-id="84e5c-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="84e5c-152">O MAPI configura um contexto específico para o processo atual.</span><span class="sxs-lookup"><span data-stu-id="84e5c-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="84e5c-153">As falhas podem ocorrer no Win16 se o número de processos exceder um determinado número ou em qualquer sistema se a memória disponível estiver esgotado.</span><span class="sxs-lookup"><span data-stu-id="84e5c-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="84e5c-154">Inicializa variáveis globais compartilhadas de todos os processos.</span><span class="sxs-lookup"><span data-stu-id="84e5c-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="84e5c-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span><span class="sxs-lookup"><span data-stu-id="84e5c-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="84e5c-156">Não havia recursos suficientes do sistema disponíveis para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="84e5c-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="84e5c-157">Inicializa o mecanismo de notificação, cria sua janela e seu thread, se solicitado pelo MAPI_MULTITHREAD_NOTIFICATIONS sinalizador.</span><span class="sxs-lookup"><span data-stu-id="84e5c-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="84e5c-158">MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="84e5c-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="84e5c-159">Pode falhar se os recursos do sistema se esgotarem.</span><span class="sxs-lookup"><span data-stu-id="84e5c-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="84e5c-160">Carrega e inicializa o provedor de perfil.</span><span class="sxs-lookup"><span data-stu-id="84e5c-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="84e5c-161">Verifica se **MAPIInitialize** pode acessar a chave do Registro onde os dados de perfil estão armazenados.</span><span class="sxs-lookup"><span data-stu-id="84e5c-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="84e5c-162">MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="84e5c-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="84e5c-163">O provedor de perfil encontrou um erro.</span><span class="sxs-lookup"><span data-stu-id="84e5c-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="84e5c-164">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="84e5c-164">MFCMAPI reference</span></span>

<span data-ttu-id="84e5c-165">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="84e5c-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="84e5c-166">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="84e5c-166">**File**</span></span>|<span data-ttu-id="84e5c-167">**Função**</span><span class="sxs-lookup"><span data-stu-id="84e5c-167">**Function**</span></span>|<span data-ttu-id="84e5c-168">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="84e5c-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="84e5c-169">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="84e5c-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="84e5c-170">MFCMAPI usa o **método MAPIInitialize** para inicializar MAPI em um thread em segundo plano para fazer alguns processamentos de tabela.</span><span class="sxs-lookup"><span data-stu-id="84e5c-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84e5c-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="84e5c-171">See also</span></span>



[<span data-ttu-id="84e5c-172">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="84e5c-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

