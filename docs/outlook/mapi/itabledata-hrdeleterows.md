---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fdd6f40b4d7aa7f65bf1a46d3d9a4f18472b19f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416451"
---
# <a name="itabledatahrdeleterows"></a><span data-ttu-id="72c31-103">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="72c31-103">ITableData::HrDeleteRows</span></span>

  
  
<span data-ttu-id="72c31-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72c31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72c31-105">Exclui várias linhas de tabela.</span><span class="sxs-lookup"><span data-stu-id="72c31-105">Deletes multiple table rows.</span></span>
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a><span data-ttu-id="72c31-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72c31-106">Parameters</span></span>

 <span data-ttu-id="72c31-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="72c31-107">_ulFlags_</span></span>
  
> <span data-ttu-id="72c31-108">no Uma bitmask de sinalizadores que controlam a exclusão.</span><span class="sxs-lookup"><span data-stu-id="72c31-108">[in] A bitmask of flags that controls the deletion.</span></span> <span data-ttu-id="72c31-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="72c31-109">The following flag can be set:</span></span>
    
<span data-ttu-id="72c31-110">TAD_ALL_ROWS</span><span class="sxs-lookup"><span data-stu-id="72c31-110">TAD_ALL_ROWS</span></span> 
  
> <span data-ttu-id="72c31-111">Exclui todas as linhas da tabela e de todos os modos de exibição correspondentes, enviando uma única notificação de TABLE_RELOAD.</span><span class="sxs-lookup"><span data-stu-id="72c31-111">Deletes all rows from the table and all corresponding views, sending a single TABLE_RELOAD notification.</span></span>
    
 <span data-ttu-id="72c31-112">_lprowsetToDelete_</span><span class="sxs-lookup"><span data-stu-id="72c31-112">_lprowsetToDelete_</span></span>
  
> <span data-ttu-id="72c31-113">no Um ponteiro para um conjunto de linhas que descreve as linhas a serem excluídas.</span><span class="sxs-lookup"><span data-stu-id="72c31-113">[in] A pointer to a row set that describes the rows to be deleted.</span></span> <span data-ttu-id="72c31-114">O parâmetro _lprowsetToDelete_ pode ser NULL se o sinalizador TAD_ALL_ROWS estiver definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="72c31-114">The  _lprowsetToDelete_ parameter can be NULL if the TAD_ALL_ROWS flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="72c31-115">_cRowsDeleted_</span><span class="sxs-lookup"><span data-stu-id="72c31-115">_cRowsDeleted_</span></span>
  
> <span data-ttu-id="72c31-116">bota A contagem das linhas excluídas.</span><span class="sxs-lookup"><span data-stu-id="72c31-116">[out] The count of the deleted rows.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="72c31-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="72c31-117">Return value</span></span>

<span data-ttu-id="72c31-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="72c31-118">S_OK</span></span> 
  
> <span data-ttu-id="72c31-119">As linhas da tabela foram excluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="72c31-119">The table rows were successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72c31-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="72c31-120">Remarks</span></span>

<span data-ttu-id="72c31-121">O método **ITableData:: HrDeleteRows** localiza e remove as linhas da tabela que contêm as colunas que correspondem à propriedade indicada pelo membro **lpProps** de cada entrada **aRow** no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="72c31-121">The **ITableData::HrDeleteRows** method locates and removes the table rows that contain the columns that match the property pointed to by the **lpProps** member of each **aRow** entry in the row set.</span></span> <span data-ttu-id="72c31-122">Uma coluna de índice é usada para identificar cada linha; Essa coluna deve ter a mesma marca de propriedade que a marca de propriedade passada no parâmetro _ulPropTagIndexColumn_ na chamada para a [](createtable.md) função CreateTable.</span><span class="sxs-lookup"><span data-stu-id="72c31-122">An index column is used to identify each row; this column must have the same property tag as the property tag passed in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
  
<span data-ttu-id="72c31-123">O número de linhas realmente excluídas é retornado em _cRowsDeleted_.</span><span class="sxs-lookup"><span data-stu-id="72c31-123">The number of rows that were actually deleted is returned in  _cRowsDeleted_.</span></span> <span data-ttu-id="72c31-124">Nenhum erro será retornado se não foi possível localizar uma ou mais linhas.</span><span class="sxs-lookup"><span data-stu-id="72c31-124">No error is returned if one or more rows could not be found.</span></span> 
  
<span data-ttu-id="72c31-125">Depois que as linhas são excluídas, as notificações são enviadas a todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamaram o método imApitable [:: Advise](imapitable-advise.md) a ser registrado para notificações.</span><span class="sxs-lookup"><span data-stu-id="72c31-125">After the rows are deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="72c31-126">A exclusão de linhas não reduz as colunas disponíveis para os modos de exibição de tabelas existentes ou, subsequentemente, abrir modos de exibição de tabela, mesmo que as linhas excluídas sejam a última que tenham valores para uma coluna específica.</span><span class="sxs-lookup"><span data-stu-id="72c31-126">Deleting rows does not reduce the columns available to existing table views or subsequently opened table views, even if the deleted rows are the last that have values for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="72c31-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="72c31-127">See also</span></span>



[<span data-ttu-id="72c31-128">CreateTable</span><span class="sxs-lookup"><span data-stu-id="72c31-128">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="72c31-129">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="72c31-129">ITableData::HrDeleteRow</span></span>](itabledata-hrdeleterow.md)
  
[<span data-ttu-id="72c31-130">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="72c31-130">ITableData::HrModifyRows</span></span>](itabledata-hrmodifyrows.md)
  
[<span data-ttu-id="72c31-131">SRowSet</span><span class="sxs-lookup"><span data-stu-id="72c31-131">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="72c31-132">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="72c31-132">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="72c31-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72c31-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

