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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322173"
---
# <a name="iolkaccounthelpergetmapisession"></a><span data-ttu-id="a13aa-103">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="a13aa-103">IOlkAccountHelper::GetMapiSession</span></span>

<span data-ttu-id="a13aa-104">Abre uma sessão MAPI e mantém uma referência à sessão para o gerente de conta.</span><span class="sxs-lookup"><span data-stu-id="a13aa-104">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a13aa-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="a13aa-105">Quick info</span></span>

<span data-ttu-id="a13aa-106">Confira [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="a13aa-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a><span data-ttu-id="a13aa-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a13aa-107">Parameters</span></span>

<span data-ttu-id="a13aa-108">_ppmsess_</span><span class="sxs-lookup"><span data-stu-id="a13aa-108">_ppmsess_</span></span>
  
> <span data-ttu-id="a13aa-109">[out] A sessão MAPI atual.</span><span class="sxs-lookup"><span data-stu-id="a13aa-109">[out] The current MAPI session.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="a13aa-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a13aa-110">Return values</span></span>

<span data-ttu-id="a13aa-111">S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="a13aa-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a13aa-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="a13aa-112">Remarks</span></span>

<span data-ttu-id="a13aa-113">Devido a problemas de referência circular, o gerente de conta em si não pode manter a referência para a sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="a13aa-113">Because of circular reference problems, the account manager itself cannot maintain the reference for the MAPI session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a13aa-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="a13aa-114">See also</span></span>

- [<span data-ttu-id="a13aa-115">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="a13aa-115">IOlkAccountHelper::HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md)
- [<span data-ttu-id="a13aa-116">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a13aa-116">IMAPISession : IUnknown</span></span>](https://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

