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
ms.openlocfilehash: 50b6581dec8211968a49b204c6d9b1ba1c65bb62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309510"
---
# <a name="smapiformproparray"></a><span data-ttu-id="a6bd0-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="a6bd0-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="a6bd0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6bd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6bd0-105">Contém uma matriz de estruturas [SMAPIFormProp](smapiformprop.md) .</span><span class="sxs-lookup"><span data-stu-id="a6bd0-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6bd0-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a6bd0-106">Header file:</span></span>  <br/> |<span data-ttu-id="a6bd0-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="a6bd0-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="a6bd0-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="a6bd0-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="a6bd0-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="a6bd0-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="a6bd0-110">Members</span><span class="sxs-lookup"><span data-stu-id="a6bd0-110">Members</span></span>

 <span data-ttu-id="a6bd0-111">**cProps**</span><span class="sxs-lookup"><span data-stu-id="a6bd0-111">**cProps**</span></span>
  
> <span data-ttu-id="a6bd0-112">Contagem de propriedades nomeadas na matriz no membro **aFormProp** .</span><span class="sxs-lookup"><span data-stu-id="a6bd0-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="a6bd0-113">**ulPad**</span><span class="sxs-lookup"><span data-stu-id="a6bd0-113">**ulPad**</span></span>
  
>  <span data-ttu-id="a6bd0-114">Oito bytes de preenchimento usados para garantir alinhamento correto.</span><span class="sxs-lookup"><span data-stu-id="a6bd0-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="a6bd0-115">**aFormProp**</span><span class="sxs-lookup"><span data-stu-id="a6bd0-115">**aFormProp**</span></span>
  
> <span data-ttu-id="a6bd0-116">Matriz de propriedades do formulário.</span><span class="sxs-lookup"><span data-stu-id="a6bd0-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6bd0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6bd0-117">Remarks</span></span>

<span data-ttu-id="a6bd0-118">A estrutura **SMAPIFormPropArray** é passada como um parâmetro para os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="a6bd0-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="a6bd0-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="a6bd0-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="a6bd0-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="a6bd0-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="a6bd0-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="a6bd0-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="a6bd0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6bd0-122">See also</span></span>



[<span data-ttu-id="a6bd0-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="a6bd0-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="a6bd0-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="a6bd0-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="a6bd0-125">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="a6bd0-125">MAPI Structures</span></span>](mapi-structures.md)

