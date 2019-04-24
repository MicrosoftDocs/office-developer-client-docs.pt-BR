---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 32d5075af34cda9753c5d082bd4ab00afab1ecff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310245"
---
# <a name="xlasyncreturn"></a><span data-ttu-id="a7937-103">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="a7937-103">xlAsyncReturn</span></span>

<span data-ttu-id="a7937-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a7937-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a7937-105">Usado para retornar o resultado de uma função assíncrona definida pelo usuário (UDF).</span><span class="sxs-lookup"><span data-stu-id="a7937-105">Used to return the result of an asynchronous user-defined function (UDF).</span></span>
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a><span data-ttu-id="a7937-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7937-106">Parameters</span></span>

<span data-ttu-id="a7937-107">_pxAsyncHandle_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="a7937-107">_pxAsyncHandle_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="a7937-108">O identificador assíncrono do UDF para o qual o resultado é retornado.</span><span class="sxs-lookup"><span data-stu-id="a7937-108">The asynchronous handle of the UDF to which the result is returned.</span></span>
  
<span data-ttu-id="a7937-109">_pxFunctionResult_</span><span class="sxs-lookup"><span data-stu-id="a7937-109">_pxFunctionResult_</span></span>
  
<span data-ttu-id="a7937-110">O valor de retorno do UDF.</span><span class="sxs-lookup"><span data-stu-id="a7937-110">The return value of the UDF.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a7937-111">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a7937-111">Property value/Return value</span></span>

<span data-ttu-id="a7937-112">Se bem-sucedido, retorna **true** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="a7937-112">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="a7937-113">Se não tiver êxito, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="a7937-113">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a7937-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7937-114">Remarks</span></span>

<span data-ttu-id="a7937-115">**xlAsyncReturn** é o único retorno de chamada que o Excel permite em threads não calculados durante o recálculo.</span><span class="sxs-lookup"><span data-stu-id="a7937-115">**xlAsyncReturn** is the only callback Excel allows on non-calculation threads during recalculation.</span></span> <span data-ttu-id="a7937-116">A parte assíncrona de um UDF assíncrono não deve realizar nenhum retorno de chamada diferente de **xlAsyncReturn**.</span><span class="sxs-lookup"><span data-stu-id="a7937-116">The asynchronous portion of an asynchronous UDF must not perform any callbacks other than **xlAsyncReturn**.</span></span> <span data-ttu-id="a7937-117">O XLL deve liberar memória alocada para armazenar o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a7937-117">The XLL must free memory allocated to hold the return value.</span></span>
  
<span data-ttu-id="a7937-118">Os parâmetros _pxAsyncHandle_ e _pxFunctionResult_ também podem ser do tipo **xltypeMulti** quando usados para retornar uma matriz de identificadores e valores correspondentes em um único retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="a7937-118">The _pxAsyncHandle_ and  _pxFunctionResult_ parameters can also be of type **xltypeMulti** when used to return an array of handles and corresponding values in a single callback.</span></span> <span data-ttu-id="a7937-119">Ao usar um único retorno de chamada, passe um LPXLOPER12 que aponta para estruturas XLOPER12 que contêm uma matriz dimensional que contém as alças assíncronas e valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="a7937-119">When using a single callback, pass an LPXLOPER12 that points to XLOPER12 structures that contain one dimensional arrays that contain the asynchronous handles and return values.</span></span> <span data-ttu-id="a7937-120">Essas matrizes devem estar na mesma ordem para que o Excel coincida corretamente um identificador assíncrono com seu valor correspondente.</span><span class="sxs-lookup"><span data-stu-id="a7937-120">These arrays must be in the same order for Excel to correctly match an asynchronous handle with its corresponding value.</span></span> 
  
<span data-ttu-id="a7937-121">O exemplo a seguir mostra como você pode fazer uma chamada em lote usando o **xlAsyncReturn**.</span><span class="sxs-lookup"><span data-stu-id="a7937-121">The following example shows how you can make a batch call using **xlAsyncReturn**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="a7937-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7937-122">See also</span></span>

- [<span data-ttu-id="a7937-123">Funções assíncronas definidas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="a7937-123">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

