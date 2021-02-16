---
title: IMAPIViewAdviseSinkOnPrint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e66315042f8b5cd5aff0e4aa076588c9f312376a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406168"
---
# <a name="imapiviewadvisesinkonprint"></a><span data-ttu-id="5feb0-103">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="5feb0-103">IMAPIViewAdviseSink::OnPrint</span></span>

  
  
<span data-ttu-id="5feb0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5feb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5feb0-105">Notifica o visualizador de formulário sobre o status de impressão de um formulário.</span><span class="sxs-lookup"><span data-stu-id="5feb0-105">Notifies the form viewer of the printing status of a form.</span></span>
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a><span data-ttu-id="5feb0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5feb0-106">Parameters</span></span>

 <span data-ttu-id="5feb0-107">_dwPageNumber_</span><span class="sxs-lookup"><span data-stu-id="5feb0-107">_dwPageNumber_</span></span>
  
> <span data-ttu-id="5feb0-108">[in] Número da última página impressa.</span><span class="sxs-lookup"><span data-stu-id="5feb0-108">[in] Number of the last page printed.</span></span>
    
 <span data-ttu-id="5feb0-109">_hrStatus_</span><span class="sxs-lookup"><span data-stu-id="5feb0-109">_hrStatus_</span></span>
  
> <span data-ttu-id="5feb0-110">[in] Um valor HRESULT que indica o status do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="5feb0-110">[in] An HRESULT value indicating the status of the print job.</span></span> <span data-ttu-id="5feb0-111">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="5feb0-111">Possible values are:</span></span>
    
<span data-ttu-id="5feb0-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="5feb0-112">S_FALSE</span></span> 
  
> <span data-ttu-id="5feb0-113">O trabalho de impressão foi concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="5feb0-113">The printing job has finished successfully.</span></span>
    
<span data-ttu-id="5feb0-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="5feb0-114">S_OK</span></span> 
  
> <span data-ttu-id="5feb0-115">O trabalho de impressão está em andamento.</span><span class="sxs-lookup"><span data-stu-id="5feb0-115">The printing job is in progress.</span></span>
    
<span data-ttu-id="5feb0-116">FALHA</span><span class="sxs-lookup"><span data-stu-id="5feb0-116">FAILED</span></span> 
  
> <span data-ttu-id="5feb0-117">O trabalho de impressão foi encerrado devido a uma falha.</span><span class="sxs-lookup"><span data-stu-id="5feb0-117">The printing job was terminated due to a failure.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5feb0-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5feb0-118">Return value</span></span>

<span data-ttu-id="5feb0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="5feb0-119">S_OK</span></span> 
  
> <span data-ttu-id="5feb0-120">A notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5feb0-120">The notification succeeded.</span></span>
    
<span data-ttu-id="5feb0-121">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="5feb0-121">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="5feb0-122">O usuário cancelou a operação, normalmente clicando no botão Cancelar em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5feb0-122">The user canceled the operation, typically by clicking the Cancel button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5feb0-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5feb0-123">Remarks</span></span>

<span data-ttu-id="5feb0-124">Os objetos de formulário chamam o método **IMAPIViewAdviseSink::OnPrint** durante a impressão para informar o visualizador sobre o progresso da impressão.</span><span class="sxs-lookup"><span data-stu-id="5feb0-124">Form objects call the **IMAPIViewAdviseSink::OnPrint** method while printing to inform the viewer of printing progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5feb0-125">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="5feb0-125">Notes to callers</span></span>

<span data-ttu-id="5feb0-126">Se o trabalho de impressão envolver várias páginas, você poderá chamar **OnPrint** depois que cada página for impressa.</span><span class="sxs-lookup"><span data-stu-id="5feb0-126">If the printing job involves multiple pages, you can call **OnPrint** after each page is printed.</span></span> <span data-ttu-id="5feb0-127">De  _definir dwPageNumber_ como a página que está sendo impressa no momento e  _hrStatus_ como S_OK.</span><span class="sxs-lookup"><span data-stu-id="5feb0-127">Set  _dwPageNumber_ to the page currently being printed and  _hrStatus_ to S_OK.</span></span> <span data-ttu-id="5feb0-128">Quando o trabalho de impressão for concluído, chame **OnPrint** com  _dwPageNumber_ definida como a última página impressa e  _hrStatus_ definida como S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="5feb0-128">When the printing job is complete, call **OnPrint** with  _dwPageNumber_ set to the last page printed and  _hrStatus_ set to S_FALSE.</span></span> 
  
<span data-ttu-id="5feb0-129">Para obter mais informações sobre notificações de formulário, consulte [Envio e recebimento de notificações de formulário.](sending-and-receiving-form-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="5feb0-129">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5feb0-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="5feb0-130">See also</span></span>



[<span data-ttu-id="5feb0-131">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5feb0-131">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

