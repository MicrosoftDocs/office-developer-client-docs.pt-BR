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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 29fdbf060576ee9309473fddf8740b06229dae9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767703"
---
# <a name="itabledatahrinsertrow"></a><span data-ttu-id="c412e-103">ITableData::HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="c412e-103">ITableData::HrInsertRow</span></span>

  
  
<span data-ttu-id="c412e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c412e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c412e-105">Insere uma linha de tabela.</span><span class="sxs-lookup"><span data-stu-id="c412e-105">Inserts a table row.</span></span> 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="c412e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c412e-106">Parameters</span></span>

 <span data-ttu-id="c412e-107">_uliRow_</span><span class="sxs-lookup"><span data-stu-id="c412e-107">_uliRow_</span></span>
  
> <span data-ttu-id="c412e-108">[in] Um número de linha sequencial que representa uma linha específica.</span><span class="sxs-lookup"><span data-stu-id="c412e-108">[in] A sequential row number that represents a specific row.</span></span> <span data-ttu-id="c412e-109">Após a linha que indica o número será colocada a nova linha.</span><span class="sxs-lookup"><span data-stu-id="c412e-109">The new row will be placed after the row that the number indicates.</span></span> <span data-ttu-id="c412e-110">O parâmetro _uliRow_ pode conter os números de linha de 0 até n, onde n é o número total de linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="c412e-110">The  _uliRow_ parameter can contains row numbers from 0 through n, where n is the total number of rows in the table.</span></span> <span data-ttu-id="c412e-111">Passando n _uliRow_ acrescenta a linha no final da tabela.</span><span class="sxs-lookup"><span data-stu-id="c412e-111">Passing n in  _uliRow_ appends the row to the end of the table.</span></span> 
    
 <span data-ttu-id="c412e-112">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="c412e-112">_lpSRow_</span></span>
  
> <span data-ttu-id="c412e-113">[in] Um ponteiro para uma estrutura de [SRow](srow.md) que descreve a linha a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="c412e-113">[in] A pointer to an [SRow](srow.md) structure that describes the row to be inserted.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c412e-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c412e-114">Return value</span></span>

<span data-ttu-id="c412e-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="c412e-115">S_OK</span></span> 
  
> <span data-ttu-id="c412e-116">A linha foi inserida com êxito.</span><span class="sxs-lookup"><span data-stu-id="c412e-116">The row was successfully inserted.</span></span>
    
<span data-ttu-id="c412e-117">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c412e-117">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="c412e-118">Uma linha que tem o mesmo valor para a coluna de seu índice, como a linha a ser inserido já existe na tabela.</span><span class="sxs-lookup"><span data-stu-id="c412e-118">A row that has the same value for its index column as the row to be inserted already exists in the table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c412e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c412e-119">Remarks</span></span>

<span data-ttu-id="c412e-120">O método **ITableData::HrInsertRow** insere uma linha em uma tabela em uma posição específica.</span><span class="sxs-lookup"><span data-stu-id="c412e-120">The **ITableData::HrInsertRow** method inserts a row into a table at a particular position.</span></span> <span data-ttu-id="c412e-121">A nova linha é inserida após a linha que está na posição especificada pelo parâmetro _uliRow_ .</span><span class="sxs-lookup"><span data-stu-id="c412e-121">The new row is inserted after the row that is in the position specified by the  _uliRow_ parameter.</span></span> 
  
<span data-ttu-id="c412e-122">Se _uliRow_ for definido como o número de linhas na tabela, a nova linha é acrescentada ao final da tabela.</span><span class="sxs-lookup"><span data-stu-id="c412e-122">If  _uliRow_ is set to the number of rows in the table, the new row is appended to the end of the table.</span></span> 
  
<span data-ttu-id="c412e-123">A propriedade que atua como a coluna de índice para a tabela deve ser incluída no membro **lpProps** da estrutura [SRow](srow.md) apontado pelo parâmetro _lpSRow_ .</span><span class="sxs-lookup"><span data-stu-id="c412e-123">The property that acts as the index column for the table must be included in the **lpProps** member of the [SRow](srow.md) structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="c412e-124">Esta propriedade index, normalmente **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) é usada para identificar exclusivamente a linha para tarefas de manutenção futura.</span><span class="sxs-lookup"><span data-stu-id="c412e-124">This index property, typically **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), is used to uniquely identify the row for future maintenance tasks.</span></span>
  
<span data-ttu-id="c412e-125">As colunas de propriedades na estrutura de **SRow** não precisará ser na mesma ordem como as colunas de propriedades da tabela.</span><span class="sxs-lookup"><span data-stu-id="c412e-125">The property columns in the **SRow** structure do not have to be in the same order as the property columns in the table.</span></span> 
  
<span data-ttu-id="c412e-126">Depois que a linha é inserida, as notificações são enviadas para todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamou o método da tabela [IMAPITable::Advise](imapitable-advise.md) para registrar para notificações.</span><span class="sxs-lookup"><span data-stu-id="c412e-126">After the row is inserted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="c412e-127">Nenhuma notificação é enviada se a linha inserida não está incluída no modo de exibição devido a uma restrição.</span><span class="sxs-lookup"><span data-stu-id="c412e-127">No notification is sent if the inserted row is not included in the view due to a restriction.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c412e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c412e-128">See also</span></span>



[<span data-ttu-id="c412e-129">SRow</span><span class="sxs-lookup"><span data-stu-id="c412e-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="c412e-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c412e-130">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="c412e-131">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c412e-131">ITableData : IUnknown</span></span>](itabledataiunknown.md)

