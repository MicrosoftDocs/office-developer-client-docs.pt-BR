---
title: Avaliar nomes e outras expressões de fórmula de planilha
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- avaliação de expressão [excel 2007],planilhas [Excel 2007], avaliação de nome, avaliação de expressões [Excel 2007], avaliação de nomes de planilha [Excel 2007],expressões [Excel 2007], avaliação, nomes [Excel 2007], avaliação, avaliação de nome [Excel 2007],cadeias de caracteres [Excel 2007], conversão em valores,função xlfEvaluate [Excel 2007],planilhas [Excel 2007], avaliação de expressão
localization_priority: Normal
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97328cbc57a9144a133524774e3be10a84a96bf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406861"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a>Avaliar nomes e outras expressões de fórmula de planilha

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Um dos recursos mais importantes que o Excel expõe por meio da API de C é a capacidade de converter qualquer fórmula de cadeia de caracteres que possa ser inserida legalmente em uma planilha em um valor ou em uma matriz de valores. Isso é essencial para funções e comandos XLL que devem ler o conteúdo de nomes definidos, por exemplo. Essa capacidade é exposta por meio [da função xlfEvaluate](xlfevaluate.md), conforme mostrado neste exemplo.
  
```C
int WINAPI evaluate_name_example(void)
{
  wchar_t *expression = L"\016!MyDefinedName";
  XLOPER12 xNameText, xNameValue;
  xNameText.xltype = xltypeStr;
  xNameText.val.str = expression;
// Try to evaluate the name. Will fail with a #NAME? error
// if MyDefinedName is not defined in the active workbook.
  Excel12(xlfEvaluate, &xNameValue, 1, &xNameText);
// Attempt to convert the value to a string and display it in
// an alert dialog. This fails if xNameValue is an error value.
  Excel12(xlcAlert, 0, 1, &xNameValue);
// Must free xNameValue in case MyDefinedName evaluated to a string
  Excel12(xlFree, 0, 1, &xNameValue);
  return 1;
}
```

Observe que, ao avaliar um nome de planilha, por conta própria ou em uma fórmula, você deve prefixar o nome com '!', pelo menos. Caso contrário, o Excel tentará encontrar o nome em um namespace oculto reservado para DLLs. Você pode criar e excluir nomes DLL ocultos usando a [função xlfSetName](xlfsetname.md). Você pode obter a definição de qualquer nome definido, seja um nome DLL oculto ou um nome de planilha, usando a função **xlfGetDef.** 
  
A especificação completa de um nome de planilha tem o seguinte formato:
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Observe que o Excel 2007 introduziu várias novas extensões de arquivo. Você pode omitir o caminho, o nome da pasta de trabalho e o nome da planilha onde não há ambiguidade entre as planilhas abertas nesta sessão do Excel. 
  
O próximo exemplo avalia a fórmula  `COUNT(A1:IV65536)` da planilha ativa e exibe o resultado. Observe a necessidade de prefixar o endereço do intervalo com '!', que é consistente com a convenção de referência de intervalo em folhas de macro XLM. O XLM da API de C segue esta convenção: 
  
- `=A1` Uma referência à célula A1 na folha de macro atual. (Não definido para XLLs). 
  
- `=!A1` Uma referência à célula A1 da planilha ativa (que pode ser uma planilha ou uma folha de macro) 
  
- `=Sheet1!A1` Uma referência à célula A1 na planilha especificada, Sheet1 neste caso. 
  
- `=[Book1.xls]Sheet1!A1` Uma referência à célula A1 na planilha especificada na pasta de trabalho especificada. 
  
Em um XLL, uma referência sem um ponto de exclamação à frente (**!**) não pode ser convertida em um valor. Isso não tem significado porque não há uma folha de macro atual. Observe que um sinal de igual à parte ( ) é **=** opcional e é omitido no próximo exemplo.
  
```C
int WINAPI evaluate_expression_example(void)
{
    wchar_t *expression = L"\022COUNT(!A1:IV65536)";
    XLOPER12 xExprText, xExprValue;
    xExprText.xltype = xltypeStr;
    xExprText.val.str = expression;
// Try to evaluate the formula.
    Excel12(xlfEvaluate, &xExprValue, 1, &xExprText);
// Attempt to convert the value to a string and display it in
// an alert dialog. Will fail if xExprValue is an error.
    Excel12(xlcAlert, 0, 1, &xExprValue);
// Not strictly necessary, as COUNT never returns a string
// but does no harm.
    Excel12(xlFree, 0, 1, &xExprValue);
    return 1;
}
```

Você também pode usar a função **xlfEvaluate** para recuperar a ID de registro de uma função XLL de seu nome registrado, que pode ser usado para chamar essa função usando a função [xlUDF](xludf.md).
  
> [!NOTE]
> O nome registrado pode ser passado diretamente para a **função xlUDF.** Isso significa que você pode evitar ter que avaliar o nome para obter a ID antes de chamar **xlUDF**. No entanto, se a função for chamada várias vezes, chamá-la usando a ID de registro será mais rápida. 
  
## <a name="see-also"></a>Confira também

- [Avaliação de expressões e planilhas do Excel](excel-worksheet-and-expression-evaluation.md)
- [Permitir intervenções de usuário em operações demoradas](permitting-user-breaks-in-lengthy-operations.md)
- [Introdução ao Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

