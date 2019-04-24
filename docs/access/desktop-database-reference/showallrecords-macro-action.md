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
# <a name="showallrecords-macro-action"></a><span data-ttu-id="8ab4c-102">Ação da macro MostrarTodosRegistros</span><span class="sxs-lookup"><span data-stu-id="8ab4c-102">ShowAllRecords macro action</span></span>


<span data-ttu-id="8ab4c-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ab4c-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="8ab4c-104">Você pode usar a ação **MostrarTodosRegistros** para remover qualquer filtro aplicado da tabela ativa, do conjunto de resultados de consulta ou do formulário e exibir todos os registros na tabela ou conjunto de resultados ou todos os registros na tabela ou consulta base do formulário.</span><span class="sxs-lookup"><span data-stu-id="8ab4c-104">You can use the **ShowAllRecords** action to remove any applied filter from the active table, query result set, or form, and display all records in the table or result set or all records in the form's underlying table or query.</span></span>

## <a name="setting"></a><span data-ttu-id="8ab4c-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="8ab4c-105">Setting</span></span>

<span data-ttu-id="8ab4c-106">A ação **MostrarTodosRegistros** não tem nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="8ab4c-106">The **ShowAllRecords** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ab4c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ab4c-107">Remarks</span></span>

<span data-ttu-id="8ab4c-108">Você pode usar essa ação para garantir que todos os registros (incluindo quaisquer registros alterados ou novos) sejam exibidos para uma tabela, um conjunto de resultados de consulta ou um formulário.</span><span class="sxs-lookup"><span data-stu-id="8ab4c-108">You can use this action to ensure that all records (including any changed or new records) are displayed for a table, query result set, or form.</span></span> <span data-ttu-id="8ab4c-109">Esta ação faz com que a reconsulta dos registros de um formulário ou subformulário.</span><span class="sxs-lookup"><span data-stu-id="8ab4c-109">This action causes a requery of the records for a form or subform.</span></span>

<span data-ttu-id="8ab4c-110">Você também pode usar essa ação para remover qualquer filtro que tenha sido aplicado com a ação **AplicarFiltro** , o comando **filtro** na **guia página inicial** ou o argumento **nome do filtro** ou **condição onde** da ação **AbrirFormulário** .</span><span class="sxs-lookup"><span data-stu-id="8ab4c-110">You can also use this action to remove any filter that was applied with the **ApplyFilter** action, the **Filter** command on the **Home** tab, or the **Filter Name** or **Where Condition** argument of the **OpenForm** action.</span></span>

<span data-ttu-id="8ab4c-111">Esta ação tem o mesmo efeito que clicar em **alternar filtro** na guia **página inicial** ou clicando com o botão direito do mouse no campo filtraDo e clicando em **Limpar filtro de...** no modo formulário, no modo de exibição de layout ou modo folha de de de base.</span><span class="sxs-lookup"><span data-stu-id="8ab4c-111">This action has the same effect as clicking **Toggle Filter** on the **Home** tab, or right-clicking the filtered field and clicking **Clear filter from...** in Form view, Layout view, or Datasheet view.</span></span>

<span data-ttu-id="8ab4c-112">Para executar a ação **MostrarTodosRegistros** em um módulo do VBA (Visual Basic for Applications), use o método **MostrarTodosRegistros** do objeto **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="8ab4c-112">To run the **ShowAllRecords** action in a Visual Basic for Applications (VBA) module, use the **ShowAllRecords** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="8ab4c-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8ab4c-113">Example</span></span>

<span data-ttu-id="8ab4c-114">**Aplicar um filtro usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="8ab4c-114">**Apply a filter by using a macro**</span></span>

