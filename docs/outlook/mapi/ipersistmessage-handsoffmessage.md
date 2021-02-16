---
title: IPersistMessageHandsOffMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.HandsOffMessage
api_type:
- COM
ms.assetid: 0e56b21d-0a2e-4fe6-83f4-c9daab2f3055
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 84f0ca88403980ff9ea1c91821a8a3d7edae74fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309713"
---
# <a name="ipersistmessagehandsoffmessage"></a><span data-ttu-id="79779-103">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="79779-103">IPersistMessage::HandsOffMessage</span></span>

  
  
<span data-ttu-id="79779-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79779-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79779-105">Faz com que o formulário libere sua mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="79779-105">Causes the form to release its current message.</span></span>
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="79779-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79779-106">Parameters</span></span>

<span data-ttu-id="79779-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="79779-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="79779-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="79779-108">Return value</span></span>

<span data-ttu-id="79779-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="79779-109">S_OK</span></span> 
  
> <span data-ttu-id="79779-110">A mensagem foi liberada com êxito.</span><span class="sxs-lookup"><span data-stu-id="79779-110">The message was successfully released.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="79779-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="79779-111">Remarks</span></span>

<span data-ttu-id="79779-112">Os formulários são transições para dois estados handsoff:</span><span class="sxs-lookup"><span data-stu-id="79779-112">Forms transition into two HandsOff states:</span></span>
  
- [<span data-ttu-id="79779-113">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="79779-113">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="79779-114">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="79779-114">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="79779-115">Quando um formulário está em qualquer um desses estados, ele está em processo de ser armazenado permanentemente.</span><span class="sxs-lookup"><span data-stu-id="79779-115">When a form is in either of these states, it is in the process of being stored permanently.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="79779-116">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="79779-116">Notes to implementers</span></span>

<span data-ttu-id="79779-117">Quando um visualizador de formulário chama o método **IPersistMessage::HandsOffMessage** enquanto o formulário está no estado [Normal](normal-state.md) ou [NoScribble,](noscribble-state.md) chame recursivamente **HandsOffMessage** em cada mensagem incorporada na mensagem atual e no método [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) em cada objeto OLE incorporado na mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="79779-117">When a form viewer calls the **IPersistMessage::HandsOffMessage** method while your form is in the [Normal](normal-state.md) or [NoScribble](noscribble-state.md) state, recursively call **HandsOffMessage** on each message embedded in the current message and the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method on each OLE object embedded in the current message.</span></span> <span data-ttu-id="79779-118">Em seguida, libere a mensagem atual e todas as mensagens e objetos OLE incorporados.</span><span class="sxs-lookup"><span data-stu-id="79779-118">Then release the current message and all embedded messages and OLE objects.</span></span> <span data-ttu-id="79779-119">Se o formulário estiver no estado Normal, transição para o estado HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="79779-119">If your form was in the Normal state, transition to the HandsOffFromNormal state.</span></span> <span data-ttu-id="79779-120">Se o formulário estava no estado NoScribble, transição para o estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="79779-120">If your form was in the NoScribble state, transition to the HandsOffAfterSave state.</span></span> <span data-ttu-id="79779-121">Após uma transição bem-sucedida, chame o [método IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) da mensagem e retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="79779-121">After a successful transition, call the message's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method and return S_OK.</span></span> 
  
<span data-ttu-id="79779-122">Quando um visualizador de formulário chamar **HandsOffMessage** enquanto o formulário estiver em um dos estados HandsOff, retorne E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="79779-122">When a form viewer calls **HandsOffMessage** while your form is in either of the HandsOff states, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="79779-123">For more information about the different states of a form, see [Form States](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="79779-123">For more information about the different states of a form, see [Form States](form-states.md).</span></span> <span data-ttu-id="79779-124">Para obter mais informações sobre como trabalhar com o estado HandsOff de objetos de armazenamento, consulte o método [IPersistStorage::HandsOffStorage.](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx)</span><span class="sxs-lookup"><span data-stu-id="79779-124">For more information about how to work with the HandsOff state of storage objects, see the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79779-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="79779-125">See also</span></span>



[<span data-ttu-id="79779-126">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="79779-126">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="79779-127">Estados do formulário</span><span class="sxs-lookup"><span data-stu-id="79779-127">Form States</span></span>](form-states.md)

