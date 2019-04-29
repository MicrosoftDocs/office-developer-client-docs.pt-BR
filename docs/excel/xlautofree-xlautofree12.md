---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- função xlAutoFree [Excel 2007]
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
# <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chamado pelo Microsoft Excel logo após uma função de planilha XLL retornar um **XLOPER**/ **XLOPER12** a ele com um sinalizador definido que diz que há memória que o XLL ainda precisa liberar. Isso permite que a XLL retorne matrizes, cadeias de caracteres e referências externas dinamicamente alocadas para a planilha sem vazamentos de memória. Saiba mais em [Gerenciamento de Memória no Excel](memory-management-in-excel.md).
  
A partir do Excel 2007, a função **xlAutoFree12** e o tipo de dados **XLOPER12** têm suporte. 
  
O Excel não requer que um XLL implemente e exporte uma dessas funções. No enTanto, você deve fazer isso se suas funções XLL retornarem XLOPER ou XLOPER12 que tenha sido alocado dinamicamente ou que contenha ponteiros para memória alocada dinamicamente. Certifique-se de que sua opção de gerenciamento de memória para esses tipos seja consistente em todo o seu XLL e com o modo como você implementou o **xlAutoFree** e o **xlAutoFree12**.
  
Dentro da função **xlAutoFree**/ **xlAutoFree12** , os retornos de chamada no Excel estão desabilitados, com uma exceção: **xlFree** pode ser chamado para liberar memória alocada no Excel. 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a>Parâmetros

 _pxFree_ (**LPXLOPER no caso de xlAutoFree**)
  
 _pxFree_ (**LPXLOPER12 no caso de xlAutoFree12**)
  
Um ponteiro para o **XLOPER** ou **XLOPER12** que tem memória que precisa ser liberada. 
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Essa função não retorna um valor e deve ser declarada como retorno de void.
  
## <a name="remarks"></a>Comentários

Quando o Excel é configurado para usar o recálculo da pasta de trabalho multi-threaded, **xlAutoFree**/ **xlAutoFree12** é chamado no mesmo thread usado para chamar a função que o retornou. A chamada para **xlAutoFree**/ **xlAutoFree12**
é sempre feita antes que as células subseqüentes da planilha sejam avaliadas nesse encadeamento. Isso simplifica o design seguro para thread em sua XLL. 
  
Se a função **xlAutoFree**/ **xlAutoFree12** que você fornecer examinar o campo **xltype** de _pxFree_, lembre-se de que o bit **xlbitDLLFree** ainda será definido. 
  
## <a name="example"></a>Exemplo

 **Exemplo de implementação 1**
  
O primeiro código de `\SAMPLES\EXAMPLE\EXAMPLE.C` demonstra uma implementação muito específica do **xlAutoFree**, que é projetada para funcionar com apenas uma função, **fArray**. Em geral, seu XLL terá mais de apenas uma função que retorna a memória que precisa ser liberada e, nesse caso, uma implementação menos restrita é necessária. 
  
 **Exemplo de implementação 2**
  
O segundo exemplo de implementação é consistente com as pressuposições usadas nos exemplos de criação de **XLOPER12** na seção 1.6.3, Xl12_Str_example, Xl12_Ref_example e xl12_Multi_example. As pressuposições são que, quando o bit **xlbitDLLFree** foi definido, todas as cadeias de caracteres, matriz e memória de referência externa foram alocadas dinamicamente usando **malloc**e, portanto, precisam ser liberadas em uma chamada gratuita.
  
 **Implementação de exemplo 3**
  
O terceiro exemplo de implementação é consistente com um XLL onde funções exportadas que retornam **XLOPER12**s Allocate cadeias de caracteres, referências externas e matrizes que usam **malloc**e onde o próprio **XLOPER12** também é alocado dinamicamente. Retornar um ponteiro para um **XLOPER12** alocado dinamicamente é uma maneira de garantir que a função é thread-safe. 
  
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