<span data-ttu-id="8ab4c-p102">A macro a seguir contém um conjunto de ações, sendo que cada uma filtra os registros de um formulário Lista de Telefones de Clientes. Ela mostra o uso das ações **AplicarFiltro**, **MostrarTodosRegistros** e **IrParaControle**. Também mostra o uso das condições para determinar qual botão de alternância de um grupo de opções foi selecionado no formulário. Cada linha de ação está associada a um botão de alternância que seleciona o conjunto de registros que começa com A, B, C e assim por diante ou todos os registros. Essa macro deve ser anexada ao evento **ApósAtualizar** do grupo de opções CompanyNameFilter.</span><span class="sxs-lookup"><span data-stu-id="8ab4c-p102">The following macro contains a set of actions, each of which filters the records for a Customer Phone List form. It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions. It also shows the use of conditions to determine which toggle button in an option group has been selected on the form. Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records. This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ab4c-120">Condição</span><span class="sxs-lookup"><span data-stu-id="8ab4c-120">Condition</span></span></p></th>
<th><p><span data-ttu-id="8ab4c-121">Ação</span><span class="sxs-lookup"><span data-stu-id="8ab4c-121">Action</span></span></p></th>
<th><p><span data-ttu-id="8ab4c-122">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="8ab4c-122">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="8ab4c-123">Comentário</span><span class="sxs-lookup"><span data-stu-id="8ab4c-123">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ab4c-124">[Filtros de nome da empresa] = 1</span><span class="sxs-lookup"><span data-stu-id="8ab4c-124">[Company Name Filters] =1</span></span></p></td>
<td><p><span data-ttu-id="8ab4c-125"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="8ab4c-125"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="8ab4c-126"><strong>Condição onde</strong>: [Company Name] like &quot;[AÀÁÂÃÄ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="8ab4c-126"><strong>Where Condition</strong>: [Company Name] Like &quot;[AÀÁÂÃÄ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="8ab4c-127">Filtrar nomes de empresas que começam com A, À, Á, Â, Ã ou Ä.</span><span class="sxs-lookup"><span data-stu-id="8ab4c-127">Filter for company names that start with A, À, Á, Â, Ã, or Ä.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ab4c-128">[Filtros de nome da empresa] = 2</span><span class="sxs-lookup"><span data-stu-id="8ab4c-128">[Company Name Filters] =2</span></span></p></td>
<td><p><span data-ttu-id="8ab4c-129"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="8ab4c-129"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="8ab4c-130"><strong>Condição onde</strong>: [Company Name] like &quot;B \*&quot;</span><span class="sxs-lookup"><span data-stu-id="8ab4c-130"><strong>Where Condition</strong>: [Company Name] Like &quot;B\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="8ab4c-131">Filtrar nomes de empresas que começam com B.</span><span class="sxs-lookup"><span data-stu-id="8ab4c-131">Filter for company names that start with B.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ab4c-132">[Filtros de nome da empresa] = 3</span><span class="sxs-lookup"><span data-stu-id="8ab4c-132">[Company Name Filters] =3</span></span></p></td>
<td><p><span data-ttu-id="8ab4c-133"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="8ab4c-133"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="8ab4c-134"><strong>Condição onde</strong>: [Company Name] like &quot;[CÇ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="8ab4c-134"><strong>Where Condition</strong>: [Company Name] Like &quot;[CÇ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="8ab4c-135">Filtrar nomes de empresas que começam com C ou Ç.</span><span class="sxs-lookup"><span data-stu-id="8ab4c-135">Filter for company names that start with C or Ç.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ab4c-136">.. As linhas de ação de D a Y têm o mesmo formato de A a C...</span><span class="sxs-lookup"><span data-stu-id="8ab4c-136">... Action rows for D through Y have the same format as A through C ...</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ab4c-137">[Filtros de nome da empresa] = 26</span><span class="sxs-lookup"><span data-stu-id="8ab4c-137">[Company Name Filters] =26</span></span></p></td>
<td><p><span data-ttu-id="8ab4c-138"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="8ab4c-138"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="8ab4c-139"><strong>Condição onde</strong>: [Company Name] like &quot;[ZÆØÅ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="8ab4c-139"><strong>Where Condition</strong>: [Company Name] Like &quot;[ZÆØÅ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="8ab4c-140">Filtrar nomes de empresas que começam com Z, Æ, Ø ou Å.</span><span class="sxs-lookup"><span data-stu-id="8ab4c-140">Filter for company names that start with Z, Æ, Ø, or Å.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ab4c-141">[Filtros de nome da empresa] = 27</span><span class="sxs-lookup"><span data-stu-id="8ab4c-141">[Company Name Filters] =27</span></span></p></td>
<td><p><span data-ttu-id="8ab4c-142"><strong>ShowAllRecords</strong></span><span class="sxs-lookup"><span data-stu-id="8ab4c-142"><strong>ShowAllRecords</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="8ab4c-143">Mostra todos os registros.</span><span class="sxs-lookup"><span data-stu-id="8ab4c-143">Show all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ab4c-144">[RecordsetClone]. RecordCount &gt;0</span><span class="sxs-lookup"><span data-stu-id="8ab4c-144">[RecordsetClone].[RecordCount]&gt;0</span></span></p></td>
<td><p><span data-ttu-id="8ab4c-145"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="8ab4c-145"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="8ab4c-146"><strong>Nome do controle</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="8ab4c-146"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="8ab4c-147">Se os registros forem retornados para a letra selecionada, mova o foco para o controle NomeDaEmpresa.</span><span class="sxs-lookup"><span data-stu-id="8ab4c-147">If records are returned for the selected letter, move focus to the CompanyName control.</span></span></p></td>
</tr>
</tbody>
</table>

