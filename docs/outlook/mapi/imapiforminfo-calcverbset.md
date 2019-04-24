---
title: IMAPIFormInfoCalcVerbSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: babff746af16d51ca154d049943f6be7e9fab589
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321686"
---
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="b55f3-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="b55f3-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="b55f3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b55f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b55f3-105">Retorna um ponteiro para o conjunto completo de verbos que um formulário usa.</span><span class="sxs-lookup"><span data-stu-id="b55f3-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="b55f3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b55f3-106">Parameters</span></span>

 <span data-ttu-id="b55f3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b55f3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b55f3-108">no Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="b55f3-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="b55f3-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="b55f3-109">The following flag can be set:</span></span>
    
<span data-ttu-id="b55f3-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b55f3-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b55f3-111">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="b55f3-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="b55f3-112">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="b55f3-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="b55f3-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="b55f3-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="b55f3-114">bota Um ponteiro para um ponteiro para a estrutura [SMAPIVerbArray](smapiverbarray.md) retornada que contém os verbos do formulário.</span><span class="sxs-lookup"><span data-stu-id="b55f3-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b55f3-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b55f3-115">Return value</span></span>

<span data-ttu-id="b55f3-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b55f3-116">S_OK</span></span> 
  
> <span data-ttu-id="b55f3-117">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="b55f3-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b55f3-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b55f3-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b55f3-119">O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.</span><span class="sxs-lookup"><span data-stu-id="b55f3-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b55f3-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b55f3-120">Remarks</span></span>

<span data-ttu-id="b55f3-121">Os aplicativos cliente chamam o método **IMAPIFormInfo:: CalcVerbSet** para obter um ponteiro para o conjunto de verbos usados por um formulário.</span><span class="sxs-lookup"><span data-stu-id="b55f3-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="b55f3-122">Na estrutura **SMAPIVerbArray** retornada no parâmetro _ppMAPIVerbArray_ , os verbos são retornados em ordem de número de índice; cada índice de verbo é encontrado no seu membro **lVerb** .</span><span class="sxs-lookup"><span data-stu-id="b55f3-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="b55f3-123">Os aplicativos cliente podem usar a matriz de verbo para criar menus dinamicamente, ocultar ou Mostrar botões e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b55f3-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b55f3-124">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b55f3-124">MFCMAPI reference</span></span>

<span data-ttu-id="b55f3-125">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b55f3-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b55f3-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b55f3-126">**File**</span></span>|<span data-ttu-id="b55f3-127">**Função**</span><span class="sxs-lookup"><span data-stu-id="b55f3-127">**Function**</span></span>|<span data-ttu-id="b55f3-128">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="b55f3-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b55f3-129">MFCOutput. cpp</span><span class="sxs-lookup"><span data-stu-id="b55f3-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="b55f3-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="b55f3-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="b55f3-131">MFCMAPI usa o método **IMAPIFormInfo:: CalcVerbSet** durante a gravação da saída de depuração para objetos de informações de formulário.</span><span class="sxs-lookup"><span data-stu-id="b55f3-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b55f3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b55f3-132">See also</span></span>



[<span data-ttu-id="b55f3-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="b55f3-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="b55f3-134">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b55f3-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="b55f3-135">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b55f3-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

