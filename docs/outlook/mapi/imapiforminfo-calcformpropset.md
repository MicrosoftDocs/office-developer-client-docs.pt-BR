---
title: IMAPIFormInfoCalcFormPropSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcFormPropSet
api_type:
- COM
ms.assetid: cc3ffb8d-9cc4-47d3-9aa9-02c3a5b7775c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e5da9ffdd3021538ec814d1367cf1b06b49cfbc6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767022"
---
# <a name="imapiforminfocalcformpropset"></a><span data-ttu-id="388fa-103">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="388fa-103">IMAPIFormInfo::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="388fa-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="388fa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="388fa-105">Retorna um ponteiro para o conjunto completo de propriedades que usa um formulário.</span><span class="sxs-lookup"><span data-stu-id="388fa-105">Returns a pointer to the complete set of properties that a form uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="388fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="388fa-106">Parameters</span></span>

 <span data-ttu-id="388fa-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="388fa-107">_ulFlags_</span></span>
  
> <span data-ttu-id="388fa-108">[in] Uma bitmask dos sinalizadores que controla o tipo de cadeias de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="388fa-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="388fa-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="388fa-109">The following flag can be set:</span></span>
    
<span data-ttu-id="388fa-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="388fa-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="388fa-111">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="388fa-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="388fa-112">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="388fa-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="388fa-113">_ppFormPropArray_</span><span class="sxs-lookup"><span data-stu-id="388fa-113">_ppFormPropArray_</span></span>
  
> <span data-ttu-id="388fa-114">[out] Um ponteiro para um ponteiro para a estrutura de [SMAPIFormPropArray](smapiformproparray.md) retornado.</span><span class="sxs-lookup"><span data-stu-id="388fa-114">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="388fa-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="388fa-115">Return value</span></span>

<span data-ttu-id="388fa-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="388fa-116">S_OK</span></span> 
  
> <span data-ttu-id="388fa-117">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="388fa-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="388fa-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="388fa-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="388fa-119">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="388fa-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="388fa-120">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="388fa-120">MFCMAPI reference</span></span>

<span data-ttu-id="388fa-121">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="388fa-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="388fa-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="388fa-122">**File**</span></span>|<span data-ttu-id="388fa-123">**Function**</span><span class="sxs-lookup"><span data-stu-id="388fa-123">**Function**</span></span>|<span data-ttu-id="388fa-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="388fa-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="388fa-125">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="388fa-125">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="388fa-126">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="388fa-126">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="388fa-127">MFCMAPI usa o método de **IMAPIFormInfo::CalcFormPropSet** durante a criação de saída de depuração para os objetos de informações do formulário.</span><span class="sxs-lookup"><span data-stu-id="388fa-127">MFCMAPI uses the **IMAPIFormInfo::CalcFormPropSet** method when writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="388fa-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="388fa-128">See also</span></span>



[<span data-ttu-id="388fa-129">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="388fa-129">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="388fa-130">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="388fa-130">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="388fa-131">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="388fa-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

