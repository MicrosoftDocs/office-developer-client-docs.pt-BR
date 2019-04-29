---
title: IMAPIViewAdviseSinkOnShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnShutdown
api_type:
- COM
ms.assetid: c9c3aecf-5e4b-407a-8ea1-6211b4c6e0a5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b43c1b96130052a05ac390f10f545a66fe72b7fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428519"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="75a0f-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="75a0f-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="75a0f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75a0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75a0f-105">Notifica o Visualizador de formulários de que um formulário está sendo fechado.</span><span class="sxs-lookup"><span data-stu-id="75a0f-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="75a0f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75a0f-106">Parameters</span></span>

<span data-ttu-id="75a0f-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="75a0f-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="75a0f-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="75a0f-108">Return value</span></span>

<span data-ttu-id="75a0f-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="75a0f-109">S_OK</span></span> 
  
> <span data-ttu-id="75a0f-110">A notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="75a0f-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="75a0f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="75a0f-111">Remarks</span></span>

<span data-ttu-id="75a0f-112">Para obter mais informações sobre notificações de formulário, consulte [envio e recebimento de notificações de formulários](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="75a0f-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="75a0f-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="75a0f-113">See also</span></span>



[<span data-ttu-id="75a0f-114">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="75a0f-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

