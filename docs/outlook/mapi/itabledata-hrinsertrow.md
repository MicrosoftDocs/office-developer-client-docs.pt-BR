---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2709ac612fc9e2edaa57b280d52c0a5229ee9978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435436"
---
# <a name="itabledatahrinsertrow"></a><span data-ttu-id="d40d1-103">ITableData::HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="d40d1-103">ITableData::HrInsertRow</span></span>

  
  
<span data-ttu-id="d40d1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d40d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d40d1-105">Insere uma linha de tabela.</span><span class="sxs-lookup"><span data-stu-id="d40d1-105">Inserts a table row.</span></span> 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="d40d1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d40d1-106">Parameters</span></span>

 <span data-ttu-id="d40d1-107">_uliRow_</span><span class="sxs-lookup"><span data-stu-id="d40d1-107">_uliRow_</span></span>
  
> <span data-ttu-id="d40d1-108">[in] Um número de linha sequencial que representa uma linha específica.</span><span class="sxs-lookup"><span data-stu-id="d40d1-108">[in] A sequential row number that represents a specific row.</span></span> <span data-ttu-id="d40d1-109">A nova linha será colocada após a linha indicada pelo número.</span><span class="sxs-lookup"><span data-stu-id="d40d1-109">The new row will be placed after the row that the number indicates.</span></span> <span data-ttu-id="d40d1-110">O  _parâmetro uliRow_ pode conter números de linha de 0 a n, onde n é o número total de linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="d40d1-110">The  _uliRow_ parameter can contains row numbers from 0 through n, where n is the total number of rows in the table.</span></span> <span data-ttu-id="d40d1-111">Passar n  _em uliRow_ anexa a linha ao final da tabela.</span><span class="sxs-lookup"><span data-stu-id="d40d1-111">Passing n in  _uliRow_ appends the row to the end of the table.</span></span> 
    
 <span data-ttu-id="d40d1-112">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="d40d1-112">_lpSRow_</span></span>
  
> <span data-ttu-id="d40d1-113">[in] Um ponteiro para uma [estrutura SRow](srow.md) que descreve a linha a ser inserida.</span><span class="sxs-lookup"><span data-stu-id="d40d1-113">[in] A pointer to an [SRow](srow.md) structure that describes the row to be inserted.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d40d1-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d40d1-114">Return value</span></span>

<span data-ttu-id="d40d1-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="d40d1-115">S_OK</span></span> 
  
> <span data-ttu-id="d40d1-116">A linha foi inserida com êxito.</span><span class="sxs-lookup"><span data-stu-id="d40d1-116">The row was successfully inserted.</span></span>
    
<span data-ttu-id="d40d1-117">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d40d1-117">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="d40d1-118">Uma linha que tem o mesmo valor de sua coluna de índice que a linha a ser inserida já existe na tabela.</span><span class="sxs-lookup"><span data-stu-id="d40d1-118">A row that has the same value for its index column as the row to be inserted already exists in the table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d40d1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d40d1-119">Remarks</span></span>

<span data-ttu-id="d40d1-120">O **método ITableData::HrInsertRow** insere uma linha em uma tabela em uma posição específica.</span><span class="sxs-lookup"><span data-stu-id="d40d1-120">The **ITableData::HrInsertRow** method inserts a row into a table at a particular position.</span></span> <span data-ttu-id="d40d1-121">A nova linha é inserida após a linha que está na posição especificada pelo _parâmetro uliRow._</span><span class="sxs-lookup"><span data-stu-id="d40d1-121">The new row is inserted after the row that is in the position specified by the  _uliRow_ parameter.</span></span> 
  
<span data-ttu-id="d40d1-122">Se  _uliRow_ for definido como o número de linhas na tabela, a nova linha será anexada ao final da tabela.</span><span class="sxs-lookup"><span data-stu-id="d40d1-122">If  _uliRow_ is set to the number of rows in the table, the new row is appended to the end of the table.</span></span> 
  
<span data-ttu-id="d40d1-123">A propriedade que atua como coluna de índice para a tabela deve ser incluída no membro **lpProps** da estrutura [SRow](srow.md) apontada pelo _parâmetro lpSRow._</span><span class="sxs-lookup"><span data-stu-id="d40d1-123">The property that acts as the index column for the table must be included in the **lpProps** member of the [SRow](srow.md) structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="d40d1-124">Essa propriedade de índice, normalmente **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), é usada para identificar exclusivamente a linha para tarefas de manutenção futuras.</span><span class="sxs-lookup"><span data-stu-id="d40d1-124">This index property, typically **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), is used to uniquely identify the row for future maintenance tasks.</span></span>
  
<span data-ttu-id="d40d1-125">As colunas de propriedades na **estrutura SRow** não devem estar na mesma ordem que as colunas de propriedades na tabela.</span><span class="sxs-lookup"><span data-stu-id="d40d1-125">The property columns in the **SRow** structure do not have to be in the same order as the property columns in the table.</span></span> 
  
<span data-ttu-id="d40d1-126">Depois que a linha é inserida, as notificações são enviadas a todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que tenham chamado o método [IMAPITable::Advise](imapitable-advise.md) da tabela para registrar para notificações.</span><span class="sxs-lookup"><span data-stu-id="d40d1-126">After the row is inserted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="d40d1-127">Nenhuma notificação será enviada se a linha inserida não for incluída no visualização devido a uma restrição.</span><span class="sxs-lookup"><span data-stu-id="d40d1-127">No notification is sent if the inserted row is not included in the view due to a restriction.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d40d1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d40d1-128">See also</span></span>



[<span data-ttu-id="d40d1-129">SRow</span><span class="sxs-lookup"><span data-stu-id="d40d1-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="d40d1-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d40d1-130">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="d40d1-131">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d40d1-131">ITableData : IUnknown</span></span>](itabledataiunknown.md)

