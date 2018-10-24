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
ms.openlocfilehash: a3343381709b7ce3370ba481ad8dbb935c7d4165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586946"
---
# <a name="imapitablewaitforcompletion"></a><span data-ttu-id="b51f9-103">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="b51f9-103">IMAPITable::WaitForCompletion</span></span>

  
  
<span data-ttu-id="b51f9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b51f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b51f9-105">Suspende o processamento até que um ou mais operações assíncronas em andamento na tabela forem concluídas.</span><span class="sxs-lookup"><span data-stu-id="b51f9-105">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a><span data-ttu-id="b51f9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b51f9-106">Parameters</span></span>

 <span data-ttu-id="b51f9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b51f9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b51f9-108">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b51f9-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b51f9-109">_ulTimeout_</span><span class="sxs-lookup"><span data-stu-id="b51f9-109">_ulTimeout_</span></span>
  
> <span data-ttu-id="b51f9-110">[in] Número máximo de milissegundos de espera para a operação assíncrona ou a conclusão das operações.</span><span class="sxs-lookup"><span data-stu-id="b51f9-110">[in] Maximum number of milliseconds to wait for the asynchronous operation or operations to complete.</span></span> <span data-ttu-id="b51f9-111">Para esperar indefinidamente até que ocorra de conclusão, defina _ulTimeout_ como 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="b51f9-111">To wait indefinitely until completion occurs, set  _ulTimeout_ to 0xFFFFFFFF.</span></span> 
    
 <span data-ttu-id="b51f9-112">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="b51f9-112">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="b51f9-113">[além, out] Na entrada, um ponteiro válido ou nulo.</span><span class="sxs-lookup"><span data-stu-id="b51f9-113">[in, out] On input, either a valid pointer or NULL.</span></span> <span data-ttu-id="b51f9-114">Na saída, se _lpulTableStatus_ for um ponteiro válido, ela aponta para o status mais recente da tabela.</span><span class="sxs-lookup"><span data-stu-id="b51f9-114">On output, if  _lpulTableStatus_ is a valid pointer, it points to the most recent status of the table.</span></span> <span data-ttu-id="b51f9-115">Se _lpulTableStatus_ for NULL, nenhuma informação de status será retornada.</span><span class="sxs-lookup"><span data-stu-id="b51f9-115">If  _lpulTableStatus_ is NULL, no status information is returned.</span></span> <span data-ttu-id="b51f9-116">Se **WaitForCompletion** retorna um valor HRESULT bem sucedido, o conteúdo de _lpulTableStatus_ é indefinido.</span><span class="sxs-lookup"><span data-stu-id="b51f9-116">If **WaitForCompletion** returns an unsuccessful HRESULT value, the contents of  _lpulTableStatus_ are undefined.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b51f9-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b51f9-117">Return value</span></span>

<span data-ttu-id="b51f9-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b51f9-118">S_OK</span></span> 
  
> <span data-ttu-id="b51f9-119">A operação de espera foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b51f9-119">The wait operation was successful.</span></span>
    
<span data-ttu-id="b51f9-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b51f9-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b51f9-121">A tabela não oferece suporte ao aguardar a conclusão de operações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="b51f9-121">The table does not support waiting for the completion of asynchronous operations.</span></span>
    
<span data-ttu-id="b51f9-122">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b51f9-122">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="b51f9-123">A operação assíncrona ou operações não foram concluída no tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="b51f9-123">The asynchronous operation or operations did not complete in the specified time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b51f9-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b51f9-124">Remarks</span></span>

<span data-ttu-id="b51f9-125">O método **IMAPITable::WaitForCompletion** suspende o processamento até que tenha concluído a qualquer operação assíncrona em andamento no momento para a tabela.</span><span class="sxs-lookup"><span data-stu-id="b51f9-125">The **IMAPITable::WaitForCompletion** method suspends processing until any asynchronous operations currently under way for the table have completed.</span></span> <span data-ttu-id="b51f9-126">**WaitForCompletion** pode permitir que as operações assíncronas para totalmente concluída ou a ser executada para um determinado número de milissegundos, conforme indicado pela _ulTimeout_, antes da interrupção.</span><span class="sxs-lookup"><span data-stu-id="b51f9-126">**WaitForCompletion** can allow the asynchronous operations either to fully complete or to run for a certain number of milliseconds, as indicated by  _ulTimeout_, before being interrupted.</span></span> <span data-ttu-id="b51f9-127">Para detectar operações assíncronas em andamento, chame o método [IMAPITable::GetStatus](imapitable-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="b51f9-127">To detect asynchronous operations in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b51f9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b51f9-128">See also</span></span>



[<span data-ttu-id="b51f9-129">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="b51f9-129">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="b51f9-130">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="b51f9-130">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="b51f9-131">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="b51f9-131">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="b51f9-132">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="b51f9-132">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="b51f9-133">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="b51f9-133">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="b51f9-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b51f9-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

