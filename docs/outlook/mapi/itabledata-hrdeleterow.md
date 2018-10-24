---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 989c6872e78ef78e5e0b18149a186d4f920ca603
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563461"
---
# <a name="itabledatahrdeleterow"></a><span data-ttu-id="cbadd-103">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="cbadd-103">ITableData::HrDeleteRow</span></span>

  
  
<span data-ttu-id="cbadd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbadd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbadd-105">Exclui uma linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="cbadd-105">Deletes a table row.</span></span>
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="cbadd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbadd-106">Parameters</span></span>

 <span data-ttu-id="cbadd-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="cbadd-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="cbadd-108">[in] Um ponteiro para uma estrutura de valor de propriedade que descreve a coluna de índice da linha a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="cbadd-108">[in] A pointer to a property value structure that describes the index column for the row to be deleted.</span></span> <span data-ttu-id="cbadd-109">O membro **ulPropTag** da estrutura de valor de propriedade deve conter a mesma marca de propriedade, como o parâmetro _ulPropTagIndexColumn_ da chamada para a função [CreateTable](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="cbadd-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cbadd-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cbadd-110">Return value</span></span>

<span data-ttu-id="cbadd-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="cbadd-111">S_OK</span></span> 
  
> <span data-ttu-id="cbadd-112">A linha foi excluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="cbadd-112">The row was successfully deleted.</span></span>
    
<span data-ttu-id="cbadd-113">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="cbadd-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="cbadd-114">A propriedade apontada pelo parâmetro _lpSPropValue_ não identifica uma linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="cbadd-114">The property pointed to by the  _lpSPropValue_ parameter does not identify a row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cbadd-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbadd-115">Remarks</span></span>

<span data-ttu-id="cbadd-116">O método **ITableData::HrDeleteRow** remove a linha da tabela que contém a coluna que coincida com a propriedade apontada pelo parâmetro _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="cbadd-116">The **ITableData::HrDeleteRow** method removes the table row that contains the column that matches the property pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="cbadd-117">Os dados para a linha serão excluídos e a linha é removida do open todos os modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="cbadd-117">The data for the row is deleted and the row is removed from all open views.</span></span> 
  
<span data-ttu-id="cbadd-118">Depois que a linha foi excluída, as notificações são enviadas para todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamou o método da tabela [IMAPITable::Advise](imapitable-advise.md) para registrar para notificações.</span><span class="sxs-lookup"><span data-stu-id="cbadd-118">After the row is deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="cbadd-119">A exclusão de uma linha não reduz o conjunto de colunas que está disponível para modos de exibição existentes ou aberto subsequentemente modos de exibição, mesmo se a linha excluída é a última linha que tem um valor para uma coluna específica.</span><span class="sxs-lookup"><span data-stu-id="cbadd-119">Deleting a row does not reduce the column set that is available to existing views or subsequently opened views, even if the deleted row is the last row that has a value for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cbadd-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbadd-120">See also</span></span>



[<span data-ttu-id="cbadd-121">CreateTable</span><span class="sxs-lookup"><span data-stu-id="cbadd-121">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="cbadd-122">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="cbadd-122">ITableData::HrDeleteRows</span></span>](itabledata-hrdeleterows.md)
  
[<span data-ttu-id="cbadd-123">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="cbadd-123">ITableData::HrModifyRow</span></span>](itabledata-hrmodifyrow.md)
  
[<span data-ttu-id="cbadd-124">SPropValue</span><span class="sxs-lookup"><span data-stu-id="cbadd-124">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="cbadd-125">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="cbadd-125">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="cbadd-126">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbadd-126">ITableData : IUnknown</span></span>](itabledataiunknown.md)

