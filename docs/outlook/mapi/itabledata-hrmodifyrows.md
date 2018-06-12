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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 15d98183548d4b73c35368d690ef63d5c3dfd9af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767725"
---
# <a name="itabledatahrmodifyrows"></a><span data-ttu-id="0569c-103">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="0569c-103">ITableData::HrModifyRows</span></span>

  
  
<span data-ttu-id="0569c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0569c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0569c-105">Insere várias linhas de tabela, substituindo possivelmente linhas existentes.</span><span class="sxs-lookup"><span data-stu-id="0569c-105">Inserts multiple table rows, possibly replacing existing rows.</span></span>
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="0569c-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="0569c-106">Parameters</span></span>

 <span data-ttu-id="0569c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0569c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0569c-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0569c-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0569c-109">_lpSRowSet_</span><span class="sxs-lookup"><span data-stu-id="0569c-109">_lpSRowSet_</span></span>
  
> <span data-ttu-id="0569c-110">[in] Um ponteiro para uma estrutura [SRowSet](srowset.md) que contém o conjunto de linhas a ser adicionado, substituindo linhas existentes, se necessário.</span><span class="sxs-lookup"><span data-stu-id="0569c-110">[in] A pointer to an [SRowSet](srowset.md) structure that contains the set of rows to be added, replacing existing rows if necessary.</span></span> <span data-ttu-id="0569c-111">Uma das estruturas de valor de propriedade apontadas pelo membro **lpProps** cada estrutura [SRow](srow.md) na linha definido deve conter uma coluna de índice, o mesmo valor que foi especificado no parâmetro _ulPropTagIndexColumn_ na chamada para o [ CreateTable](createtable.md) função.</span><span class="sxs-lookup"><span data-stu-id="0569c-111">One of the property value structures pointed to by the **lpProps** member of each [SRow](srow.md) structure in the row set should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0569c-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0569c-112">Return value</span></span>

<span data-ttu-id="0569c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="0569c-113">S_OK</span></span> 
  
> <span data-ttu-id="0569c-114">As linhas com êxito foram inseridas ou modificadas.</span><span class="sxs-lookup"><span data-stu-id="0569c-114">The rows were successfully inserted or modified.</span></span>
    
<span data-ttu-id="0569c-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0569c-115">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="0569c-116">Um ou mais das linhas no passado não tem uma coluna de índice.</span><span class="sxs-lookup"><span data-stu-id="0569c-116">One or more of the passed-in rows does not have an index column.</span></span> <span data-ttu-id="0569c-117">Se esse erro for retornado, nenhuma linha é alterada.</span><span class="sxs-lookup"><span data-stu-id="0569c-117">If this error is returned, no rows are changed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0569c-118">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="0569c-118">Remarks</span></span>

<span data-ttu-id="0569c-119">O método **ITableData::HrModifyRows** insere as linhas descritas pela estrutura [SRowSet](srowset.md) apontada pelo parâmetro _lpSRowSet_ .</span><span class="sxs-lookup"><span data-stu-id="0569c-119">The **ITableData::HrModifyRows** method inserts the rows described by the [SRowSet](srowset.md) structure pointed to by the  _lpSRowSet_ parameter.</span></span> <span data-ttu-id="0569c-120">Se o valor de índice de coluna de uma linha no conjunto de linha corresponder ao valor de uma linha existente na tabela, linha existente será substituída.</span><span class="sxs-lookup"><span data-stu-id="0569c-120">If the index column value of a row in the row set matches the value for an existing row in the table, the existing row is replaced.</span></span> <span data-ttu-id="0569c-121">Se não há nenhuma linha que corresponde o um incluída na estrutura de **SRowSet** , **HrModifyRows** adiciona a linha no final da tabela.</span><span class="sxs-lookup"><span data-stu-id="0569c-121">If no row exists that matches the one included in the **SRowSet** structure, **HrModifyRows** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="0569c-122">Todos os modos de exibição da tabela são modificados para incluir as linhas apontadas pela _lpSRowSet_.</span><span class="sxs-lookup"><span data-stu-id="0569c-122">All views of the table are modified to include the rows pointed to by  _lpSRowSet_.</span></span> <span data-ttu-id="0569c-123">No entanto, se um modo de exibição tiver uma restrição vigentes que exclui uma linha, talvez não seja visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="0569c-123">However, if a view has a restriction in place that excludes a row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="0569c-124">As colunas nas linhas apontadas pela _lpSRowSet_ não precisará ser na mesma ordem como as colunas na tabela.</span><span class="sxs-lookup"><span data-stu-id="0569c-124">The columns in the rows pointed to by  _lpSRowSet_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="0569c-125">O chamador também pode incluir como propriedades de colunas que não estão atualmente na tabela.</span><span class="sxs-lookup"><span data-stu-id="0569c-125">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="0569c-126">Para modos de exibição existentes, **HrModifyRows** disponibiliza essas novas colunas, mas não inclui-los no conjunto atual de coluna.</span><span class="sxs-lookup"><span data-stu-id="0569c-126">For existing views, **HrModifyRows** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="0569c-127">Para futuras exibições, **HrModifyRows** inclui as novas colunas no conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="0569c-127">For future views, **HrModifyRows** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="0569c-128">Depois **HrModifyRows** tiver adicionado as linhas, as notificações são enviadas para todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamou o método da tabela [IMAPITable::Advise](imapitable-advise.md) para registrar para notificações.</span><span class="sxs-lookup"><span data-stu-id="0569c-128">After **HrModifyRows** has added the rows, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="0569c-129">MAPI envia notificações de TABLE_ROW_ADDED ou TABLE_ROW_MODIFIED para cada linha, até oito linhas.</span><span class="sxs-lookup"><span data-stu-id="0569c-129">MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows.</span></span> <span data-ttu-id="0569c-130">Se mais de oito linhas são afetadas pela chamada **HrModifyRows** , MAPI envia uma notificação de TABLE_CHANGED única em vez disso.</span><span class="sxs-lookup"><span data-stu-id="0569c-130">If more than eight rows are affected by the **HrModifyRows** call, MAPI sends a single TABLE_CHANGED notification instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0569c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="0569c-131">See also</span></span>



[<span data-ttu-id="0569c-132">SRowSet</span><span class="sxs-lookup"><span data-stu-id="0569c-132">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="0569c-133">ITableData: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0569c-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

