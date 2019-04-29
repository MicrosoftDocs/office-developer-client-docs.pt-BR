---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 096f57335572c3788fdf129dd3bcf4a76cf62b01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433007"
---
# <a name="calludf"></a><span data-ttu-id="592b4-103">CallUDF</span><span class="sxs-lookup"><span data-stu-id="592b4-103">CallUDF</span></span>

<span data-ttu-id="592b4-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="592b4-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="592b4-105">Chama uma função definida pelo usuário em um ambiente de computação de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="592b4-105">Calls a user-defined function in a high-performance computing environment.</span></span>
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a><span data-ttu-id="592b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="592b4-106">Parameters</span></span>

<span data-ttu-id="592b4-107">_Identificação_da_sessão_</span><span class="sxs-lookup"><span data-stu-id="592b4-107">_SessionId_</span></span>
  
> <span data-ttu-id="592b4-108">A ID da sessão na qual a chamada será feita.</span><span class="sxs-lookup"><span data-stu-id="592b4-108">The ID of the session in which to make the call.</span></span>
    
<span data-ttu-id="592b4-109">_XLLName_</span><span class="sxs-lookup"><span data-stu-id="592b4-109">_XLLName_</span></span>
  
> <span data-ttu-id="592b4-110">O nome do XLL que contém a função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="592b4-110">The name of the XLL that contains the user-defined function.</span></span>
    
<span data-ttu-id="592b4-111">_UDFName_</span><span class="sxs-lookup"><span data-stu-id="592b4-111">_UDFName_</span></span>
  
> <span data-ttu-id="592b4-112">O nome da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="592b4-112">The name of the user-defined function.</span></span>
    
<span data-ttu-id="592b4-113">_CallBackAddr_</span><span class="sxs-lookup"><span data-stu-id="592b4-113">_CallBackAddr_</span></span>
  
> <span data-ttu-id="592b4-114">A função que o conector deve chamar quando a função definida pelo usuário estiver concluída.</span><span class="sxs-lookup"><span data-stu-id="592b4-114">The function that the connector should call when the user-defined function is finished.</span></span>
    
<span data-ttu-id="592b4-115">_pxAsyncHandle_</span><span class="sxs-lookup"><span data-stu-id="592b4-115">_pxAsyncHandle_</span></span>
  
> <span data-ttu-id="592b4-116">O identificador assíncrono usado pelo Excel e o conector para rastrear a chamada de função definida pelo usuário pendente.</span><span class="sxs-lookup"><span data-stu-id="592b4-116">The asynchronous handle used by Excel and the connector to track the pending user-defined function call.</span></span> <span data-ttu-id="592b4-117">O conector o utiliza posteriormente quando a chamada for concluída, quando ele chamar de volta para o Excel usando o ponteiro de função passado no argumento _CallBackAddr_ .</span><span class="sxs-lookup"><span data-stu-id="592b4-117">The connector uses it later when the call is finished, when it calls back into Excel using the function pointer passed in the  _CallBackAddr_ argument.</span></span> 
    
<span data-ttu-id="592b4-118">_ArgCount_</span><span class="sxs-lookup"><span data-stu-id="592b4-118">_ArgCount_</span></span>
  
> <span data-ttu-id="592b4-119">O número de argumentos a serem passados para a função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="592b4-119">The number of arguments to pass to the user-defined function.</span></span> <span data-ttu-id="592b4-120">O valor máximo permitido é 255.</span><span class="sxs-lookup"><span data-stu-id="592b4-120">The maximum value allowed is 255.</span></span>
    
<span data-ttu-id="592b4-121">_Parâmetro1_</span><span class="sxs-lookup"><span data-stu-id="592b4-121">_Parameter1_</span></span>
  
> <span data-ttu-id="592b4-122">Um valor a ser passado para a função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="592b4-122">A value to pass to the user-defined function.</span></span> <span data-ttu-id="592b4-123">Repita esse argumento para cada parâmetro indicado por _ArgCount_.</span><span class="sxs-lookup"><span data-stu-id="592b4-123">Repeat this argument for each parameter indicated by  _ArgCount_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="592b4-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="592b4-124">Return value</span></span>

<span data-ttu-id="592b4-125">**xlHpcRetSuccess** se a chamada UDF for iniciada com êxito; **xlHpcRetInvalidSessionId** se o argumento _SessionID_ for inválido; **xlHpcRetCallFailed** em outras falhas, incluindo o tempo limite. Se a chamada retornar qualquer código de erro (qualquer coisa exceto **xlHpcRetSuccess**), o Excel considerará a chamada UDF para ter falhado, invalidará o _pxAsyncHandle_e não esperará que um retorno de chamada ocorra.</span><span class="sxs-lookup"><span data-stu-id="592b4-125">**xlHpcRetSuccess** if the UDF call is successfully initiated; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures, including time-out. If the call returns any error code (anything except **xlHpcRetSuccess**), then Excel considers the UDF call to have failed, invalidates the  _pxAsyncHandle_, and does not expect a callback to occur.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="592b4-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="592b4-126">Remarks</span></span>

<span data-ttu-id="592b4-127">Essa função é executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="592b4-127">This function executes asynchronously.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="592b4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="592b4-128">See also</span></span>

- [<span data-ttu-id="592b4-129">Funções de conector de cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="592b4-129">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

