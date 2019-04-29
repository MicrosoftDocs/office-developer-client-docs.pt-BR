---
title: ITableDataHrModifyRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRows
api_type:
- COM
ms.assetid: d295c896-9882-4d6f-9689-5cf40db208c0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d0074dd006fda6d44252011d0b979169e0c3d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405356"
---
# <a name="itabledatahrmodifyrows"></a><span data-ttu-id="18ce0-103">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="18ce0-103">ITableData::HrModifyRows</span></span>

  
  
<span data-ttu-id="18ce0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18ce0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18ce0-105">Insere várias linhas de tabela, possivelmente substituindo linhas existentes.</span><span class="sxs-lookup"><span data-stu-id="18ce0-105">Inserts multiple table rows, possibly replacing existing rows.</span></span>
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="18ce0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18ce0-106">Parameters</span></span>

 <span data-ttu-id="18ce0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="18ce0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="18ce0-108">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="18ce0-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="18ce0-109">_lpSRowSet_</span><span class="sxs-lookup"><span data-stu-id="18ce0-109">_lpSRowSet_</span></span>
  
> <span data-ttu-id="18ce0-110">no Um ponteiro para uma estrutura [SRowSet](srowset.md) que contém o conjunto de linhas a serem adicionadas, substituindo linhas existentes, se necessário.</span><span class="sxs-lookup"><span data-stu-id="18ce0-110">[in] A pointer to an [SRowSet](srowset.md) structure that contains the set of rows to be added, replacing existing rows if necessary.</span></span> <span data-ttu-id="18ce0-111">Uma das estruturas de valor de propriedade apontadas pelo membro **lpProps** de cada estrutura [SRow](srow.md) no conjunto de linhas deve conter a coluna de índice, o mesmo valor que foi especificado no parâmetro _ulPropTagIndexColumn_ na chamada para o [ ](createtable.md)Função CreateTable.</span><span class="sxs-lookup"><span data-stu-id="18ce0-111">One of the property value structures pointed to by the **lpProps** member of each [SRow](srow.md) structure in the row set should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="18ce0-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="18ce0-112">Return value</span></span>

<span data-ttu-id="18ce0-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="18ce0-113">S_OK</span></span> 
  
> <span data-ttu-id="18ce0-114">As linhas foram inseridas ou modificadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="18ce0-114">The rows were successfully inserted or modified.</span></span>
    
<span data-ttu-id="18ce0-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="18ce0-115">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="18ce0-116">Uma ou mais das linhas passadas não têm uma coluna de índice.</span><span class="sxs-lookup"><span data-stu-id="18ce0-116">One or more of the passed-in rows does not have an index column.</span></span> <span data-ttu-id="18ce0-117">Se esse erro for retornado, nenhuma linha será alterada.</span><span class="sxs-lookup"><span data-stu-id="18ce0-117">If this error is returned, no rows are changed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18ce0-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="18ce0-118">Remarks</span></span>

<span data-ttu-id="18ce0-119">O método **ITableData:: HrModifyRows** insere as linhas descritas pela estrutura [SRowSet](srowset.md) apontada pelo parâmetro _lpSRowSet_ .</span><span class="sxs-lookup"><span data-stu-id="18ce0-119">The **ITableData::HrModifyRows** method inserts the rows described by the [SRowSet](srowset.md) structure pointed to by the  _lpSRowSet_ parameter.</span></span> <span data-ttu-id="18ce0-120">Se o valor da coluna de índice de uma linha no conjunto de linhas corresponder ao valor de uma linha existente na tabela, a linha existente será substituída.</span><span class="sxs-lookup"><span data-stu-id="18ce0-120">If the index column value of a row in the row set matches the value for an existing row in the table, the existing row is replaced.</span></span> <span data-ttu-id="18ce0-121">Se não existir nenhuma linha que coincida com a incluída na estrutura **SRowSet** , **HrModifyRows** adicionará a linha ao final da tabela.</span><span class="sxs-lookup"><span data-stu-id="18ce0-121">If no row exists that matches the one included in the **SRowSet** structure, **HrModifyRows** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="18ce0-122">Todos os modos de exibição da tabela são modificados para incluir as linhas apontadas pelo _lpSRowSet_.</span><span class="sxs-lookup"><span data-stu-id="18ce0-122">All views of the table are modified to include the rows pointed to by  _lpSRowSet_.</span></span> <span data-ttu-id="18ce0-123">No enTanto, se um modo de exibição tiver uma restrição no lugar que exclua uma linha, ele pode não estar visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="18ce0-123">However, if a view has a restriction in place that excludes a row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="18ce0-124">As colunas nas linhas apontadas por _lpSRowSet_ não precisam estar na mesma ordem das colunas da tabela.</span><span class="sxs-lookup"><span data-stu-id="18ce0-124">The columns in the rows pointed to by  _lpSRowSet_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="18ce0-125">O chamador também pode incluir as propriedades de colunas que não estão na tabela no momento.</span><span class="sxs-lookup"><span data-stu-id="18ce0-125">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="18ce0-126">Para modos de exibição existentes, o **HrModifyRows** torna essas novas colunas disponíveis, mas não as inclui no conjunto de colunas atual.</span><span class="sxs-lookup"><span data-stu-id="18ce0-126">For existing views, **HrModifyRows** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="18ce0-127">Para modos de exibição futuros, o **HrModifyRows** inclui as novas colunas no conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="18ce0-127">For future views, **HrModifyRows** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="18ce0-128">Após o **HrModifyRows** ter adicionado as linhas, as notificações são enviadas a todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamaram o método IMAPITable [:: Advise](imapitable-advise.md) da tabela para se registrarem para notificações.</span><span class="sxs-lookup"><span data-stu-id="18ce0-128">After **HrModifyRows** has added the rows, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="18ce0-129">MAPI envia notificações TABLE_ROW_ADDED ou TABLE_ROW_MODIFIED para cada linha, até oito linhas.</span><span class="sxs-lookup"><span data-stu-id="18ce0-129">MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows.</span></span> <span data-ttu-id="18ce0-130">Se mais de oito linhas forem afetadas pela chamada **HrModifyRows** , o MAPI enviará uma única notificação TABLE_CHANGED em vez disso.</span><span class="sxs-lookup"><span data-stu-id="18ce0-130">If more than eight rows are affected by the **HrModifyRows** call, MAPI sends a single TABLE_CHANGED notification instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="18ce0-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="18ce0-131">See also</span></span>



[<span data-ttu-id="18ce0-132">SRowSet</span><span class="sxs-lookup"><span data-stu-id="18ce0-132">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="18ce0-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="18ce0-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

