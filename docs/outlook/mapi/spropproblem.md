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
ms.openlocfilehash: 7c19cce33ec351a5627870782ebb4fe509a98be2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573282"
---
# <a name="spropproblem"></a><span data-ttu-id="81ab0-103">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="81ab0-103">SPropProblem</span></span>

  
  
<span data-ttu-id="81ab0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81ab0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81ab0-105">Descreve um erro que se relacionam com uma operação envolvendo uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="81ab0-105">Describes an error that relate to an operation involving a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81ab0-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="81ab0-106">Header file:</span></span>  <br/> |<span data-ttu-id="81ab0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81ab0-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a><span data-ttu-id="81ab0-108">Members</span><span class="sxs-lookup"><span data-stu-id="81ab0-108">Members</span></span>

 <span data-ttu-id="81ab0-109">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="81ab0-109">**ulIndex**</span></span>
  
> <span data-ttu-id="81ab0-110">Um índice em uma matriz das marcas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="81ab0-110">An index in an array of property tags.</span></span>
    
 <span data-ttu-id="81ab0-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="81ab0-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="81ab0-112">Marca de propriedade para a propriedade que tem o erro.</span><span class="sxs-lookup"><span data-stu-id="81ab0-112">Property tag for the property that has the error.</span></span>
    
 <span data-ttu-id="81ab0-113">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="81ab0-113">**scode**</span></span>
  
> <span data-ttu-id="81ab0-114">Valor de erro descrevendo o problema com a propriedade.</span><span class="sxs-lookup"><span data-stu-id="81ab0-114">Error value describing the problem with the property.</span></span> <span data-ttu-id="81ab0-115">Esse valor pode ser qualquer valor MAPI [SCODE](scode.md) .</span><span class="sxs-lookup"><span data-stu-id="81ab0-115">This value can be any MAPI [SCODE](scode.md) value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="81ab0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="81ab0-116">Remarks</span></span>

<span data-ttu-id="81ab0-117">Uma matriz de estruturas de **SPropProblem** é retornada dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="81ab0-117">An array of **SPropProblem** structures is returned from the following methods:</span></span> 
  
- [<span data-ttu-id="81ab0-118">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="81ab0-118">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
    
- [<span data-ttu-id="81ab0-119">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="81ab0-119">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
    
- [<span data-ttu-id="81ab0-120">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="81ab0-120">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
    
- [<span data-ttu-id="81ab0-121">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="81ab0-121">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="81ab0-122">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="81ab0-122">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
- [<span data-ttu-id="81ab0-123">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="81ab0-123">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="81ab0-124">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="81ab0-124">IPropData::HrAddObjProps</span></span>](ipropdata-hraddobjprops.md)
    
<span data-ttu-id="81ab0-125">Uma estrutura **SPropProblem** contém um valor de erro **SCODE** resultante de uma operação tentando modificar ou excluir uma propriedade MAPI.</span><span class="sxs-lookup"><span data-stu-id="81ab0-125">An **SPropProblem** structure contains an **SCODE** error value that results from an operation trying to modify or delete a MAPI property.</span></span> 
  
<span data-ttu-id="81ab0-126">Para obter mais informações sobre como a estrutura de **SPropProblem** funciona com erros relacionados às propriedades, consulte [Propriedades de chamada de MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="81ab0-126">For more information about how the **SPropProblem** structure works with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="81ab0-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="81ab0-127">See also</span></span>



[<span data-ttu-id="81ab0-128">SCODE</span><span class="sxs-lookup"><span data-stu-id="81ab0-128">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="81ab0-129">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="81ab0-129">SPropProblemArray</span></span>](spropproblemarray.md)


[<span data-ttu-id="81ab0-130">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="81ab0-130">MAPI Structures</span></span>](mapi-structures.md)

