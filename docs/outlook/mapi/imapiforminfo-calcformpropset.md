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
ms.openlocfilehash: 0b62c21348da71c1ee863f70d6e6a549a5d10003
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342123"
---
# <a name="imapiforminfocalcformpropset"></a><span data-ttu-id="c3cf0-103">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="c3cf0-103">IMAPIFormInfo::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="c3cf0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3cf0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3cf0-105">Retorna um ponteiro para o conjunto completo de propriedades que um formulário usa.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-105">Returns a pointer to the complete set of properties that a form uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="c3cf0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3cf0-106">Parameters</span></span>

 <span data-ttu-id="c3cf0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c3cf0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c3cf0-108">no Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="c3cf0-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="c3cf0-109">The following flag can be set:</span></span>
    
<span data-ttu-id="c3cf0-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c3cf0-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c3cf0-111">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="c3cf0-112">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="c3cf0-113">_ppFormPropArray_</span><span class="sxs-lookup"><span data-stu-id="c3cf0-113">_ppFormPropArray_</span></span>
  
> <span data-ttu-id="c3cf0-114">bota Um ponteiro para um ponteiro para a estrutura [SMAPIFormPropArray](smapiformproparray.md) retornada.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-114">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c3cf0-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c3cf0-115">Return value</span></span>

<span data-ttu-id="c3cf0-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="c3cf0-116">S_OK</span></span> 
  
> <span data-ttu-id="c3cf0-117">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c3cf0-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c3cf0-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c3cf0-119">O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="c3cf0-120">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c3cf0-120">MFCMAPI reference</span></span>

<span data-ttu-id="c3cf0-121">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c3cf0-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="c3cf0-122">**File**</span></span>|<span data-ttu-id="c3cf0-123">**Função**</span><span class="sxs-lookup"><span data-stu-id="c3cf0-123">**Function**</span></span>|<span data-ttu-id="c3cf0-124">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="c3cf0-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c3cf0-125">MFCOutput. cpp</span><span class="sxs-lookup"><span data-stu-id="c3cf0-125">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="c3cf0-126">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="c3cf0-126">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="c3cf0-127">MFCMAPI usa o método **IMAPIFormInfo:: CalcFormPropSet** ao gravar saída de depuração para objetos de informações de formulário.</span><span class="sxs-lookup"><span data-stu-id="c3cf0-127">MFCMAPI uses the **IMAPIFormInfo::CalcFormPropSet** method when writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c3cf0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3cf0-128">See also</span></span>



[<span data-ttu-id="c3cf0-129">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="c3cf0-129">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="c3cf0-130">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c3cf0-130">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="c3cf0-131">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="c3cf0-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

