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
ms.openlocfilehash: d22c24088960debcd18ccd818dad23656f6a01f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768005"
---
# <a name="mapiinitialize"></a><span data-ttu-id="fd3b6-103">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="fd3b6-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="fd3b6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd3b6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd3b6-105">Incrementa a contagem de referência do subsistema MAPI e inicializa dados globais para a DLL de MAPI.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd3b6-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="fd3b6-106">Header file:</span></span>  <br/> |<span data-ttu-id="fd3b6-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="fd3b6-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="fd3b6-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="fd3b6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fd3b6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fd3b6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fd3b6-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="fd3b6-110">Called by:</span></span>  <br/> |<span data-ttu-id="fd3b6-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="fd3b6-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="fd3b6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd3b6-112">Parameters</span></span>

 <span data-ttu-id="fd3b6-113">_lpMapiInit_</span><span class="sxs-lookup"><span data-stu-id="fd3b6-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="fd3b6-114">[in] Ponteiro para uma estrutura [MAPIINIT_0](mapiinit_0.md) .</span><span class="sxs-lookup"><span data-stu-id="fd3b6-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="fd3b6-115">O parâmetro _lpMapiInit_ pode ser definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fd3b6-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fd3b6-116">Return value</span></span>

<span data-ttu-id="fd3b6-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd3b6-117">S_OK</span></span> 
  
> <span data-ttu-id="fd3b6-118">O subsistema de MAPI foi inicializado com êxito.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd3b6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd3b6-119">Remarks</span></span>

<span data-ttu-id="fd3b6-120">Os incrementos de função **MAPIInitialize** a MAPI contagem de referência para o subsistema de MAPI e o diminui de função [MAPIUninitialize](mapiuninitialize.md) a interna contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="fd3b6-121">Assim, o número de chamadas para uma função deve ser igual o número de chamadas para outro.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="fd3b6-122">**MAPIInitialize** Retorna S_OK se MAPI não foi inicializado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="fd3b6-123">Um provedor de cliente ou serviço deve chamar **MAPIInitialize** antes de fazer qualquer outra chamada MAPI.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="fd3b6-124">Falha ao fazer isso faz com que o cliente ou serviço de chamadas do provedor retornar o valor MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="fd3b6-125">Ao chamar **MAPIInitialize** de um aplicativo multithreaded, defina o parâmetro _lpMapiInit_ para uma estrutura [MAPIINIT_0](mapiinit_0.md) que é declarada como se segue:</span><span class="sxs-lookup"><span data-stu-id="fd3b6-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="fd3b6-126">**MAPIINIT_0** MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS}</span><span class="sxs-lookup"><span data-stu-id="fd3b6-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="fd3b6-127">e a chamada:</span><span class="sxs-lookup"><span data-stu-id="fd3b6-127">and call:</span></span> 
  
 <span data-ttu-id="fd3b6-128">**MAPIInitialize** (&amp;MAPIINIT);</span><span class="sxs-lookup"><span data-stu-id="fd3b6-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="fd3b6-129">Quando essa estrutura é declarada, MAPI cria um segmento separado para manipular a janela de notificação, que continua até que a contagem de referência initialize cai para zero.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="fd3b6-130">Um serviço do Windows deve definir o membro **ulflags** da estrutura **MAPIINIT_0** apontado pela _lpMapiInit_ para MAPI_NT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fd3b6-131">Você não pode chamar **MAPIInitialize** ou **MAPIUninitialize** de dentro de uma função do Win32 **DllMain** ou qualquer outra função que cria ou finaliza threads.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="fd3b6-132">Para obter mais informações, consulte [Usando objetos de Thread-Safe](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="fd3b6-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="fd3b6-133">**MAPIInitialize** não devolvem nenhuma informação de erro estendidas.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="fd3b6-134">Ao contrário da maioria das outras chamadas MAPI, os significados de seus valores de retorno estritamente são definidos para corresponder à etapa específica da inicialização que falharam:</span><span class="sxs-lookup"><span data-stu-id="fd3b6-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="fd3b6-135">Verifica os parâmetros e os sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="fd3b6-136">MAPI_E_INVALID_PARAMETER ou MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="fd3b6-137">Chamador passou um parâmetro ou sinalizador inválido.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="fd3b6-138">Inicializa chaves do registro necessárias pelo MAPI e confirma o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="fd3b6-139">Esta etapa ocorre apenas se o processo do cliente está sendo executado como um serviço no Windows e define o sinalizador de serviço de MAPI_NT na estrutura **MAPIINIT_0** .</span><span class="sxs-lookup"><span data-stu-id="fd3b6-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="fd3b6-140">MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="fd3b6-141">O processo de chamada é um serviço do Windows e chaves do registro necessárias pelo MAPI não pôde ser inicializadas.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="fd3b6-142">Informações adicionais podem estar disponíveis no log de eventos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="fd3b6-143">Verificar a compatibilidade do MAPI com OLE e inicializar OLE.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="fd3b6-144">Verifica a compatibilidade entre as versões atuais dos OLE e MAPI.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="fd3b6-145">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="fd3b6-146">A versão do OLE instalada na estação de trabalho não é compatível com esta versão do MAPI.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="fd3b6-147">Inicializa OLE.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="fd3b6-148">Durante esta etapa somente, essa função pode retornar um código de erro não listado aqui.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="fd3b6-149">Qualquer erro _não_ listado aqui deve ser adotada para a função OLE **CoInitialize**são provenientes.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="fd3b6-150">Inicializa variáveis globais por processo.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="fd3b6-151">MAPI_E_SESSION_LIMIT.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="fd3b6-152">MAPI configura contexto específica para o processo atual.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="fd3b6-153">Podem ocorrer falhas Win16 se um determinado número de exceder o número de processos, ou em qualquer sistema se for esgotada a memória disponível.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="fd3b6-154">Inicializa compartilhadas variáveis globais de todos os processos.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="fd3b6-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="fd3b6-156">Recursos do sistema insuficientes estavam disponíveis para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="fd3b6-157">Inicializa o mecanismo de notificação, cria sua janela e seu thread se solicitado pelo sinalizador de MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="fd3b6-158">MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="fd3b6-159">Pode falhar se os recursos do sistema são esgotados.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="fd3b6-160">Carrega e inicializa o provedor de perfil.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="fd3b6-161">Verifica se **MAPIInitialize** pode acessar a chave do registro onde estão armazenados os dados de perfil.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="fd3b6-162">MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="fd3b6-163">O provedor de perfil encontrou um erro.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="fd3b6-164">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fd3b6-164">MFCMAPI reference</span></span>

<span data-ttu-id="fd3b6-165">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fd3b6-166">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="fd3b6-166">**File**</span></span>|<span data-ttu-id="fd3b6-167">**Function**</span><span class="sxs-lookup"><span data-stu-id="fd3b6-167">**Function**</span></span>|<span data-ttu-id="fd3b6-168">**Comment**</span><span class="sxs-lookup"><span data-stu-id="fd3b6-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fd3b6-169">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="fd3b6-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="fd3b6-170">MFCMAPI usa o método **MAPIInitialize** para inicializar MAPI em um segmento de plano de fundo fazer algumas processamento da tabela.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd3b6-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd3b6-171">See also</span></span>



[<span data-ttu-id="fd3b6-172">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="fd3b6-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

