---
title: ROWLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWLIST
api_type:
- COM
ms.assetid: ce0be0d5-4962-4d53-828f-c93d1c5aae32
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4cbaf08c58a98be45ad33aebb8f230fb53c234f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577657"
---
# <a name="rowlist"></a><span data-ttu-id="743f0-103">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="743f0-103">ROWLIST</span></span>

  
  
<span data-ttu-id="743f0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="743f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="743f0-105">Contém uma matriz de estruturas [ROWENTRY](rowentry.md) representando as linhas e as operações que são executadas nessas linhas em uma tabela por meio da interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="743f0-105">Contains an array of [ROWENTRY](rowentry.md) structures representing rows and the operations that are performed on those rows in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a><span data-ttu-id="743f0-106">Members</span><span class="sxs-lookup"><span data-stu-id="743f0-106">Members</span></span>

 <span data-ttu-id="743f0-107">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="743f0-107">**cEntries**</span></span>
  
> <span data-ttu-id="743f0-108">Contagem de entradas na matriz especificada pelo membro **aEntries** .</span><span class="sxs-lookup"><span data-stu-id="743f0-108">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
 <span data-ttu-id="743f0-109">**aEntries [MAPI_DIM]**</span><span class="sxs-lookup"><span data-stu-id="743f0-109">**aEntries[MAPI_DIM]**</span></span>
  
> <span data-ttu-id="743f0-110">Matriz de estruturas **ROWENTRY** que contém as linhas e as operações que são realizadas nessas linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="743f0-110">Array of **ROWENTRY** structures that contains the rows and the operations that are performed on those rows in the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="743f0-111">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="743f0-111">MFCMAPI reference</span></span>

<span data-ttu-id="743f0-112">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="743f0-112">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="743f0-113">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="743f0-113">**File**</span></span>|<span data-ttu-id="743f0-114">**Function**</span><span class="sxs-lookup"><span data-stu-id="743f0-114">**Function**</span></span>|<span data-ttu-id="743f0-115">**Comment**</span><span class="sxs-lookup"><span data-stu-id="743f0-115">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="743f0-116">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="743f0-116">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="743f0-117">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="743f0-117">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="743f0-118">Usado para criar uma lista das regras selecionadas para ações de **ModifyTable** subsequentes.</span><span class="sxs-lookup"><span data-stu-id="743f0-118">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="743f0-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="743f0-119">See also</span></span>



[<span data-ttu-id="743f0-120">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="743f0-120">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="743f0-121">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="743f0-121">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="743f0-122">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="743f0-122">MAPI Structures</span></span>](mapi-structures.md)

