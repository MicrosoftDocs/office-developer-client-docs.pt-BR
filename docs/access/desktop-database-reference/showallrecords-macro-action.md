---
title: Ação de Macro ShowAllRecords
TOCTitle: ShowAllRecords Macro Action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b6482bcd34562e13e1783f8e0702718eeaed0b0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881731"
---
# <a name="showallrecords-macro-action"></a><span data-ttu-id="ed566-102">Ação de Macro ShowAllRecords</span><span class="sxs-lookup"><span data-stu-id="ed566-102">ShowAllRecords Macro Action</span></span>


<span data-ttu-id="ed566-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed566-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="ed566-104">Você pode usar a ação **MostrarTodosRegistros** para remover qualquer filtro aplicado da tabela ativa, do conjunto de resultados de consulta ou do formulário e exibir todos os registros na tabela ou resultado conjunto ou todos os registros na tabela base do formulário ou uma consulta.</span><span class="sxs-lookup"><span data-stu-id="ed566-104">You can use the **ShowAllRecords** action to remove any applied filter from the active table, query result set, or form, and display all records in the table or result set or all records in the form's underlying table or query.</span></span>

## <a name="setting"></a><span data-ttu-id="ed566-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="ed566-105">Setting</span></span>

<span data-ttu-id="ed566-106">A ação **MostrarTodosRegistros** não tem nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="ed566-106">The **ShowAllRecords** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed566-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed566-107">Remarks</span></span>

<span data-ttu-id="ed566-108">Você pode usar esta ação para garantir que todos os registros (incluindo quaisquer registros novos ou alterados) sejam exibidos para uma tabela, um conjunto de resultados de consulta ou um formulário.</span><span class="sxs-lookup"><span data-stu-id="ed566-108">You can use this action to ensure that all records (including any changed or new records) are displayed for a table, query result set, or form.</span></span> <span data-ttu-id="ed566-109">Esta ação faz com que a repetição da consulta dos registros para um formulário ou subformulário.</span><span class="sxs-lookup"><span data-stu-id="ed566-109">This action causes a requery of the records for a form or subform.</span></span>

<span data-ttu-id="ed566-110">Você também pode usar esta ação para remover qualquer filtro que tenha sido aplicado com a ação **AplicarFiltro** , o comando de **filtro** na guia **página inicial** , ou o **Nome do filtro** ou argumento **Condição Where** da ação **AbrirFormulário** .</span><span class="sxs-lookup"><span data-stu-id="ed566-110">You can also use this action to remove any filter that was applied with the **ApplyFilter** action, the **Filter** command on the **Home** tab, or the **Filter Name** or **Where Condition** argument of the **OpenForm** action.</span></span>

<span data-ttu-id="ed566-111">Essa ação tem o mesmo efeito que clicar em **Filtro de alternância** na guia **Home** , ou clicando o campo filtrado e clicando em **Limpar filtro da …** no modo formulário, modo de exibição de Layout ou modo folha de dados.</span><span class="sxs-lookup"><span data-stu-id="ed566-111">This action has the same effect as clicking **Toggle Filter** on the **Home** tab, or right-clicking the filtered field and clicking **Clear filter from...** in Form view, Layout view, or Datasheet view.</span></span>

<span data-ttu-id="ed566-112">Para executar a ação **MostrarTodosRegistros** em um módulo Visual Basic for Applications (VBA), use o método **ShowAllRecords** do objeto **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="ed566-112">To run the **ShowAllRecords** action in a Visual Basic for Applications (VBA) module, use the **ShowAllRecords** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="ed566-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed566-113">Example</span></span>

<span data-ttu-id="ed566-114">**Aplicar um filtro usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="ed566-114">**Apply a filter by using a macro**</span></span>

