---
title: Ação de macro de eco (referência de banco de dados da área de trabalho do Access)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 03eeab3884e093b7c22f8fd23d5471d1dc620bc8
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997452"
---
# <a name="echo-macro-action"></a>Ação da macro Eco

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **eco** para especificar se o eco está ativado. Por exemplo, você pode usar essa ação para ocultar ou mostrar os resultados de uma macro enquanto ele é executado.

## <a name="setting"></a>Configuração

> [!NOTE]
> [!OBSERVAçãO] This action will not be allowed if the database is not trusted.

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
<td><p><strong>Eco ativo</strong></p></td>
<td><p>Clique em <strong>Sim</strong> (ativar o eco) ou <strong>não</strong> (desativar o eco) na caixa <strong>Eco na</strong> seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros. O padrão é <strong>Sim</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Texto da Barra de Status</strong></p></td>
<td><p>O texto a ser exibido na barra quando o eco está desativado de status. Por exemplo, quando o eco está desativado, a barra de status pode exibir &quot;a macro está sendo executada.&quot;</p></td>
</tr>
</tbody>
</table>


Quando uma macro for executada, a atualização da tela frequentemente mostra informações que não são essenciais para o funcionamento da macro. Quando você define o argumento **Echo ativo** como **não**, a macro será executada sem atualizar a tela. Quando a macro é concluída, o Access automaticamente ativa eco e redesenha a janela. A configuração **não** para o argumento **Eco ativo** não afeta a funcionalidade da macro ou seus resultados.

A ação **Echo** não suprime a exibição de caixas de diálogo modal, mensagens de erro ou formulários pop-up, como folhas de propriedades. Você pode usar caixas de diálogo e formulários pop-up para coletar ou exibir informações, mesmo se o eco está desativado. Para suprimir todas as caixas de diálogo ou de mensagem, exceto as caixas de mensagem de erro e caixas de diálogo que exigem que o usuário insira informações, use a ação **DefinirAvisos** .

Você pode executar a ação **eco** mais de uma vez em uma macro. Isso permite que você altere o texto da barra de status enquanto a macro será executada.

Se você desativar o eco, você pode usar a ação **Exibirponteirodeampulheta** para alterar o ponteiro do mouse em um ícone de ampulheta (ou qualquer outro ícone de ponteiro do mouse definido para "Ocupado") para fornecer uma indicação visual que a macro está sendo executada.

Para executar a ação **eco** em um módulo Visual Basic for Applications (VBA), use o método **Echo** do objeto **DoCmd** .

## <a name="examples"></a>Exemplos

### <a name="set-the-value-of-a-control-by-using-a-macro"></a>Definir o valor de um controle usando uma macro

A macro a seguir abre o formulário Adicionar produtos com um botão no formulário Suppliers. Ela mostra o uso do **eco**, **fecharJanela**, **AbrirFormulário**, **DefinirValor**e **GoToControl** ações. A ação **DefinirValor** define o controle de código do fornecedor no formulário produtos como o fornecedor atual no formulário fornecedores. A ação **GoToControl** , em seguida, move o foco para o campo ID da categoria, onde você pode começar a inserir dados para o novo produto. Essa macro deve ser anexada ao botão Adicionar produtos no formulário fornecedores.

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
<td><p><strong>Eco no</strong>: <strong>não</strong></p></td>
<td><p>Pare a atualização da tela enquanto a macro é executada.</p></td>
</tr>
<tr class="even">
<td><p><strong>FecharJanela</strong></p></td>
<td><p><strong>Tipo de objeto</strong>: <strong>Nome FormObject</strong>: lista de produto para <strong>Salvar</strong>: <strong>não</strong></p></td>
<td><p>Feche o formulário de lista de produtos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nome do formulário</strong>: produtos <strong>modo de exibição</strong>: <strong>Modo FormData</strong>: <strong>Modo AddWindow</strong>: <strong>Normal</strong></p></td>
<td><p>Abra o formulário Products.</p></td>
</tr>
<tr class="even">
<td><p><strong>SetValue</strong></p></td>
<td><p><strong>Item</strong>: [formulários]! [Produtos]! [SupplierID] <strong>Expressão</strong>: SupplierID</p></td>
<td><p>Defina o controle de código do fornecedor como o fornecedor atual no formulário fornecedores.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IrParaControle</strong></p></td>
<td><p><strong>Nome do controle</strong>: CategoryID</p></td>
<td><p>Vá para o controle de ID da categoria.</p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a>Sincronizar formulários usando uma macro

A macro a seguir abre o formulário de lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual. Ela mostra o uso do **eco**, **MessageBox**, **GoToControl**, **PararMacro**, **AbrirFormulário**e **Moveredimensionarjanela** ações. Ele também mostra o uso de uma expressão condicional com as ações **MessageBox**, **GoToControl**e **PararMacro** . Essa macro deve ser anexada ao botão Revisar produtos no formulário fornecedores.

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
<td><p><strong>Eco no</strong>: <strong>não</strong></p></td>
<td><p>Pare a atualização da tela enquanto a macro é executada.</p></td>
</tr>
<tr class="even">
<td><p>ÉNulo ([ID do fornecedor])</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: mover para o registro do fornecedor cujos produtos você deseja ver, em seguida, clique no botão Revisar produtos novamente. <strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: selecione um fornecedor</p></td>
<td><p>Se não houver nenhum fornecedor atual no formulário fornecedores, exiba uma mensagem.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>IrParaControle</strong></p></td>
<td><p><strong>Nome do controle</strong>: NomeDaEmpresa</p></td>
<td><p>Mova o foco para o controle NomeDaEmpresa.</p></td>
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
<td><p><strong>Nome do formulário</strong>: <strong>modo de exibição</strong>da lista de produto: <strong>DatasheetFilter nome</strong>: <strong>condição onde</strong>: [código do fornecedor] = [formulários]! Fornecedores! [SupplierID] <strong>Modo de dados</strong>: <strong>Modo de OnlyWindow de leitura</strong>: <strong>Normal</strong></p></td>
<td><p>Abra o formulário de lista de produtos e mostram os produtos do fornecedor atual.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>Moveredimensionarjanela</strong></p></td>
<td><p><strong>Direita</strong>: 0.7799&quot; <strong>para baixo</strong>: 1,8&quot;</p></td>
<td><p>Posiciona o formulário de lista de produtos no canto inferior direito do formulário fornecedores.</p></td>
</tr>
</tbody>
</table>

