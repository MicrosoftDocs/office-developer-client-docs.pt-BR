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
ms.openlocfilehash: 2ec78331fd013777f001d39bd7e978a67abb5342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351195"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="a229a-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="a229a-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="a229a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a229a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a229a-105">Notifica o Visualizador de formulários de que a mensagem atual em um formulário foi salva.</span><span class="sxs-lookup"><span data-stu-id="a229a-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="a229a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a229a-106">Parameters</span></span>

<span data-ttu-id="a229a-107">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a229a-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="a229a-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a229a-108">Return value</span></span>

<span data-ttu-id="a229a-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="a229a-109">S_OK</span></span> 
  
> <span data-ttu-id="a229a-110">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="a229a-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a229a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a229a-111">Remarks</span></span>

<span data-ttu-id="a229a-112">Um objeto Form chama o método **IMAPIViewAdviseSink::** onsaved após a mensagem atual em um formulário ter sido salva com êxito.</span><span class="sxs-lookup"><span data-stu-id="a229a-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="a229a-113">Isso permite que os visualizadores atualizem suas janelas para refletir as alterações na mensagem.</span><span class="sxs-lookup"><span data-stu-id="a229a-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="a229a-114">Para obter mais informações sobre notificações de formulário, consulte [envio e recebimento de notificações de formulários](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="a229a-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a229a-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="a229a-115">See also</span></span>



[<span data-ttu-id="a229a-116">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a229a-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

