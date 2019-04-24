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
# <a name="xlasyncreturn"></a>xlAsyncReturn

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usado para retornar o resultado de uma função assíncrona definida pelo usuário (UDF).
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>Parâmetros

_pxAsyncHandle_ (**xltypeBigData**)
  
O identificador assíncrono do UDF para o qual o resultado é retornado.
  
_pxFunctionResult_
  
O valor de retorno do UDF.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Se bem-sucedido, retorna **true** (**xltypeBool**). Se não tiver êxito, retornará **false**.
  
## <a name="remarks"></a>Comentários

**xlAsyncReturn** é o único retorno de chamada que o Excel permite em threads não calculados durante o recálculo. A parte assíncrona de um UDF assíncrono não deve realizar nenhum retorno de chamada diferente de **xlAsyncReturn**. O XLL deve liberar memória alocada para armazenar o valor de retorno.
  
Os parâmetros _pxAsyncHandle_ e _pxFunctionResult_ também podem ser do tipo **xltypeMulti** quando usados para retornar uma matriz de identificadores e valores correspondentes em um único retorno de chamada. Ao usar um único retorno de chamada, passe um LPXLOPER12 que aponta para estruturas XLOPER12 que contêm uma matriz dimensional que contém as alças assíncronas e valores de retorno. Essas matrizes devem estar na mesma ordem para que o Excel coincida corretamente um identificador assíncrono com seu valor correspondente. 
  
O exemplo a seguir mostra como você pode fazer uma chamada em lote usando o **xlAsyncReturn**.
  
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

