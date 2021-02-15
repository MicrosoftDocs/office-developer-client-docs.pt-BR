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
# <a name="showallrecords-macro-action"></a><span data-ttu-id="e9053-102">Ação da macro MostrarTodosRegistros</span><span class="sxs-lookup"><span data-stu-id="e9053-102">ShowAllRecords macro action</span></span>


<span data-ttu-id="e9053-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9053-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="e9053-104">Você pode usar a ação **MostrarTodosRegistres** para remover qualquer filtro aplicado da tabela ativa, do conjunto de resultados de consulta ou do formulário e exibir todos os registros na tabela ou no conjunto de resultados ou em todos os registros da tabela ou consulta base do formulário.</span><span class="sxs-lookup"><span data-stu-id="e9053-104">You can use the **ShowAllRecords** action to remove any applied filter from the active table, query result set, or form, and display all records in the table or result set or all records in the form's underlying table or query.</span></span>

## <a name="setting"></a><span data-ttu-id="e9053-105">Setting</span><span class="sxs-lookup"><span data-stu-id="e9053-105">Setting</span></span>

<span data-ttu-id="e9053-106">A **ação MostrarTodosRegiscords** não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="e9053-106">The **ShowAllRecords** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9053-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9053-107">Remarks</span></span>

<span data-ttu-id="e9053-108">Você pode usar essa ação para garantir que todos os registros (incluindo quaisquer registros alterados ou novos) sejam exibidos para uma tabela, um conjunto de resultados de consulta ou um formulário.</span><span class="sxs-lookup"><span data-stu-id="e9053-108">You can use this action to ensure that all records (including any changed or new records) are displayed for a table, query result set, or form.</span></span> <span data-ttu-id="e9053-109">Essa ação faz com que um formulário ou subformário reaqueia os registros.</span><span class="sxs-lookup"><span data-stu-id="e9053-109">This action causes a requery of the records for a form or subform.</span></span>

<span data-ttu-id="e9053-110">Você também pode usar essa ação para remover qualquer filtro que  foi aplicado  com a ação AplicarFiltro, o comando Filtrar na guia Página Início ou o argumento **Filter Name** ou **Where Condition** da ação **OpenForm.** </span><span class="sxs-lookup"><span data-stu-id="e9053-110">You can also use this action to remove any filter that was applied with the **ApplyFilter** action, the **Filter** command on the **Home** tab, or the **Filter Name** or **Where Condition** argument of the **OpenForm** action.</span></span>

<span data-ttu-id="e9053-111">Esta ação tem o mesmo  efeito que  clicar em Filtro de Alternância na guia Página Início ou clicar com o botão direito do mouse no campo filtrado e clicar em Limpar filtro **de...** no modo Formulário, modo Layout ou modo Folha de Dados.</span><span class="sxs-lookup"><span data-stu-id="e9053-111">This action has the same effect as clicking **Toggle Filter** on the **Home** tab, or right-clicking the filtered field and clicking **Clear filter from...** in Form view, Layout view, or Datasheet view.</span></span>

<span data-ttu-id="e9053-112">Para executar a **ação ShowAllRecords** em um módulo do VBA (Visual Basic for Applications), use o método **ShowAllRecords** do objeto **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="e9053-112">To run the **ShowAllRecords** action in a Visual Basic for Applications (VBA) module, use the **ShowAllRecords** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="e9053-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e9053-113">Example</span></span>

<span data-ttu-id="e9053-114">**Aplicar um filtro usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="e9053-114">**Apply a filter by using a macro**</span></span>

