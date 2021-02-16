---
title: SPropProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblem
api_type:
- COM
ms.assetid: 55943197-fd11-442d-bb4b-0bff565b846e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b3a0872c94459fc7c24d13e35adf335ef8012182
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407771"
---
# <a name="spropproblem"></a><span data-ttu-id="fe732-103">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="fe732-103">SPropProblem</span></span>

  
  
<span data-ttu-id="fe732-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe732-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe732-105">Descreve um erro relacionado a uma operação envolvendo uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="fe732-105">Describes an error that relate to an operation involving a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe732-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="fe732-106">Header file:</span></span>  <br/> |<span data-ttu-id="fe732-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe732-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a><span data-ttu-id="fe732-108">Members</span><span class="sxs-lookup"><span data-stu-id="fe732-108">Members</span></span>

 <span data-ttu-id="fe732-109">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="fe732-109">**ulIndex**</span></span>
  
> <span data-ttu-id="fe732-110">Um índice em uma matriz de marcas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="fe732-110">An index in an array of property tags.</span></span>
    
 <span data-ttu-id="fe732-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="fe732-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="fe732-112">Marca de propriedade da propriedade que tem o erro.</span><span class="sxs-lookup"><span data-stu-id="fe732-112">Property tag for the property that has the error.</span></span>
    
 <span data-ttu-id="fe732-113">**scode**</span><span class="sxs-lookup"><span data-stu-id="fe732-113">**scode**</span></span>
  
> <span data-ttu-id="fe732-114">Valor de erro que descreve o problema com a propriedade.</span><span class="sxs-lookup"><span data-stu-id="fe732-114">Error value describing the problem with the property.</span></span> <span data-ttu-id="fe732-115">Esse valor pode ser qualquer valor [de SCODE MAPI.](scode.md)</span><span class="sxs-lookup"><span data-stu-id="fe732-115">This value can be any MAPI [SCODE](scode.md) value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fe732-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe732-116">Remarks</span></span>

<span data-ttu-id="fe732-117">Uma matriz de **estruturas SPropProblem** é retornada dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="fe732-117">An array of **SPropProblem** structures is returned from the following methods:</span></span> 
  
- [<span data-ttu-id="fe732-118">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="fe732-118">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
    
- [<span data-ttu-id="fe732-119">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="fe732-119">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
    
- [<span data-ttu-id="fe732-120">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="fe732-120">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
    
- [<span data-ttu-id="fe732-121">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="fe732-121">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="fe732-122">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="fe732-122">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
- [<span data-ttu-id="fe732-123">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="fe732-123">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="fe732-124">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="fe732-124">IPropData::HrAddObjProps</span></span>](ipropdata-hraddobjprops.md)
    
<span data-ttu-id="fe732-125">Uma **estrutura SPropProblem** contém um valor de erro **SCODE** que resulta de uma operação tentando modificar ou excluir uma propriedade MAPI.</span><span class="sxs-lookup"><span data-stu-id="fe732-125">An **SPropProblem** structure contains an **SCODE** error value that results from an operation trying to modify or delete a MAPI property.</span></span> 
  
<span data-ttu-id="fe732-126">Para obter mais informações sobre como **a estrutura SPropProblem** funciona com erros relacionados a propriedades, consulte [MAPI Named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="fe732-126">For more information about how the **SPropProblem** structure works with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fe732-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe732-127">See also</span></span>



[<span data-ttu-id="fe732-128">SCODE</span><span class="sxs-lookup"><span data-stu-id="fe732-128">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="fe732-129">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="fe732-129">SPropProblemArray</span></span>](spropproblemarray.md)


[<span data-ttu-id="fe732-130">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="fe732-130">MAPI Structures</span></span>](mapi-structures.md)

