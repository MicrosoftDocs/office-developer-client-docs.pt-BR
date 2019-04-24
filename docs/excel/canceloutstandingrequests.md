---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 882458ab096cbced8e0635dab65fe0b1d680388f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310994"
---
# <a name="canceloutstandingrequests"></a><span data-ttu-id="66283-103">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="66283-103">CancelOutstandingRequests</span></span>

<span data-ttu-id="66283-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="66283-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="66283-105">Informa ao conector de cluster que um cálculo do Excel foi cancelado e, portanto, todas as chamadas de função pendentes nessa sessão podem ser canceladas também (e o Excel não espera retornos de chamada com seus resultados).</span><span class="sxs-lookup"><span data-stu-id="66283-105">Informs the cluster connector that an Excel calculation has been canceled, and therefore all pending function calls within that session may be cancelled as well (and that Excel does not expect callbacks with their results).</span></span>
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="66283-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66283-106">Parameters</span></span>

<span data-ttu-id="66283-107">_SessionID_</span><span class="sxs-lookup"><span data-stu-id="66283-107">_SessionID_</span></span>
  
> <span data-ttu-id="66283-108">A ID da sessão usada pelo cálculo cancelado.</span><span class="sxs-lookup"><span data-stu-id="66283-108">The ID of the session used by the canceled calculation.</span></span> <span data-ttu-id="66283-109">Esse valor corresponde ao valor retornado por [OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="66283-109">This value matches the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="66283-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="66283-110">Return value</span></span>

<span data-ttu-id="66283-111">**xlHpcRetSuccess** se o argumento _SessionID_ for válido; **xlHpcRetInvalidSessionId** se o argumento _SessionID_ for inválido; **xlHpcRetCallFailed** em outras falhas.</span><span class="sxs-lookup"><span data-stu-id="66283-111">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="66283-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="66283-112">Remarks</span></span>

<span data-ttu-id="66283-113">Os implementadores devem interromper todos os processos da sessão para melhorar o desempenho, como os resultados recebidos depois que essa chamada será descartada pelo Excel.</span><span class="sxs-lookup"><span data-stu-id="66283-113">Implementers should stop all processes for the session for improved performance, as any results received after this call will be discarded by Excel.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="66283-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="66283-114">See also</span></span>

- [<span data-ttu-id="66283-115">Funções de conector de cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="66283-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

