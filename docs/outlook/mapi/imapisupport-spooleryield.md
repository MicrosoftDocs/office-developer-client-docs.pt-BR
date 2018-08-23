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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d90f502e2cd7f97ac273ebecedbd0363097b1d60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584951"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="c6231-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="c6231-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="c6231-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6231-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6231-105">Fornece o controle da CPU para o spooler MAPI para que ele pode executar qualquer tarefa que ele considera necessário.</span><span class="sxs-lookup"><span data-stu-id="c6231-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c6231-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6231-106">Parameters</span></span>

 <span data-ttu-id="c6231-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c6231-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c6231-108">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c6231-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c6231-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c6231-109">Return value</span></span>

<span data-ttu-id="c6231-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c6231-110">S_OK</span></span> 
  
> <span data-ttu-id="c6231-111">O provedor de transporte com êxito liberado da CPU.</span><span class="sxs-lookup"><span data-stu-id="c6231-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="c6231-112">MAPI_W_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="c6231-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="c6231-113">Instrui o provedor de transporte para interromper a entrega da mensagem para qualquer destinatários que ainda não recebeu-lo.</span><span class="sxs-lookup"><span data-stu-id="c6231-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6231-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6231-114">Remarks</span></span>

<span data-ttu-id="c6231-115">O método **IMAPISupport::SpoolerYield** é implementado para objetos de suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="c6231-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="c6231-116">Provedores de transporte chamarem **SpoolerYield** para permitir que o spooler MAPI realizar qualquer processamento necessário.</span><span class="sxs-lookup"><span data-stu-id="c6231-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c6231-117">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="c6231-117">Notes to callers</span></span>

<span data-ttu-id="c6231-118">Chame **SpoolerYield** quando você estiver executando operações demoradas que podem ser pausadas.</span><span class="sxs-lookup"><span data-stu-id="c6231-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="c6231-119">Isso permite que aplicativos de primeiro plano para serem executados durante uma operação longa, como entrega para uma grande lista de destinatários em uma rede ocupada.</span><span class="sxs-lookup"><span data-stu-id="c6231-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="c6231-120">Se **SpoolerYield** retornar com MAPI_W_CANCEL_MESSAGE, o MAPI spooler determinou que a mensagem não é mais deve ser enviada.</span><span class="sxs-lookup"><span data-stu-id="c6231-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="c6231-121">Retorne MAPI_E_USER_CANCEL ao seu processo de chamada e a saída, se possível.</span><span class="sxs-lookup"><span data-stu-id="c6231-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="c6231-122">Para obter mais informações sobre como resultando no MAPI spooler, consulte [interagindo com o Spooler de MAPI](interacting-with-the-mapi-spooler.md).</span><span class="sxs-lookup"><span data-stu-id="c6231-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c6231-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6231-123">See also</span></span>



[<span data-ttu-id="c6231-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6231-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

