---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f477c617533d66fc129c7192c9f86bb8a46afbb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419006"
---
# <a name="imapicontrolgetstate"></a><span data-ttu-id="18bf6-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="18bf6-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="18bf6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18bf6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18bf6-105">Recupera um valor que indica se o controle de botão está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="18bf6-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="18bf6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18bf6-106">Parameters</span></span>

 <span data-ttu-id="18bf6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="18bf6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="18bf6-108">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="18bf6-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="18bf6-109">_lpulState_</span><span class="sxs-lookup"><span data-stu-id="18bf6-109">_lpulState_</span></span>
  
> <span data-ttu-id="18bf6-110">bota Um ponteiro para um valor que indica o estado do controle de botão.</span><span class="sxs-lookup"><span data-stu-id="18bf6-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="18bf6-111">Um dos valores a seguir pode ser retornado:</span><span class="sxs-lookup"><span data-stu-id="18bf6-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="18bf6-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="18bf6-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="18bf6-113">O controle de botão está desabilitado e não pode ser clicado.</span><span class="sxs-lookup"><span data-stu-id="18bf6-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="18bf6-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="18bf6-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="18bf6-115">O controle de botão está habilitado e pode ser clicado.</span><span class="sxs-lookup"><span data-stu-id="18bf6-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="18bf6-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="18bf6-116">Return value</span></span>

<span data-ttu-id="18bf6-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="18bf6-117">S_OK</span></span> 
  
> <span data-ttu-id="18bf6-118">O estado do controle de botão foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="18bf6-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18bf6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="18bf6-119">Remarks</span></span>

<span data-ttu-id="18bf6-120">Os provedores de serviços implementam o método **IMAPIControl:: GetState** para fornecer MAPI com o estado de um controle de botão.</span><span class="sxs-lookup"><span data-stu-id="18bf6-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="18bf6-121">Se o botão estiver habilitado, ele poderá responder a um clique do mouse ou pressionar tecla.</span><span class="sxs-lookup"><span data-stu-id="18bf6-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="18bf6-122">Se estiver desabilitada, o botão aparecerá esmaecido e não responderá a um clique do mouse ou a um pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="18bf6-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="18bf6-123">Para obter mais informações sobre como implementar **GetState** e outros métodos [IMAPIControl: IUnknown](imapicontroliunknown.md) , consulte [Control Object Implementation](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="18bf6-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="18bf6-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="18bf6-124">See also</span></span>



[<span data-ttu-id="18bf6-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="18bf6-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="18bf6-126">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="18bf6-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

