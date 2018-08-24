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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5ef210aedc884e5c09eca6335199e2ef284b901c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574824"
---
# <a name="itabledatahrmodifyrow"></a><span data-ttu-id="730b3-103">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="730b3-103">ITableData::HrModifyRow</span></span>

  
  
<span data-ttu-id="730b3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="730b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="730b3-105">Insere uma nova linha de tabela, possivelmente, substituindo uma linha existente.</span><span class="sxs-lookup"><span data-stu-id="730b3-105">Inserts a new table row, possibly replacing an existing row.</span></span>
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="730b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="730b3-106">Parameters</span></span>

 <span data-ttu-id="730b3-107">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="730b3-107">_lpSRow_</span></span>
  
> <span data-ttu-id="730b3-108">[in] Um ponteiro para uma estrutura de [SRow](srow.md) que descreve a linha a ser adicionado ou substituir uma linha existente.</span><span class="sxs-lookup"><span data-stu-id="730b3-108">[in] A pointer to an [SRow](srow.md) structure that describes the row to be added or to replace an existing row.</span></span> <span data-ttu-id="730b3-109">Uma das estruturas de valor de propriedade apontadas pelo membro **lpProps** da estrutura **SRow** deve conter uma coluna de índice, o mesmo valor que foi especificado no parâmetro _ulPropTagIndexColumn_ na chamada para o [CreateTable ](createtable.md)função.</span><span class="sxs-lookup"><span data-stu-id="730b3-109">One of the property value structures pointed to by the **lpProps** member of the **SRow** structure should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="730b3-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="730b3-110">Return value</span></span>

<span data-ttu-id="730b3-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="730b3-111">S_OK</span></span> 
  
> <span data-ttu-id="730b3-112">A linha foi inserida ou modificada com êxito.</span><span class="sxs-lookup"><span data-stu-id="730b3-112">The row was successfully inserted or modified.</span></span>
    
<span data-ttu-id="730b3-113">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="730b3-113">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="730b3-114">A linha no passado não tem uma coluna de índice.</span><span class="sxs-lookup"><span data-stu-id="730b3-114">The passed-in row does not have an index column.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="730b3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="730b3-115">Remarks</span></span>

<span data-ttu-id="730b3-116">O método **ITableData::HrModifyRow** insere a linha descrita pela estrutura **SRow** apontada pelo parâmetro _lpSRow_ .</span><span class="sxs-lookup"><span data-stu-id="730b3-116">The **ITableData::HrModifyRow** method inserts the row described by the **SRow** structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="730b3-117">Se uma linha que tem o mesmo valor para a coluna de seu índice como a linha que aponta de _lpSRow_ para já existe na tabela, linha existente será substituída.</span><span class="sxs-lookup"><span data-stu-id="730b3-117">If a row that has the same value for its index column as the row that  _lpSRow_ points to already exists in the table, the existing row is replaced.</span></span> <span data-ttu-id="730b3-118">Se não há nenhuma linha que corresponde o um incluída na estrutura de **SRow** , **HrModifyRow** adiciona a linha no final da tabela.</span><span class="sxs-lookup"><span data-stu-id="730b3-118">If no row exists that matches the one included in the **SRow** structure, **HrModifyRow** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="730b3-119">Todos os modos de exibição da tabela são modificados para incluir a linha apontada pela _lpSRow_.</span><span class="sxs-lookup"><span data-stu-id="730b3-119">All views of the table are modified to include the row pointed to by  _lpSRow_.</span></span> <span data-ttu-id="730b3-120">No entanto, se um modo de exibição tiver uma restrição vigentes que exclui a linha, talvez não seja visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="730b3-120">However, if a view has a restriction in place that excludes the row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="730b3-121">As colunas na linha apontado pela _lpSRow_ não precisará ser na mesma ordem como as colunas na tabela.</span><span class="sxs-lookup"><span data-stu-id="730b3-121">The columns in the row pointed to by  _lpSRow_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="730b3-122">O chamador também pode incluir como propriedades de colunas que não estão atualmente na tabela.</span><span class="sxs-lookup"><span data-stu-id="730b3-122">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="730b3-123">Para modos de exibição existentes, **HrModifyRow** disponibiliza essas novas colunas, mas não inclui-los no conjunto atual de coluna.</span><span class="sxs-lookup"><span data-stu-id="730b3-123">For existing views, **HrModifyRow** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="730b3-124">Para futuras exibições, **HrModifyRow** inclui as novas colunas no conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="730b3-124">For future views, **HrModifyRow** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="730b3-125">Após **HrModifyRow** adiciona a linha, as notificações são enviadas para todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamou o método da tabela [IMAPITable::Advise](imapitable-advise.md) para registrar para notificações.</span><span class="sxs-lookup"><span data-stu-id="730b3-125">After **HrModifyRow** adds the row, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="730b3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="730b3-126">See also</span></span>



[<span data-ttu-id="730b3-127">SRow</span><span class="sxs-lookup"><span data-stu-id="730b3-127">SRow</span></span>](srow.md)
  
[<span data-ttu-id="730b3-128">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="730b3-128">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="730b3-129">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="730b3-129">ITableData : IUnknown</span></span>](itabledataiunknown.md)

