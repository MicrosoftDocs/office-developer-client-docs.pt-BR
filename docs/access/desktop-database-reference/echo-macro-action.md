---
title: Ação de macro eco (referência do banco de dados do Access)
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

Você pode usar a ação **eco** para especificar se o eco está ativado. Por exemplo, você pode usar essa ação para ocultar ou mostrar os resultados de uma macro durante a execução.

## <a name="setting"></a>Configuração

> [!NOTE]
> This action will not be allowed if the database is not trusted.

A ação **eco** tem os seguintes argumentos.

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
<td><p><strong>Eco ativado</strong></p></td>
<td><p>Clique em <strong>Sim</strong> (ativar eco) ou em <strong>não</strong> (desativar o eco) na caixa <strong>eco ativado</strong> na seção <strong>argumentos da ação</strong> do painel Construtor de macros. O padrão é <strong>Sim</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Texto da Barra de Status</strong></p></td>
<td><p>O texto a ser exibido na barra de status quando o eco está desativado. Por exemplo, quando o eco está desativado, a barra de status pode &quot;exibir a macro está sendo executada.&quot;</p></td>
</tr>
</tbody>
</table>


Quando uma macro é executada, a atualização de tela freqüentemente mostra informações não essenciais para o funcionamento da macro. Quando você define o argumento **Echo on** como **não**, a macro é executada sem Atualizar a tela. Quando a macro é concluída, o Access automaticamente ativa novamente o eco e redesenha a janela. A **** configuração no para o argumento **Echo on** não afeta a funcionalidade da macro ou seus resultados.

A ação **eco** não suprime a exibição de caixas de diálogo modais, como mensagens de erro ou formulários pop-up, como folhas de propriedades. Você pode usar caixas de diálogo e formulários pop-up para coletar ou exibir informações, mesmo se o eco estiver desativado. Para suprimir todas as caixas de diálogo ou mensagens de erro, exceto caixas de mensagem de erro e caixas de diálogo que exigem que o usuário insira informações, use a ação **DefinirAvisos** .

Você pode executar a ação **eco** mais de uma vez em uma macro. Isso permite que você altere o texto da barra de status enquanto a macro é executada.

Se você desativar o eco, poderá usar a ação **exibirponteirodeampulheta** para alterar o ponteiro do mouse para um ícone de ampulheta (ou qualquer ícone de ponteiro de mouse que você tenha definido para "ocupado") para fornecer uma indicação visual de que a macro está sendo executada.

Para executar a ação **eco** em um módulo do VBA (Visual Basic for Applications), use o método **Echo** do objeto **DoCmd** .

## <a name="examples"></a>Exemplos

### <a name="set-the-value-of-a-control-by-using-a-macro"></a>Definir o valor de um controle usando uma macro

A macro a seguir abre o formulário Adicionar produtos a partir de um botão no formulário fornecedores. Ela mostra o uso das ações **eco**, **fecharJanela**, **AbrirFormulário**, **DefinirValor**e **IrParaControle** . A ação **DefinirValor** define o controle de ID do fornecedor no formulário produtos como o fornecedor atual no formulário fornecedores. A ação **IrParaControle** move o foco para o campo ID da categoria, onde você pode começar a inserir dados para o novo produto. Essa macro deve ser anexada ao botão Adicionar produtos no formulário fornecedores.

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
<td><p><strong>Echo ativado</strong>: <strong>não</strong></p></td>
<td><p>Interrompa a atualização da tela enquanto a macro estiver em execução.</p></td>
</tr>
<tr class="even">
<td><p><strong>FecharJanela</strong></p></td>
<td><p><strong>Tipo de objeto</strong>: <strong>nome</strong>do formObject: <strong>salvamento</strong>da lista de produtos: <strong>não</strong></p></td>
<td><p>Feche o formulário lista de produtos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nome do formulário</strong>: modo de <strong>exibição</strong>de produtos: <strong>modo FormData</strong>: <strong>modo AddWindow</strong>: <strong>normal</strong></p></td>
<td><p>Abra o formulário produtos.</p></td>
</tr>
<tr class="even">
<td><p><strong>SetValue</strong></p></td>
<td><p><strong>Item</strong>: [formulários]! [Produtos]! [CódigoDoFornecedor] <strong>Expressão</strong>: CódigoDoFornecedor</p></td>
<td><p>Defina o controle de ID do fornecedor como o fornecedor atual no formulário fornecedores.</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nome do controle</strong>: CategoryID</p></td>
<td><p>Vá para o controle de ID de categoria.</p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a>Sincronizar formulários usando uma macro

A macro a seguir abre o formulário lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual. Ela mostra o uso das ações **eco**, **MessageBox**, **IrParaControle**, **PararMacro**, **AbrirFormulário**e **moveredimensionarjanela** . Também mostra o uso de uma expressão condicional com as ações **MessageBox**, **IrParaControle**e **PararMacro** . Essa macro deve ser anexada ao botão reVisar produtos no formulário fornecedores.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condição</p></th>
<th><p>Ação</p></th>
<th><p>Argumentos: Configuração</p></th>
<th><p>Comentário</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo ativado</strong>: <strong>não</strong></p></td>
<td><p>Interrompa a atualização da tela enquanto a macro estiver em execução.</p></td>
</tr>
<tr class="even">
<td><p>Énulo ([código do fornecedor])</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: mova para o registro de fornecedor cujos produtos você deseja ver e, em seguida, clique no botão revisar produtos novamente. <strong>Aviso sonoro</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: selecionar um fornecedor</p></td>
<td><p>Se não houver um fornecedor atual no formulário fornecedores, exiba uma mensagem.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nome do controle</strong>: CompanyName</p></td>
<td><p>Mover o foco para o controle CompanyName.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>PararMacro</strong></p></td>
<td><p></p></td>
<td><p>Interrompa a macro.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nome do formulário</strong>: <strong>modo de exibição</strong>de lista de produtos: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [CódigoDoFornecedor ID] = [formulários]! [Fornecedores]! [CódigoDoFornecedor] <strong>Modo de dados</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>normal</strong></p></td>
<td><p>Abra o formulário lista de produtos e mostre os produtos do fornecedor atual.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>Moveredimensionarjanela</strong></p></td>
<td><p><strong>direita</strong>: 0,7799&quot; <strong>baixo</strong>: 1,8&quot;</p></td>
<td><p>Posicione o formulário lista de produtos no canto inferior direito do formulário fornecedores.</p></td>
</tr>
</tbody>
</table>

