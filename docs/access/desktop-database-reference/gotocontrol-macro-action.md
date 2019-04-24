---
title: Ação da macro IrParaControle
TOCTitle: GoToControl macro action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c056f2b0922402ea7cde7cf767969b73f912f572
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292164"
---
# <a name="gotocontrol-macro-action"></a>Ação da macro IrParaControle

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **IrParaControle** para mover o foco para o campo ou controle especificado no registro atual do formulário aberto, da folha de de formulário ou da folha de pesquisa da consulta. Use esta ação quando quiser que um campo ou controle específico tenha o foco. Este controle ou campo pode ser usado para comparações ou ações **LocalizarRegistro** . Você também pode usar esta ação para navegar em um formulário de acordo com certas condições. Por exemplo, se o usuário inserir Não em um controle Casado de um formulário de seguro de saúde, o foco automaticamente poderá ignorar o controle Nome do cônjuge/parceiro e passar para o próximo controle.

## <a name="setting"></a>Configuração

> [!NOTE]
> Esta ação não está disponível para uso com páginas de acesso a dados.

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
<td><p>O nome do campo ou do controle em que você deseja focar. Insira o nome do campo ou controle na caixa <strong>nome do controle</strong> na seção argumentos da <strong>ação</strong> do painel do construtor de macros. É um argumento obrigatório.</p>
<p><strong>Observação</strong>: insira somente o nome do campo ou controle no argumento <strong>nome do controle</strong> , não o identificador totalmente qualificado, como formulários! Produtos! [ID do produto].</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você não pode usar a ação **IrParaControle** para mover o foco para um controle em um formulário oculto.

> [!TIP]
> Você pode usar a ação **IrParaControle** para mover para um subformulário, que é um tipo de controle. Você pode usar a ação **IrParaRegistro** para mover para um registro específico no subformulário. Você também pode mover para um controle em um subformulário usando a ação **IrParaControle** para mover primeiro para o subformulário e, em seguida, para o controle no subformulário.

Para executar a ação **IrParaControle** em um módulo do VBA (Visual Basic for Applications), use o método **GoToControl** do objeto **DoCmd** . Você também pode usar o método **SetFocus** para mover o foco para um controle em um formulário ou qualquer um de seus subformulários ou para um campo em uma tabela, consulta ou folha de formulários aberta.

## <a name="examples"></a>Exemplos

**Definir o valor de um controle usando uma macro**

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


**Validar dados usando uma macro**

A macro de validação a seguir verifica os códigos postais inseridos em um formulário Fornecedores. Ela mostra o uso das ações **PararMacro**, **CaixadeMensagem**, **CancelarEvento** e **IrParaControle**. Uma expressão condicional verifica o país/região e o código postal inseridos em um registro do formulário. Se o código postal não estiver no formato certo para o país/região, a macro exibirá uma caixa de mensagem e cancelará o salvamento do registro. A macro, em seguida, retorna ao controle do código postal, onde você pode corrigir o erro. Essa macro deve ser anexada à propriedade **AntesdeAtualizar** do formulário Fornecedores.

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
<td><p>IsNull ([CountryRegion])</p></td>
<td><p><strong>PararMacro</strong></p></td>
<td><p></p></td>
<td><p>Se CountryRegion for <strong>NULL</strong>, o código postal não poderá ser validado.</p></td>
</tr>
<tr class="even">
<td><p>CountryRegion In (&quot;França&quot;,&quot;Itália&quot;,&quot;Espanha&quot;) e compr ([CEP]) &lt; &gt; 5</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: o código postal deve ter 5 caracteres. <strong>Aviso sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de código postal</p></td>
<td><p>Se o código postal não tiver 5 caracteres, exibe uma mensagem.</p></td>
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
<td><p>CountryRegion In (&quot;Austrália&quot;,&quot;Cingapura&quot;) e compr ([CEP]) &lt; &gt; 4</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p>Mensagem: O código postal precisa ter 4 caracteres. <strong>Aviso sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de código postal</p></td>
<td><p>Se o código postal não tiver 4 caracteres, exibe uma mensagem.</p></td>
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
<td><p>([CountryRegion] = &quot;Canadá&quot;) E ([código postal] não like&quot;[A-z] [0-9] [A-z] [0-9] [A-z] [0-9]&quot;)</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: o código postal não é válido. Exemplo de código canadense: H1J 1C3 <strong>beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de código postal</p></td>
<td><p>Se o código postal não estiver correto para o Canadá, exibe uma mensagem. (Exemplo de código de Canadá: H1J 1C3)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Cancele o evento.</p></td>
</tr>
</tbody>
</table>

