---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Libera o objeto de sessão MAPI que foi retornado por IOlkAccountHelper::GetMapiSession.
ms.openlocfilehash: 71931be73e75e858224d3da2c92071341ac45e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765950"
---
# <a name="iolkaccounthelperhandsoffsession"></a><span data-ttu-id="f5e2c-103">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="f5e2c-103">IOlkAccountHelper::HandsOffSession</span></span>

<span data-ttu-id="f5e2c-104">Libera o objeto de sessão MAPI que foi retornado por - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="f5e2c-104">Releases the MAPI session object that was returned by - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f5e2c-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="f5e2c-105">Quick info</span></span>

<span data-ttu-id="f5e2c-106">Consulte [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="f5e2c-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a><span data-ttu-id="f5e2c-107">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="f5e2c-107">Return values</span></span>

|<span data-ttu-id="f5e2c-108">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f5e2c-108">**HRESULT**</span></span>|<span data-ttu-id="f5e2c-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f5e2c-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5e2c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5e2c-110">S_OK</span></span>  <br/> |<span data-ttu-id="f5e2c-111">Se a implementação dos **IOlkAccountHelper** criar sua própria sessão MAPI que é retornado em **IOlkAccountHelper::GetMapiSession**, você deve liberar aqui, a sessão e retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="f5e2c-111">If your implementation of **IOlkAccountHelper** creates its own MAPI session that is returned in **IOlkAccountHelper::GetMapiSession**, you must release the session here and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="f5e2c-112">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="f5e2c-112">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="f5e2c-113">Se a implementação dos **IOlkAccountHelper** não criou seu próprio sessão MAPI, você deverá retornar somente E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="f5e2c-113">If your implementation of **IOlkAccountHelper** did not create its own MAPI session, you must return only E_NOTIMPL.</span></span> <span data-ttu-id="f5e2c-114">Nesse caso, isso é o único valor de retorno com suporte.</span><span class="sxs-lookup"><span data-stu-id="f5e2c-114">In this case, this is the only supported return value.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f5e2c-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5e2c-115">See also</span></span>

- [<span data-ttu-id="f5e2c-116">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="f5e2c-116">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="f5e2c-117">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="f5e2c-117">IOlkAccountHelper::GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md)

