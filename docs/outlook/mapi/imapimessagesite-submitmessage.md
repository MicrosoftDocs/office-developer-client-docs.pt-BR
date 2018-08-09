---
title: IMAPIMessageSiteSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 694ee8b12b9918502e60c0c6ea92992cc1062945
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767098"
---
# <a name="imapimessagesitesubmitmessage"></a><span data-ttu-id="d7fe9-103">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="d7fe9-103">IMAPIMessageSite::SubmitMessage</span></span>

  
  
<span data-ttu-id="d7fe9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7fe9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7fe9-105">Solicita que a mensagem atual ser colocados na fila de entrega.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-105">Requests that the current message be queued for delivery.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d7fe9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7fe9-106">Parameters</span></span>

 <span data-ttu-id="d7fe9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d7fe9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d7fe9-108">[in] Uma bitmask dos sinalizadores que controla como uma mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-108">[in] A bitmask of flags that controls how a message is submitted.</span></span> <span data-ttu-id="d7fe9-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="d7fe9-109">The following flag can be set:</span></span>
    
<span data-ttu-id="d7fe9-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="d7fe9-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="d7fe9-111">MAPI deve enviar a mensagem, mesmo que não podem ser enviado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-111">MAPI should submit the message even if it might not be sent immediately.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d7fe9-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d7fe9-112">Return value</span></span>

<span data-ttu-id="d7fe9-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7fe9-113">S_OK</span></span> 
  
> <span data-ttu-id="d7fe9-114">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7fe9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7fe9-115">Remarks</span></span>

<span data-ttu-id="d7fe9-116">Objetos de formulário chame o método de **IMAPIMessageSite::SubmitMessage** para solicitar que uma mensagem ser colocados na fila de entrega.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-116">Form objects call the **IMAPIMessageSite::SubmitMessage** method to request that a message be queued for delivery.</span></span> <span data-ttu-id="d7fe9-117">O site de mensagem deve chamar o método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) antes de enviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-117">The message site should call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method before submitting the message.</span></span> <span data-ttu-id="d7fe9-118">A mensagem não precisa tenha sido salva anteriormente, porque **SubmitMessage** deve fazer com que a mensagem a ser salvo se a mensagem tiver sido modificada.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-118">The message does not need to have been previously saved, because **SubmitMessage** should cause the message to be saved if the message has been modified.</span></span> <span data-ttu-id="d7fe9-119">Após o retorno de **SubmitMessage**, o formulário deve verificar se há uma mensagem atual e, em seguida, descartar a próprio se não houver nenhum.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-119">After the return of **SubmitMessage**, the form must check for a current message and then dismiss itself if none exists.</span></span> 
  
<span data-ttu-id="d7fe9-120">Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="d7fe9-120">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d7fe9-121">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d7fe9-121">MFCMAPI reference</span></span>

<span data-ttu-id="d7fe9-122">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d7fe9-123">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d7fe9-123">**File**</span></span>|<span data-ttu-id="d7fe9-124">**Function**</span><span class="sxs-lookup"><span data-stu-id="d7fe9-124">**Function**</span></span>|<span data-ttu-id="d7fe9-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d7fe9-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d7fe9-126">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="d7fe9-126">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="d7fe9-127">CMyMAPIFormViewer::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="d7fe9-127">CMyMAPIFormViewer::SubmitMessage</span></span>  <br/> |<span data-ttu-id="d7fe9-128">MFCMAPI usa o método **IMAPIMessageSite::SubmitMessage** para salvar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-128">MFCMAPI uses the **IMAPIMessageSite::SubmitMessage** method to save the message.</span></span> <span data-ttu-id="d7fe9-129">Primeiro, ele chama o método **IPersistMessage::HandsOffMessage** e, em seguida, ele chama **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-129">First, it calls the **IPersistMessage::HandsOffMessage** method, and then it calls **SubmitMessage**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7fe9-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7fe9-130">See also</span></span>



[<span data-ttu-id="d7fe9-131">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="d7fe9-131">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="d7fe9-132">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d7fe9-132">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="d7fe9-133">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d7fe9-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="d7fe9-134">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="d7fe9-134">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

