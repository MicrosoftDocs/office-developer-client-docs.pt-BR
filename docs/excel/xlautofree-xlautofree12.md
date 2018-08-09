---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- função xlAutoFree [excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2d2b8e60b484ba8156acc80d543493e3ec9c564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765459"
---
# <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chamado pelo Microsoft Excel logo depois que uma função de planilha XLL retorna **XLOPER**/ **XLOPER12** a ela com um sinalizador definido que ele informa a memória que o XLL precisa release. Isso permite que o XLL retornar alocadas dinamicamente matrizes, cadeias de caracteres e as referências externas à planilha sem vazamento de memória. Para saber mais, consulte [Memory Management in Excel](memory-management-in-excel.md).
  
Iniciando no Excel 2007, a função **xlAutoFree12** e o tipo de dados **XLOPER12** são suportadas. 
  
Excel não exige um XLL implementar e exportar qualquer uma dessas funções. No entanto, você deve fazer isso se suas funções XLL retornam um XLOPER ou XLOPER12 que alocadas dinamicamente ou que contém ponteiros para memória alocada dinamicamente. Certifique-se de que sua escolha de como gerenciar memória para esses tipos é consistente em toda a sua XLL e com como você implementou **xlAutoFree** e **xlAutoFree12**.
  
Dentro do **xlAutoFree**/ **xlAutoFree12** função, retornos de chamada para o Excel estiver desabilitado, com uma exceção: **xlFree** pode ser chamado para liberar memória alocada para Excel. 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a>Parâmetros

 _pxFree_ (**LPXLOPER no caso de xlAutoFree**)
  
 _pxFree_ (**LPXLOPER12 no caso de xlAutoFree12**)
  
Um ponteiro para o **XLOPER** ou **XLOPER12** com memória que precisa ser liberado. 
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Essa função não retorna um valor e deve ser declarada como retornando void.
  
## <a name="remarks"></a>Comentários

Quando o Excel está configurado para usar o recálculo de pasta de trabalho multithreaded, **xlAutoFree**/ **xlAutoFree12** é chamado no mesmo thread usado para chamar a função que retornados a ele. A chamada para **xlAutoFree**/ **xlAutoFree12** sempre é feita antes de alguma célula da planilha subsequentes é avaliada naquele segmento. Isso simplifica o design de thread-safe em seu XLL. 
  
Se o **xlAutoFree**/ função**xlAutoFree12** fornecidas por você observa o campo **xltype** de _pxFree_, lembre-se de que o bit **xlbitDLLFree** ainda será definido. 
  
## <a name="example"></a>Exemplo

 **Implementação de exemplo 1**
  
O primeiro código de `\SAMPLES\EXAMPLE\EXAMPLE.C` demonstra uma implementação muito específica do **xlAutoFree**, que é projetado para funcionar com apenas uma função, **fArray**. Em geral, seu XLL terá mais de apenas uma função retornando memória que precisa ser liberado, caso em que uma implementação menos restritivas é necessária. 
  
 **Implementação de exemplo 2**
  
O segundo exemplo de implementação é consistente com as suposições usadas nos exemplos de criação de **XLOPER12** na seção 1.6.3, xl12_Str_example, xl12_Ref_example e xl12_Multi_example. As suposições são que, quando estará definido o bit **xlbitDLLFree** tiver sido definido, todas as string, matriz e memória referência externa tenha sido alocada dinamicamente usando **malloc**e, portanto, precisa ser liberada em uma chamada para liberar.
  
 **Implementação de exemplo 3**
  
Implementação de exemplo do terceira é consistente com um XLL onde exportadas funções que retornam **XLOPER12**s alocar as cadeias de caracteres, as referências externas e matrizes usando **malloc**e onde **XLOPER12** propriamente dito é alocado também dinamicamente. Retornando um ponteiro para um alocadas dinamicamente **XLOPER12** é uma maneira de garantir que a função é thread-safe. 
  
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

## <a name="see-also"></a>Confira também



[Gerenciador de Suplemento e Funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)

