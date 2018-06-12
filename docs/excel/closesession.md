---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: af8f7398ed9d5edfbf1615930874a800d8835487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765267"
---
# <a name="closesession"></a><span data-ttu-id="13770-103">CloseSession</span><span class="sxs-lookup"><span data-stu-id="13770-103">CloseSession</span></span>

<span data-ttu-id="13770-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="13770-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="13770-105">Finaliza uma sessão com um cluster.</span><span class="sxs-lookup"><span data-stu-id="13770-105">Ends a session with a cluster.</span></span>
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="13770-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13770-106">Parameters</span></span>

<span data-ttu-id="13770-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="13770-107">_SessionId_</span></span>
  
> <span data-ttu-id="13770-108">A identificação da sessão para fechar.</span><span class="sxs-lookup"><span data-stu-id="13770-108">The ID of the session to close.</span></span> <span data-ttu-id="13770-109">Este valor deve corresponder o valor retornado pela [OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="13770-109">This value must match the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="13770-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="13770-110">Return value</span></span>

<span data-ttu-id="13770-111">**xlHpcRetSuccess** se a sessão é fechada; **xlHpcRetInvalidSessionId** se o argumento _SessionId_ é inválido; **xlHpcRetCallFailed** em outras falhas.</span><span class="sxs-lookup"><span data-stu-id="13770-111">**xlHpcRetSuccess** if the session closed; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="13770-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="13770-112">See also</span></span>

- [<span data-ttu-id="13770-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="13770-113">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="13770-114">Funções de conector de Cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="13770-114">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

