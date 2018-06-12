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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 00662d7a5bf1c2addc5c4e0b39d657abd7073753
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767704"
---
# <a name="itabledatahrdeleterows"></a><span data-ttu-id="63dad-103">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="63dad-103">ITableData::HrDeleteRows</span></span>

  
  
<span data-ttu-id="63dad-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63dad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63dad-105">Exclui a várias linhas de tabela.</span><span class="sxs-lookup"><span data-stu-id="63dad-105">Deletes multiple table rows.</span></span>
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a><span data-ttu-id="63dad-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="63dad-106">Parameters</span></span>

 <span data-ttu-id="63dad-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="63dad-107">_ulFlags_</span></span>
  
> <span data-ttu-id="63dad-108">[in] Uma bitmask dos sinalizadores que controla a exclusão.</span><span class="sxs-lookup"><span data-stu-id="63dad-108">[in] A bitmask of flags that controls the deletion.</span></span> <span data-ttu-id="63dad-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="63dad-109">The following flag can be set:</span></span>
    
<span data-ttu-id="63dad-110">TAD_ALL_ROWS</span><span class="sxs-lookup"><span data-stu-id="63dad-110">TAD_ALL_ROWS</span></span> 
  
> <span data-ttu-id="63dad-111">Exclui todas as linhas da tabela e todos os modos de exibição correspondentes, enviar a notificação de TABLE_RELOAD única.</span><span class="sxs-lookup"><span data-stu-id="63dad-111">Deletes all rows from the table and all corresponding views, sending a single TABLE_RELOAD notification.</span></span>
    
 <span data-ttu-id="63dad-112">_lprowsetToDelete_</span><span class="sxs-lookup"><span data-stu-id="63dad-112">_lprowsetToDelete_</span></span>
  
> <span data-ttu-id="63dad-113">[in] Um ponteiro para um conjunto de linha que descreve as linhas a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="63dad-113">[in] A pointer to a row set that describes the rows to be deleted.</span></span> <span data-ttu-id="63dad-114">O parâmetro _lprowsetToDelete_ pode ser NULL se o sinalizador TAD_ALL_ROWS é definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="63dad-114">The  _lprowsetToDelete_ parameter can be NULL if the TAD_ALL_ROWS flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="63dad-115">_cRowsDeleted_</span><span class="sxs-lookup"><span data-stu-id="63dad-115">_cRowsDeleted_</span></span>
  
> <span data-ttu-id="63dad-116">[out] A contagem de linhas excluídas.</span><span class="sxs-lookup"><span data-stu-id="63dad-116">[out] The count of the deleted rows.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="63dad-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="63dad-117">Return value</span></span>

<span data-ttu-id="63dad-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="63dad-118">S_OK</span></span> 
  
> <span data-ttu-id="63dad-119">As linhas de tabela foram excluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="63dad-119">The table rows were successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63dad-120">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="63dad-120">Remarks</span></span>

<span data-ttu-id="63dad-121">O método **ITableData::HrDeleteRows** localiza e remove as linhas de tabela que contêm as colunas que coincidem com a propriedade apontada para pelo membro de cada entrada de **aRow** na linha **lpProps** definir.</span><span class="sxs-lookup"><span data-stu-id="63dad-121">The **ITableData::HrDeleteRows** method locates and removes the table rows that contain the columns that match the property pointed to by the **lpProps** member of each **aRow** entry in the row set.</span></span> <span data-ttu-id="63dad-122">Uma coluna de índice é usada para identificar cada linha; Essa coluna deve ter a mesma marca de propriedade, como a marca de propriedade passada no parâmetro _ulPropTagIndexColumn_ na chamada para a função [CreateTable](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="63dad-122">An index column is used to identify each row; this column must have the same property tag as the property tag passed in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
  
<span data-ttu-id="63dad-123">O número de linhas que foram excluídas realmente é retornado no _cRowsDeleted_.</span><span class="sxs-lookup"><span data-stu-id="63dad-123">The number of rows that were actually deleted is returned in  _cRowsDeleted_.</span></span> <span data-ttu-id="63dad-124">Nenhum erro será retornado se uma ou mais linhas não pôde ser encontradas.</span><span class="sxs-lookup"><span data-stu-id="63dad-124">No error is returned if one or more rows could not be found.</span></span> 
  
<span data-ttu-id="63dad-125">Depois que as linhas são excluídas, as notificações são enviadas para todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamou o método da tabela [IMAPITable::Advise](imapitable-advise.md) para registrar para notificações.</span><span class="sxs-lookup"><span data-stu-id="63dad-125">After the rows are deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="63dad-126">A exclusão de linhas não reduz as colunas disponíveis para modos de exibição de tabela existente ou aberto subsequentemente modos de exibição de tabela, mesmo se as linhas excluídas são a última que têm valores para uma coluna específica.</span><span class="sxs-lookup"><span data-stu-id="63dad-126">Deleting rows does not reduce the columns available to existing table views or subsequently opened table views, even if the deleted rows are the last that have values for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63dad-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="63dad-127">See also</span></span>



[<span data-ttu-id="63dad-128">CreateTable</span><span class="sxs-lookup"><span data-stu-id="63dad-128">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="63dad-129">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="63dad-129">ITableData::HrDeleteRow</span></span>](itabledata-hrdeleterow.md)
  
[<span data-ttu-id="63dad-130">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="63dad-130">ITableData::HrModifyRows</span></span>](itabledata-hrmodifyrows.md)
  
[<span data-ttu-id="63dad-131">SRowSet</span><span class="sxs-lookup"><span data-stu-id="63dad-131">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="63dad-132">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="63dad-132">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="63dad-133">ITableData: IUnknown</span><span class="sxs-lookup"><span data-stu-id="63dad-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

