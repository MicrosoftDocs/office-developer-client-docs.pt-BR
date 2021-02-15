---
title: Ação de macro Eco (referência do banco de dados da área de trabalho do Access)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d536ed47c780b7f9f1675a9879e86aeff80b67f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293620"
---
# <a name="echo-macro-action"></a>Ação da macro Eco

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a **ação Eco** para especificar se o eco está ligado. Por exemplo, você pode usar essa ação para ocultar ou mostrar os resultados de uma macro enquanto ela é executado.

## <a name="setting"></a>Setting

> [!NOTE]
> Essa ação não será permitida se o banco de dados não for confiável.

A **ação Eco** tem os seguintes argumentos.

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
<td><p><strong>Eco on</strong></p></td>
<td><p>Clique <strong>em Sim</strong> (ativar eco) ou Não <strong></strong> (desativar eco) na caixa Eco Ligar na seção <strong>Argumentos</strong> da Ação do painel Construtor de Macros. <strong></strong> O padrão é <strong>Sim</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Texto da Barra de Status</strong></p></td>
<td><p>O texto a ser exibido na barra de status quando o eco está desligado. Por exemplo, quando o eco está desligado, a barra de status pode exibir &quot; a macro que está sendo executado.&quot;</p></td>
</tr>
</tbody>
</table>


Quando uma macro é executado, a atualização de tela geralmente mostra informações não essenciais para o funcionamento da macro. Quando você definir o **argumento Eco Em** como **Não**, a macro será executado sem atualizar a tela. Quando a macro termina, o Access readere o eco automaticamente e redesegue a janela. A **configuração** Não para o argumento **Eco Em** não afeta a funcionalidade da macro ou seus resultados.

A **ação Eco** não suprime a exibição de caixas de diálogo modais, como mensagens de erro ou formulários pop-up, como folhas de propriedades. Você pode usar caixas de diálogo e formulários pop-up para coletar ou exibir informações, mesmo se o eco estiver desligado. Para suprimir todas as caixas de diálogo ou mensagens, exceto caixas de mensagem de erro e caixas de diálogo que exigem que o usuário insira informações, use a ação **DefinirAvisos.**

Você pode executar a **ação Eco** mais de uma vez em uma macro. Isso permite alterar o texto da barra de status enquanto a macro é executado.

Se você desativar o eco, poderá usar a ação **DisplayHourglassPointer** para alterar o ponteiro do mouse para um ícone de ampulheta (ou qualquer ícone de ponteiro do mouse definido para "Ocupado") para fornecer uma indicação visual de que a macro está em execução.

Para executar a **ação Eco** em um módulo do VBA (Visual Basic for Applications), use o método **Echo** do **objeto DoCmd.**

## <a name="examples"></a>Exemplos

### <a name="set-the-value-of-a-control-by-using-a-macro"></a>Definir o valor de um controle, usando uma macro

A macro a seguir abre o formulário Adicionar Produtos de um botão no formulário de Fornecedores. Mostra o uso das ações **Echo**, **CloseWindow**, **OpenForm**, **SetValue** e **GoToControl**. A **ação SetValue** define o controle de ID do Fornecedor no formulário Produtos para o fornecedor atual no formulário Fornecedores. A **ação IrParaControle** move o foco para o campo ID da categoria, onde você pode começar a inserir dados para o novo produto. Essa macro deve estar anexada ao botão Adicionar Produtos no formulário de Fornecedores.

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
<td><p>Interrompe a atualização de tela quando a macro é executada.</p></td>
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
<td><p>De definir o controle de ID de fornecedor para o fornecedor atual no formulário Fornecedores.</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Control Name</strong>: CategoryID</p></td>
<td><p>Vá para o controle de ID da categoria.</p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a>Sincronizar formulários usando uma macro

A macro a seguir abre o formulário Lista de Produtos no canto inferior direito do formulário Fornecedores, exibindo os produtos do fornecedor atual. Ele mostra o uso das ações **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm** e **MoveAndSizeWindow.** Ele também mostra o uso de uma expressão condicional com as ações **MessageBox**, **GoToControl** e **StopMacro.** Essa macro deve ser anexada ao botão Revisar Produtos no formulário Fornecedores.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
<th><p>Ação</p></th>
<th><p>Argumentos: Configuração</p></th>
<th><p>Comentário</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo On</strong>: <strong>No</strong></p></td>
<td><p>Interrompe a atualização de tela quando a macro é executada.</p></td>
</tr>
<tr class="even">
<td><p>IsNull([ID do fornecedor])</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem:</strong>vá para o registro do fornecedor cujos produtos você deseja ver e clique no botão Revisar Produtos novamente. <strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</p></td>
<td><p>Se não houver fornecedor atual no formulário Fornecedores, exibe uma mensagem.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nome do controle</strong>: CompanyName</p></td>
<td><p>Mova o foco para o controle CompanyName.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>PararMacro</strong></p></td>
<td><p></p></td>
<td><p>Pare a macro.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nome do formulário</strong>: Exibição de Lista <strong>de</strong>Produtos : <strong>Nome do Filtro de</strong>Folha de Dados : <strong>Condição</strong>Onde : [ID do fornecedor] = [Formulários]! [Fornecedores]! [SupplierID] <strong>Modo de Dados</strong>: <strong>Ler Modo Somente Janela</strong>: <strong>Normal</strong></p></td>
<td><p>Abra o formulário Lista de Produtos e mostre os produtos do fornecedor atual.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>À</strong>direita: 0,7799 &quot; <strong>para baixo:</strong>1,8&quot;</p></td>
<td><p>Posiciona o formulário Lista de Produtos no canto inferior direito do formulário Fornecedores.</p></td>
</tr>
</tbody>
</table>

