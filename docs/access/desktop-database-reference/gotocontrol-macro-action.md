---
title: Ação da macro IrParaControle
TOCTitle: GoToControl macro action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e5318652430f6cb9564fb1bb02832cc120b080b
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026243"
---
# <a name="gotocontrol-macro-action"></a>Ação da macro IrParaControle

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **GoToControl** para mover o foco para o campo ou controle especificado no registro atual do formulário aberto, folha de dados de formulário, folha de dados da tabela ou consulta a folha de dados. Use esta ação quando quiser que um campo ou controle específico tenha o foco. Esse campo ou controle pode ser usado para comparações ou ações **EncontrarRegistro** . Você também pode usar esta ação para navegar em um formulário de acordo com certas condições. Por exemplo, se o usuário inserir Não em um controle Casado de um formulário de seguro de saúde, o foco automaticamente poderá ignorar o controle Nome do cônjuge/parceiro e passar para o próximo controle.

## <a name="setting"></a>Configuração

> [!NOTE]
> Essa ação não está disponível para uso com páginas de acesso a dados.

A ação **IrParaControle** tem os argumentos a seguir.

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
<td><p><strong>Nome do Controle</strong></p></td>
<td><p>O nome do campo ou do controle em que você deseja focar. Insira o nome do campo ou controle na caixa <strong>Nome do controle</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros. Este é um argumento obrigatório.</p>
<p><strong>Observação</strong>: insira apenas o nome do campo ou controle no argumento <strong>Nome do controle</strong> , não o identificador totalmente qualificado, como formulários! Produtos! [Product ID].</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você não pode usar a ação **GoToControl** para mover o foco para um controle em um formulário oculto.

> [!TIP]
> Você pode usar a ação **GoToControl** para mover para o subformulário, que é um tipo de controle. Em seguida, você pode usar a ação **IrParaRegistro** para mover para um determinado registro no subformulário. Você também pode mover para um controle em um subformulário, usando a ação **GoToControl** para mover-se primeiro para o subformulário e, em seguida, para o controle no subformulário.

Para executar a ação **GoToControl** em um módulo Visual Basic for Applications (VBA), use o método **GoToControl** do objeto **DoCmd** . Você também pode usar o método **SetFocus** para mover o foco para um controle em um formulário ou qualquer um dos seus subformulários ou para um campo em uma tabela aberta, consulta ou folha de dados do formulário.

## <a name="examples"></a>Exemplos

**Definir o valor de um controle usando uma macro**

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
<td><p>Fechar o formulário de lista de produtos.</p></td>
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
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nome do controle</strong>: CategoryID</p></td>
<td><p>Vá para o controle de ID da categoria.</p></td>
</tr>
</tbody>
</table>


**Validar dados usando uma macro**

A macro de validação a seguir verifica os códigos postais inseridos em um formulário Fornecedores. Ela mostra o uso das ações **PararMacro**, **CaixadeMensagem**, **CancelarEvento** e **IrParaControle**. Uma expressão condicional verifica o país/região e o código postal inseridos em um registro do formulário. Se o código postal não estiver no formato certo para o país/região, a macro exibirá uma caixa de mensagem e cancelará o salvamento do registro. A macro retorna você ao controle CEP, onde é possível corrigir o erro. Essa macro deve ser anexada à propriedade **AntesdeAtualizar** do formulário Fornecedores.

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
<td><p>IsNull([CountryRegion])</p></td>
<td><p><strong>PararMacro</strong></p></td>
<td><p></p></td>
<td><p>Se CountryRegion for <strong>Nulo</strong>, o código postal não pode ser validado.</p></td>
</tr>
<tr class="even">
<td><p>[Paísregião] No (&quot;França&quot;,&quot;Itália&quot;,&quot;Espanha&quot;) e Compr ([CEP]) &lt; &gt; 5</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: O código postal precisa ter 5 caracteres. <strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de CEP</p></td>
<td><p>Se o código postal não tiver 5 caracteres, exiba uma mensagem.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Cancele o evento.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nome do controle</strong>: CEP</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[Paísregião] No (&quot;Austrália&quot;,&quot;Cingapura&quot;) e Compr ([CEP]) &lt; &gt; 4</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p>Mensagem: O código postal precisa ter 4 caracteres. 

 <strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de CEP</p></td>
<td><p>Se o código postal não tiver 4 caracteres, exiba uma mensagem.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Cancele o evento.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nome do controle</strong>: CEP</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([Paísregião] = &quot;Canadá&quot;) E ([CEP] não igual a&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: O código postal não é válido. Exemplo de código canadense: H1J 1C3 <strong>alarme sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de código Postal</p></td>
<td><p>Se o código postal não estiver correto para o Canadá, exiba uma mensagem. (O exemplo de código canadense: H1J 1C3)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Cancele o evento.</p></td>
</tr>
</tbody>
</table>

