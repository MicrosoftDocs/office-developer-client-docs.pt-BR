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
# <a name="calludf"></a><span data-ttu-id="58e50-103">CallUDF</span><span class="sxs-lookup"><span data-stu-id="58e50-103">CallUDF</span></span>

<span data-ttu-id="58e50-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="58e50-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="58e50-105">Chama uma função definida pelo usuário em um ambiente de computação de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="58e50-105">Calls a user-defined function in a high-performance computing environment.</span></span>
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a><span data-ttu-id="58e50-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58e50-106">Parameters</span></span>

<span data-ttu-id="58e50-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="58e50-107">_SessionId_</span></span>
  
> <span data-ttu-id="58e50-108">A ID da sessão na qual fazer a chamada.</span><span class="sxs-lookup"><span data-stu-id="58e50-108">The ID of the session in which to make the call.</span></span>
    
<span data-ttu-id="58e50-109">_XLLName_</span><span class="sxs-lookup"><span data-stu-id="58e50-109">_XLLName_</span></span>
  
> <span data-ttu-id="58e50-110">O nome da XLL que contém a função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="58e50-110">The name of the XLL that contains the user-defined function.</span></span>
    
<span data-ttu-id="58e50-111">_UDFName_</span><span class="sxs-lookup"><span data-stu-id="58e50-111">_UDFName_</span></span>
  
> <span data-ttu-id="58e50-112">O nome da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="58e50-112">The name of the user-defined function.</span></span>
    
<span data-ttu-id="58e50-113">_CallBackAddr_</span><span class="sxs-lookup"><span data-stu-id="58e50-113">_CallBackAddr_</span></span>
  
> <span data-ttu-id="58e50-114">A função que o conector deve chamar quando a função definida pelo usuário for concluída.</span><span class="sxs-lookup"><span data-stu-id="58e50-114">The function that the connector should call when the user-defined function is finished.</span></span>
    
<span data-ttu-id="58e50-115">_pxAsyncHandle_</span><span class="sxs-lookup"><span data-stu-id="58e50-115">_pxAsyncHandle_</span></span>
  
> <span data-ttu-id="58e50-116">O alça assíncrona usada pelo Excel e pelo conector para controlar a chamada de função pendente definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="58e50-116">The asynchronous handle used by Excel and the connector to track the pending user-defined function call.</span></span> <span data-ttu-id="58e50-117">O conector o usa mais tarde quando a chamada é concluída, quando ele chama de volta para o Excel usando o ponteiro de função passado no _argumento CallBackAddr._</span><span class="sxs-lookup"><span data-stu-id="58e50-117">The connector uses it later when the call is finished, when it calls back into Excel using the function pointer passed in the  _CallBackAddr_ argument.</span></span> 
    
<span data-ttu-id="58e50-118">_ArgCount_</span><span class="sxs-lookup"><span data-stu-id="58e50-118">_ArgCount_</span></span>
  
> <span data-ttu-id="58e50-119">O número de argumentos a passar para a função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="58e50-119">The number of arguments to pass to the user-defined function.</span></span> <span data-ttu-id="58e50-120">O valor máximo permitido é 255.</span><span class="sxs-lookup"><span data-stu-id="58e50-120">The maximum value allowed is 255.</span></span>
    
<span data-ttu-id="58e50-121">_Parameter1_</span><span class="sxs-lookup"><span data-stu-id="58e50-121">_Parameter1_</span></span>
  
> <span data-ttu-id="58e50-122">Um valor a ser aprovado para a função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="58e50-122">A value to pass to the user-defined function.</span></span> <span data-ttu-id="58e50-123">Repita esse argumento para cada parâmetro indicado por  _ArgCount_.</span><span class="sxs-lookup"><span data-stu-id="58e50-123">Repeat this argument for each parameter indicated by  _ArgCount_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="58e50-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="58e50-124">Return value</span></span>

<span data-ttu-id="58e50-125">**xlHpcRetSuccess** se a chamada UDF for iniciada com êxito; **xlHpcRetInvalidSessionId** se o  _argumento SessionId_ for inválido; **xlHpcRetCallFailed** em outras falhas, incluindo tempo o tempo exemportado. Se a chamada retornar qualquer código de erro (qualquer coisa exceto **xlHpcRetSuccess**), o Excel considerará que a chamada UDF falhou, invalida o  _pxAsyncHandle_ e não espera que ocorra um retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="58e50-125">**xlHpcRetSuccess** if the UDF call is successfully initiated; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures, including time-out. If the call returns any error code (anything except **xlHpcRetSuccess**), then Excel considers the UDF call to have failed, invalidates the  _pxAsyncHandle_, and does not expect a callback to occur.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58e50-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="58e50-126">Remarks</span></span>

<span data-ttu-id="58e50-127">Essa função é executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="58e50-127">This function executes asynchronously.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="58e50-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="58e50-128">See also</span></span>

- [<span data-ttu-id="58e50-129">Funções de conector de cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="58e50-129">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

