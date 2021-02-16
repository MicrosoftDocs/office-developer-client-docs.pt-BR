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
ms.openlocfilehash: 496732e334d2d39672048dd1a02346aaee4b70e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417025"
---
# <a name="imapimessagesitesubmitmessage"></a><span data-ttu-id="fcfb1-103">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="fcfb1-103">IMAPIMessageSite::SubmitMessage</span></span>

  
  
<span data-ttu-id="fcfb1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcfb1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcfb1-105">Solicita que a mensagem atual seja en fila para entrega.</span><span class="sxs-lookup"><span data-stu-id="fcfb1-105">Requests that the current message be queued for delivery.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="fcfb1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcfb1-106">Parameters</span></span>

 <span data-ttu-id="fcfb1-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fcfb1-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fcfb1-108">[in] Uma máscara de bits de sinalizadores que controla como uma mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="fcfb1-108">[in] A bitmask of flags that controls how a message is submitted.</span></span> <span data-ttu-id="fcfb1-109">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="fcfb1-109">The following flag can be set:</span></span>
    
<span data-ttu-id="fcfb1-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="fcfb1-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="fcfb1-111">O MAPI deve enviar a mensagem, mesmo que não possa ser enviada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="fcfb1-111">MAPI should submit the message even if it might not be sent immediately.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fcfb1-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fcfb1-112">Return value</span></span>

<span data-ttu-id="fcfb1-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="fcfb1-113">S_OK</span></span> 
  
> <span data-ttu-id="fcfb1-114">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="fcfb1-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fcfb1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcfb1-115">Remarks</span></span>

<span data-ttu-id="fcfb1-116">Os objetos de formulário chamam o método **IMAPIMessageSite::SubmitMessage** para solicitar que uma mensagem seja en fila para entrega.</span><span class="sxs-lookup"><span data-stu-id="fcfb1-116">Form objects call the **IMAPIMessageSite::SubmitMessage** method to request that a message be queued for delivery.</span></span> <span data-ttu-id="fcfb1-117">O site de mensagens deve chamar [o método IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) antes de enviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="fcfb1-117">The message site should call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method before submitting the message.</span></span> <span data-ttu-id="fcfb1-118">A mensagem não precisa ter sido salva anteriormente, porque **SubmitMessage** deve fazer com que a mensagem seja salva se a mensagem tiver sido modificada.</span><span class="sxs-lookup"><span data-stu-id="fcfb1-118">The message does not need to have been previously saved, because **SubmitMessage** should cause the message to be saved if the message has been modified.</span></span> <span data-ttu-id="fcfb1-119">Após o retorno de **SubmitMessage**, o formulário deve verificar se há uma mensagem atual e, em seguida, descartar a si mesmo se não existe.</span><span class="sxs-lookup"><span data-stu-id="fcfb1-119">After the return of **SubmitMessage**, the form must check for a current message and then dismiss itself if none exists.</span></span> 
  
<span data-ttu-id="fcfb1-120">Para uma lista de interfaces relacionadas a servidores de formulário, consulte [MAPI Form Interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="fcfb1-120">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fcfb1-121">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fcfb1-121">MFCMAPI reference</span></span>

<span data-ttu-id="fcfb1-122">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fcfb1-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fcfb1-123">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="fcfb1-123">**File**</span></span>|<span data-ttu-id="fcfb1-124">**Função**</span><span class="sxs-lookup"><span data-stu-id="fcfb1-124">**Function**</span></span>|<span data-ttu-id="fcfb1-125">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="fcfb1-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fcfb1-126">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="fcfb1-126">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="fcfb1-127">CMyMAPIFormViewer::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="fcfb1-127">CMyMAPIFormViewer::SubmitMessage</span></span>  <br/> |<span data-ttu-id="fcfb1-128">MFCMAPI usa o **método IMAPIMessageSite::SubmitMessage** para salvar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="fcfb1-128">MFCMAPI uses the **IMAPIMessageSite::SubmitMessage** method to save the message.</span></span> <span data-ttu-id="fcfb1-129">Primeiro, ele chama o **método IPersistMessage::HandsOffMessage** e, em seguida, chama **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="fcfb1-129">First, it calls the **IPersistMessage::HandsOffMessage** method, and then it calls **SubmitMessage**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fcfb1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcfb1-130">See also</span></span>



[<span data-ttu-id="fcfb1-131">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="fcfb1-131">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="fcfb1-132">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fcfb1-132">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="fcfb1-133">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="fcfb1-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="fcfb1-134">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="fcfb1-134">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

