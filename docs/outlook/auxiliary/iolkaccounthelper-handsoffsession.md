---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Lança o objeto de sessão MAPI retornado por IOlkAccountHelper::GetMapiSession.
ms.openlocfilehash: c481cee1ecb8c2bd3997cdee8ae86c9c3b5a712e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322089"
---
# <a name="iolkaccounthelperhandsoffsession"></a><span data-ttu-id="9fb13-103">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="9fb13-103">IOlkAccountHelper::HandsOffSession</span></span>

<span data-ttu-id="9fb13-104">Libera o objeto de sessão MAPI retornado por- [IOlkAccountHelper:: GetMapiSession](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="9fb13-104">Releases the MAPI session object that was returned by - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9fb13-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="9fb13-105">Quick info</span></span>

<span data-ttu-id="9fb13-106">Confira [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="9fb13-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a><span data-ttu-id="9fb13-107">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="9fb13-107">Return values</span></span>

|<span data-ttu-id="9fb13-108">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9fb13-108">**HRESULT**</span></span>|<span data-ttu-id="9fb13-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9fb13-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9fb13-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="9fb13-110">S_OK</span></span>  <br/> |<span data-ttu-id="9fb13-111">Se sua implementação do **IOlkAccountHelper** criar sua própria sessão MAPI retornada no **IOlkAccountHelper:: GetMapiSession**, você deve liberar a sessão aqui e retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="9fb13-111">If your implementation of **IOlkAccountHelper** creates its own MAPI session that is returned in **IOlkAccountHelper::GetMapiSession**, you must release the session here and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="9fb13-112">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="9fb13-112">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="9fb13-113">Se sua implementação do **IOlkAccountHelper** não criou sua própria sessão MAPI, você deve retornar apenas E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="9fb13-113">If your implementation of **IOlkAccountHelper** did not create its own MAPI session, you must return only E_NOTIMPL.</span></span> <span data-ttu-id="9fb13-114">Nesse caso, esse é o único valor de retorno com suporte.</span><span class="sxs-lookup"><span data-stu-id="9fb13-114">In this case, this is the only supported return value.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fb13-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fb13-115">See also</span></span>

- [<span data-ttu-id="9fb13-116">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="9fb13-116">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="9fb13-117">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="9fb13-117">IOlkAccountHelper::GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md)

