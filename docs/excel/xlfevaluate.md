---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- função xlfevaluate [Excel 2007]
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 527f7e932a41103c374e327a1bd0dd4c7d8e92a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303924"
---
# <a name="xlfevaluate"></a>xlfEvaluate

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usa o Microsoft Excel Parser e o avaliador de função para avaliar qualquer expressão que possa ser inserida em uma célula de planilha.
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a>Parâmetros

 _pxFormulaText (xltypeStr)_
  
A cadeia de caracteres a ser avaliada. Um sinal de igual (=) à esquerda é opcional. A cadeia de caracteres pode ser qualquer texto que possa ser inserido legalmente em uma planilha ou célula de planilha de macro.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Retorna o resultado da avaliação da cadeia de caracteres que pode ser qualquer um dos tipos **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.
  
## <a name="remarks"></a>Comentários

A cadeia de caracteres pode conter apenas funções, não equivalentes de comando. É equivalente a pressionar **F9** da barra de fórmulas. Se **xlfEvaluate** for chamado a partir de uma função de planilha XLL registrada como thread-safe, a expressão deve conter apenas funções thread-safe. 
  
O uso principal da função **xlfEvaluate** é permitir que as DLLs descubram o valor atribuído a um nome definido em uma planilha ou um nome oculto definido dentro da dll. Observe que, em uma DLL/XLL, um nome de planilha deve ser prefixado com pelo menos um ponto de exclamação (!) para garantir que ele seja interpretado como externo à DLL. Para obter mais informações, consulte [avaliar nomes e outras expressões de fórmula de planilha](evaluating-names-and-other-worksheet-formula-expressions.md).
  
 **xlfEvaluate** não pode ser usado para avaliar referências a uma planilha externa que não está aberta. 
  
## <a name="example"></a>Exemplo

Este exemplo usa **xlfEvaluate** para forçar o texto "! B38 "com o conteúdo da célula B38. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Essa função chama uma macro de comando (**xlcAlert**) e funcionará corretamente somente quando for chamado a partir de uma folha de macro ou como um comando de macro.
  
```cs
short WINAPI EvaluateExample(void)
{
    XLOPER12 xFormulaText, xRes, xRes2, xInt;
    xFormulaText.xltype = xltypeStr;
    xFormulaText.val.str = L"\004!B38";
    Excel12(xlfEvaluate, &xRes, 1, (LPXLOPER12)&xFormulaText);
    xInt.xltype = xltypeInt;
    xInt.val.w = 2;
    Excel12(xlcAlert, &xRes2, 2, (LPXLOPER12)&xRes, (LPXLOPER12)&xInt);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes2);
    return 1;
}
```

## <a name="see-also"></a>Confira também

- [Funções XLM essenciais e úteis para a API C](essential-and-useful-c-api-xlm-functions.md)

