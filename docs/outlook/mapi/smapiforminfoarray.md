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
ms.openlocfilehash: 6389bbf2094f51711d80896db0db9862059826cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770456"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="279b5-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="279b5-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="279b5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="279b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="279b5-105">Contém uma matriz de ponteiros para objetos de informações do formulário.</span><span class="sxs-lookup"><span data-stu-id="279b5-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="279b5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="279b5-106">Header file:</span></span>  <br/> |<span data-ttu-id="279b5-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="279b5-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="279b5-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="279b5-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="279b5-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="279b5-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="279b5-110">Members</span><span class="sxs-lookup"><span data-stu-id="279b5-110">Members</span></span>

 <span data-ttu-id="279b5-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="279b5-111">**cForms**</span></span>
  
> <span data-ttu-id="279b5-112">Contagem de ponteiros na matriz apontado pelo membro **aFormInfo** .</span><span class="sxs-lookup"><span data-stu-id="279b5-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="279b5-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="279b5-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="279b5-114">Ponteiro para uma matriz de ponteiros para objetos de informações do formulário.</span><span class="sxs-lookup"><span data-stu-id="279b5-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="279b5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="279b5-115">Remarks</span></span>

<span data-ttu-id="279b5-116">A estrutura **SMAPIFormInfoArray** é passada como um parâmetro nos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="279b5-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="279b5-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="279b5-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="279b5-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="279b5-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="279b5-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="279b5-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="279b5-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="279b5-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="279b5-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="279b5-121">See also</span></span>



[<span data-ttu-id="279b5-122">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="279b5-122">MAPI Structures</span></span>](mapi-structures.md)

