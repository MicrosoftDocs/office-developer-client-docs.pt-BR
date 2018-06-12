---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- função xlfevaluate [excel 2007]
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e468dc18b8f78f56acaa67c2f23dd53254088ad0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765462"
---
# <a name="xlfevaluate"></a>xlfEvaluate

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usa o analisador do Microsoft Excel e do avaliador de função para avaliar qualquer expressão que poderia ser inserido em uma célula da planilha.
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a>Par�metros

 _pxFormulaText (xltypeStr)_
  
A cadeia de caracteres a ser avaliada. Um sinal de igual (=) à esquerda é opcional. A cadeia de caracteres pode ser qualquer texto que legalmente pode ser inserido em uma célula de planilha de planilha ou uma macro.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

Retorna o resultado da avaliação da cadeia de caracteres que pode ser qualquer um dos tipos **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.
  
## <a name="remarks"></a>Coment�rios

A cadeia de caracteres pode conter somente funções, não equivalentes do comando. É equivalente a pressionar **F9** da barra de fórmulas. Se **xlfEvaluate** é chamado de uma função de planilha XLL que foi registrada como thread-safe, a expressão deve conter somente funções thread-safe. 
  
O uso principal da função **xlfEvaluate** é permitir DLLs descobrir o valor atribuído a um nome definido que está em uma planilha ou um nome de oculto definidas dentro da DLL. Observe que dentro de um DLL/XLL, um nome de planilha deve ser prefixado com pelo menos um ponto de exclamação (!) para garantir que ele será interpretado como externa para a DLL. Para obter mais informações, consulte [avaliando nomes e outras expressões da fórmula de planilha](evaluating-names-and-other-worksheet-formula-expressions.md).
  
 **xlfEvaluate** não pode ser usado para avaliar as referências a uma folha de externa que não está aberto. 
  
## <a name="example"></a>Example

Este exemplo usa **xlfEvaluate** para forçar o texto "! B38 "para o conteúdo da célula B38. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Esta função chama uma macro de comando (**xlcAlert**) e funcionará corretamente apenas quando a chamada a partir de uma folha de macro ou como um comando de macro.
  
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

- [Funções de XLM API C essenciais e úteis](essential-and-useful-c-api-xlm-functions.md)

