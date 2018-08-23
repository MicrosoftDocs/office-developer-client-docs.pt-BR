---
title: SMAPIFormPropArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropArray
api_type:
- COM
ms.assetid: bb243bc4-4974-4ad6-aa76-2426c1ebe84b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 389984f9d98ece6b2040edd741e3028fd7d766ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579309"
---
# <a name="smapiformproparray"></a><span data-ttu-id="dfc32-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="dfc32-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="dfc32-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfc32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfc32-105">Contém uma matriz de estruturas de [SMAPIFormProp](smapiformprop.md) .</span><span class="sxs-lookup"><span data-stu-id="dfc32-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dfc32-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="dfc32-106">Header file:</span></span>  <br/> |<span data-ttu-id="dfc32-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="dfc32-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="dfc32-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="dfc32-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="dfc32-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="dfc32-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="dfc32-110">Members</span><span class="sxs-lookup"><span data-stu-id="dfc32-110">Members</span></span>

 <span data-ttu-id="dfc32-111">**cProps**</span><span class="sxs-lookup"><span data-stu-id="dfc32-111">**cProps**</span></span>
  
> <span data-ttu-id="dfc32-112">Contagem de propriedades nomeadas na matriz no membro **aFormProp** .</span><span class="sxs-lookup"><span data-stu-id="dfc32-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="dfc32-113">**ulPad**</span><span class="sxs-lookup"><span data-stu-id="dfc32-113">**ulPad**</span></span>
  
>  <span data-ttu-id="dfc32-114">Oito bytes de preenchimento usados para garantir o alinhamento correto.</span><span class="sxs-lookup"><span data-stu-id="dfc32-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="dfc32-115">**aFormProp**</span><span class="sxs-lookup"><span data-stu-id="dfc32-115">**aFormProp**</span></span>
  
> <span data-ttu-id="dfc32-116">Matriz de propriedades do formulário.</span><span class="sxs-lookup"><span data-stu-id="dfc32-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dfc32-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfc32-117">Remarks</span></span>

<span data-ttu-id="dfc32-118">A estrutura **SMAPIFormPropArray** é passada como um parâmetro para os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="dfc32-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="dfc32-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="dfc32-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="dfc32-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="dfc32-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="dfc32-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="dfc32-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="dfc32-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfc32-122">See also</span></span>



[<span data-ttu-id="dfc32-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="dfc32-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="dfc32-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="dfc32-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="dfc32-125">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="dfc32-125">MAPI Structures</span></span>](mapi-structures.md)

