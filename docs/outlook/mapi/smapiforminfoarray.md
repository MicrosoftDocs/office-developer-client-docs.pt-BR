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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416969"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="4c514-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="4c514-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="4c514-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c514-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c514-105">Contém uma matriz de ponteiros para objetos de informações de formulário.</span><span class="sxs-lookup"><span data-stu-id="4c514-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c514-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4c514-106">Header file:</span></span>  <br/> |<span data-ttu-id="4c514-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="4c514-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="4c514-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="4c514-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="4c514-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="4c514-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="4c514-110">Members</span><span class="sxs-lookup"><span data-stu-id="4c514-110">Members</span></span>

 <span data-ttu-id="4c514-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="4c514-111">**cForms**</span></span>
  
> <span data-ttu-id="4c514-112">Contagem de ponteiros na matriz apontada pelo membro **aFormInfo.**</span><span class="sxs-lookup"><span data-stu-id="4c514-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="4c514-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="4c514-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="4c514-114">Ponteiro para uma matriz de ponteiros para objetos de informações de formulário.</span><span class="sxs-lookup"><span data-stu-id="4c514-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4c514-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c514-115">Remarks</span></span>

<span data-ttu-id="4c514-116">A **estrutura SMAPIFormInfoArray** é passada como um parâmetro nos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="4c514-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="4c514-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="4c514-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="4c514-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="4c514-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="4c514-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="4c514-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="4c514-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="4c514-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="4c514-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c514-121">See also</span></span>



[<span data-ttu-id="4c514-122">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="4c514-122">MAPI Structures</span></span>](mapi-structures.md)

