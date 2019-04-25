---
title: Ação da macro SetValue
TOCTitle: SetValue macro action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 6b6f16c22e9265159c73279cfa1b2644adbc0277
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306815"
---
# <a name="setvalue-macro-action"></a>Ação da macro SetValue

**Aplica-se ao**: Access 2013, Office 2013

Você pode usar a ação **SetValue** para definir o valor de um campo do Microsoft Access, o controle ou a propriedade em um formulário, uma folha de dados do formulário ou um relatório.

> [!NOTE]
> - Não é possível usar uma ação **SetValue** para definir o valor de uma propriedade do Access que retorna um objeto.
> - Essa ação não será permitida se o banco de dados não for confiável. 

## <a name="setting"></a>Setting

A ação **SetValue** tem os seguintes argumentos.

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
<td><p><strong>Item</strong></p></td>
<td><p>O nome do campo, controle ou propriedades cujo valor você deseja definir. Insira o nome de campo, controle ou propriedades na caixa <strong>Item</strong> na seção <strong>Argumentos da Ação</strong> no painel do Construtor de Macros. Você deve usar a sintaxe completa para fazer referência a esse item, como <em>controlname</em> (para um controle no formulário ou relatório de onde o macro foi chamado) ou <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>. Este é um argumento obrigatório.</p></td>
</tr>
<tr class="even">
<td><p><strong>Expressão</strong>.</p></td>
<td><p>A expressão Access usa para definir o valor para esse item. Você sempre deve usar a sintaxe completa para referir-se a quaisquer objetos na expressão. Por exemplo, para aumentar o valor em um controle de Salário em um formulário de Funcionários em 10%, use 1.1Forms!Employees!Salary*1.1. Este é um argumento obrigatório.</p><p><strong>OBSERVAÇÃO</strong>: Você não deve usar um sinal de igual (=) antes da expressão nesse argumento. Nesse caso, o Access avalia a expressão e usa esse valor como a expressão nesse argumento. Isso pode produzir resultados inesperados se a expressão for uma cadeia de caracteres.</p>
<p>Por exemplo, se você digitar <strong>=&quot;String1&quot;</strong> para esse argumento, o Access primeiro avalia a expressão como String1. Em seguida, ele usa a String1 como a expressão nesse argumento, esperando encontrar um controle ou propriedade denominada String1 no formulário ou relatório que chamou o macro.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Em um banco de dados do Access (.mdb ou .accdb), clique no botão **Build** para usar o Construtor de Expressões para criar uma expressão para qualquer um desses argumentos.

## <a name="remarks"></a>Comentários

Você pode usar essa ação para definir um valor para um campo ou controle em um formulário, uma folha de dados do formulário ou um relatório. Você também pode definir o valor de quase todas as propriedades de controle, do formulário e do relatório em qualquer modo de exibição. Para saber se uma propriedade em particular pode ser definida usando um macro e em quais modos de exibição podem ser definidas, consulte o tópico de Ajuda para essa propriedade no Editor do Visual Basic.

Você também pode definir o valor para um campo em uma tabela subjacente, mesmo que a forma não contenha um controle associado ao campo. Usa a sintaxe **Forms**\!*formname*\!*fieldname* na caixa **Item** para definir o valor para tal campo. Você também pode referir um campo na tabela subjacente do relatório usando a sintaxe **Reports**\!*reportname*\!*fieldname*, mas deve haver um controle no relatório associado a esse campo ou o campo deve ser referenciado em um controle calculado no relatório.

Se você definir o valor do controle no formulário, a ação **SetValue** não dispara regras de validação de nível de formulário de controle, mas aciona regras de validação de nível de tabela do campo subjacente se o controle for um controle associado. A ação **SetValue** também aciona um recálculo, mas o recálculo pode não ocorrer imediatamente. Para acionar a repintura imediata e forçar o recálculo até a conclusão, use a ação **RepaintObject**. O valor definido em um controle usando a ação **SetValue** também não é afetado por uma máscara de entrada definida na propriedade **InputMask** do campo subjacente ou do controle.

Para alterar o valor de um controle, você pode usar a ação **SetValue** em um macro especificado pela propriedade do evento **AfterUpdate** do controle. No entanto, é possível usar a ação **SetValue** em um macro especificado pela propriedade do evento **BeforeUpdate** do controle para alterar o valor do controle (embora você possa usar a ação **SetValue** para alterar o valor dos outros controles). Você também pode usar a ação **SetValue** em um macro especificado pela propriedade **BeforeUpdate** ou **AfterUpdate** de um formulário para alterar o valor de todos os controles do atual registro.

> [!NOTE]
> Não é possível usar a ação **SetValue** para definir o valor dos controles a seguir:
> - Controles associados e os controles calculados em relatórios.
> - Controles calculados em formulários.

> [!TIP]
> Você pode usar a ação **SetValue** para mostrar ou ocultar um formulário no modo de exibição Formulário. Insira **Forms**!*formname***.Visible** na caixa **Item** box, e **Não** ou **Sim** na caixa **Expressão**. Definir uma propriedade modal **Visível** do formulário para **Não** oculta o formulário e o torna sem restrição. Definir a propriedade para **Sim** exibe o formulário e o torna restrito novamente.

Alterar o valor de ou adicionar novos dados em um controle usando a ação**SetValue** em um macro não dispara, eventos como **BeforeUpdate**, **BeforeInsert**, ou **Change** que ocorrem quando você altera ou insere dados em um desses controles na interface do usuário. Esses eventos também não ocorrerem se você definir o valor do controle usando um módulo do Visual Basic for Applications (VBA).

Essa ação não está disponível em um módulo do VBA. Defina o valor diretamente no VBA.

## <a name="example"></a>Exemplo

**Definir o valor de um controle usando um macro**

O macro a seguir abre o formulário Adicionar Produtos de um botão no formulário de Fornecedores. Mostra o uso das ações **Echo**, **CloseWindow**, **OpenForm**, **SetValue** e **GoToControl** actions. A ação **SetValue** define o controle SupplierID no formulário de Produtos dos fornecedores atuais no formulário Fornecedores. A ação **GoToControl** move o foco para o campo CategoryID, onde você pode começar a inserir dados do novo produto. Esse macro deve estar anexado ao botão Adicionar Produtos no formulário de Fornecedores.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ação</p></th>
<th><p>Argumentos: Configuração</p></th>
<th><p>Comentário</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo On</strong>: <strong>No</strong></p></td>
<td><p>Interrompe a atualização de tela quando macro é executado.</p></td>
</tr>
<tr class="even">
<td><p><strong>CloseWindow</strong></p></td>
<td><p><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></p></td>
<td><p>Fecha o Formulário de Lista de Produtos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></p></td>
<td><p>Abre o formulário de produtos.</p></td>
</tr>
<tr class="even">
<td><p><strong>SetValue</strong></p></td>
<td><p><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</p></td>
<td><p>Define o controle SupplierID para o fornecedor atual no formulário de Fornecedores.</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Control Name</strong>: CategoryID</p></td>
<td><p>Vai para o controle CategoryID.</p></td>
</tr>
</tbody>
</table>

