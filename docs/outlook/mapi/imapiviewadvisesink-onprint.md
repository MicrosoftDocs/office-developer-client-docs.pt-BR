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
ms.openlocfilehash: 202d461d4acefe18e69b47db9319cb328c61406e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592315"
---
# <a name="imapiviewadvisesinkonprint"></a><span data-ttu-id="7954d-103">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="7954d-103">IMAPIViewAdviseSink::OnPrint</span></span>

  
  
<span data-ttu-id="7954d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7954d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7954d-105">Notifica o Visualizador de formulário do status impressão de um formulário.</span><span class="sxs-lookup"><span data-stu-id="7954d-105">Notifies the form viewer of the printing status of a form.</span></span>
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a><span data-ttu-id="7954d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7954d-106">Parameters</span></span>

 <span data-ttu-id="7954d-107">_dwPageNumber_</span><span class="sxs-lookup"><span data-stu-id="7954d-107">_dwPageNumber_</span></span>
  
> <span data-ttu-id="7954d-108">[in] Número da última página impressa.</span><span class="sxs-lookup"><span data-stu-id="7954d-108">[in] Number of the last page printed.</span></span>
    
 <span data-ttu-id="7954d-109">_hsStatus diferente_</span><span class="sxs-lookup"><span data-stu-id="7954d-109">_hrStatus_</span></span>
  
> <span data-ttu-id="7954d-110">[in] Um valor HRESULT que indica o status do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="7954d-110">[in] An HRESULT value indicating the status of the print job.</span></span> <span data-ttu-id="7954d-111">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="7954d-111">Possible values are:</span></span>
    
<span data-ttu-id="7954d-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="7954d-112">S_FALSE</span></span> 
  
> <span data-ttu-id="7954d-113">O trabalho de impressão foi concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="7954d-113">The printing job has finished successfully.</span></span>
    
<span data-ttu-id="7954d-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="7954d-114">S_OK</span></span> 
  
> <span data-ttu-id="7954d-115">O trabalho de impressão está em andamento.</span><span class="sxs-lookup"><span data-stu-id="7954d-115">The printing job is in progress.</span></span>
    
<span data-ttu-id="7954d-116">FALHA</span><span class="sxs-lookup"><span data-stu-id="7954d-116">FAILED</span></span> 
  
> <span data-ttu-id="7954d-117">O trabalho de impressão foi encerrado devido a uma falha.</span><span class="sxs-lookup"><span data-stu-id="7954d-117">The printing job was terminated due to a failure.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7954d-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7954d-118">Return value</span></span>

<span data-ttu-id="7954d-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="7954d-119">S_OK</span></span> 
  
> <span data-ttu-id="7954d-120">A notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7954d-120">The notification succeeded.</span></span>
    
<span data-ttu-id="7954d-121">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="7954d-121">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="7954d-122">O usuário cancelou a operação, geralmente clicando no botão Cancelar em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7954d-122">The user canceled the operation, typically by clicking the Cancel button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7954d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="7954d-123">Remarks</span></span>

<span data-ttu-id="7954d-124">Objetos de formulário chame o método de **IMAPIViewAdviseSink::OnPrint** durante a impressão para informar o Visualizador do progresso da impressão.</span><span class="sxs-lookup"><span data-stu-id="7954d-124">Form objects call the **IMAPIViewAdviseSink::OnPrint** method while printing to inform the viewer of printing progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7954d-125">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="7954d-125">Notes to callers</span></span>

<span data-ttu-id="7954d-126">Se o trabalho de impressão envolve várias páginas, é possível chamar **OnPrint** após cada página ser impressa.</span><span class="sxs-lookup"><span data-stu-id="7954d-126">If the printing job involves multiple pages, you can call **OnPrint** after each page is printed.</span></span> <span data-ttu-id="7954d-127">Definir _dwPageNumber_ para a página que está sendo impressa no momento e _hsStatus diferente_ para S_OK.</span><span class="sxs-lookup"><span data-stu-id="7954d-127">Set  _dwPageNumber_ to the page currently being printed and  _hrStatus_ to S_OK.</span></span> <span data-ttu-id="7954d-128">Quando o trabalho de impressão estiver concluído, chamada **OnPrint** com _dwPageNumber_ definido para a última página impressa e _hsStatus diferente_ definido como S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="7954d-128">When the printing job is complete, call **OnPrint** with  _dwPageNumber_ set to the last page printed and  _hrStatus_ set to S_FALSE.</span></span> 
  
<span data-ttu-id="7954d-129">Para obter mais informações sobre as notificações do formulário, consulte [de envio e recebimento de notificações de formulário](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="7954d-129">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7954d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7954d-130">See also</span></span>



[<span data-ttu-id="7954d-131">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7954d-131">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

