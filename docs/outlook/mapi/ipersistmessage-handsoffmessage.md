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
# <a name="ipersistmessagehandsoffmessage"></a><span data-ttu-id="34c52-103">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="34c52-103">IPersistMessage::HandsOffMessage</span></span>

  
  
<span data-ttu-id="34c52-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34c52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34c52-105">Faz com que o formulário libere a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="34c52-105">Causes the form to release its current message.</span></span>
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="34c52-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34c52-106">Parameters</span></span>

<span data-ttu-id="34c52-107">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="34c52-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="34c52-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="34c52-108">Return value</span></span>

<span data-ttu-id="34c52-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="34c52-109">S_OK</span></span> 
  
> <span data-ttu-id="34c52-110">A mensagem foi liberada com êxito.</span><span class="sxs-lookup"><span data-stu-id="34c52-110">The message was successfully released.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="34c52-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="34c52-111">Remarks</span></span>

<span data-ttu-id="34c52-112">Transição de formulários para dois Estados do HandsOff:</span><span class="sxs-lookup"><span data-stu-id="34c52-112">Forms transition into two HandsOff states:</span></span>
  
- [<span data-ttu-id="34c52-113">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="34c52-113">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="34c52-114">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="34c52-114">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="34c52-115">Quando um formulário está em um desses Estados, ele está no processo de ser armazenado permanentemente.</span><span class="sxs-lookup"><span data-stu-id="34c52-115">When a form is in either of these states, it is in the process of being stored permanently.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="34c52-116">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="34c52-116">Notes to implementers</span></span>

<span data-ttu-id="34c52-117">Quando um visualizador de formulários chama o método **IPersistMessage:: HandsOffMessage** enquanto o formulário está no estado [normal](normal-state.md) ou norabisco, chame recursivamente **HandsOffMessage** em cada mensagem inserida na mensagem atual e na [](noscribble-state.md) [ IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) método em cada objeto OLE incorporado na mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="34c52-117">When a form viewer calls the **IPersistMessage::HandsOffMessage** method while your form is in the [Normal](normal-state.md) or [NoScribble](noscribble-state.md) state, recursively call **HandsOffMessage** on each message embedded in the current message and the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method on each OLE object embedded in the current message.</span></span> <span data-ttu-id="34c52-118">Em seguida, libere a mensagem atual e todas as mensagens inseridas e objetos OLE.</span><span class="sxs-lookup"><span data-stu-id="34c52-118">Then release the current message and all embedded messages and OLE objects.</span></span> <span data-ttu-id="34c52-119">Se o formulário estava no estado normal, transição para o estado HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="34c52-119">If your form was in the Normal state, transition to the HandsOffFromNormal state.</span></span> <span data-ttu-id="34c52-120">Se o formulário estava no estado noRabisco, transição para o estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="34c52-120">If your form was in the NoScribble state, transition to the HandsOffAfterSave state.</span></span> <span data-ttu-id="34c52-121">Após uma transição bem-sucedida, chame o método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) do Message e retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="34c52-121">After a successful transition, call the message's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method and return S_OK.</span></span> 
  
<span data-ttu-id="34c52-122">Quando um visualizador de formulários chama **HandsOffMessage** enquanto o formulário está em um dos Estados HandsOff, retorne E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="34c52-122">When a form viewer calls **HandsOffMessage** while your form is in either of the HandsOff states, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="34c52-123">Para obter mais informações sobre os diferentes Estados de um formulário, confira [Estados de formulário](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="34c52-123">For more information about the different states of a form, see [Form States](form-states.md).</span></span> <span data-ttu-id="34c52-124">Para obter mais informações sobre como trabalhar com o estado HandsOff de objetos de armazenamento, consulte o método [IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) .</span><span class="sxs-lookup"><span data-stu-id="34c52-124">For more information about how to work with the HandsOff state of storage objects, see the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="34c52-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="34c52-125">See also</span></span>



[<span data-ttu-id="34c52-126">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="34c52-126">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="34c52-127">Estados de formulário</span><span class="sxs-lookup"><span data-stu-id="34c52-127">Form States</span></span>](form-states.md)

