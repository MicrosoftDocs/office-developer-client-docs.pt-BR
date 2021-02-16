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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418628"
---
# <a name="iolkaccounthelperhandsoffsession"></a><span data-ttu-id="53171-103">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="53171-103">IOlkAccountHelper::HandsOffSession</span></span>

<span data-ttu-id="53171-104">Libera o objeto de sessão MAPI retornado por - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="53171-104">Releases the MAPI session object that was returned by - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="53171-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="53171-105">Quick info</span></span>

<span data-ttu-id="53171-106">Confira [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="53171-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a><span data-ttu-id="53171-107">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="53171-107">Return values</span></span>

|<span data-ttu-id="53171-108">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="53171-108">**HRESULT**</span></span>|<span data-ttu-id="53171-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="53171-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53171-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="53171-110">S_OK</span></span>  <br/> |<span data-ttu-id="53171-111">Se sua implementação de **IOlkAccountHelper** criar sua própria sessão MAPI retornada em **IOlkAccountHelper::GetMapiSession**, você deverá liberar a sessão aqui e retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="53171-111">If your implementation of **IOlkAccountHelper** creates its own MAPI session that is returned in **IOlkAccountHelper::GetMapiSession**, you must release the session here and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="53171-112">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="53171-112">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="53171-113">Se a implementação de **IOlkAccountHelper** não tiver criado sua própria sessão MAPI, você deverá retornar somente E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="53171-113">If your implementation of **IOlkAccountHelper** did not create its own MAPI session, you must return only E_NOTIMPL.</span></span> <span data-ttu-id="53171-114">Nesse caso, este é o único valor de retorno com suporte.</span><span class="sxs-lookup"><span data-stu-id="53171-114">In this case, this is the only supported return value.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53171-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="53171-115">See also</span></span>

- [<span data-ttu-id="53171-116">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="53171-116">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="53171-117">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="53171-117">IOlkAccountHelper::GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md)

