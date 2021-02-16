---
title: IMAPISupportSpoolerYield
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerYield
api_type:
- COM
ms.assetid: f5c6ba8f-4ef5-4d60-b4e6-5b9160ec4e99
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f6cdebf82d8b84ada3d029865867c5192af90b0d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409906"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="855b8-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="855b8-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="855b8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="855b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="855b8-105">Dá controle da CPU ao spooler MAPI para que ele possa executar todas as tarefas que considera necessárias.</span><span class="sxs-lookup"><span data-stu-id="855b8-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="855b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="855b8-106">Parameters</span></span>

 <span data-ttu-id="855b8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="855b8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="855b8-108">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="855b8-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="855b8-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="855b8-109">Return value</span></span>

<span data-ttu-id="855b8-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="855b8-110">S_OK</span></span> 
  
> <span data-ttu-id="855b8-111">O provedor de transporte lançou com êxito a CPU.</span><span class="sxs-lookup"><span data-stu-id="855b8-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="855b8-112">MAPI_W_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="855b8-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="855b8-113">Instrui o provedor de transporte a interromper a entrega da mensagem para todos os destinatários que ainda não a receberam.</span><span class="sxs-lookup"><span data-stu-id="855b8-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="855b8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="855b8-114">Remarks</span></span>

<span data-ttu-id="855b8-115">O **método IMAPISupport::SpoolerYield** é implementado para objetos de suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="855b8-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="855b8-116">Os provedores de transporte **chamam SpoolerYield** para permitir que o spooler MAPI realize qualquer processamento necessário.</span><span class="sxs-lookup"><span data-stu-id="855b8-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="855b8-117">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="855b8-117">Notes to callers</span></span>

<span data-ttu-id="855b8-118">Chame **SpoolerYield** quando estiver executando operações demoradas que podem ser pausadas.</span><span class="sxs-lookup"><span data-stu-id="855b8-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="855b8-119">Isso permite que aplicativos em primeiro plano executem durante uma longa operação, como a entrega para uma lista de destinatários grande em uma rede ocupada.</span><span class="sxs-lookup"><span data-stu-id="855b8-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="855b8-120">Se **SpoolerYield** retornar com MAPI_W_CANCEL_MESSAGE, o spooler MAPI determinou que a mensagem não deve mais ser enviada.</span><span class="sxs-lookup"><span data-stu-id="855b8-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="855b8-121">Retorne MAPI_E_USER_CANCEL processo de chamada e saia, se possível.</span><span class="sxs-lookup"><span data-stu-id="855b8-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="855b8-122">Para obter mais informações sobre como gerar para o spooler MAPI, consulte [Interagindo com o Spooler MAPI.](interacting-with-the-mapi-spooler.md)</span><span class="sxs-lookup"><span data-stu-id="855b8-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="855b8-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="855b8-123">See also</span></span>



[<span data-ttu-id="855b8-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="855b8-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

