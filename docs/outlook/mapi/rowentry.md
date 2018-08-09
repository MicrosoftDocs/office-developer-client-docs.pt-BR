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
ms.openlocfilehash: f8ac73b1977886208290285fec2d1bd0de1b4f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770281"
---
# <a name="rowentry"></a><span data-ttu-id="5b96e-103">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="5b96e-103">ROWENTRY</span></span>

<span data-ttu-id="5b96e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5b96e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5b96e-105">Contém uma linha e a operação é realizada nessa linha em uma tabela por meio da interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="5b96e-105">Contains a row and the operation that is performed on that row in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a><span data-ttu-id="5b96e-106">Members</span><span class="sxs-lookup"><span data-stu-id="5b96e-106">Members</span></span>

<span data-ttu-id="5b96e-107">**ulRowFlags**</span><span class="sxs-lookup"><span data-stu-id="5b96e-107">**ulRowFlags**</span></span>
  
> <span data-ttu-id="5b96e-108">Uma das seguintes operações a serem executadas nos dados:</span><span class="sxs-lookup"><span data-stu-id="5b96e-108">One of the following operations to be performed on the data:</span></span> 
    
  - <span data-ttu-id="5b96e-109">ROW_ADD: Adicione os dados à tabela como uma nova linha.</span><span class="sxs-lookup"><span data-stu-id="5b96e-109">ROW_ADD: Add the data to the table as a new row.</span></span>
      
  - <span data-ttu-id="5b96e-110">ROW_MODIFY: Modifica essa linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="5b96e-110">ROW_MODIFY: Modify this row in the table.</span></span>
      
  - <span data-ttu-id="5b96e-111">ROW_REMOVE: Remova essa linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="5b96e-111">ROW_REMOVE: Remove this row from the table.</span></span>
      
  - <span data-ttu-id="5b96e-112">ROW_EMPTY: Não adicione os dados de linha à tabela.</span><span class="sxs-lookup"><span data-stu-id="5b96e-112">ROW_EMPTY: Do not add the row data to the table.</span></span> <span data-ttu-id="5b96e-113">(A linha estará vazia).</span><span class="sxs-lookup"><span data-stu-id="5b96e-113">(The row is empty.)</span></span>
    
<span data-ttu-id="5b96e-114">**cValues**</span><span class="sxs-lookup"><span data-stu-id="5b96e-114">**cValues**</span></span>
  
> <span data-ttu-id="5b96e-115">O número de valores de propriedade em **rgPropvals**.</span><span class="sxs-lookup"><span data-stu-id="5b96e-115">The number of property values in **rgPropvals**.</span></span>
    
<span data-ttu-id="5b96e-116">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="5b96e-116">**rgPropVals**</span></span>
  
> <span data-ttu-id="5b96e-117">Uma matriz de estruturas de [SPropValue](spropvalue.md) que representam os valores de colunas a ser inserido na tabela.</span><span class="sxs-lookup"><span data-stu-id="5b96e-117">An array of [SPropValue](spropvalue.md) structures representing the columns values to be inserted into the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="5b96e-118">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5b96e-118">MFCMAPI reference</span></span>

<span data-ttu-id="5b96e-119">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b96e-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5b96e-120">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="5b96e-120">**File**</span></span>|<span data-ttu-id="5b96e-121">**Function**</span><span class="sxs-lookup"><span data-stu-id="5b96e-121">**Function**</span></span>|<span data-ttu-id="5b96e-122">**Comment**</span><span class="sxs-lookup"><span data-stu-id="5b96e-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5b96e-123">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="5b96e-123">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="5b96e-124">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="5b96e-124">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="5b96e-125">Usado para criar uma lista das regras selecionadas para ações de **ModifyTable** subsequentes.</span><span class="sxs-lookup"><span data-stu-id="5b96e-125">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b96e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b96e-126">See also</span></span>
  
- [<span data-ttu-id="5b96e-127">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b96e-127">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
- [<span data-ttu-id="5b96e-128">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="5b96e-128">MAPI Structures</span></span>](mapi-structures.md)