<span data-ttu-id="e9053-p102">A macro a seguir contém um conjunto de ações, sendo que cada uma filtra os registros de um formulário Lista de Telefones de Clientes. Ela mostra o uso das ações **AplicarFiltro**, **MostrarTodosRegistros** e **IrParaControle**. Também mostra o uso das condições para determinar qual botão de alternância de um grupo de opções foi selecionado no formulário. Cada linha de ação está associada a um botão de alternância que seleciona o conjunto de registros que começa com A, B, C e assim por diante ou todos os registros. Essa macro deve ser anexada ao evento **ApósAtualizar** do grupo de opções CompanyNameFilter.</span><span class="sxs-lookup"><span data-stu-id="e9053-p102">The following macro contains a set of actions, each of which filters the records for a Customer Phone List form. It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions. It also shows the use of conditions to determine which toggle button in an option group has been selected on the form. Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records. This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9053-120">Condition</span><span class="sxs-lookup"><span data-stu-id="e9053-120">Condition</span></span></p></th>
<th><p><span data-ttu-id="e9053-121">Ação</span><span class="sxs-lookup"><span data-stu-id="e9053-121">Action</span></span></p></th>
<th><p><span data-ttu-id="e9053-122">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="e9053-122">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="e9053-123">Comentário</span><span class="sxs-lookup"><span data-stu-id="e9053-123">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9053-124">[Filtros de Nome da Empresa] =1</span><span class="sxs-lookup"><span data-stu-id="e9053-124">[Company Name Filters] =1</span></span></p></td>
<td><p><span data-ttu-id="e9053-125"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="e9053-125"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="e9053-126"><strong>Condição Where</strong>: [nome da empresa] como &quot; [AÀÁÂÃÄ]\*&quot;</span><span class="sxs-lookup"><span data-stu-id="e9053-126"><strong>Where Condition</strong>: [Company Name] Like &quot;[AÀÁÂÃÄ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="e9053-127">Filtrar nomes de empresas que começam com A, À, Á, Â, Ã ou Ä.</span><span class="sxs-lookup"><span data-stu-id="e9053-127">Filter for company names that start with A, À, Á, Â, Ã, or Ä.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9053-128">[Filtros de Nome da Empresa] =2</span><span class="sxs-lookup"><span data-stu-id="e9053-128">[Company Name Filters] =2</span></span></p></td>
<td><p><span data-ttu-id="e9053-129"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="e9053-129"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="e9053-130"><strong>Condição Where:</strong>[nome da empresa] como &quot; b\*&quot;</span><span class="sxs-lookup"><span data-stu-id="e9053-130"><strong>Where Condition</strong>: [Company Name] Like &quot;B\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="e9053-131">Filtrar nomes de empresas que começam com B.</span><span class="sxs-lookup"><span data-stu-id="e9053-131">Filter for company names that start with B.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9053-132">[Filtros de Nome da Empresa] =3</span><span class="sxs-lookup"><span data-stu-id="e9053-132">[Company Name Filters] =3</span></span></p></td>
<td><p><span data-ttu-id="e9053-133"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="e9053-133"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="e9053-134"><strong>Condição Where:</strong>[nome da empresa] Como &quot; [CÇ]\*&quot;</span><span class="sxs-lookup"><span data-stu-id="e9053-134"><strong>Where Condition</strong>: [Company Name] Like &quot;[CÇ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="e9053-135">Filtrar nomes de empresas que começam com C ou Ç.</span><span class="sxs-lookup"><span data-stu-id="e9053-135">Filter for company names that start with C or Ç.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9053-136">.. As linhas de ação de D a Y têm o mesmo formato de A a C...</span><span class="sxs-lookup"><span data-stu-id="e9053-136">... Action rows for D through Y have the same format as A through C ...</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9053-137">[Filtros de Nome da Empresa] =26</span><span class="sxs-lookup"><span data-stu-id="e9053-137">[Company Name Filters] =26</span></span></p></td>
<td><p><span data-ttu-id="e9053-138"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="e9053-138"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="e9053-139"><strong>Condição Where</strong>: [nome da empresa] Como &quot; [ZÆØÅ]\*&quot;</span><span class="sxs-lookup"><span data-stu-id="e9053-139"><strong>Where Condition</strong>: [Company Name] Like &quot;[ZÆØÅ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="e9053-140">Filtrar nomes de empresas que começam com Z, Æ, Ø ou Å.</span><span class="sxs-lookup"><span data-stu-id="e9053-140">Filter for company names that start with Z, Æ, Ø, or Å.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9053-141">[Filtros de Nome da Empresa] =27</span><span class="sxs-lookup"><span data-stu-id="e9053-141">[Company Name Filters] =27</span></span></p></td>
<td><p><span data-ttu-id="e9053-142"><strong>ShowAllRecords</strong></span><span class="sxs-lookup"><span data-stu-id="e9053-142"><strong>ShowAllRecords</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e9053-143">Mostra todos os registros.</span><span class="sxs-lookup"><span data-stu-id="e9053-143">Show all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9053-144">[RecordsetClone]. [RecordCount] &gt; 0</span><span class="sxs-lookup"><span data-stu-id="e9053-144">[RecordsetClone].[RecordCount]&gt;0</span></span></p></td>
<td><p><span data-ttu-id="e9053-145"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="e9053-145"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="e9053-146"><strong>Nome do controle</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="e9053-146"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="e9053-147">Se os registros forem retornados para a letra selecionada, mova o foco para o controle NomeDaEmpresa.</span><span class="sxs-lookup"><span data-stu-id="e9053-147">If records are returned for the selected letter, move focus to the CompanyName control.</span></span></p></td>
</tr>
</tbody>
</table>

