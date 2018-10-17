---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: Abre uma sessão MAPI e mantém uma referência à sessão para o gerente de conta.
ms.openlocfilehash: 5886ac1ae1bb8f3b43e09f49e48434d9a73656ce
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392596"
---
# <a name="iolkaccounthelpergetmapisession"></a><span data-ttu-id="debb2-103">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="debb2-103">IOlkAccountHelper::GetMapiSession</span></span>

<span data-ttu-id="debb2-104">Abre uma sessão MAPI e mantém uma referência à sessão para o gerente de conta.</span><span class="sxs-lookup"><span data-stu-id="debb2-104">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="debb2-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="debb2-105">Quick info</span></span>

<span data-ttu-id="debb2-106">Confira [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="debb2-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a><span data-ttu-id="debb2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="debb2-107">Parameters</span></span>

<span data-ttu-id="debb2-108">_ppmsess_</span><span class="sxs-lookup"><span data-stu-id="debb2-108">_ppmsess_</span></span>
  
> <span data-ttu-id="debb2-109">[out] A sessão MAPI atual.</span><span class="sxs-lookup"><span data-stu-id="debb2-109">[out] The current MAPI session.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="debb2-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="debb2-110">Return Values</span></span>

<span data-ttu-id="debb2-111">S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="debb2-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="debb2-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="debb2-112">Remarks</span></span>

<span data-ttu-id="debb2-113">Devido a problemas de referência circular, o gerente de conta em si não pode manter a referência para a sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="debb2-113">Because of circular reference problems, the account manager itself cannot maintain the reference for the MAPI session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="debb2-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="debb2-114">See also</span></span>

- [<span data-ttu-id="debb2-115">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="debb2-115">IOlkAccountHelper::HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md)
- [<span data-ttu-id="debb2-116">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="debb2-116">IMAPISession : IUnknown</span></span>](https://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

