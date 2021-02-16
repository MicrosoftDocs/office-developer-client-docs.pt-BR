---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0fa5fe57e537a7b8c7d880b934809a6f68ce27a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408359"
---
# <a name="pingsession"></a><span data-ttu-id="d507c-103">PingSession</span><span class="sxs-lookup"><span data-stu-id="d507c-103">PingSession</span></span>

<span data-ttu-id="d507c-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d507c-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d507c-105">Verifica se uma sessão é válida.</span><span class="sxs-lookup"><span data-stu-id="d507c-105">Checks whether a session is valid.</span></span> <span data-ttu-id="d507c-106">Essa função normalmente é chamada quando o Excel precisa determinar se uma ID de sessão retornada anteriormente ainda está ativa e pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="d507c-106">This function is typically called when Excel needs to determine if a previously returned session ID is still active and can be used.</span></span>
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="d507c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d507c-107">Parameters</span></span>

<span data-ttu-id="d507c-108">_SessionID_</span><span class="sxs-lookup"><span data-stu-id="d507c-108">_SessionID_</span></span>
  
> <span data-ttu-id="d507c-109">A ID da sessão a ser ping.</span><span class="sxs-lookup"><span data-stu-id="d507c-109">The ID of the session to ping.</span></span> <span data-ttu-id="d507c-110">Esse valor deve corresponder a uma ID retornada por uma chamada anterior para [OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="d507c-110">This value must match an ID returned by a previous call to [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d507c-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d507c-111">Return value</span></span>

<span data-ttu-id="d507c-112">**xlHpcRetSuccess** se o  _argumento SessionId_ for válido; caso **contrário, xlHpcRetInvalidSessionId**.</span><span class="sxs-lookup"><span data-stu-id="d507c-112">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; otherwise **xlHpcRetInvalidSessionId**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d507c-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="d507c-113">See also</span></span>

- [<span data-ttu-id="d507c-114">OpenSession</span><span class="sxs-lookup"><span data-stu-id="d507c-114">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="d507c-115">Funções de conector de cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="d507c-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

