---
title: Problemas conhecidos no desenvolvimento de XLL do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- problemas conhecidos [excel 2007]
localization_priority: Normal
ms.assetid: 3dfecc0b-a91c-448e-8721-5d3486b625fa
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9cdbb10ea68723bd7e1cd9289e8592a7cc087c46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765379"
---
# <a name="known-issues-in-excel-xll-development"></a>Problemas conhecidos no desenvolvimento de XLL do Excel

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Este tópico descreve os problemas conhecidos do Microsoft Excel que podem ser encontrados no desenvolvimento de XLL.
  
## <a name="unregistering-xll-commands-and-functions"></a>Cancelando o registro dos comandos XLL e funções

Quando um XLL registra uma função ou comando, o Excel cria um novo nome para o recurso e associa uma referência para a função DLL com esse nome. O nome será obtido do quarto argumento, *pxFunctionText* , da função [xlfRegister](xlfregister-form-1.md) . Esse nome é oculto as caixas de diálogo normal para gerenciar os nomes de planilha. Para cancelar o registro de um comando ou uma função, você deve excluir o nome por usando a função [xlfSetName](xlfsetname.md) , passando o nome, mas não passando uma definição. No entanto, um bug impede que isso removendo o nome das listas Assistente de função. 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a>Truncamento de cadeia de caracteres de descrição do argumento no Assistente de função

O parâmetro *pxArgumentHelp1* e todos os parâmetros subsequentes da função **xlfRegister** são cadeias de caracteres opcionais que correspondem aos argumentos da função XLL. O Assistente de função exibe essas para fornecer ajuda na caixa de diálogo do argumento construção. Em alguns casos, o Excel trunca a cadeia de caracteres que corresponde ao argumento final por um ou dois caracteres quando exibi-las na caixa de diálogo. Você pode evitar isso adicionando um ou dois espaços até o final da cadeia de caracteres final. 
  
## <a name="binary-name-scope-limitation"></a>Limitação de escopo de nome binário

Nomes de binários e seus dados podem ser recuperados somente quando a planilha que estava ativa no momento em que eles foram criados novamente está ativa. Porque as funções de planilha não é possível ativar planilhas em uma pasta de trabalho (somente comandos podem fazer isso), aplicativos de nomes binários são muito limitados. Por exemplo, se você tiver um comando que é invocado somente de uma determinada planilha, você poderá usar um nome binário para armazenar dados relacionados ao comando.
  
## <a name="xlset-and-workbooks-with-array-formulas"></a>xlSet e pastas de trabalho com fórmulas de matriz

No Excel 2003 e versões anteriores, a [função xlSet](xlset.md) falhará se você tentar atribuir valores para um intervalo em uma planilha que não seja a planilha ativa, onde o equivalente intervalo na planilha ativa contém uma fórmula de matriz. Nesse caso, o Excel exibe a mensagem "Não é possível alterar parte de uma matriz." Isso foi corrigido no Excel 2007. 
  
## <a name="circular-references-are-tolerated-in-data-tables"></a>Referências circulares são toleradas nas tabelas de dados

Excel atualmente não gera um erro se o cálculo baseado em uma tabela de dados se refere a algo na tabela em si. Como é improvável como esse cenário pode ser, tenha cuidado quando você está criando ou modificando as fórmulas que são usadas para calcular os valores da tabela de dados.
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a>Convertendo XLOPER12 inteiro para XLOPER

Porque o tipo de inteiro **xltypeInt** é um inteiro assinado de 32 bits no tipo de dados **XLOPER12** , mas é apenas um inteiro assinado de 16 bits no tipo de dados **XLOPER** , é possível que alguns valores de **XLOPER12** inteiro não podem estar contidos em um inteiro **XLOPER**. Onde o Excel converte desse tipo internamente, ele obtém alternativa para esse problema, convertendo o tipo para um ponto de flutuação **xltypeNum** **XLOPER**.
  
A função Framework [XLOper12ToXLOper](xloper12toxloper.md) espelha esse comportamento para ser consistente com o Excel internamente. Quando você chamar essa função, você não deve considerar retornado **XLOPER** sempre será **xltypeInt**; ler **my_xloper.val.w** retornará um valor false se o tipo de **my_xloper** for **xltypeNum**.
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a>Retornando XLOPER ou XLOPER12 modificando argumentos in-loco

Excel permite que o registro de funções que retornam um **XLOPER** ou **XLOPER12** modificando um argumento in-loco. No entanto, se um **XLOPER**/ **XLOPER12** pontos de argumento a memória e o ponteiro, em seguida, será substituído pelo valor de retorno da função DLL, Excel pode causar o vazamento de memória. Excel não exibe um erro, mas ela pode travar eventualmente. Além disso, se a DLL de memória alocada para o valor de retorno, Excel está tentando gratuito que a memória, que pode causar uma falha de aplicativo imediata. Portanto, você não deve modificar **XLOPER**/ argumentos**XLOPER12** in-loco. Todos os **XLOPER** ou **XLOPER12** argumentos devem ser tratados como estritamente somente leitura. 
  
Para saber mais, consulte [Memory Management in Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Ver tamb�m



[XLOper12ToXLOper](xloper12toxloper.md)


[Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)
  
[Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md)
  
[Gerenciamento de memória no Excel](memory-management-in-excel.md)

