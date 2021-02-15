---
title: Ação da macro MostrarTodosRegistros
TOCTitle: ShowAllRecords macro action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 201b284a56fbd3030b41a95424b41c73ee13e385
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308642"
---
# <a name="showallrecords-macro-action"></a>Ação da macro MostrarTodosRegistros


**Aplica-se ao:** Access 2013, Office 2013


Você pode usar a ação **MostrarTodosRegistres** para remover qualquer filtro aplicado da tabela ativa, do conjunto de resultados de consulta ou do formulário e exibir todos os registros na tabela ou no conjunto de resultados ou em todos os registros da tabela ou consulta base do formulário.

## <a name="setting"></a>Setting

A **ação MostrarTodosRegiscords** não tem argumentos.

## <a name="remarks"></a>Comentários

Você pode usar essa ação para garantir que todos os registros (incluindo quaisquer registros alterados ou novos) sejam exibidos para uma tabela, um conjunto de resultados de consulta ou um formulário. Essa ação faz com que um formulário ou subformário reaqueia os registros.

Você também pode usar essa ação para remover qualquer filtro que  foi aplicado  com a ação AplicarFiltro, o comando Filtrar na guia Página Início ou o argumento **Filter Name** ou **Where Condition** da ação **OpenForm.** 

Esta ação tem o mesmo  efeito que  clicar em Filtro de Alternância na guia Página Início ou clicar com o botão direito do mouse no campo filtrado e clicar em Limpar filtro **de...** no modo Formulário, modo Layout ou modo Folha de Dados.

Para executar a **ação ShowAllRecords** em um módulo do VBA (Visual Basic for Applications), use o método **ShowAllRecords** do objeto **DoCmd.**

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
<th><p>Condition</p></th>
<th><p>Ação</p></th>
<th><p>Argumentos: Configuração</p></th>
<th><p>Comentário</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[Filtros de Nome da Empresa] =1</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condição Where</strong>: [nome da empresa] como &quot; [AÀÁÂÃÄ]*&quot;</p></td>
<td><p>Filtrar nomes de empresas que começam com A, À, Á, Â, Ã ou Ä.</p></td>
</tr>
<tr class="even">
<td><p>[Filtros de Nome da Empresa] =2</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condição Where:</strong>[nome da empresa] como &quot; b*&quot;</p></td>
<td><p>Filtrar nomes de empresas que começam com B.</p></td>
</tr>
<tr class="odd">
<td><p>[Filtros de Nome da Empresa] =3</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condição Where:</strong>[nome da empresa] Como &quot; [CÇ]*&quot;</p></td>
<td><p>Filtrar nomes de empresas que começam com C ou Ç.</p></td>
</tr>
<tr class="even">
<td><p>.. As linhas de ação de D a Y têm o mesmo formato de A a C...</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[Filtros de Nome da Empresa] =26</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Condição Where</strong>: [nome da empresa] Como &quot; [ZÆØÅ]*&quot;</p></td>
<td><p>Filtrar nomes de empresas que começam com Z, Æ, Ø ou Å.</p></td>
</tr>
<tr class="even">
<td><p>[Filtros de Nome da Empresa] =27</p></td>
<td><p><strong>ShowAllRecords</strong></p></td>
<td><p></p></td>
<td><p>Mostra todos os registros.</p></td>
</tr>
<tr class="odd">
<td><p>[RecordsetClone]. [RecordCount] &gt; 0</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nome do controle</strong>: CompanyName</p></td>
<td><p>Se os registros forem retornados para a letra selecionada, mova o foco para o controle NomeDaEmpresa.</p></td>
</tr>
</tbody>
</table>

