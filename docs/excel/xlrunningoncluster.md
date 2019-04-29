---
title: xlRunningOnCluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- xlrunningoncluster
localization_priority: Normal
ms.assetid: 7662f255-4184-4af0-97f5-9a89347a201a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f5c630c73899b07e2727a7d42b18eb1891797bab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418285"
---
# <a name="xlrunningoncluster"></a><span data-ttu-id="3f70c-104">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="3f70c-104">xlRunningOnCluster</span></span>

<span data-ttu-id="3f70c-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3f70c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3f70c-106">Retorna um valor que indica se a função definida pelo usuário está sendo executada em um cluster.</span><span class="sxs-lookup"><span data-stu-id="3f70c-106">Returns a value that indicates whether the user-defined function is running on a cluster.</span></span> 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="3f70c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f70c-107">Parameters</span></span>

<span data-ttu-id="3f70c-108">Esta função não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="3f70c-108">This function has no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="3f70c-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3f70c-109">Return value</span></span>

<span data-ttu-id="3f70c-110">Se a função estiver em execução em um processo do Excel, retornará 0 em um **XLOPER12** do tipo **xlTypeInt**.</span><span class="sxs-lookup"><span data-stu-id="3f70c-110">If the function is running in an Excel process, returns 0 in an **XLOPER12** of type **xlTypeInt**.</span></span> <span data-ttu-id="3f70c-111">Se a função estiver em execução em um cluster, o tipo de retorno e o valor serão determinados pelo provedor do conector de cluster.</span><span class="sxs-lookup"><span data-stu-id="3f70c-111">If the function is running on a cluster, the return type and value is determined by the cluster connector provider.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="3f70c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f70c-112">Requirements</span></span>

<span data-ttu-id="3f70c-113">Essa função é definida no arquivo de cabeçalho xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="3f70c-113">This function is defined in the Xlcall.h header file.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f70c-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f70c-114">See also</span></span>

- [<span data-ttu-id="3f70c-115">Funções seguras para clusters</span><span class="sxs-lookup"><span data-stu-id="3f70c-115">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
- [<span data-ttu-id="3f70c-116">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="3f70c-116">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

