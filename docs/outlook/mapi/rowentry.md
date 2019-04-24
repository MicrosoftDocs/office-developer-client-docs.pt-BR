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
ms.openlocfilehash: 243ab1e926171ee66b95cfd8e969cd77e2b31faf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279598"
---
# <a name="rowentry"></a><span data-ttu-id="2d7da-103">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="2d7da-103">ROWENTRY</span></span>

<span data-ttu-id="2d7da-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d7da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d7da-105">Contém uma linha e a operação que é executada nessa linha em uma tabela através da interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="2d7da-105">Contains a row and the operation that is performed on that row in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a><span data-ttu-id="2d7da-106">Members</span><span class="sxs-lookup"><span data-stu-id="2d7da-106">Members</span></span>

<span data-ttu-id="2d7da-107">**ulRowFlags**</span><span class="sxs-lookup"><span data-stu-id="2d7da-107">**ulRowFlags**</span></span>
  
> <span data-ttu-id="2d7da-108">Uma das operações a seguir a ser executada nos dados:</span><span class="sxs-lookup"><span data-stu-id="2d7da-108">One of the following operations to be performed on the data:</span></span> 
    
  - <span data-ttu-id="2d7da-109">ROW_ADD: adicionar os dados à tabela como uma nova linha.</span><span class="sxs-lookup"><span data-stu-id="2d7da-109">ROW_ADD: Add the data to the table as a new row.</span></span>
      
  - <span data-ttu-id="2d7da-110">ROW_MODIFY: modifique essa linha na tabela.</span><span class="sxs-lookup"><span data-stu-id="2d7da-110">ROW_MODIFY: Modify this row in the table.</span></span>
      
  - <span data-ttu-id="2d7da-111">ROW_REMOVE: remova essa linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="2d7da-111">ROW_REMOVE: Remove this row from the table.</span></span>
      
  - <span data-ttu-id="2d7da-112">ROW_EMPTY: Não adicione os dados da linha à tabela.</span><span class="sxs-lookup"><span data-stu-id="2d7da-112">ROW_EMPTY: Do not add the row data to the table.</span></span> <span data-ttu-id="2d7da-113">(A linha está vazia.)</span><span class="sxs-lookup"><span data-stu-id="2d7da-113">(The row is empty.)</span></span>
    
<span data-ttu-id="2d7da-114">**cValues**</span><span class="sxs-lookup"><span data-stu-id="2d7da-114">**cValues**</span></span>
  
> <span data-ttu-id="2d7da-115">O número de valores de propriedade em **rgPropvals**.</span><span class="sxs-lookup"><span data-stu-id="2d7da-115">The number of property values in **rgPropvals**.</span></span>
    
<span data-ttu-id="2d7da-116">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="2d7da-116">**rgPropVals**</span></span>
  
> <span data-ttu-id="2d7da-117">Uma matriz de estruturas [SPropValue](spropvalue.md) que representa os valores das colunas a serem inseridas na tabela.</span><span class="sxs-lookup"><span data-stu-id="2d7da-117">An array of [SPropValue](spropvalue.md) structures representing the columns values to be inserted into the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="2d7da-118">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2d7da-118">MFCMAPI reference</span></span>

<span data-ttu-id="2d7da-119">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d7da-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2d7da-120">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="2d7da-120">**File**</span></span>|<span data-ttu-id="2d7da-121">**Função**</span><span class="sxs-lookup"><span data-stu-id="2d7da-121">**Function**</span></span>|<span data-ttu-id="2d7da-122">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="2d7da-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2d7da-123">RulesDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="2d7da-123">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="2d7da-124">CRulesDlg:: getSelectedItems</span><span class="sxs-lookup"><span data-stu-id="2d7da-124">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="2d7da-125">Usado para criar uma lista de regras selecionadas para ações **modificadas** subsequentes.</span><span class="sxs-lookup"><span data-stu-id="2d7da-125">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d7da-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d7da-126">See also</span></span>
  
- [<span data-ttu-id="2d7da-127">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d7da-127">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
- [<span data-ttu-id="2d7da-128">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="2d7da-128">MAPI Structures</span></span>](mapi-structures.md)

