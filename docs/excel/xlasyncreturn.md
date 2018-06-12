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
# <a name="xlasyncreturn"></a>xlAsyncReturn

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usado para retornar o resultado de uma função definida pelo usuário assíncrona (UDF).
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>Par�metros

_pxAsyncHandle_ (**xltypeBigData**)
  
O identificador assíncrona do UDF para o qual o resultado é retornado.
  
_pxFunctionResult_
  
O valor de retorno do UDF.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

Se tiver êxito, retornará **TRUE** (**xltypeBool**). Se for bem sucedida, retornará **FALSE**.
  
## <a name="remarks"></a>Coment�rios

**xlAsyncReturn** é o retorno de chamada somente que Excel permite em segmentos de não-cálculo durante o recálculo. A parte assíncrona de uma UDF assíncrona não deve executar qualquer retornos de chamada que não seja **xlAsyncReturn**. XLL deve liberar memória alocada para manter o valor de retorno.
  
Os parâmetros _pxAsyncHandle_ e _pxFunctionResult_ também podem ser do tipo **xltypeMulti** quando usado para retornar uma matriz de identificadores e os valores correspondentes em um retorno de chamada único. Ao usar um único retorno de chamada, passe uma LPXLOPER12 que aponta para XLOPER12 estruturas que contêm um matrizes dimensionais que contêm as alças assíncronas e valores de retorno. Essas matrizes devem ser na mesma ordem para o Excel corretamente corresponder a um identificador assíncrona com seu valor correspondente. 
  
O exemplo a seguir mostra como você pode fazer com que um lote de chamada usando **xlAsyncReturn**.
  
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

## <a name="see-also"></a>Confira também

- [Funções assíncronas definidas pelo usuário](asynchronous-user-defined-functions.md)

