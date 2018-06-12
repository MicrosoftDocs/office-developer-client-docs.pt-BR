---
title: Avaliando os nomes e outras expressões de fórmula de planilha
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- avaliação da expressão [excel 2007], planilhas [Excel 2007], avaliação de nome, avaliando expressões [Excel 2007], avaliando os nomes de planilha [Excel 2007], expressões [Excel 2007], avaliando, nomes [Excel 2007], avaliando, nomeie avaliação [Excel 2007] , cadeias de caracteres [Excel 2007], convertendo em valores, a função de xlfEvaluate [Excel 2007], planilhas [Excel 2007], avaliação de expressão
localization_priority: Normal
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9d726d89c859e2f7428b459971d5d13586f144e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765288"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a>Avaliando os nomes e outras expressões de fórmula de planilha

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Um dos recursos mais importantes que expõe do Excel por meio da API C é a capacidade de converter qualquer fórmula de cadeia de caracteres que pode ser inserida legalmente em uma planilha para um valor, ou uma matriz de valores. Isso é essencial para funções XLL e comandos que devem ler o conteúdo de nomes definidos, por exemplo. Essa capacidade é exposta por meio da [função xlfEvaluate](xlfevaluate.md), conforme mostrado neste exemplo.
  
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

Observe que, quando você está avaliando um nome da planilha, por conta própria ou em uma fórmula, você deve prefixo o nome com '!', pelo menos. Caso contrário, o Excel tenta localizar o nome em um namespace oculto reservada para DLLs. Você pode criar e excluir nomes DLL ocultos usando a [função xlfSetName](xlfsetname.md). Você pode obter a definição de qualquer nome definido, se ele é um nome DLL oculto ou uma planilha, usando a função **xlfGetDef** . 
  
A especificação completa para um nome de planilha possui o seguinte formato:
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Observe que o Excel 2007 introduziu um número de novas extensões de arquivo. Você pode omitir o caminho, o nome da pasta de trabalho e o nome da planilha onde não há nenhum ambiguidade entre as pastas de trabalho abertas nesta sessão do Excel. 
  
O próximo exemplo avalia a fórmula `COUNT(A1:IV65536)` para a planilha ativa e exibe o resultado. Observe a necessidade de prefixo o endereço do intervalo com '!', que é consistente com a convenção de referência de intervalo em folhas de macro XLM. A C API XLM segue esta convenção: 
  
- `=A1`Uma referência à célula A1 na folha de macro atual. (Não definido para XLLs). 
  
- `=!A1`Uma referência à célula A1 na planilha ativa (que pode ser uma planilha ou folha de macro) 
  
- `=Sheet1!A1`Uma referência para a célula A1 na planilha especificada, Sheet1 nesse caso. 
  
- `=[Book1.xls]Sheet1!A1`Uma referência à célula A1 na planilha especificada na pasta de trabalho especificada. 
  
Em um XLL, uma referência sem um ponto de exclamação líder (**!**) não pode ser convertida para um valor. Ele tem nenhum significado porque não há nenhuma folha de macro atual. Observe que um líder do sinal de igual (**=**) é opcional e é omitido no próximo exemplo.
  
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

Você também pode usar a função **xlfEvaluate** para recuperar a ID de registro de uma função XLL do seu nome registrado, que pode ser usado para chamar essa função usando a [função xlUDF](xludf.md).
  
> [!NOTE]
> O nome registrado pode ser passado diretamente para a função **xlUDF** . Isso significa que você pode evitar a necessidade de avaliar o nome para obter o ID antes de chamar **xlUDF**. No entanto, se a função deve ser chamado muitas vezes, chamá-lo usando o registro que ID é mais rápido. 
  
## <a name="see-also"></a>Confira também

- [Planilha do Excel e avaliação de expressão](excel-worksheet-and-expression-evaluation.md)
- [Quebras de autorizações de usuário em operações demoradas](permitting-user-breaks-in-lengthy-operations.md)
- [Getting Started with the Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

