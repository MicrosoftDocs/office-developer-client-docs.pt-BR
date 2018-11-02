---
title: Ação da macro DefinirFiltro
TOCTitle: SetFilter macro action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1b21c918f4a55d66cd4e7c7b91cd5612b6309619
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925559"
---
# <a name="setfilter-macro-action"></a><span data-ttu-id="c537f-102">Ação da macro DefinirFiltro</span><span class="sxs-lookup"><span data-stu-id="c537f-102">SetFilter macro action</span></span>

<span data-ttu-id="c537f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c537f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c537f-104">Você pode usar a ação **DefinirFiltro** para aplicar um filtro aos registros na folha de dados, formulário, relatório ou tabela ativa.</span><span class="sxs-lookup"><span data-stu-id="c537f-104">You can use the **SetFilter** action to apply a filter to the records in the active datasheet, form, report, or table.</span></span>

## <a name="setting"></a><span data-ttu-id="c537f-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="c537f-105">Setting</span></span>

<span data-ttu-id="c537f-106">A ação **DefinirFiltro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="c537f-106">The **SetFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c537f-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="c537f-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c537f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c537f-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c537f-109">Nome do Filtro</span><span class="sxs-lookup"><span data-stu-id="c537f-109">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="c537f-110">Se for fornecido, o nome de uma consulta ou de um filtro salvo como consulta.</span><span class="sxs-lookup"><span data-stu-id="c537f-110">If provided, the name of a query or of a filter saved as a query.</span></span> <span data-ttu-id="c537f-111">Este argumento ou o argumento WhereCondition é necessário em um banco de dados do cliente.</span><span class="sxs-lookup"><span data-stu-id="c537f-111">This argument or the WhereCondition argument is required in a client database.</span></span> <span data-ttu-id="c537f-112">Um banco de dados da web, esse argumento não está disponível.</span><span class="sxs-lookup"><span data-stu-id="c537f-112">In a web database, this argument is not available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c537f-113">Condição Where</span><span class="sxs-lookup"><span data-stu-id="c537f-113">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="c537f-114">Se for fornecido, uma cláusula SQL WHERE que restringe os registros na folha de dados, formulário, relatório ou tabela.</span><span class="sxs-lookup"><span data-stu-id="c537f-114">If provided, a SQL WHERE clause that restricts the records in the datasheet, form, report, or table.</span></span> <span data-ttu-id="c537f-115">Um banco de dados da web, este argumento será necessário.</span><span class="sxs-lookup"><span data-stu-id="c537f-115">In a web database, this argument is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c537f-116">Nome do Controle</span><span class="sxs-lookup"><span data-stu-id="c537f-116">Control Name</span></span></p></td>
<td><p><span data-ttu-id="c537f-p103">Se for fornecido, o nome do controle que corresponde ao subformulário ou ao subrelatório a ser filtrado. Se estiver em branco, o objeto atual será filtrado.</span><span class="sxs-lookup"><span data-stu-id="c537f-p103">If provided, the name of the control that corresponds to the subform or subreport to be filtered. If empty, the current object is filtered.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c537f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c537f-119">Remarks</span></span>

<span data-ttu-id="c537f-120">Em um banco de dados da Web, o argumento Condição Where não pode começar por um sinal de igualdade (=).</span><span class="sxs-lookup"><span data-stu-id="c537f-120">In a web database, the Where Condition argument cannot begin with an equal sign (=).</span></span>

<span data-ttu-id="c537f-121">Quando você executar essa ação, o filtro será aplicado à tabela, ao formulário, ao relatório ou à folha de dados (por exemplo, resultado da pesquisa) que está ativa e que tem o foco.</span><span class="sxs-lookup"><span data-stu-id="c537f-121">When you run this action, the filter is applied to the table, form, report or datasheet (for example, query result) that is active and has the focus.</span></span>

<span data-ttu-id="c537f-p104">A propriedade **Filtro** do objeto ativo é usada para salvar o argumento CondiçãoWhere e aplicá-lo posteriormente. Os filtros são salvos com os objetos nos quais foram criados. Eles são automaticamente carregados quando o objeto é aberto, mas não são automaticamente aplicados.</span><span class="sxs-lookup"><span data-stu-id="c537f-p104">The **Filter** property of the active object is used to save the WhereCondition argument and apply it at a later time. Filters are saved with the objects in which they are created. They are automatically loaded when the object is opened, but they are not automatically applied.</span></span>

<span data-ttu-id="c537f-125">Em um banco de dados cliente, para aplicar um filtro automaticamente quando o objeto é aberto, defina a propriedade como **FiltrarNoCarregamento** com o valor True.</span><span class="sxs-lookup"><span data-stu-id="c537f-125">In a client database, to automatically apply a filter when the object is opened, set the **FilterOnLoad** property to True.</span></span>

<span data-ttu-id="c537f-126">Em um banco de dados da Web, para aplicar um filtro automaticamente quando o objeto é aberto, adicione a ação **DefinirFiltro** a uma macro e adicione a macro ao evento **OnLoad** do objeto.</span><span class="sxs-lookup"><span data-stu-id="c537f-126">In a web database, to automatically apply a filter when the object is opened, add the **SetFilter** action to a macro, and add the macro to the object's **OnLoad** event.</span></span>

## <a name="example"></a><span data-ttu-id="c537f-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c537f-127">Example</span></span>

<span data-ttu-id="c537f-128">O exemplo a seguir mostra como usar a ação Definirfiltro para filtrar o formulário no qual a macro é definida.</span><span class="sxs-lookup"><span data-stu-id="c537f-128">The following example shows how to use the SetFilter action to filter the form in which the macro is defined.</span></span>

<span data-ttu-id="c537f-129">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="c537f-129">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
