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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 74c307fca27f1adec18d236792f8a58d97e33ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328943"
---
# <a name="imapitableabort"></a><span data-ttu-id="f396c-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="f396c-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="f396c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f396c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f396c-105">Para todas as operações assíncronas atualmente em andamento para a tabela.</span><span class="sxs-lookup"><span data-stu-id="f396c-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="f396c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f396c-106">Parameters</span></span>

<span data-ttu-id="f396c-107">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f396c-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="f396c-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f396c-108">Return value</span></span>

<span data-ttu-id="f396c-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="f396c-109">S_OK</span></span> 
  
> <span data-ttu-id="f396c-110">Uma ou mais operações assíncronas foram interrompidas.</span><span class="sxs-lookup"><span data-stu-id="f396c-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="f396c-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="f396c-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="f396c-112">Uma operação assíncrona está em andamento e não pode ser interrompida ou já foi concluída.</span><span class="sxs-lookup"><span data-stu-id="f396c-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f396c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f396c-113">Remarks</span></span>

<span data-ttu-id="f396c-114">O método imApitable **:: Abort** interrompe qualquer operação assíncrona que está atualmente em andamento.</span><span class="sxs-lookup"><span data-stu-id="f396c-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f396c-115">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f396c-115">Notes to callers</span></span>

<span data-ttu-id="f396c-116">Para descobrir se uma operação assíncrona está em andamento, chame o método imApitable [:: GetStatus](imapitable-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="f396c-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="f396c-117">Se **Abort** parar o processamento de uma chamada para o método [IMAPITable:: Restrict](imapitable-restrict.md) , o estado da tabela será o que estava no momento em que a chamada de **anulação** é processada.</span><span class="sxs-lookup"><span data-stu-id="f396c-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="f396c-118">Se **Abort** parar o processamento de uma chamada para o método [IMAPITable:: SortTable](imapitable-sorttable.md) , a ordem de classificação da tabela não será afetada e permanecerá como antes da chamada **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="f396c-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f396c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="f396c-119">See also</span></span>



[<span data-ttu-id="f396c-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="f396c-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="f396c-121">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="f396c-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="f396c-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="f396c-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="f396c-123">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f396c-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

