---
title: Ação da macro MostrarTodosRegistros
TOCTitle: ShowAllRecords macro action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c4ea531de8c5b99c9ff85eacddcc79a596caebd5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922038"
---
# <a name="showallrecords-macro-action"></a>Ação da macro MostrarTodosRegistros


**Aplica-se a**: Access 2013, o Office 2013


Você pode usar a ação **MostrarTodosRegistros** para remover qualquer filtro aplicado da tabela ativa, do conjunto de resultados de consulta ou do formulário e exibir todos os registros na tabela ou resultado conjunto ou todos os registros na tabela base do formulário ou uma consulta.

## <a name="setting"></a>Configuração

A ação **MostrarTodosRegistros** não tem nenhum argumento.

## <a name="remarks"></a>Comentários

Você pode usar esta ação para garantir que todos os registros (incluindo quaisquer registros novos ou alterados) sejam exibidos para uma tabela, um conjunto de resultados de consulta ou um formulário. Esta ação faz com que a repetição da consulta dos registros para um formulário ou subformulário.

Você também pode usar esta ação para remover qualquer filtro que tenha sido aplicado com a ação **AplicarFiltro** , o comando de **filtro** na guia **página inicial** , ou o **Nome do filtro** ou argumento **Condição Where** da ação **AbrirFormulário** .

Essa ação tem o mesmo efeito que clicar em **Filtro de alternância** na guia **Home** , ou clicando o campo filtrado e clicando em **Limpar filtro da …** no modo formulário, modo de exibição de Layout ou modo folha de dados.

Para executar a ação **MostrarTodosRegistros** em um módulo Visual Basic for Applications (VBA), use o método **ShowAllRecords** do objeto **DoCmd** .

## <a name="example"></a>Exemplo

**Aplicar um filtro usando uma macro**

A macro a seguir contém um conjunto de ações, sendo que cada uma filtra os registros de um formulário Lista de Telefones de Clientes. Ela mostra o uso das ações **AplicarFiltro**, **MostrarTodosRegistros** e **IrParaControle**. Também mostra o uso das condições para determinar qual botão de alternância de um grupo de opções foi selecionado no formulário. Cada linha de ação está associada a um botão de alternância que seleciona o conjunto de registros que começa com A, B, C e assim por diante ou todos os registros. Essa macro deve ser anexada ao evento **ApósAtualizar** do grupo de opções CompanyNameFilter.

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
<td><p>[Filtros de nome da empresa] = 1</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condição onde</strong>: [Company Name] como &quot;[AÀÁÂÃÄ] *&quot;</p></td>
<td><p>Filtrar nomes de empresas que começam com A, À, Á, Â, Ã ou Ä.</p></td>
</tr>
<tr class="even">
<td><p>[Filtros de nome da empresa] = 2</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condição onde</strong>: [Company Name] como &quot;B *&quot;</p></td>
<td><p>Filtrar nomes de empresas que começam com B.</p></td>
</tr>
<tr class="odd">
<td><p>[Filtros de nome da empresa] = 3</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condição onde</strong>: [Company Name] como &quot;[CÇ] *&quot;</p></td>
<td><p>Filtrar nomes de empresas que começam com C ou Ç.</p></td>
</tr>
<tr class="even">
<td><p>.. As linhas de ação de D a Y têm o mesmo formato de A a C...</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[Filtros de nome da empresa] = 26</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condição onde</strong>: [Company Name] como &quot;[ZÆØÅ] *&quot;</p></td>
<td><p>Filtrar nomes de empresas que começam com Z, Æ, Ø ou Å.</p></td>
</tr>
<tr class="even">
<td><p>[Filtros de nome da empresa] = 27</p></td>
<td><p><strong>ShowAllRecords</strong></p></td>
<td><p></p></td>
<td><p>Mostra todos os registros.</p></td>
</tr>
<tr class="odd">
<td><p>[RecordsetClone]. [RecordCount] &gt;0</p></td>
<td><p><strong>IrParaControle</strong></p></td>
<td><p><strong>Nome do controle</strong>: NomeDaEmpresa</p></td>
<td><p>Se os registros forem retornados para a letra selecionada, mova o foco para o controle NomeDaEmpresa.</p></td>
</tr>
</tbody>
</table>

