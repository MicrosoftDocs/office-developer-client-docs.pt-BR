---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- função xlautofree [excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3dfba5ae98b0635c95308eac01bf2f10867678e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413287"
---
# <a name="xlautofreexlautofree12"></a><span data-ttu-id="888a7-104">xlAutoFree/xlAutoFree12</span><span class="sxs-lookup"><span data-stu-id="888a7-104">xlAutoFree/xlAutoFree12</span></span>

 <span data-ttu-id="888a7-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="888a7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="888a7-106">Chamado pelo Microsoft Excel logo após uma função de planilha XLL retornar um /  **XLOPER XLOPER12** para ele com um conjunto de sinalizadores que informa que há memória que o XLL ainda precisa liberar.</span><span class="sxs-lookup"><span data-stu-id="888a7-106">Called by Microsoft Excel just after an XLL worksheet function returns an **XLOPER**/ **XLOPER12** to it with a flag set that tells it there is memory that the XLL still needs to release.</span></span> <span data-ttu-id="888a7-107">Isso permite que a XLL retorne matrizes, cadeias de caracteres e referências externas dinamicamente alocadas para a planilha sem vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="888a7-107">This enables the XLL to return dynamically allocated arrays, strings, and external references to the worksheet without memory leaks.</span></span> <span data-ttu-id="888a7-108">Saiba mais em [Gerenciamento de Memória no Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="888a7-108">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="888a7-109">A partir do Excel 2007, há suporte para a função **xlAutoFree12** e o tipo de dados **XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="888a7-109">Starting in Excel 2007, the **xlAutoFree12** function and the **XLOPER12** data type are supported.</span></span> 
  
<span data-ttu-id="888a7-110">O Excel não exige um XLL para implementar e exportar qualquer uma dessas funções.</span><span class="sxs-lookup"><span data-stu-id="888a7-110">Excel does not require an XLL to implement and export either of these functions.</span></span> <span data-ttu-id="888a7-111">No entanto, você deverá fazer isso se suas funções XLL retornarem um XLOPER ou XLOPER12 que tenha sido alocado dinamicamente ou que contenha ponteiros para memória alocada dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="888a7-111">However, you must do so if your XLL functions return an XLOPER or XLOPER12 that has been dynamically allocated or that contains pointers to dynamically allocated memory.</span></span> <span data-ttu-id="888a7-112">Certifique-se de que sua escolha de como gerenciar a memória para esses tipos seja consistente em todo o XLL e com a maneira como você implementou **xlAutoFree** e **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="888a7-112">Ensure that your choice of how to manage memory for these types is consistent throughout your XLL and with how you implemented **xlAutoFree** and **xlAutoFree12**.</span></span>
  
<span data-ttu-id="888a7-113">Dentro da **função xlAutoFree** /  **xlAutoFree12,** os retornos de chamada no Excel são desabilitados, com uma exceção: **xlFree** pode ser chamado para liberar memória alocada no Excel.</span><span class="sxs-lookup"><span data-stu-id="888a7-113">Inside the **xlAutoFree**/ **xlAutoFree12** function, callbacks into Excel are disabled, with one exception: **xlFree** can be called to free Excel-allocated memory.</span></span> 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a><span data-ttu-id="888a7-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="888a7-114">Parameters</span></span>

 <span data-ttu-id="888a7-115">_pxFree_ (**LPXLOPER no caso de xlAutoFree**)</span><span class="sxs-lookup"><span data-stu-id="888a7-115">_pxFree_ (**LPXLOPER in the case of xlAutoFree**)</span></span>
  
 <span data-ttu-id="888a7-116">_pxFree_ (**LPXLOPER12 no caso de xlAutoFree12**)</span><span class="sxs-lookup"><span data-stu-id="888a7-116">_pxFree_ (**LPXLOPER12 in the case of xlAutoFree12**)</span></span>
  
<span data-ttu-id="888a7-117">Um ponteiro para **o XLOPER ou** **o XLOPER12** que tem memória que precisa ser liberada.</span><span class="sxs-lookup"><span data-stu-id="888a7-117">A pointer to the **XLOPER** or the **XLOPER12** that has memory that needs to be freed.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="888a7-118">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="888a7-118">Property value/Return value</span></span>

<span data-ttu-id="888a7-119">Esta função não retorna um valor e deve ser declarada como retornando nulo.</span><span class="sxs-lookup"><span data-stu-id="888a7-119">This function does not return a value and should be declared as returning void.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="888a7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="888a7-120">Remarks</span></span>

<span data-ttu-id="888a7-121">Quando o Excel é configurado para usar o recálculo de planilha com vários threads, **xlAutoFree** /  **xlAutoFree12** é chamado no mesmo thread usado para chamar a função que a retornou.</span><span class="sxs-lookup"><span data-stu-id="888a7-121">When Excel is configured to use multithreaded workbook recalculation, **xlAutoFree**/ **xlAutoFree12** is called on the same thread used to call the function that returned it.</span></span> <span data-ttu-id="888a7-122">A chamada para **xlAutoFree**/ **xlAutoFree12**
é sempre feita antes que as células subseqüentes da planilha sejam avaliadas nesse encadeamento.</span><span class="sxs-lookup"><span data-stu-id="888a7-122">The call to **xlAutoFree**/ **xlAutoFree12** is always made before any subsequent worksheet cells are evaluated on that thread.</span></span> <span data-ttu-id="888a7-123">Isso simplifica o design seguro para thread em sua XLL.</span><span class="sxs-lookup"><span data-stu-id="888a7-123">This simplifies thread-safe design in your XLL.</span></span> 
  
<span data-ttu-id="888a7-124">Se a **função xlAutoFree** /  **xlAutoFree12** que você fornece analisa o campo **xltype** de _pxFree_, lembre-se de que o bit **xlbitDLLFree** ainda será definido.</span><span class="sxs-lookup"><span data-stu-id="888a7-124">If the **xlAutoFree**/ **xlAutoFree12** function you provide looks at the **xltype** field of  _pxFree_, remember that the **xlbitDLLFree** bit will still be set.</span></span> 
  
## <a name="example"></a><span data-ttu-id="888a7-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="888a7-125">Example</span></span>

 <span data-ttu-id="888a7-126">**Exemplo de implementação 1**</span><span class="sxs-lookup"><span data-stu-id="888a7-126">**Example Implementation 1**</span></span>
  
<span data-ttu-id="888a7-127">O primeiro código de demonstra uma implementação muito específica de xlAutoFree , que é projetado para funcionar com apenas uma `\SAMPLES\EXAMPLE\EXAMPLE.C` função, **fArray**. </span><span class="sxs-lookup"><span data-stu-id="888a7-127">The first code from  `\SAMPLES\EXAMPLE\EXAMPLE.C` demonstrates a very specific implementation of **xlAutoFree**, which is designed to work with just one function, **fArray**.</span></span> <span data-ttu-id="888a7-128">Em geral, seu XLL terá mais de uma função retornando memória que precisa ser liberada; nesse caso, uma implementação menos restrita é necessária.</span><span class="sxs-lookup"><span data-stu-id="888a7-128">In general, your XLL will have more than just one function returning memory that needs to be freed, in which case a less restricted implementation is required.</span></span> 
  
 <span data-ttu-id="888a7-129">**Exemplo de implementação 2**</span><span class="sxs-lookup"><span data-stu-id="888a7-129">**Example implementation 2**</span></span>
  
<span data-ttu-id="888a7-130">O segundo exemplo de implementação é consistente com as suposições usadas nos exemplos de criação **XLOPER12** na seção 1.6.3, xl12_Str_example, xl12_Ref_example e xl12_Multi_example.</span><span class="sxs-lookup"><span data-stu-id="888a7-130">The second example implementation is consistent with the assumptions used in the **XLOPER12** creation examples in section 1.6.3, xl12_Str_example, xl12_Ref_example, and xl12_Multi_example.</span></span> <span data-ttu-id="888a7-131">As suposições são de que, quando o bit **xlbitDLLFree** foi definido, toda a cadeia de caracteres, matriz e memória de referência externa foi alocada dinamicamente usando **malloc** e, portanto, precisa ser liberado em uma chamada para liberar.</span><span class="sxs-lookup"><span data-stu-id="888a7-131">The assumptions are that, when the **xlbitDLLFree** bit has been set, all string, array, and external reference memory has been dynamically allocated using **malloc**, and so needs to be freed in a call to free.</span></span>
  
 <span data-ttu-id="888a7-132">**Exemplo de implementação 3**</span><span class="sxs-lookup"><span data-stu-id="888a7-132">**Example implementation 3**</span></span>
  
<span data-ttu-id="888a7-133">O terceiro exemplo de implementação é consistente com um XLL onde as funções exportadas que retornam **xlOPER12** s alocam cadeias de caracteres, referências externas e matrizes usando **malloc**, e onde o **próprio XLOPER12** também é alocado dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="888a7-133">The third example implementation is consistent with an XLL where exported functions that return **XLOPER12** s allocate strings, external references and arrays using **malloc**, and where the **XLOPER12** itself is also dynamically allocated.</span></span> <span data-ttu-id="888a7-134">Retornar um ponteiro para um **XLOPER12** alocado dinamicamente é uma maneira de garantir que a função seja thread-safe.</span><span class="sxs-lookup"><span data-stu-id="888a7-134">Returning a pointer to a dynamically allocated **XLOPER12** is one way to ensure that the function is thread safe.</span></span> 
  
```cs
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 1
//////////////////////////////////////////
LPXLOPER12 WINAPI fArray(void)
{
    LPXLOPER12 pxArray;
    static XLOPER12 xMulti;
    int i;
    int rwcol;
    xMulti.xltype = xltypeMulti | xlbitDLLFree;
    xMulti.val.array.columns = 1;
    xMulti.val.array.rows = 8;
    // For large values of rows and columns, this would overflow
    // use __int64 in that case and return an error if rwcol
    // contains a number that won't fit in sizeof(int) bytes
    rwcol = xMulti.val.array.columns * xMulti.val.array.rows; 
    pxArray = (LPXLOPER12)GlobalLock(hArray = GlobalAlloc(GMEM_ZEROINIT, rwcol * sizeof(XLOPER12)));
    xMulti.val.array.lparray = pxArray;
    for(i = 0; i < rwcol; i++) 
    {
        pxArray[i].xltype = xltypeInt;
        pxArray[i].val.w = i;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe, use alternate memory allocation mechanisms
    return (LPXLOPER12)&xMulti;
}
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    GlobalUnlock(hArray);
    GlobalFree(hArray);
    return;
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 2
//////////////////////////////////////////
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
/* Assume all string elements were allocated using malloc, and
** need to be freed using free.  Then free the array itself.
*/
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 3
//////////////////////////////////////////
LPXLOPER12 WINAPI example_xll_function(LPXLOPER12 pxArg)
{
// Thread-safe return value. Every invocation of this function
// gets its own piece of memory.
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
// Initialize to a safe default
    pxRtnValue->xltype = xltypeNil;
// Set the value of pxRtnValue making sure that strings, external
// references, arrays, and strings within arrays are all dynamically
// allocated using malloc.
//    (code omitted)
//    ...
// Set xlbitDLLFree regardless of the type of the return value to
// ensure xlAutoFree12 is called and pxRtnValue is freed.
    pxRtnValue->xltype |= xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
// Assume all string elements were allocated using malloc, and
// need to be freed using free. Then free the array itself.
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
// Assume pxFree was itself dynamically allocated using malloc.
    free(pxFree);
}
```

## <a name="see-also"></a><span data-ttu-id="888a7-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="888a7-135">See also</span></span>



[<span data-ttu-id="888a7-136">Gerenciador de Suplemento e Funções da Interface XLL</span><span class="sxs-lookup"><span data-stu-id="888a7-136">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

