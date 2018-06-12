---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4b578f287a532475b53fb69cc4499662b6c4b6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767312"
---
# <a name="imapitableabort"></a><span data-ttu-id="bd665-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="bd665-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="bd665-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd665-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd665-105">Interrompe a qualquer operação assíncrona em andamento atualmente para a tabela.</span><span class="sxs-lookup"><span data-stu-id="bd665-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="bd665-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd665-106">Parameters</span></span>

<span data-ttu-id="bd665-107">None</span><span class="sxs-lookup"><span data-stu-id="bd665-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="bd665-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bd665-108">Return value</span></span>

<span data-ttu-id="bd665-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="bd665-109">S_OK</span></span> 
  
> <span data-ttu-id="bd665-110">Uma ou mais operações assíncronas foram interrompidas.</span><span class="sxs-lookup"><span data-stu-id="bd665-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="bd665-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="bd665-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="bd665-112">Uma operação assíncrona está em andamento e não pode ser parada ou já foi concluída.</span><span class="sxs-lookup"><span data-stu-id="bd665-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bd665-113">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="bd665-113">Remarks</span></span>

<span data-ttu-id="bd665-114">O método **IMAPITable::Abort** interrompe qualquer operação assíncrona que está em andamento.</span><span class="sxs-lookup"><span data-stu-id="bd665-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bd665-115">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="bd665-115">Notes to callers</span></span>

<span data-ttu-id="bd665-116">Para descobrir se uma operação assíncrona está em andamento, chame o método [IMAPITable::GetStatus](imapitable-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="bd665-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="bd665-117">Se **Anular** interrompe o processamento de uma chamada para o método [IMAPITable:: Restrict](imapitable-restrict.md) , o estado da tabela será como era no momento em que a chamada **Anular** é processada.</span><span class="sxs-lookup"><span data-stu-id="bd665-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="bd665-118">Se **Anular** interrompe o processamento de uma chamada para o método [IMAPITable:: SortTable](imapitable-sorttable.md) , ordem de classificação da tabela não é afetado e permanecerá como era antes da chamada **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="bd665-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bd665-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd665-119">See also</span></span>



[<span data-ttu-id="bd665-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="bd665-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="bd665-121">IMAPITable:: Restrict</span><span class="sxs-lookup"><span data-stu-id="bd665-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="bd665-122">IMAPITable:: SortTable</span><span class="sxs-lookup"><span data-stu-id="bd665-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="bd665-123">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bd665-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

