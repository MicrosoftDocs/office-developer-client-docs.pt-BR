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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278944"
---
# <a name="itabledatahrdeleterows"></a><span data-ttu-id="524c1-103">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="524c1-103">ITableData::HrDeleteRows</span></span>

  
  
<span data-ttu-id="524c1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="524c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="524c1-105">Exclui várias linhas de tabela.</span><span class="sxs-lookup"><span data-stu-id="524c1-105">Deletes multiple table rows.</span></span>
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a><span data-ttu-id="524c1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="524c1-106">Parameters</span></span>

 <span data-ttu-id="524c1-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="524c1-107">_ulFlags_</span></span>
  
> <span data-ttu-id="524c1-108">no Uma bitmask de sinalizadores que controlam a exclusão.</span><span class="sxs-lookup"><span data-stu-id="524c1-108">[in] A bitmask of flags that controls the deletion.</span></span> <span data-ttu-id="524c1-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="524c1-109">The following flag can be set:</span></span>
    
<span data-ttu-id="524c1-110">TAD_ALL_ROWS</span><span class="sxs-lookup"><span data-stu-id="524c1-110">TAD_ALL_ROWS</span></span> 
  
> <span data-ttu-id="524c1-111">Exclui todas as linhas da tabela e de todos os modos de exibição correspondentes, enviando uma única notificação de TABLE_RELOAD.</span><span class="sxs-lookup"><span data-stu-id="524c1-111">Deletes all rows from the table and all corresponding views, sending a single TABLE_RELOAD notification.</span></span>
    
 <span data-ttu-id="524c1-112">_lprowsetToDelete_</span><span class="sxs-lookup"><span data-stu-id="524c1-112">_lprowsetToDelete_</span></span>
  
> <span data-ttu-id="524c1-113">no Um ponteiro para um conjunto de linhas que descreve as linhas a serem excluídas.</span><span class="sxs-lookup"><span data-stu-id="524c1-113">[in] A pointer to a row set that describes the rows to be deleted.</span></span> <span data-ttu-id="524c1-114">O parâmetro _lprowsetToDelete_ pode ser NULL se o sinalizador TAD_ALL_ROWS estiver definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="524c1-114">The  _lprowsetToDelete_ parameter can be NULL if the TAD_ALL_ROWS flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="524c1-115">_cRowsDeleted_</span><span class="sxs-lookup"><span data-stu-id="524c1-115">_cRowsDeleted_</span></span>
  
> <span data-ttu-id="524c1-116">bota A contagem das linhas excluídas.</span><span class="sxs-lookup"><span data-stu-id="524c1-116">[out] The count of the deleted rows.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="524c1-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="524c1-117">Return value</span></span>

<span data-ttu-id="524c1-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="524c1-118">S_OK</span></span> 
  
> <span data-ttu-id="524c1-119">As linhas da tabela foram excluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="524c1-119">The table rows were successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="524c1-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="524c1-120">Remarks</span></span>

<span data-ttu-id="524c1-121">O método **ITableData:: HrDeleteRows** localiza e remove as linhas da tabela que contêm as colunas que correspondem à propriedade indicada pelo membro **lpProps** de cada entrada **aRow** no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="524c1-121">The **ITableData::HrDeleteRows** method locates and removes the table rows that contain the columns that match the property pointed to by the **lpProps** member of each **aRow** entry in the row set.</span></span> <span data-ttu-id="524c1-122">Uma coluna de índice é usada para identificar cada linha; Essa coluna deve ter a mesma marca de propriedade que a marca de propriedade passada no parâmetro _ulPropTagIndexColumn_ na chamada para a [](createtable.md) função CreateTable.</span><span class="sxs-lookup"><span data-stu-id="524c1-122">An index column is used to identify each row; this column must have the same property tag as the property tag passed in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
  
<span data-ttu-id="524c1-123">O número de linhas realmente excluídas é retornado em _cRowsDeleted_.</span><span class="sxs-lookup"><span data-stu-id="524c1-123">The number of rows that were actually deleted is returned in  _cRowsDeleted_.</span></span> <span data-ttu-id="524c1-124">Nenhum erro será retornado se não foi possível localizar uma ou mais linhas.</span><span class="sxs-lookup"><span data-stu-id="524c1-124">No error is returned if one or more rows could not be found.</span></span> 
  
<span data-ttu-id="524c1-125">Depois que as linhas são excluídas, as notificações são enviadas a todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamaram o método imApitable [:: Advise](imapitable-advise.md) a ser registrado para notificações.</span><span class="sxs-lookup"><span data-stu-id="524c1-125">After the rows are deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="524c1-126">A exclusão de linhas não reduz as colunas disponíveis para os modos de exibição de tabelas existentes ou, subsequentemente, abrir modos de exibição de tabela, mesmo que as linhas excluídas sejam a última que tenham valores para uma coluna específica.</span><span class="sxs-lookup"><span data-stu-id="524c1-126">Deleting rows does not reduce the columns available to existing table views or subsequently opened table views, even if the deleted rows are the last that have values for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="524c1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="524c1-127">See also</span></span>



[<span data-ttu-id="524c1-128">CreateTable</span><span class="sxs-lookup"><span data-stu-id="524c1-128">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="524c1-129">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="524c1-129">ITableData::HrDeleteRow</span></span>](itabledata-hrdeleterow.md)
  
[<span data-ttu-id="524c1-130">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="524c1-130">ITableData::HrModifyRows</span></span>](itabledata-hrmodifyrows.md)
  
[<span data-ttu-id="524c1-131">SRowSet</span><span class="sxs-lookup"><span data-stu-id="524c1-131">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="524c1-132">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="524c1-132">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="524c1-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="524c1-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

