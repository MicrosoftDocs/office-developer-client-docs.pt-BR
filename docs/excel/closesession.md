---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9186fb14c33d507b8c9ae709a67f1b43e6206d5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422534"
---
# <a name="closesession"></a><span data-ttu-id="bcc50-103">CloseSession</span><span class="sxs-lookup"><span data-stu-id="bcc50-103">CloseSession</span></span>

<span data-ttu-id="bcc50-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bcc50-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bcc50-105">Encerra uma sessão com um cluster.</span><span class="sxs-lookup"><span data-stu-id="bcc50-105">Ends a session with a cluster.</span></span>
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="bcc50-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bcc50-106">Parameters</span></span>

<span data-ttu-id="bcc50-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="bcc50-107">_SessionId_</span></span>
  
> <span data-ttu-id="bcc50-108">A ID da sessão a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="bcc50-108">The ID of the session to close.</span></span> <span data-ttu-id="bcc50-109">Esse valor deve corresponder ao valor retornado por [OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="bcc50-109">This value must match the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bcc50-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bcc50-110">Return value</span></span>

<span data-ttu-id="bcc50-111">**xlHpcRetSuccess** se a sessão foi fechada; **xlHpcRetInvalidSessionId** se o  _argumento SessionId_ for inválido; **xlHpcRetCallFailed** em outras falhas.</span><span class="sxs-lookup"><span data-stu-id="bcc50-111">**xlHpcRetSuccess** if the session closed; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bcc50-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcc50-112">See also</span></span>

- [<span data-ttu-id="bcc50-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="bcc50-113">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="bcc50-114">Funções de conector de cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="bcc50-114">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

