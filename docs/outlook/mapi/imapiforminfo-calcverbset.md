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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428778"
---
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="9eaea-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="9eaea-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="9eaea-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9eaea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9eaea-105">Retorna um ponteiro para o conjunto completo de verbos que um formulário usa.</span><span class="sxs-lookup"><span data-stu-id="9eaea-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="9eaea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9eaea-106">Parameters</span></span>

 <span data-ttu-id="9eaea-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9eaea-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9eaea-108">[in] Uma máscara de bits de sinalizadores que controla o tipo de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="9eaea-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="9eaea-109">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="9eaea-109">The following flag can be set:</span></span>
    
<span data-ttu-id="9eaea-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9eaea-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9eaea-111">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="9eaea-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="9eaea-112">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="9eaea-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="9eaea-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="9eaea-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="9eaea-114">[out] Um ponteiro para um ponteiro para a estrutura [SMAPIVerbArray](smapiverbarray.md) retornada que contém os verbos do formulário.</span><span class="sxs-lookup"><span data-stu-id="9eaea-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9eaea-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9eaea-115">Return value</span></span>

<span data-ttu-id="9eaea-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="9eaea-116">S_OK</span></span> 
  
> <span data-ttu-id="9eaea-117">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="9eaea-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="9eaea-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9eaea-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9eaea-119">O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.</span><span class="sxs-lookup"><span data-stu-id="9eaea-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9eaea-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9eaea-120">Remarks</span></span>

<span data-ttu-id="9eaea-121">Os aplicativos cliente chamam o método **IMAPIFormInfo::CalcVerbSet** para obter um ponteiro para o conjunto de verbos usados por um formulário.</span><span class="sxs-lookup"><span data-stu-id="9eaea-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="9eaea-122">Na estrutura **SMAPIVerbArray** retornada no parâmetro _ppMAPIVerbArray,_ os verbos são retornados na ordem do número de índice; o índice de cada verbo é encontrado em seu **membro lVerb.**</span><span class="sxs-lookup"><span data-stu-id="9eaea-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="9eaea-123">Os aplicativos cliente podem usar a matriz de verbos para criar menus dinamicamente, ocultar ou mostrar botões e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9eaea-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9eaea-124">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9eaea-124">MFCMAPI reference</span></span>

<span data-ttu-id="9eaea-125">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9eaea-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9eaea-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="9eaea-126">**File**</span></span>|<span data-ttu-id="9eaea-127">**Função**</span><span class="sxs-lookup"><span data-stu-id="9eaea-127">**Function**</span></span>|<span data-ttu-id="9eaea-128">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="9eaea-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9eaea-129">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="9eaea-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="9eaea-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="9eaea-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="9eaea-131">MFCMAPI usa o **método IMAPIFormInfo::CalcVerbSet** ao escrever a saída de depuração para objetos de informações de formulário.</span><span class="sxs-lookup"><span data-stu-id="9eaea-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9eaea-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="9eaea-132">See also</span></span>



[<span data-ttu-id="9eaea-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="9eaea-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="9eaea-134">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9eaea-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="9eaea-135">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="9eaea-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

