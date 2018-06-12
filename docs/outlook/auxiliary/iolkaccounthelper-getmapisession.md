---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: Abre uma sessão MAPI e mantém uma referência para a sessão para o gerente de conta.
ms.openlocfilehash: 50809a00d13fd9f2a93bebc2961a134b3625e82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765975"
---
# <a name="iolkaccounthelpergetmapisession"></a><span data-ttu-id="dfa01-103">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="dfa01-103">IOlkAccountHelper::GetMapiSession</span></span>

<span data-ttu-id="dfa01-104">Abre uma sessão MAPI e mantém uma referência para a sessão para o gerente de conta.</span><span class="sxs-lookup"><span data-stu-id="dfa01-104">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dfa01-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="dfa01-105">Quick info</span></span>

<span data-ttu-id="dfa01-106">Consulte [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="dfa01-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a><span data-ttu-id="dfa01-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="dfa01-107">Parameters</span></span>

<span data-ttu-id="dfa01-108">_ppmsess_</span><span class="sxs-lookup"><span data-stu-id="dfa01-108">_ppmsess_</span></span>
  
> <span data-ttu-id="dfa01-109">[out] Sessão MAPI atual.</span><span class="sxs-lookup"><span data-stu-id="dfa01-109">[out] The current MAPI session.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="dfa01-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="dfa01-110">Return values</span></span>

<span data-ttu-id="dfa01-111">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="dfa01-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dfa01-112">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="dfa01-112">Remarks</span></span>

<span data-ttu-id="dfa01-113">Devido a problemas de referência circular, o próprio Gerenciador de conta não pode manter a referência para a sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="dfa01-113">Because of circular reference problems, the account manager itself cannot maintain the reference for the MAPI session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dfa01-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfa01-114">See also</span></span>

- [<span data-ttu-id="dfa01-115">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="dfa01-115">IOlkAccountHelper::HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md)
- [<span data-ttu-id="dfa01-116">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dfa01-116">IMAPISession : IUnknown</span></span>](http://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