<span data-ttu-id="ed566-p102">A macro a seguir contém um conjunto de ações, sendo que cada uma filtra os registros de um formulário Lista de Telefones de Clientes. Ela mostra o uso das ações **AplicarFiltro**, **MostrarTodosRegistros** e **IrParaControle**. Também mostra o uso das condições para determinar qual botão de alternância de um grupo de opções foi selecionado no formulário. Cada linha de ação está associada a um botão de alternância que seleciona o conjunto de registros que começa com A, B, C e assim por diante ou todos os registros. Essa macro deve ser anexada ao evento **ApósAtualizar** do grupo de opções CompanyNameFilter.</span><span class="sxs-lookup"><span data-stu-id="ed566-p102">The following macro contains a set of actions, each of which filters the records for a Customer Phone List form. It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions. It also shows the use of conditions to determine which toggle button in an option group has been selected on the form. Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records. This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ed566-120">Condição</span><span class="sxs-lookup"><span data-stu-id="ed566-120">Condition</span></span></p></th>
<th><p><span data-ttu-id="ed566-121">Ação</span><span class="sxs-lookup"><span data-stu-id="ed566-121">Action</span></span></p></th>
<th><p><span data-ttu-id="ed566-122">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="ed566-122">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="ed566-123">Comentário</span><span class="sxs-lookup"><span data-stu-id="ed566-123">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed566-124">[Filtros de nome da empresa] = 1</span><span class="sxs-lookup"><span data-stu-id="ed566-124">[Company Name Filters] =1</span></span></p></td>
<td><p><span data-ttu-id="ed566-125"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="ed566-125"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="ed566-126"><strong>Condição onde</strong>: [Company Name] como &quot;[AÀÁÂÃÄ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="ed566-126"><strong>Where Condition</strong>: [Company Name] Like &quot;[AÀÁÂÃÄ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="ed566-127">Filtrar nomes de empresas que começam com A, À, Á, Â, Ã ou Ä.</span><span class="sxs-lookup"><span data-stu-id="ed566-127">Filter for company names that start with A, À, Á, Â, Ã, or Ä.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed566-128">[Filtros de nome da empresa] = 2</span><span class="sxs-lookup"><span data-stu-id="ed566-128">[Company Name Filters] =2</span></span></p></td>
<td><p><span data-ttu-id="ed566-129"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="ed566-129"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="ed566-130"><strong>Condição onde</strong>: [Company Name] como &quot;B \*&quot;</span><span class="sxs-lookup"><span data-stu-id="ed566-130"><strong>Where Condition</strong>: [Company Name] Like &quot;B\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="ed566-131">Filtrar nomes de empresas que começam com B.</span><span class="sxs-lookup"><span data-stu-id="ed566-131">Filter for company names that start with B.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed566-132">[Filtros de nome da empresa] = 3</span><span class="sxs-lookup"><span data-stu-id="ed566-132">[Company Name Filters] =3</span></span></p></td>
<td><p><span data-ttu-id="ed566-133"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="ed566-133"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="ed566-134"><strong>Condição onde</strong>: [Company Name] como &quot;[CÇ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="ed566-134"><strong>Where Condition</strong>: [Company Name] Like &quot;[CÇ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="ed566-135">Filtrar nomes de empresas que começam com C ou Ç.</span><span class="sxs-lookup"><span data-stu-id="ed566-135">Filter for company names that start with C or Ç.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed566-136">.. As linhas de ação de D a Y têm o mesmo formato de A a C...</span><span class="sxs-lookup"><span data-stu-id="ed566-136">... Action rows for D through Y have the same format as A through C ...</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed566-137">[Filtros de nome da empresa] = 26</span><span class="sxs-lookup"><span data-stu-id="ed566-137">[Company Name Filters] =26</span></span></p></td>
<td><p><span data-ttu-id="ed566-138"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="ed566-138"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="ed566-139"><strong>Condição onde</strong>: [Company Name] como &quot;[ZÆØÅ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="ed566-139"><strong>Where Condition</strong>: [Company Name] Like &quot;[ZÆØÅ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="ed566-140">Filtrar nomes de empresas que começam com Z, Æ, Ø ou Å.</span><span class="sxs-lookup"><span data-stu-id="ed566-140">Filter for company names that start with Z, Æ, Ø, or Å.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed566-141">[Filtros de nome da empresa] = 27</span><span class="sxs-lookup"><span data-stu-id="ed566-141">[Company Name Filters] =27</span></span></p></td>
<td><p><span data-ttu-id="ed566-142"><strong>ShowAllRecords</strong></span><span class="sxs-lookup"><span data-stu-id="ed566-142"><strong>ShowAllRecords</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ed566-143">Mostra todos os registros.</span><span class="sxs-lookup"><span data-stu-id="ed566-143">Show all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed566-144">[RecordsetClone]. [RecordCount] &gt;0</span><span class="sxs-lookup"><span data-stu-id="ed566-144">[RecordsetClone].[RecordCount]&gt;0</span></span></p></td>
<td><p><span data-ttu-id="ed566-145"><strong>IrParaControle</strong></span><span class="sxs-lookup"><span data-stu-id="ed566-145"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="ed566-146"><strong>Nome do controle</strong>: NomeDaEmpresa</span><span class="sxs-lookup"><span data-stu-id="ed566-146"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="ed566-147">Se os registros forem retornados para a letra selecionada, mova o foco para o controle NomeDaEmpresa.</span><span class="sxs-lookup"><span data-stu-id="ed566-147">If records are returned for the selected letter, move focus to the CompanyName control.</span></span></p></td>
</tr>
</tbody>
</table>

