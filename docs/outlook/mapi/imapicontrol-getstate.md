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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a6ae89bf9b2b16439cc06f0e106859dda10ea22c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766943"
---
# <a name="imapicontrolgetstate"></a><span data-ttu-id="7ca56-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="7ca56-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="7ca56-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ca56-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ca56-105">Recupera um valor que indica se o controle de botão está ativado ou desativado.</span><span class="sxs-lookup"><span data-stu-id="7ca56-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="7ca56-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="7ca56-106">Parameters</span></span>

 <span data-ttu-id="7ca56-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7ca56-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7ca56-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7ca56-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7ca56-109">_lpulState_</span><span class="sxs-lookup"><span data-stu-id="7ca56-109">_lpulState_</span></span>
  
> <span data-ttu-id="7ca56-110">[out] Um ponteiro para um valor que indica o estado do controle de botão.</span><span class="sxs-lookup"><span data-stu-id="7ca56-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="7ca56-111">Pode ser retornado um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7ca56-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="7ca56-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="7ca56-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="7ca56-113">O controle de botão está desabilitado e não pode ser clicado.</span><span class="sxs-lookup"><span data-stu-id="7ca56-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="7ca56-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="7ca56-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="7ca56-115">O controle de botão é ativado e pode ser clicado.</span><span class="sxs-lookup"><span data-stu-id="7ca56-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7ca56-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7ca56-116">Return value</span></span>

<span data-ttu-id="7ca56-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ca56-117">S_OK</span></span> 
  
> <span data-ttu-id="7ca56-118">O estado do controle botão foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="7ca56-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ca56-119">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="7ca56-119">Remarks</span></span>

<span data-ttu-id="7ca56-120">Provedores de serviços de implementam o método **IMAPIControl::GetState** para fornecer MAPI com o estado de um controle de botão.</span><span class="sxs-lookup"><span data-stu-id="7ca56-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="7ca56-121">Se o botão estiver habilitado, ele pode responder a um clique do mouse ou pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="7ca56-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="7ca56-122">Se ele estiver desabilitado, o botão aparece esmaecido e não responde a um clique do mouse ou pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="7ca56-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="7ca56-123">Para obter mais informações sobre como implementar **GetState** e o outro [IMAPIControl: IUnknown](imapicontroliunknown.md) métodos, consulte a [Implementação do objeto de controle](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="7ca56-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7ca56-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ca56-124">See also</span></span>



[<span data-ttu-id="7ca56-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="7ca56-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="7ca56-126">IMAPIControl: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ca56-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

