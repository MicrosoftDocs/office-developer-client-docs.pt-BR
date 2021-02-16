---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e4df0c5772f28ab4ab8d84eaddfe4409a88061b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421834"
---
# <a name="opensession"></a><span data-ttu-id="bbfeb-103">OpenSession</span><span class="sxs-lookup"><span data-stu-id="bbfeb-103">OpenSession</span></span>

<span data-ttu-id="bbfeb-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bbfeb-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bbfeb-105">Cria uma sessão na qual funções definidas pelo usuário podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="bbfeb-105">Creates a session in which user-defined functions can be executed.</span></span>
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a><span data-ttu-id="bbfeb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbfeb-106">Parameters</span></span>

<span data-ttu-id="bbfeb-107">_Parâmetros_</span><span class="sxs-lookup"><span data-stu-id="bbfeb-107">_Params_</span></span>
  
> <span data-ttu-id="bbfeb-108">Um ponteiro para a cadeia de caracteres UNICODE delimitada por ponto-e-vírgula dos parâmetros da sessão.</span><span class="sxs-lookup"><span data-stu-id="bbfeb-108">A pointer to semicolon-delimited UNICODE string of parameters for the session.</span></span> <span data-ttu-id="bbfeb-109">O Excel não usa esse argumento.</span><span class="sxs-lookup"><span data-stu-id="bbfeb-109">Excel does not use this argument.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bbfeb-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bbfeb-110">Return value</span></span>

<span data-ttu-id="bbfeb-111">Uma ID de sessão a ser usada em outras chamadas para o conector do cluster, se a sessão tiver sido criada com êxito; Caso **contrário, xlHpcRetCallFailed**.</span><span class="sxs-lookup"><span data-stu-id="bbfeb-111">A session ID to use in other calls to the cluster connector, if the session was successfully created; otherwise **xlHpcRetCallFailed**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bbfeb-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbfeb-112">See also</span></span>

- [<span data-ttu-id="bbfeb-113">Funções de conector de cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="bbfeb-113">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

