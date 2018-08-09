---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 782843f11643e203488b313181d224443a1d36c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765430"
---
# <a name="opensession"></a><span data-ttu-id="52250-103">OpenSession</span><span class="sxs-lookup"><span data-stu-id="52250-103">OpenSession</span></span>

<span data-ttu-id="52250-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="52250-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="52250-105">Cria uma sessão em que as funções definidas pelo usuário podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="52250-105">Creates a session in which user-defined functions can be executed.</span></span>
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a><span data-ttu-id="52250-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52250-106">Parameters</span></span>

<span data-ttu-id="52250-107">_Parâmetros_</span><span class="sxs-lookup"><span data-stu-id="52250-107">_Params_</span></span>
  
> <span data-ttu-id="52250-108">Um ponteiro para separados por ponto-e-vírgula de cadeia de caracteres UNICODE de parâmetros para a sessão.</span><span class="sxs-lookup"><span data-stu-id="52250-108">A pointer to semicolon-delimited UNICODE string of parameters for the session.</span></span> <span data-ttu-id="52250-109">O Excel não usa este argumento.</span><span class="sxs-lookup"><span data-stu-id="52250-109">Excel does not use this argument.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="52250-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="52250-110">Return value</span></span>

<span data-ttu-id="52250-111">Uma identificação de sessão para usar em outras chamadas para o conector de cluster, se a sessão foi criada com êxito; Caso contrário **xlHpcRetCallFailed**.</span><span class="sxs-lookup"><span data-stu-id="52250-111">A session ID to use in other calls to the cluster connector, if the session was successfully created; otherwise **xlHpcRetCallFailed**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="52250-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="52250-112">See also</span></span>

- [<span data-ttu-id="52250-113">Funções de conector de cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="52250-113">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

