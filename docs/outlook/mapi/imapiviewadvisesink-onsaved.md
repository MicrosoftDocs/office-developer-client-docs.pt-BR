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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1ae94b40d984adee0f3c888f69dfdbffb1e352e1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584433"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="67e55-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="67e55-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="67e55-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67e55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67e55-105">Notifica o Visualizador de formulário que tenha sido salva a mensagem atual em um formulário.</span><span class="sxs-lookup"><span data-stu-id="67e55-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="67e55-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67e55-106">Parameters</span></span>

<span data-ttu-id="67e55-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="67e55-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="67e55-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67e55-108">Return value</span></span>

<span data-ttu-id="67e55-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="67e55-109">S_OK</span></span> 
  
> <span data-ttu-id="67e55-110">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="67e55-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="67e55-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="67e55-111">Remarks</span></span>

<span data-ttu-id="67e55-112">Um objeto form chama o método **IMAPIViewAdviseSink::OnSaved** depois que a mensagem atual em um formulário foi salvo com êxito.</span><span class="sxs-lookup"><span data-stu-id="67e55-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="67e55-113">Isso permite que os visualizadores atualizam suas janelas para refletir as alterações à mensagem.</span><span class="sxs-lookup"><span data-stu-id="67e55-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="67e55-114">Para obter mais informações sobre as notificações do formulário, consulte [de envio e recebimento de notificações de formulário](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="67e55-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="67e55-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="67e55-115">See also</span></span>



[<span data-ttu-id="67e55-116">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="67e55-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

