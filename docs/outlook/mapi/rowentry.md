---
title: ROWENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWENTRY
api_type:
- COM
ms.assetid: bd6c0d8e-68cc-4d60-9029-13ed81c816cd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fb0bfaba1ca0a0d7d34096b3b0b1db9863207097
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576264"
---
# <a name="rowentry"></a><span data-ttu-id="d26de-103">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="d26de-103">ROWENTRY</span></span>

<span data-ttu-id="d26de-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d26de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d26de-105">Contém uma linha e a operação é realizada nessa linha em uma tabela por meio da interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="d26de-105">Contains a row and the operation that is performed on that row in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a><span data-ttu-id="d26de-106">Members</span><span class="sxs-lookup"><span data-stu-id="d26de-106">Members</span></span>

<span data-ttu-id="d26de-107">**ulRowFlags**</span><span class="sxs-lookup"><span data-stu-id="d26de-107">**ulRowFlags**</span></span>
  
> <span data-ttu-id="d26de-108">Uma das seguintes operações a serem executadas nos dados:</span><span class="sxs-lookup"><span data-stu-id="d26de-108">One of the following operations to be performed on the data:</span></span> 
    
  - <span data-ttu-id="d26de-109">ROW_ADD: Adicione os dados à tabela como uma nova linha.</span><span class="sxs-lookup"><span data-stu-id="d26de-109">ROW_ADD: Add the data to the table as a new row.</span></span>
      
  - <span data-ttu-id="d26de-110">ROW_MODIFY: Modifica essa linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="d26de-110">ROW_MODIFY: Modify this row in the table.</span></span>
      
  - <span data-ttu-id="d26de-111">ROW_REMOVE: Remova essa linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="d26de-111">ROW_REMOVE: Remove this row from the table.</span></span>
      
  - <span data-ttu-id="d26de-112">ROW_EMPTY: Não adicione os dados de linha à tabela.</span><span class="sxs-lookup"><span data-stu-id="d26de-112">ROW_EMPTY: Do not add the row data to the table.</span></span> <span data-ttu-id="d26de-113">(A linha estará vazia).</span><span class="sxs-lookup"><span data-stu-id="d26de-113">(The row is empty.)</span></span>
    
<span data-ttu-id="d26de-114">**cValues**</span><span class="sxs-lookup"><span data-stu-id="d26de-114">**cValues**</span></span>
  
> <span data-ttu-id="d26de-115">O número de valores de propriedade em **rgPropvals**.</span><span class="sxs-lookup"><span data-stu-id="d26de-115">The number of property values in **rgPropvals**.</span></span>
    
<span data-ttu-id="d26de-116">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="d26de-116">**rgPropVals**</span></span>
  
> <span data-ttu-id="d26de-117">Uma matriz de estruturas de [SPropValue](spropvalue.md) que representam os valores de colunas a ser inserido na tabela.</span><span class="sxs-lookup"><span data-stu-id="d26de-117">An array of [SPropValue](spropvalue.md) structures representing the columns values to be inserted into the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="d26de-118">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d26de-118">MFCMAPI reference</span></span>

<span data-ttu-id="d26de-119">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d26de-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d26de-120">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d26de-120">**File**</span></span>|<span data-ttu-id="d26de-121">**Function**</span><span class="sxs-lookup"><span data-stu-id="d26de-121">**Function**</span></span>|<span data-ttu-id="d26de-122">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d26de-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d26de-123">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="d26de-123">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="d26de-124">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="d26de-124">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="d26de-125">Usado para criar uma lista das regras selecionadas para ações de **ModifyTable** subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d26de-125">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d26de-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d26de-126">See also</span></span>
  
- [<span data-ttu-id="d26de-127">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d26de-127">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
- [<span data-ttu-id="d26de-128">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="d26de-128">MAPI Structures</span></span>](mapi-structures.md)

