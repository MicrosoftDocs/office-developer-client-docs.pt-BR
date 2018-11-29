---
title: 'Problemas conhecidos no desenvolvimento do Excel XLL '
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- problemas conhecidos [excel 2007]
localization_priority: Normal
ms.assetid: 3dfecc0b-a91c-448e-8721-5d3486b625fa
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34784f6895386efe7e6c3ca7ec213c7d71931058
ms.sourcegitcommit: f139451a43598b59da22775333779df691df460a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26685176"
---
# <a name="known-issues-in-excel-xll-development"></a>Problemas conhecidos no desenvolvimento do Excel XLL 

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Este tópico descreve problemas conhecidos no Microsoft Excel que podem ocorrer no desenvolvimento XLL.
  
## <a name="unregistering-xll-commands-and-functions"></a>Removendo o registro de comandos e funções do XLL

Quando um XLL registra uma função ou comando, o Excel cria um novo nome para o recurso e associa uma referência para a função DLL com esse nome. O nome é retirado do quarto argumento *pxFunctionText* , da função [xlfRegister](xlfregister-form-1.md). Esse nome estará oculto de caixas de diálogo normais para gerenciar nomes de planilha. Para cancelar o registro de uma função ou comando, você deve excluir o nome usando a função [xlfSetName](xlfsetname.md), passando o nome, mas não passando uma definição. No entanto, um bug impede que isso remova o nome das listas de Assistente de função. 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a>Truncamento de cadeia de caracteres de descrição do argumento no Assistente de função

O parâmetro*pxArgumentHelp1* e todos os parâmetros subsequentes da função **xlfRegister** são cadeias de caracteres opcionais que correspondem aos argumentos da função XLL. O Assistente de função exibe essas informações para fornecer ajuda na caixa de diálogo de construção do argumento. Às vezes, o Excel trunca a cadeia de caracteres que corresponde ao argumento final por um ou dois caracteres ao exibi-lo na caixa de diálogo. Para evitar isso adicione uma "cadeia de caracteres vazia" adicional como o último parâmetro "ajuda de argumento" do seu registro de função.
  
## <a name="binary-name-scope-limitation"></a>Limitação de escopo de nome binário

Nomes binários e seus dados podem ser recuperados somente quando a planilha que estava ativa no momento em que eles foram criados estiver ativa novamente. Como as funções de planilha não podem ativar planilhas em uma pasta de trabalho (somente comandos podem fazer isso), aplicativos de nomes binários são muito limitados. Por exemplo, se você tiver um comando que é chamado somente de uma determinada planilha, você poderá usar um nome binário para armazenar dados relacionadas ao comando.
  
## <a name="xlset-and-workbooks-with-array-formulas"></a>xlSet e Workbooks com fórmulas de matriz

No Excel 2003 e em versões anteriores, a [função xlSet ](xlset.md)falha se você tentar atribuir valores a um intervalo em uma planilha que não seja a planilha ativa, em que o intervalo equivalente na planilha ativa contém uma fórmula de matriz. Nesse caso, o Excel exibirá a mensagem "Não é possível alterar parte de uma matriz." Esse problema foi corrigido no Excel 2007. 
  
## <a name="circular-references-are-tolerated-in-data-tables"></a>Referências circulares são toleradas nas tabelas de dados

O Excel no momento não gera um erro se o cálculo no qual uma tabela de dados é baseada refere-se a algo na própria tabela. Por mais improvável que esse cenário seja, você deve ter cuidado ao criar ou modificar fórmulas usadas para calcular valores de tabela de dados.
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a>Converter um número inteiro XLOPER12 em XLOPER

Como o tipo inteiro **xltypeInt** é um inteiro assinado de 32 bits no tipo de dados **XLOPER12**, mas é apenas um inteiro assinado de 16 bits no tipo de dados **XLOPER**, é possível que alguns valores inteiros **XLOPER12** não possam estar contidos em um inteiro **XLOPER**. Onde o Excel converte internamente esse tipo, a alternativa para esse problema é converter o tipo em um ponto flutuante **xltypeNum** **XLOPER**.
  
A estrutura da função [XLOper12ToXLOper](xloper12toxloper.md) espelha esse comportamento para ser consistente com o Excel internamente. Ao ligar para essa função, você não deve considerar que o **XLOPER** fornecido sempre será **xltypeInt**; leitura **my_xloper.val.w** retornará um valor falso se o **my_xloper** tipo for **xltypeNum**.
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a>Retornar XLOPER ou XLOPER12 modificando argumentos in-loco

Excel permite o registro de funções que retornam um **XLOPER** ou **XLOPER12** modificando um argumento no local. No entanto, se um argumento **XLOPER**/ **XLOPER12** aponta para a memória, e o ponteiro do mouse for substituído pelo valor de retorno da função DLL, o Excel pode estender a memória. O Excel não exibe um erro, mas ele pode falhar. Além disso, se O DLL alocar memória para o valor de retorno, o Excel pode tentar liberar essa memória, o que pode causar uma falha do aplicativo imediatamente. Portanto, não modifique os argumentos **XLOPER**/ **XLOPER12** no local. Todos os argumentos **XLOPER** ou **XLOPER12** devem ser tratados estritamente como somente leitura. 
  
Para saber mais, consulte [Gerenciamento de Memória no Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Confira também



[XLOper12ToXLOper](xloper12toxloper.md)


[Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)
  
[Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md)
  
[Gerenciamento de Memória no Excel](memory-management-in-excel.md)

