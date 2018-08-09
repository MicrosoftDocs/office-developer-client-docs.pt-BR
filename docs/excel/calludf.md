---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1d55f22de88b274d0403f81717d0fddefbea0219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765253"
---
# <a name="calludf"></a><span data-ttu-id="355d0-103">CallUDF</span><span class="sxs-lookup"><span data-stu-id="355d0-103">CallUDF</span></span>

<span data-ttu-id="355d0-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="355d0-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="355d0-105">Chama uma função definida pelo usuário em um ambiente de computação de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="355d0-105">Calls a user-defined function in a high-performance computing environment.</span></span>
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a><span data-ttu-id="355d0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="355d0-106">Parameters</span></span>

<span data-ttu-id="355d0-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="355d0-107">_SessionId_</span></span>
  
> <span data-ttu-id="355d0-108">A identificação da sessão em que deseja que a chamada.</span><span class="sxs-lookup"><span data-stu-id="355d0-108">The ID of the session in which to make the call.</span></span>
    
<span data-ttu-id="355d0-109">_XLLName_</span><span class="sxs-lookup"><span data-stu-id="355d0-109">_XLLName_</span></span>
  
> <span data-ttu-id="355d0-110">O nome da XLL que contém a função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="355d0-110">The name of the XLL that contains the user-defined function.</span></span>
    
<span data-ttu-id="355d0-111">_UDFName_</span><span class="sxs-lookup"><span data-stu-id="355d0-111">_UDFName_</span></span>
  
> <span data-ttu-id="355d0-112">O nome da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="355d0-112">The name of the user-defined function.</span></span>
    
<span data-ttu-id="355d0-113">_CallBackAddr_</span><span class="sxs-lookup"><span data-stu-id="355d0-113">_CallBackAddr_</span></span>
  
> <span data-ttu-id="355d0-114">A função que o conector deve chamar quando termina a função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="355d0-114">The function that the connector should call when the user-defined function is finished.</span></span>
    
<span data-ttu-id="355d0-115">_pxAsyncHandle_</span><span class="sxs-lookup"><span data-stu-id="355d0-115">_pxAsyncHandle_</span></span>
  
> <span data-ttu-id="355d0-116">O identificador assíncrona usado pelo Excel e o conector para controlar a chamada pendente de função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="355d0-116">The asynchronous handle used by Excel and the connector to track the pending user-defined function call.</span></span> <span data-ttu-id="355d0-117">O conector usa mais tarde quando a chamada for concluída, quando ele chama de volta para o Excel usando o ponteiro de função passados no argumento _CallBackAddr_ .</span><span class="sxs-lookup"><span data-stu-id="355d0-117">The connector uses it later when the call is finished, when it calls back into Excel using the function pointer passed in the  _CallBackAddr_ argument.</span></span> 
    
<span data-ttu-id="355d0-118">_ArgCount_</span><span class="sxs-lookup"><span data-stu-id="355d0-118">_ArgCount_</span></span>
  
> <span data-ttu-id="355d0-119">O número de argumentos a serem passados para a função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="355d0-119">The number of arguments to pass to the user-defined function.</span></span> <span data-ttu-id="355d0-120">O valor máximo permitido é 255.</span><span class="sxs-lookup"><span data-stu-id="355d0-120">The maximum value allowed is 255.</span></span>
    
<span data-ttu-id="355d0-121">_Parâmetro1_</span><span class="sxs-lookup"><span data-stu-id="355d0-121">_Parameter1_</span></span>
  
> <span data-ttu-id="355d0-122">Um valor para passar para a função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="355d0-122">A value to pass to the user-defined function.</span></span> <span data-ttu-id="355d0-123">Repita este argumento para cada parâmetro indicado pelo _ArgCount_.</span><span class="sxs-lookup"><span data-stu-id="355d0-123">Repeat this argument for each parameter indicated by  _ArgCount_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="355d0-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="355d0-124">Return value</span></span>

<span data-ttu-id="355d0-125">**xlHpcRetSuccess** se a chamada UDF é iniciada com êxito; **xlHpcRetInvalidSessionId** se o argumento _SessionId_ é inválido; **xlHpcRetCallFailed** em outras falhas, incluindo o tempo limite. Se a chamada retornar qualquer código de erro (nada, exceto **xlHpcRetSuccess**), em seguida, Excel considera que a chamada UDF para ter falhado, invalida o _pxAsyncHandle_e não esperar que ocorra um retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="355d0-125">**xlHpcRetSuccess** if the UDF call is successfully initiated; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures, including time-out. If the call returns any error code (anything except **xlHpcRetSuccess**), then Excel considers the UDF call to have failed, invalidates the  _pxAsyncHandle_, and does not expect a callback to occur.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="355d0-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="355d0-126">Remarks</span></span>

<span data-ttu-id="355d0-127">Esta função executa de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="355d0-127">This function executes asynchronously.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="355d0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="355d0-128">See also</span></span>

- [<span data-ttu-id="355d0-129">Funções de conector de cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="355d0-129">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

