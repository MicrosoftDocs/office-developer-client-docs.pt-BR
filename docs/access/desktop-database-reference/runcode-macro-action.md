---
title: Ação da macro ExecutarCódigo
TOCTitle: RunCode macro action
ms:assetid: cb0625be-4b5d-4927-9b0e-59a6e411b5bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834373(v=office.15)
ms:contentKeyID: 48547706
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98700
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bac15bed3b416d57f75dc7482b085478a27d5fa4
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996696"
---
# <a name="runcode-macro-action"></a>Ação da macro ExecutarCódigo

**Aplica-se a**: Access 2013, o Office 2013

Use a ação **ExecutarCódigo** para chamar um procedimento Function do VBA(Visual Basic for Applications).

## <a name="setting"></a>Configuração

A ação **ExecutarCódigo** tem o argumento a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Nome da função</strong></p></td>
<td><p>O nome do procedimento Function do VBA a ser chamado. Coloque entre parênteses todos os argumentos da função. Digite o nome da função na caixa <strong>Nome da Função</strong>, na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Este é um argumento obrigatório.</p><p><strong>Observação</strong>: banco de dados de um acesso (. mdb ou. accdb), clique no botão <strong>Construir</strong> para usar o construtor de expressões para selecionar uma função para este argumento. Clique na função desejada na lista no construtor de expressões.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Os procedimentos Function definidos pelo usuário são armazenados nos módulos do Microsoft Access.

Você deve incluí-los entre parênteses, mesmo que o procedimento Function não tenha nenhum argumento. Por exemplo:

`TestFunction()`

Ao contrário de nomes de função definida pelo usuário usados para configurações de propriedade de evento, o nome da função no argumento **Nome da função** não começa com um sinal de igualdade (**=**).

O Access ignora o valor de retorno da função.

> [!NOTE]
> [!OBSERVAçãO] Não será possível chamar um procedimento Function em uma macro se o nome da função for igual ao nome do módulo.

> [!TIP]
> [!DICA] Para executar um procedimento Sub ou um procedimento de evento escrito em Visual Basic, crie um procedimento Function que possa chamar o procedimento Sub ou o procedimento de evento. Use a ação **ExecutarCódigo** para executar o procedimento Function.

Se você usar a ação **ExecutarCódigo** para chamar uma função, o Access pesquisará a função com o nome especificado pelo argumento **Nome da Função** nos módulos padrão do banco de dados. Entretanto, quando essa ação for executada em resposta ao acionamento de um comando de menu em um formulário ou relatório, ou em resposta a um evento em um formulário ou relatório, o Access primeiro pesquisará a função no módulo de classe do formulário ou do relatório e depois nos módulos padrão. O Access não pesquisa os módulos de classe mostrados na área **Módulos** do Painel de Navegação para localizar a função especificada pelo argumento **Nome da Função**.

Esta ação não está disponível em um módulo do VBA. Em vez disso, execute o procedimento Function desejado diretamente no VBA.

