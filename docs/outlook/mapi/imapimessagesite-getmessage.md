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
ms.openlocfilehash: 03dd0553d0203585850ac5c4f8c91c86ef60236a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321277"
---
# <a name="imapimessagesitegetmessage"></a><span data-ttu-id="9791e-103">IMAPIMessageSite::GetMessage</span><span class="sxs-lookup"><span data-stu-id="9791e-103">IMAPIMessageSite::GetMessage</span></span>

  
  
<span data-ttu-id="9791e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9791e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9791e-105">Retorna a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="9791e-105">Returns the current message.</span></span>
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="9791e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9791e-106">Parameters</span></span>

 <span data-ttu-id="9791e-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="9791e-107">_ppmsg_</span></span>
  
> <span data-ttu-id="9791e-108">bota Um ponteiro para um ponteiro para a interface retornada para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="9791e-108">[out] A pointer to a pointer to the returned interface for the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9791e-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9791e-109">Return value</span></span>

<span data-ttu-id="9791e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="9791e-110">S_OK</span></span> 
  
> <span data-ttu-id="9791e-111">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="9791e-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="9791e-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="9791e-112">S_FALSE</span></span> 
  
> <span data-ttu-id="9791e-113">Nenhuma mensagem existe atualmente para o formulário de chamada.</span><span class="sxs-lookup"><span data-stu-id="9791e-113">No message currently exists for the calling form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9791e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9791e-114">Remarks</span></span>

<span data-ttu-id="9791e-115">Os formulários chamam o método **IMAPIMessageSite:: GetMessage** para obter uma interface de mensagem para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="9791e-115">Forms call the **IMAPIMessageSite::GetMessage** method to obtain a message interface for the current message.</span></span> <span data-ttu-id="9791e-116">A mensagem atual é a mesma que foi passada anteriormente no método [IPersistMessage:: InitNew](ipersistmessage-initnew.md), [IPersistMessage:: Load](ipersistmessage-load.md)ou [IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="9791e-116">The current message is the same message as was previously passed in the [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md), or [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method.</span></span> 
  
 <span data-ttu-id="9791e-117">**GetMessage** retornará S_FALSE se nenhuma mensagem existir no momento.</span><span class="sxs-lookup"><span data-stu-id="9791e-117">**GetMessage** returns S_FALSE if no message currently exists.</span></span> <span data-ttu-id="9791e-118">Este estado pode ocorrer após chamadas para o método [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) ou antes da próxima chamada a **IPersistMessage:: Load** ou **IPersistMessage:: SaveCompleted** é feita.</span><span class="sxs-lookup"><span data-stu-id="9791e-118">This state can occur after calls to the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method or before the next call to **IPersistMessage::Load** or **IPersistMessage::SaveCompleted** is made.</span></span> 
  
<span data-ttu-id="9791e-119">Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulário MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="9791e-119">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9791e-120">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9791e-120">MFCMAPI reference</span></span>

<span data-ttu-id="9791e-121">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9791e-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9791e-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="9791e-122">**File**</span></span>|<span data-ttu-id="9791e-123">**Função**</span><span class="sxs-lookup"><span data-stu-id="9791e-123">**Function**</span></span>|<span data-ttu-id="9791e-124">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="9791e-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9791e-125">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="9791e-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="9791e-126">CMyMAPIFormViewer:: GetSession</span><span class="sxs-lookup"><span data-stu-id="9791e-126">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="9791e-127">MFCMAPI usa o método **IMAPIMessageSite:: GetMessage** para retornar o ponteiro de mensagem atualmente em cache, se estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="9791e-127">MFCMAPI uses the **IMAPIMessageSite::GetMessage** method to return the currently cached message pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9791e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="9791e-128">See also</span></span>



[<span data-ttu-id="9791e-129">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="9791e-129">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="9791e-130">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="9791e-130">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="9791e-131">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9791e-131">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="9791e-132">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="9791e-132">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="9791e-133">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="9791e-133">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="9791e-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9791e-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="9791e-135">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="9791e-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="9791e-136">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="9791e-136">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

