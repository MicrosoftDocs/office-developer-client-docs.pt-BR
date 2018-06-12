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
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f42ccbeb94e1fc6b6cf880f1b32ee1bfeb24997e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765501"
---
# <a name="xlrunningoncluster"></a><span data-ttu-id="52d21-104">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="52d21-104">xlRunningOnCluster</span></span>

<span data-ttu-id="52d21-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="52d21-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="52d21-106">Retorna um valor que indica se a função definida pelo usuário está sendo executado em um cluster.</span><span class="sxs-lookup"><span data-stu-id="52d21-106">Returns a value that indicates whether the user-defined function is running on a cluster.</span></span> 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="52d21-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="52d21-107">Parameters</span></span>

<span data-ttu-id="52d21-108">Essa função não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="52d21-108">This function has no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="52d21-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="52d21-109">Return value</span></span>

<span data-ttu-id="52d21-110">Se a função estiver em execução em um processo de Excel, retornará 0 no **XLOPER12** do tipo **xlTypeInt**.</span><span class="sxs-lookup"><span data-stu-id="52d21-110">If the function is running in an Excel process, returns 0 in an **XLOPER12** of type **xlTypeInt**.</span></span> <span data-ttu-id="52d21-111">Se a função estiver em execução em um cluster, o tipo de retorno e o valor é determinado pelo provedor de conector de cluster.</span><span class="sxs-lookup"><span data-stu-id="52d21-111">If the function is running on a cluster, the return type and value is determined by the cluster connector provider.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="52d21-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52d21-112">Requirements</span></span>

<span data-ttu-id="52d21-113">Esta função é definida no arquivo de cabeçalho xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="52d21-113">This function is defined in the Xlcall.h header file.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="52d21-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="52d21-114">See also</span></span>

- [<span data-ttu-id="52d21-115">Funções de segurança de cluster</span><span class="sxs-lookup"><span data-stu-id="52d21-115">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
- [<span data-ttu-id="52d21-116">Funções da API C que podem ser chamadas apenas por um DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="52d21-116">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

