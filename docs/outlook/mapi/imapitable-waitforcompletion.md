---
title: IMAPITableWaitForCompletion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.WaitForCompletion
api_type:
- COM
ms.assetid: 7663c640-396e-4720-9345-370d0856bd49
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 778ff8f36478740e5ee23ba439db1e328eca2e06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407057"
---
# <a name="imapitablewaitforcompletion"></a><span data-ttu-id="6f751-103">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="6f751-103">IMAPITable::WaitForCompletion</span></span>

  
  
<span data-ttu-id="6f751-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f751-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f751-105">Suspende o processamento até que uma ou mais operações assíncronas em andamento na tabela tenham sido concluídas.</span><span class="sxs-lookup"><span data-stu-id="6f751-105">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a><span data-ttu-id="6f751-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f751-106">Parameters</span></span>

 <span data-ttu-id="6f751-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6f751-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6f751-108">Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6f751-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6f751-109">_ulTimeout_</span><span class="sxs-lookup"><span data-stu-id="6f751-109">_ulTimeout_</span></span>
  
> <span data-ttu-id="6f751-110">no Número máximo de milissegundos para aguardar a conclusão da operação ou operações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="6f751-110">[in] Maximum number of milliseconds to wait for the asynchronous operation or operations to complete.</span></span> <span data-ttu-id="6f751-111">Para esperar indefinidamente até a conclusão ocorrer, defina _ulTimeout_ como 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="6f751-111">To wait indefinitely until completion occurs, set  _ulTimeout_ to 0xFFFFFFFF.</span></span> 
    
 <span data-ttu-id="6f751-112">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="6f751-112">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="6f751-113">[in, out] Na entrada, um ponteiro válido ou nulo.</span><span class="sxs-lookup"><span data-stu-id="6f751-113">[in, out] On input, either a valid pointer or NULL.</span></span> <span data-ttu-id="6f751-114">Na saída, se _lpulTableStatus_ for um ponteiro válido, apontará para o status mais recente da tabela.</span><span class="sxs-lookup"><span data-stu-id="6f751-114">On output, if  _lpulTableStatus_ is a valid pointer, it points to the most recent status of the table.</span></span> <span data-ttu-id="6f751-115">Se _lpulTableStatus_ for NULL, nenhuma informação de status será retornada.</span><span class="sxs-lookup"><span data-stu-id="6f751-115">If  _lpulTableStatus_ is NULL, no status information is returned.</span></span> <span data-ttu-id="6f751-116">Se **WaitForCompletion** retornar um valor de HRESULT sem êxito, o conteúdo de _lpulTableStatus_ será indefinido.</span><span class="sxs-lookup"><span data-stu-id="6f751-116">If **WaitForCompletion** returns an unsuccessful HRESULT value, the contents of  _lpulTableStatus_ are undefined.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6f751-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6f751-117">Return value</span></span>

<span data-ttu-id="6f751-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="6f751-118">S_OK</span></span> 
  
> <span data-ttu-id="6f751-119">A operação de espera foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6f751-119">The wait operation was successful.</span></span>
    
<span data-ttu-id="6f751-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6f751-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="6f751-121">A tabela não dá suporte à espera para a conclusão de operações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="6f751-121">The table does not support waiting for the completion of asynchronous operations.</span></span>
    
<span data-ttu-id="6f751-122">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6f751-122">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="6f751-123">A operação assíncrona ou as operações não foram concluídas no tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="6f751-123">The asynchronous operation or operations did not complete in the specified time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6f751-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f751-124">Remarks</span></span>

<span data-ttu-id="6f751-125">O método imApitable **:: WaitForCompletion** suspende o processamento até que qualquer operação assíncrona atualmente em andamento para a tabela tenha sido concluída.</span><span class="sxs-lookup"><span data-stu-id="6f751-125">The **IMAPITable::WaitForCompletion** method suspends processing until any asynchronous operations currently under way for the table have completed.</span></span> <span data-ttu-id="6f751-126">**WaitForCompletion** pode permitir que as operações assíncronas sejam totalmente concluídas ou sejam executadas por um determinado número de milissegundos, conforme indicado por _ulTimeout_, antes de ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="6f751-126">**WaitForCompletion** can allow the asynchronous operations either to fully complete or to run for a certain number of milliseconds, as indicated by  _ulTimeout_, before being interrupted.</span></span> <span data-ttu-id="6f751-127">Para detectar operações assíncronas em andamento, chame o método imApitable [:: GetStatus](imapitable-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="6f751-127">To detect asynchronous operations in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6f751-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f751-128">See also</span></span>



[<span data-ttu-id="6f751-129">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="6f751-129">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="6f751-130">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="6f751-130">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="6f751-131">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="6f751-131">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="6f751-132">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="6f751-132">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="6f751-133">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="6f751-133">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="6f751-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6f751-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

