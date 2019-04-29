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
ms.openlocfilehash: c13b741b1e0ddfd964b9325d736a26dac4bff2af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419181"
---
# <a name="rowlist"></a><span data-ttu-id="24352-103">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="24352-103">ROWLIST</span></span>

  
  
<span data-ttu-id="24352-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24352-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24352-105">Contém uma matriz de [](rowentry.md) estruturas de transentry que representam linhas e as operações realizadas em uma tabela através da interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="24352-105">Contains an array of [ROWENTRY](rowentry.md) structures representing rows and the operations that are performed on those rows in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a><span data-ttu-id="24352-106">Members</span><span class="sxs-lookup"><span data-stu-id="24352-106">Members</span></span>

 <span data-ttu-id="24352-107">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="24352-107">**cEntries**</span></span>
  
> <span data-ttu-id="24352-108">Contagem de entradas na matriz especificada pelo membro **aEntries** .</span><span class="sxs-lookup"><span data-stu-id="24352-108">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
 <span data-ttu-id="24352-109">**aEntries [MAPI_DIM]**</span><span class="sxs-lookup"><span data-stu-id="24352-109">**aEntries[MAPI_DIM]**</span></span>
  
> <span data-ttu-id="24352-110">Matriz de \*\*\*\* estruturas de transentry que contém as linhas e as operações que são executadas nessas linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="24352-110">Array of **ROWENTRY** structures that contains the rows and the operations that are performed on those rows in the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="24352-111">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="24352-111">MFCMAPI reference</span></span>

<span data-ttu-id="24352-112">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="24352-112">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="24352-113">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="24352-113">**File**</span></span>|<span data-ttu-id="24352-114">**Função**</span><span class="sxs-lookup"><span data-stu-id="24352-114">**Function**</span></span>|<span data-ttu-id="24352-115">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="24352-115">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="24352-116">RulesDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="24352-116">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="24352-117">CRulesDlg:: getSelectedItems</span><span class="sxs-lookup"><span data-stu-id="24352-117">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="24352-118">Usado para criar uma lista de regras selecionadas para ações **modificadas** subsequentes.</span><span class="sxs-lookup"><span data-stu-id="24352-118">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24352-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="24352-119">See also</span></span>



[<span data-ttu-id="24352-120">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="24352-120">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="24352-121">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="24352-121">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="24352-122">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="24352-122">MAPI Structures</span></span>](mapi-structures.md)

