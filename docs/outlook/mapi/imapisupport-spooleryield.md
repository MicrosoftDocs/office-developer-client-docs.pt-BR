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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329033"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="e3cb6-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="e3cb6-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="e3cb6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3cb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3cb6-105">Dá controle da CPU ao spooler MAPI para que ele possa executar qualquer tarefa que ele considere necessário.</span><span class="sxs-lookup"><span data-stu-id="e3cb6-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e3cb6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3cb6-106">Parameters</span></span>

 <span data-ttu-id="e3cb6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e3cb6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e3cb6-108">Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e3cb6-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e3cb6-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e3cb6-109">Return value</span></span>

<span data-ttu-id="e3cb6-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3cb6-110">S_OK</span></span> 
  
> <span data-ttu-id="e3cb6-111">O provedor de transporte liberou com êxito a CPU.</span><span class="sxs-lookup"><span data-stu-id="e3cb6-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="e3cb6-112">MAPI_W_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="e3cb6-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="e3cb6-113">Instrui o provedor de transporte a interromper a entrega da mensagem para todos os destinatários que ainda não a receberam.</span><span class="sxs-lookup"><span data-stu-id="e3cb6-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3cb6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3cb6-114">Remarks</span></span>

<span data-ttu-id="e3cb6-115">O método **IMAPISupport:: SpoolerYield** é implementado para objetos de suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="e3cb6-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="e3cb6-116">Os provedores de transporte chamam o **SpoolerYield** para permitir que o spooler MAPI realize qualquer processamento necessário.</span><span class="sxs-lookup"><span data-stu-id="e3cb6-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e3cb6-117">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="e3cb6-117">Notes to callers</span></span>

<span data-ttu-id="e3cb6-118">Chame **SpoolerYield** quando você estiver executando operações demoradas que podem ser pausadas.</span><span class="sxs-lookup"><span data-stu-id="e3cb6-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="e3cb6-119">Isso permite que aplicativos de primeiro plano sejam executados durante uma operação longa, como a entrega para uma lista de destinatários grande em uma rede ocupada.</span><span class="sxs-lookup"><span data-stu-id="e3cb6-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="e3cb6-120">Se **SpoolerYield** retornar com MAPI_W_CANCEL_MESSAGE, o spooler MAPI determinou que a mensagem não deve mais ser enviada.</span><span class="sxs-lookup"><span data-stu-id="e3cb6-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="e3cb6-121">ReTorne MAPI_E_USER_CANCEL ao processo de chamada e saia, se possível.</span><span class="sxs-lookup"><span data-stu-id="e3cb6-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="e3cb6-122">Para obter mais informações sobre como produzir o spooler MAPI, consulte [interagindo com o spooler MAPI](interacting-with-the-mapi-spooler.md).</span><span class="sxs-lookup"><span data-stu-id="e3cb6-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e3cb6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3cb6-123">See also</span></span>



[<span data-ttu-id="e3cb6-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3cb6-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

