---
title: IMAPIViewAdviseSinkOnSaved
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0f9aa5d508afeaf5933c50763e1e42832ae4e3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767364"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="674e7-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="674e7-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="674e7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="674e7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="674e7-105">Notifica o Visualizador de formulário que tenha sido salva a mensagem atual em um formulário.</span><span class="sxs-lookup"><span data-stu-id="674e7-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="674e7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="674e7-106">Parameters</span></span>

<span data-ttu-id="674e7-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="674e7-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="674e7-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="674e7-108">Return value</span></span>

<span data-ttu-id="674e7-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="674e7-109">S_OK</span></span> 
  
> <span data-ttu-id="674e7-110">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="674e7-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="674e7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="674e7-111">Remarks</span></span>

<span data-ttu-id="674e7-112">Um objeto form chama o método **IMAPIViewAdviseSink::OnSaved** depois que a mensagem atual em um formulário foi salvo com êxito.</span><span class="sxs-lookup"><span data-stu-id="674e7-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="674e7-113">Isso permite que os visualizadores atualizam suas janelas para refletir as alterações à mensagem.</span><span class="sxs-lookup"><span data-stu-id="674e7-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="674e7-114">Para obter mais informações sobre as notificações do formulário, consulte [de envio e recebimento de notificações de formulário](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="674e7-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="674e7-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="674e7-115">See also</span></span>



[<span data-ttu-id="674e7-116">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="674e7-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

