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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 362afb1efeddeae72cc19256c377cb2c0f7ecba0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767032"
---
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="5a5d8-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="5a5d8-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="5a5d8-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a5d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a5d8-105">Retorna um ponteiro para o conjunto completo de verbos que usa um formulário.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="5a5d8-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="5a5d8-106">Parameters</span></span>

 <span data-ttu-id="5a5d8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5a5d8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5a5d8-108">[in] Uma bitmask dos sinalizadores que controla o tipo de cadeias de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="5a5d8-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="5a5d8-109">The following flag can be set:</span></span>
    
<span data-ttu-id="5a5d8-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5a5d8-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5a5d8-111">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="5a5d8-112">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="5a5d8-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="5a5d8-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="5a5d8-114">[out] Um ponteiro para um ponteiro para a estrutura [SMAPIVerbArray](smapiverbarray.md) retornado que contém os verbos do formulário.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5a5d8-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5a5d8-115">Return value</span></span>

<span data-ttu-id="5a5d8-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5a5d8-116">S_OK</span></span> 
  
> <span data-ttu-id="5a5d8-117">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="5a5d8-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5a5d8-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5a5d8-119">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5a5d8-120">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="5a5d8-120">Remarks</span></span>

<span data-ttu-id="5a5d8-121">Aplicativos cliente chamam o método **IMAPIFormInfo::CalcVerbSet** para obter um ponteiro para o conjunto de verbos usado por um formulário.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="5a5d8-122">Na estrutura de **SMAPIVerbArray** retornada no parâmetro _ppMAPIVerbArray_ , os verbos são retornados em ordem de número de índice; índice da cada verbo é encontrado na sua lista de membros **lVerb** .</span><span class="sxs-lookup"><span data-stu-id="5a5d8-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="5a5d8-123">Aplicativos cliente podem usar a matriz de verbo para dinamicamente construir menus, ocultar ou Mostrar botões e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5a5d8-124">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5a5d8-124">MFCMAPI reference</span></span>

<span data-ttu-id="5a5d8-125">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5a5d8-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="5a5d8-126">**File**</span></span>|<span data-ttu-id="5a5d8-127">**Function**</span><span class="sxs-lookup"><span data-stu-id="5a5d8-127">**Function**</span></span>|<span data-ttu-id="5a5d8-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="5a5d8-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5a5d8-129">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="5a5d8-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="5a5d8-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="5a5d8-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="5a5d8-131">MFCMAPI usa o método de **IMAPIFormInfo::CalcVerbSet** ao gravar a saída de depuração para os objetos de informações do formulário.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a5d8-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a5d8-132">See also</span></span>



[<span data-ttu-id="5a5d8-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="5a5d8-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="5a5d8-134">IMAPIFormInfo: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5a5d8-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="5a5d8-135">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="5a5d8-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

