---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 165be9eada54b2030471fc10e7a0bf0c7dcc7c8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765443"
---
# <a name="pingsession"></a><span data-ttu-id="7d5c4-103">PingSession</span><span class="sxs-lookup"><span data-stu-id="7d5c4-103">PingSession</span></span>

<span data-ttu-id="7d5c4-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7d5c4-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7d5c4-105">Verifica se a uma sessão é válida.</span><span class="sxs-lookup"><span data-stu-id="7d5c4-105">Checks whether a session is valid.</span></span> <span data-ttu-id="7d5c4-106">Essa função geralmente é chamada quando o Excel precisa para determinar se uma identificação de sessão retornadas anteriormente ainda está ativa e pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="7d5c4-106">This function is typically called when Excel needs to determine if a previously returned session ID is still active and can be used.</span></span>
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="7d5c4-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="7d5c4-107">Parameters</span></span>

<span data-ttu-id="7d5c4-108">_SessionID_</span><span class="sxs-lookup"><span data-stu-id="7d5c4-108">_SessionID_</span></span>
  
> <span data-ttu-id="7d5c4-109">A identificação da sessão de ping.</span><span class="sxs-lookup"><span data-stu-id="7d5c4-109">The ID of the session to ping.</span></span> <span data-ttu-id="7d5c4-110">Este valor deve corresponder a uma ID retornada por uma chamada anterior para [OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="7d5c4-110">This value must match an ID returned by a previous call to [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7d5c4-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7d5c4-111">Return value</span></span>

<span data-ttu-id="7d5c4-112">**xlHpcRetSuccess** se o argumento _SessionId_ é válido. Caso contrário **xlHpcRetInvalidSessionId**.</span><span class="sxs-lookup"><span data-stu-id="7d5c4-112">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; otherwise **xlHpcRetInvalidSessionId**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7d5c4-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d5c4-113">See also</span></span>

- [<span data-ttu-id="7d5c4-114">OpenSession</span><span class="sxs-lookup"><span data-stu-id="7d5c4-114">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="7d5c4-115">Funções de conector de Cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="7d5c4-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

