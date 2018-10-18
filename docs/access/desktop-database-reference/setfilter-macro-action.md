---
title: Ação de macro DefinirFiltro
TOCTitle: SetFilter Macro Action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4fe2bceb53b835d4c8adab1a1550185c3a7a122a
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606392"
---
# <a name="setfilter-macro-action"></a><span data-ttu-id="22f30-102">Ação de macro DefinirFiltro</span><span class="sxs-lookup"><span data-stu-id="22f30-102">SetFilter Macro Action</span></span>

<span data-ttu-id="22f30-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="22f30-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="22f30-104">Você pode usar a ação **DefinirFiltro** para aplicar um filtro aos registros na folha de dados, formulário, relatório ou tabela ativa.</span><span class="sxs-lookup"><span data-stu-id="22f30-104">You can use the **SetFilter** action to apply a filter to the records in the active datasheet, form, report, or table.</span></span>

## <a name="setting"></a><span data-ttu-id="22f30-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="22f30-105">Setting</span></span>

<span data-ttu-id="22f30-106">A ação **DefinirFiltro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="22f30-106">The **SetFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22f30-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="22f30-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="22f30-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="22f30-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22f30-109">Nome do Filtro</span><span class="sxs-lookup"><span data-stu-id="22f30-109">Filter Name</span></span></p></td>
<span data-ttu-id="22f30-110"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="22f30-110"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="22f30-111">Se for fornecido, o nome de uma consulta ou de um filtro salvo como consulta.</span><span class="sxs-lookup"><span data-stu-id="22f30-111">If provided, the name of a query or of a filter saved as a query.</span></span> <span data-ttu-id="22f30-112">Este argumento ou o argumento WhereCondition é necessário em um banco de dados do cliente.</span><span class="sxs-lookup"><span data-stu-id="22f30-112">This argument or the WhereCondition argument is required in a client database.</span></span> <span data-ttu-id="22f30-113">Um banco de dados da Web, esse argumento não está disponível.</span><span class="sxs-lookup"><span data-stu-id="22f30-113">In a Web database, this argument is not available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22f30-114">Condição Where</span><span class="sxs-lookup"><span data-stu-id="22f30-114">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="22f30-p102">Se for fornecido, uma cláusula SQL WHERE que restringe os registros na folha de dados, no formulário, no relatório ou na tabela. Em um banco de dados da Web, esse argumento é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="22f30-p102">If provided, a SQL WHERE clause that restricts the records in the datasheet, form, report, or table. In a Web database, this argument is required.</span></span></p></td>
=======
<td><p><span data-ttu-id="22f30-117">Se for fornecido, o nome de uma consulta ou de um filtro salvo como consulta.</span><span class="sxs-lookup"><span data-stu-id="22f30-117">If provided, the name of a query or of a filter saved as a query.</span></span> <span data-ttu-id="22f30-118">Este argumento ou o argumento WhereCondition é necessário em um banco de dados do cliente.</span><span class="sxs-lookup"><span data-stu-id="22f30-118">This argument or the WhereCondition argument is required in a client database.</span></span> <span data-ttu-id="22f30-119">Um banco de dados da web, esse argumento não está disponível.</span><span class="sxs-lookup"><span data-stu-id="22f30-119">In a web database, this argument is not available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22f30-120">Condição Where</span><span class="sxs-lookup"><span data-stu-id="22f30-120">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="22f30-121">Se for fornecido, uma cláusula SQL WHERE que restringe os registros na folha de dados, formulário, relatório ou tabela.</span><span class="sxs-lookup"><span data-stu-id="22f30-121">If provided, a SQL WHERE clause that restricts the records in the datasheet, form, report, or table.</span></span> <span data-ttu-id="22f30-122">Um banco de dados da web, este argumento será necessário.</span><span class="sxs-lookup"><span data-stu-id="22f30-122">In a web database, this argument is required.</span></span></p></td><span data-ttu-id="22f30-123">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="22f30-123">
>>>>>>> master</span></span>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22f30-124">Nome do Controle</span><span class="sxs-lookup"><span data-stu-id="22f30-124">Control Name</span></span></p></td>
<td><p><span data-ttu-id="22f30-p105">Se for fornecido, o nome do controle que corresponde ao subformulário ou ao subrelatório a ser filtrado. Se estiver em branco, o objeto atual será filtrado.</span><span class="sxs-lookup"><span data-stu-id="22f30-p105">If provided, the name of the control that corresponds to the subform or subreport to be filtered. If empty, the current object is filtered.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="22f30-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="22f30-127">Remarks</span></span>

<span data-ttu-id="22f30-128">Em um banco de dados da Web, o argumento Condição Where não pode começar por um sinal de igualdade (=).</span><span class="sxs-lookup"><span data-stu-id="22f30-128">In a web database, the Where Condition argument cannot begin with an equal sign (=).</span></span>

<span data-ttu-id="22f30-129">Quando você executar essa ação, o filtro será aplicado à tabela, ao formulário, ao relatório ou à folha de dados (por exemplo, resultado da pesquisa) que está ativa e que tem o foco.</span><span class="sxs-lookup"><span data-stu-id="22f30-129">When you run this action, the filter is applied to the table, form, report or datasheet (for example, query result) that is active and has the focus.</span></span>

<span data-ttu-id="22f30-p106">A propriedade **Filtro** do objeto ativo é usada para salvar o argumento CondiçãoWhere e aplicá-lo posteriormente. Os filtros são salvos com os objetos nos quais foram criados. Eles são automaticamente carregados quando o objeto é aberto, mas não são automaticamente aplicados.</span><span class="sxs-lookup"><span data-stu-id="22f30-p106">The **Filter** property of the active object is used to save the WhereCondition argument and apply it at a later time. Filters are saved with the objects in which they are created. They are automatically loaded when the object is opened, but they are not automatically applied.</span></span>

<span data-ttu-id="22f30-133">Em um banco de dados cliente, para aplicar um filtro automaticamente quando o objeto é aberto, defina a propriedade como **FiltrarNoCarregamento** com o valor True.</span><span class="sxs-lookup"><span data-stu-id="22f30-133">In a client database, to automatically apply a filter when the object is opened, set the **FilterOnLoad** property to True.</span></span>

<span data-ttu-id="22f30-134">Em um banco de dados da Web, para aplicar um filtro automaticamente quando o objeto é aberto, adicione a ação **DefinirFiltro** a uma macro e adicione a macro ao evento **OnLoad** do objeto.</span><span class="sxs-lookup"><span data-stu-id="22f30-134">In a web database, to automatically apply a filter when the object is opened, add the **SetFilter** action to a macro, and add the macro to the object's **OnLoad** event.</span></span>

## <a name="example"></a><span data-ttu-id="22f30-135">Exemplo</span><span class="sxs-lookup"><span data-stu-id="22f30-135">Example</span></span>

<span data-ttu-id="22f30-136">O exemplo a seguir mostra como usar a ação Definirfiltro para filtrar o formulário no qual a macro é definida.</span><span class="sxs-lookup"><span data-stu-id="22f30-136">The following example shows how to use the SetFilter action to filter the form in which the macro is defined.</span></span>

<span data-ttu-id="22f30-137">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="22f30-137">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    SetFilter
        Filter Name
        Where Condtion =[display_name] Like "*cheese*"
        Control Name
```
