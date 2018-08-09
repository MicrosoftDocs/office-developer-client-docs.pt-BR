---
title: IMAPIMessageSiteGetMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetMessage
api_type:
- COM
ms.assetid: 49d12c49-84f8-44ac-bc4a-2ee44a46f8c1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b3cdd9994de3e2a02a5302068881abce57a632a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767078"
---
# <a name="imapimessagesitegetmessage"></a><span data-ttu-id="a5af5-103">IMAPIMessageSite::GetMessage</span><span class="sxs-lookup"><span data-stu-id="a5af5-103">IMAPIMessageSite::GetMessage</span></span>

  
  
<span data-ttu-id="a5af5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a5af5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a5af5-105">Retorna a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="a5af5-105">Returns the current message.</span></span>
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="a5af5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5af5-106">Parameters</span></span>

 <span data-ttu-id="a5af5-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="a5af5-107">_ppmsg_</span></span>
  
> <span data-ttu-id="a5af5-108">[out] Um ponteiro para um ponteiro para a interface retornada para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="a5af5-108">[out] A pointer to a pointer to the returned interface for the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5af5-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a5af5-109">Return value</span></span>

<span data-ttu-id="a5af5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a5af5-110">S_OK</span></span> 
  
> <span data-ttu-id="a5af5-111">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="a5af5-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a5af5-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="a5af5-112">S_FALSE</span></span> 
  
> <span data-ttu-id="a5af5-113">Nenhuma mensagem atualmente existe para o formulário de chamada.</span><span class="sxs-lookup"><span data-stu-id="a5af5-113">No message currently exists for the calling form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5af5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5af5-114">Remarks</span></span>

<span data-ttu-id="a5af5-115">Formulários chamar o método **IMAPIMessageSite::GetMessage** para obter uma interface de mensagem para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="a5af5-115">Forms call the **IMAPIMessageSite::GetMessage** method to obtain a message interface for the current message.</span></span> <span data-ttu-id="a5af5-116">A mensagem atual é a mesma mensagem conforme passado anteriormente no método [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md)ou [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="a5af5-116">The current message is the same message as was previously passed in the [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md), or [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method.</span></span> 
  
 <span data-ttu-id="a5af5-117">**GetMessage** retorna S_FALSE se nenhuma mensagem existir no momento.</span><span class="sxs-lookup"><span data-stu-id="a5af5-117">**GetMessage** returns S_FALSE if no message currently exists.</span></span> <span data-ttu-id="a5af5-118">Nesse estado pode ocorrer após a chamada para o método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) ou antes da próxima chamada para **IPersistMessage::Load** ou **IPersistMessage::SaveCompleted** é feita.</span><span class="sxs-lookup"><span data-stu-id="a5af5-118">This state can occur after calls to the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method or before the next call to **IPersistMessage::Load** or **IPersistMessage::SaveCompleted** is made.</span></span> 
  
<span data-ttu-id="a5af5-119">Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="a5af5-119">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a5af5-120">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a5af5-120">MFCMAPI reference</span></span>

<span data-ttu-id="a5af5-121">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5af5-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a5af5-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="a5af5-122">**File**</span></span>|<span data-ttu-id="a5af5-123">**Function**</span><span class="sxs-lookup"><span data-stu-id="a5af5-123">**Function**</span></span>|<span data-ttu-id="a5af5-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a5af5-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a5af5-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="a5af5-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="a5af5-126">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="a5af5-126">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="a5af5-127">MFCMAPI usa o método **IMAPIMessageSite::GetMessage** para retornar o ponteiro de mensagem atualmente em cache, se ele estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="a5af5-127">MFCMAPI uses the **IMAPIMessageSite::GetMessage** method to return the currently cached message pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a5af5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5af5-128">See also</span></span>



[<span data-ttu-id="a5af5-129">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="a5af5-129">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="a5af5-130">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="a5af5-130">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="a5af5-131">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5af5-131">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="a5af5-132">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="a5af5-132">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="a5af5-133">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="a5af5-133">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="a5af5-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5af5-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="a5af5-135">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="a5af5-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a5af5-136">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="a5af5-136">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

