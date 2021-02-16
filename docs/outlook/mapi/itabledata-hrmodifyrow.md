---
title: ITableDataHrModifyRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRow
api_type:
- COM
ms.assetid: 9e255b3e-dd17-4528-ba4e-c3a1aef32b04
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 44ecf095ad24dd266dc5f603ace9c7b9f21c1b41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408996"
---
# <a name="itabledatahrmodifyrow"></a><span data-ttu-id="4f646-103">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="4f646-103">ITableData::HrModifyRow</span></span>

  
  
<span data-ttu-id="4f646-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f646-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f646-105">Insere uma nova linha de tabela, possivelmente substituindo uma linha existente.</span><span class="sxs-lookup"><span data-stu-id="4f646-105">Inserts a new table row, possibly replacing an existing row.</span></span>
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="4f646-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f646-106">Parameters</span></span>

 <span data-ttu-id="4f646-107">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="4f646-107">_lpSRow_</span></span>
  
> <span data-ttu-id="4f646-108">[in] Um ponteiro para uma [estrutura SRow](srow.md) que descreve a linha a ser adicionada ou para substituir uma linha existente.</span><span class="sxs-lookup"><span data-stu-id="4f646-108">[in] A pointer to an [SRow](srow.md) structure that describes the row to be added or to replace an existing row.</span></span> <span data-ttu-id="4f646-109">Uma das estruturas de valor de propriedade apontadas pelo membro **lpProps** da estrutura **SRow** deve conter a coluna de índice, o mesmo valor especificado no parâmetro _ulPropTagIndexColumn_ na chamada para a função [CreateTable.](createtable.md)</span><span class="sxs-lookup"><span data-stu-id="4f646-109">One of the property value structures pointed to by the **lpProps** member of the **SRow** structure should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4f646-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4f646-110">Return value</span></span>

<span data-ttu-id="4f646-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f646-111">S_OK</span></span> 
  
> <span data-ttu-id="4f646-112">A linha foi inserida ou modificada com êxito.</span><span class="sxs-lookup"><span data-stu-id="4f646-112">The row was successfully inserted or modified.</span></span>
    
<span data-ttu-id="4f646-113">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4f646-113">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="4f646-114">A linha passada não tem uma coluna de índice.</span><span class="sxs-lookup"><span data-stu-id="4f646-114">The passed-in row does not have an index column.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f646-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f646-115">Remarks</span></span>

<span data-ttu-id="4f646-116">O **método ITableData::HrModifyRow** insere a linha descrita pela estrutura **SRow** apontada pelo _parâmetro lpSRow._</span><span class="sxs-lookup"><span data-stu-id="4f646-116">The **ITableData::HrModifyRow** method inserts the row described by the **SRow** structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="4f646-117">Se uma linha com o mesmo valor de sua coluna de índice que a linha  _que lpSRow_ aponta já existir na tabela, a linha existente será substituída.</span><span class="sxs-lookup"><span data-stu-id="4f646-117">If a row that has the same value for its index column as the row that  _lpSRow_ points to already exists in the table, the existing row is replaced.</span></span> <span data-ttu-id="4f646-118">Se não existir uma linha que corresponde à que está incluída na estrutura **SRow,** **HrModifyRow** adiciona a linha ao final da tabela.</span><span class="sxs-lookup"><span data-stu-id="4f646-118">If no row exists that matches the one included in the **SRow** structure, **HrModifyRow** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="4f646-119">Todos os exibições da tabela são modificados para incluir a linha apontada por  _lpSRow_.</span><span class="sxs-lookup"><span data-stu-id="4f646-119">All views of the table are modified to include the row pointed to by  _lpSRow_.</span></span> <span data-ttu-id="4f646-120">No entanto, se um ponto de vista tiver uma restrição no local que exclua a linha, talvez ele não seja visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="4f646-120">However, if a view has a restriction in place that excludes the row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="4f646-121">As colunas na linha apontada por  _lpSRow_ não devem estar na mesma ordem que as colunas na tabela.</span><span class="sxs-lookup"><span data-stu-id="4f646-121">The columns in the row pointed to by  _lpSRow_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="4f646-122">O chamador também pode incluir como propriedades de colunas que não estão atualmente na tabela.</span><span class="sxs-lookup"><span data-stu-id="4f646-122">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="4f646-123">Para exibições existentes, **HrModifyRow** disponibiliza essas novas colunas, mas não as inclui no conjunto de colunas atual.</span><span class="sxs-lookup"><span data-stu-id="4f646-123">For existing views, **HrModifyRow** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="4f646-124">Para exibições futuras, **HrModifyRow** inclui as novas colunas no conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="4f646-124">For future views, **HrModifyRow** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="4f646-125">Depois **que HrModifyRow** adiciona a linha, as notificações são enviadas a todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamam o método [IMAPITable::Advise](imapitable-advise.md) da tabela para registrar para notificações.</span><span class="sxs-lookup"><span data-stu-id="4f646-125">After **HrModifyRow** adds the row, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f646-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f646-126">See also</span></span>



[<span data-ttu-id="4f646-127">SRow</span><span class="sxs-lookup"><span data-stu-id="4f646-127">SRow</span></span>](srow.md)
  
[<span data-ttu-id="4f646-128">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4f646-128">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="4f646-129">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f646-129">ITableData : IUnknown</span></span>](itabledataiunknown.md)

