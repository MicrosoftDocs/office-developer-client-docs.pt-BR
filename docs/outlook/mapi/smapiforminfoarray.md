---
title: SMAPIFormInfoArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormInfoArray
api_type:
- COM
ms.assetid: f5eeb75d-debb-4ac1-b239-e8e852460ce0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e274e24d9aff30bb39b1865306477164d413d9a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319170"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="166b2-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="166b2-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="166b2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="166b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="166b2-105">Contém uma matriz de ponteiros para objetos de informação de formulário.</span><span class="sxs-lookup"><span data-stu-id="166b2-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="166b2-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="166b2-106">Header file:</span></span>  <br/> |<span data-ttu-id="166b2-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="166b2-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="166b2-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="166b2-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="166b2-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="166b2-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="166b2-110">Members</span><span class="sxs-lookup"><span data-stu-id="166b2-110">Members</span></span>

 <span data-ttu-id="166b2-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="166b2-111">**cForms**</span></span>
  
> <span data-ttu-id="166b2-112">Contagem de ponteiros na matriz apontada pelo membro **aFormInfo** .</span><span class="sxs-lookup"><span data-stu-id="166b2-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="166b2-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="166b2-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="166b2-114">Ponteiro para uma matriz de ponteiros para objetos de informação de formulário.</span><span class="sxs-lookup"><span data-stu-id="166b2-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="166b2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="166b2-115">Remarks</span></span>

<span data-ttu-id="166b2-116">A estrutura **SMAPIFormInfoArray** é passada como um parâmetro nos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="166b2-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="166b2-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="166b2-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="166b2-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="166b2-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="166b2-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="166b2-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="166b2-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="166b2-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="166b2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="166b2-121">See also</span></span>



[<span data-ttu-id="166b2-122">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="166b2-122">MAPI Structures</span></span>](mapi-structures.md)

