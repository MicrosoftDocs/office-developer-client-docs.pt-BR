---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e7ba37629ff2198339394448410ffd16477d4766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765455"
---
# <a name="xlasyncreturn"></a><span data-ttu-id="ce34b-103">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="ce34b-103">xlAsyncReturn</span></span>

<span data-ttu-id="ce34b-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ce34b-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ce34b-105">Usado para retornar o resultado de uma função definida pelo usuário assíncrona (UDF).</span><span class="sxs-lookup"><span data-stu-id="ce34b-105">Used to return the result of an asynchronous user-defined function (UDF).</span></span>
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a><span data-ttu-id="ce34b-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="ce34b-106">Parameters</span></span>

<span data-ttu-id="ce34b-107">_pxAsyncHandle_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="ce34b-107">_pxAsyncHandle_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="ce34b-108">O identificador assíncrona do UDF para o qual o resultado é retornado.</span><span class="sxs-lookup"><span data-stu-id="ce34b-108">The asynchronous handle of the UDF to which the result is returned.</span></span>
  
<span data-ttu-id="ce34b-109">_pxFunctionResult_</span><span class="sxs-lookup"><span data-stu-id="ce34b-109">_pxFunctionResult_</span></span>
  
<span data-ttu-id="ce34b-110">O valor de retorno do UDF.</span><span class="sxs-lookup"><span data-stu-id="ce34b-110">The return value of the UDF.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ce34b-111">Propriedade valor/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ce34b-111">Property value/Return value</span></span>

<span data-ttu-id="ce34b-112">Se tiver êxito, retornará **TRUE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="ce34b-112">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="ce34b-113">Se for bem sucedida, retornará **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="ce34b-113">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ce34b-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="ce34b-114">Remarks</span></span>

<span data-ttu-id="ce34b-115">**xlAsyncReturn** é o retorno de chamada somente que Excel permite em segmentos de não-cálculo durante o recálculo.</span><span class="sxs-lookup"><span data-stu-id="ce34b-115">**xlAsyncReturn** is the only callback Excel allows on non-calculation threads during recalculation.</span></span> <span data-ttu-id="ce34b-116">A parte assíncrona de uma UDF assíncrona não deve executar qualquer retornos de chamada que não seja **xlAsyncReturn**.</span><span class="sxs-lookup"><span data-stu-id="ce34b-116">The asynchronous portion of an asynchronous UDF must not perform any callbacks other than **xlAsyncReturn**.</span></span> <span data-ttu-id="ce34b-117">XLL deve liberar memória alocada para manter o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="ce34b-117">The XLL must free memory allocated to hold the return value.</span></span>
  
<span data-ttu-id="ce34b-118">Os parâmetros _pxAsyncHandle_ e _pxFunctionResult_ também podem ser do tipo **xltypeMulti** quando usado para retornar uma matriz de identificadores e os valores correspondentes em um retorno de chamada único.</span><span class="sxs-lookup"><span data-stu-id="ce34b-118">The _pxAsyncHandle_ and  _pxFunctionResult_ parameters can also be of type **xltypeMulti** when used to return an array of handles and corresponding values in a single callback.</span></span> <span data-ttu-id="ce34b-119">Ao usar um único retorno de chamada, passe uma LPXLOPER12 que aponta para XLOPER12 estruturas que contêm um matrizes dimensionais que contêm as alças assíncronas e valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="ce34b-119">When using a single callback, pass an LPXLOPER12 that points to XLOPER12 structures that contain one dimensional arrays that contain the asynchronous handles and return values.</span></span> <span data-ttu-id="ce34b-120">Essas matrizes devem ser na mesma ordem para o Excel corretamente corresponder a um identificador assíncrona com seu valor correspondente.</span><span class="sxs-lookup"><span data-stu-id="ce34b-120">These arrays must be in the same order for Excel to correctly match an asynchronous handle with its corresponding value.</span></span> 
  
<span data-ttu-id="ce34b-121">O exemplo a seguir mostra como você pode fazer com que um lote de chamada usando **xlAsyncReturn**.</span><span class="sxs-lookup"><span data-stu-id="ce34b-121">The following example shows how you can make a batch call using **xlAsyncReturn**.</span></span>
  
```cpp
int batchSize = 10;
    LPXLOPER12 pHandles = new XLOPER12[batchSize];
    LPXLOPER12 pValues = new XLOPER12[batchSize];
    /*Add code to fill in LPXLOPER12 arrays (pHandles and pValues)
    with the XOPER12 structures that contain the asynchronous handles
    and values, in respective order*/
    //Create an XLOPER12 of type xltypeMulti, and fill the Handle array
    XLOPER12 handleArray;
    handleArray.xltype = xltypeMulti;
    handleArray.val.array.rows = 1;
    handleArray.val.array.columns = (COL)batchSize;
    handleArray.val.array.lparray = pHandles;
    
    //Create an XLOPER12 if type xltypeMulti, and fill the Values array
    XLOPER12 valueArray;
    valueArray.xltype = xltypeMulti;
    valueArray.val.array.rows = 1;
    valueArray.val.array.columns = (COL)batchSize;
    valueArray.val.array.lparray = pValues;
    //Make the callback with the return value
    int ret = Excel12(xlAsyncReturn, 0, 2, &amp;handleArray, &amp;valueArray);
    //Add code to free the allocated memory here (pHandles, pValues, valueArray, handleArray)
    return ret;

```

## <a name="see-also"></a><span data-ttu-id="ce34b-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce34b-122">See also</span></span>

- [<span data-ttu-id="ce34b-123">Funções assíncronas definidas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="ce34b-123">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

