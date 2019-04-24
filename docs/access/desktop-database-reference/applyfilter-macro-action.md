---
title: Ação da macro AplicarFiltro
TOCTitle: ApplyFilter macro action
ms:assetid: c63988c4-4506-cc51-98f7-478d1f3fe668
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823130(v=office.15)
ms:contentKeyID: 48547623
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm79035
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e79ab56778f9429e7f1a985f0f81864ae4363606
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296994"
---
# <a name="applyfilter-macro-action"></a><span data-ttu-id="3bd52-102">Ação da macro AplicarFiltro</span><span class="sxs-lookup"><span data-stu-id="3bd52-102">ApplyFilter macro action</span></span>

<span data-ttu-id="3bd52-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3bd52-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3bd52-p101">Você pode usar a ação **AplicarFiltro** para aplicar um filtro, uma consulta ou uma cláusula SQL WHERE a uma tabela, um formulário ou um relatório para restringir ou classificar os registros da tabela, ou os registros da tabela ou consulta subjacente do formulário ou relatório. Para relatórios, é possível usar esta ação somente em uma macro especificada pela propriedade de evento **AoAbrir** do relatório.</span><span class="sxs-lookup"><span data-stu-id="3bd52-p101">You can use the **ApplyFilter** action to apply a filter, a query, or an SQL WHERE clause to a table, form, or report to restrict or sort the records in the table, or the records from the underlying table or query of the form or report. For reports, you can use this action only in a macro specified by the report's **OnOpen** event property.</span></span>

> [!NOTE]
> <span data-ttu-id="3bd52-p102">[!OBSERVAçãO] Você pode usar esta ação para aplicar uma cláusula WHERE do SQL apenas ao aplicar um filtro de servidor. Um filtro de servidor não pode ser aplicado a uma fonte de registros do procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="3bd52-p102">You can use this action to apply an SQL WHERE clause only when applying a server filter. A server filter cannot be applied to a stored procedure's record source.</span></span>

## <a name="setting"></a><span data-ttu-id="3bd52-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="3bd52-108">Setting</span></span>

<span data-ttu-id="3bd52-109">A ação **AplicarFiltro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="3bd52-109">The **ApplyFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3bd52-110">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="3bd52-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3bd52-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="3bd52-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3bd52-112">Nome do Filtro</span><span class="sxs-lookup"><span data-stu-id="3bd52-112">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="3bd52-113">O nome de um filtro ou consulta que restringe ou classifica os registros da tabela, do formulário ou do relatório.</span><span class="sxs-lookup"><span data-stu-id="3bd52-113">The name of a filter or query that restricts or sorts the records of the table, form, or report.</span></span> <span data-ttu-id="3bd52-114">Você pode inserir o nome de uma consulta existente ou de um filtro que tenha sido salvo como uma consulta na caixa <strong>nome do filtro</strong> na seção <strong>argumentos da ação</strong> do painel <strong>Construtor</strong> de macros.</span><span class="sxs-lookup"><span data-stu-id="3bd52-114">You can enter the name of either an existing query or a filter that has been saved as a query in the <strong>Filter Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane.</span></span></p><p><span data-ttu-id="3bd52-115"><strong>Observação</strong>: quando você estiver usando esta ação para aplicar um filtro de servidor, o argumento Nome do filtro deverá ficar em branco.</span><span class="sxs-lookup"><span data-stu-id="3bd52-115"><strong>NOTE</strong>: When you are using this action to apply a server filter, the Filter Name argument must be blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bd52-116">Condição Where</span><span class="sxs-lookup"><span data-stu-id="3bd52-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="3bd52-117">Uma cláusula SQL WHERE válida (sem a palavra WHERE) ou uma expressão que restringe os registros da tabela, do formulário ou do relatório.</span><span class="sxs-lookup"><span data-stu-id="3bd52-117">A valid SQL WHERE clause (without the word WHERE) or an expression that restricts the records of the table, form, or report.</span></span></p>
<p><span data-ttu-id="3bd52-118"><b>Observação</b>: em uma expressão de argumento condição onde, o lado esquerdo da expressão normalmente contém um nome de campo da tabela ou consulta base para o formulário ou relatório.</span><span class="sxs-lookup"><span data-stu-id="3bd52-118"><b>NOTE</b>: In a Where Condition argument expression, the left side of the expression typically contains a field name from the underlying table or query for the form or report.</span></span> <span data-ttu-id="3bd52-119">O lado direito da expressão normalmente contém os critérios que você deseja aplicar a esse campo para restringir ou classificar os registros.</span><span class="sxs-lookup"><span data-stu-id="3bd52-119">The right side of the expression typically contains the criteria you want to apply to this field to restrict or sort the records.</span></span> <span data-ttu-id="3bd52-120">Por exemplo, os critérios podem ser o nome de um controle em outro formulário que contém o valor com o qual você deseja que os registros do primeiro formulário correspondam.</span><span class="sxs-lookup"><span data-stu-id="3bd52-120">For example, the criteria can be the name of a control on another form that contains the value you want the records in the first form to match.</span></span> <span data-ttu-id="3bd52-121">O nome do controle deve ser totalmente qualificado, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="3bd52-121">The name of the control should be fully qualified, for example:</span></span></p>
<p><span data-ttu-id="3bd52-122"><strong>Formulários</strong>! <em>FormName</em>! <em>ControlName</em> Os nomes de campo devem ser circundados por aspas duplas e os literais de cadeia de caracteres devem ser circundados por aspas simples.</span><span class="sxs-lookup"><span data-stu-id="3bd52-122"><strong>Forms</strong>!<em>formname</em>!<em>controlname</em> Field names should be surrounded by double quotation marks and string literals should be surrounded by single quotation marks.</span></span> <span data-ttu-id="3bd52-123">A extensão máxima do argumento Condição Onde é de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3bd52-123">The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="3bd52-124">Se precisar usar uma cláusula SQL WHERE mais extensa, use o método <strong>ApplyFilter</strong> do objeto <strong>DoCmd</strong> em um módulo do VBA (Visual Basic for Applications).</span><span class="sxs-lookup"><span data-stu-id="3bd52-124">If you need to enter a longer SQL WHERE clause, use the <strong>ApplyFilter</strong> method of the <strong>DoCmd</strong> object in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="3bd52-125">Você pode inserir instruções de cláusula SQL WHERE de até 32.768 caracteres no VBA.</span><span class="sxs-lookup"><span data-stu-id="3bd52-125">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="3bd52-126">[!OBSERVAçãO] Use o argumento Nome do Filtro se você já tiver definido um filtro que forneça os dados apropriados.</span><span class="sxs-lookup"><span data-stu-id="3bd52-126">You can use the Filter Name argument if you have already defined a filter that provides the appropriate data.</span></span> <span data-ttu-id="3bd52-127">É possível usar o argumento Where Condition para inserir diretamente os critérios de restrição.</span><span class="sxs-lookup"><span data-stu-id="3bd52-127">You can use the Where Condition argument to enter the restriction criteria directly.</span></span> <span data-ttu-id="3bd52-128">Se você usar ambos os argumentos, o Microsoft Office Access 2007 aplicará a cláusula WHERE aos resultados do filtro.</span><span class="sxs-lookup"><span data-stu-id="3bd52-128">If you use both arguments, Microsoft Office Access 2007 applies the WHERE clause to the results of the filter.</span></span> <span data-ttu-id="3bd52-129">Use um dos argumentos, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="3bd52-129">You must use one or both arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bd52-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bd52-130">Remarks</span></span>

<span data-ttu-id="3bd52-131">Você pode aplicar um filtro ou uma consulta a um formulário no modo Formulário ou no modo Folha de Dados.</span><span class="sxs-lookup"><span data-stu-id="3bd52-131">You can apply a filter or query to a form in Form view or Datasheet view.</span></span>

<span data-ttu-id="3bd52-132">O filtro e a condição WHERE aplicados tornam-se a configuração da propriedade **Filtrar** ou **ServerFilter** do formulário ou relatório.</span><span class="sxs-lookup"><span data-stu-id="3bd52-132">The filter and WHERE condition you apply become the setting of the form's or report's **Filter** or **ServerFilter** property.</span></span>

<span data-ttu-id="3bd52-p107">Para tabelas e formulários, esta ação é semelhante a clicar em **Aplicar Filtro/Classificar** ou **Aplicar Filtro do Servidor** no menu **Registros**. O comando do menu aplica o filtro criado mais recentemente à tabela ou ao formulário, enquanto a ação **AplicarFiltro** aplica um filtro ou consulta especificado.</span><span class="sxs-lookup"><span data-stu-id="3bd52-p107">For tables and forms, this action is similar to clicking **Apply Filter/Sort** or **Apply Server Filter** on the **Records** menu. The menu command applies the most recently created filter to the table or form, whereas the **ApplyFilter** action applies a specified filter or query.</span></span>

<span data-ttu-id="3bd52-135">Em um banco de dados do Access, se você apontar para **Filtrar** no menu **Registros** e clicar em **Filtrar/Classificar Avançado** após executar a ação **AplicarFiltro**, a janela Filtrar/Classificar Avançado mostrará os critérios de filtragem selecionados com esta ação.</span><span class="sxs-lookup"><span data-stu-id="3bd52-135">In an Access database, if you point to **Filter** on the **Records** menu and then click **Advanced Filter/Sort** after running the **ApplyFilter** action, the Advanced Filter/Sort window shows the filter criteria you have selected with this action.</span></span>

<span data-ttu-id="3bd52-p108">Para remover um filtro e exibir todos os registros de uma tabela ou formulário em um banco de dados do Office Access 2007, você pode usar a ação **MostrarTodosRegistros** ou o comando **Remover Filtro/Classificação** no menu **Registros**. Para remover um filtro em um projeto do Access (.adp), você pode retornar para a janela Filtro do Servidor por Formulário, remover todos os critérios de filtragem e clicar em **Aplicar Filtro do Servidor** no menu **Registros** da barra de ferramentas ou definir a propriedade **ServerFilterByForm** como **False** (0).</span><span class="sxs-lookup"><span data-stu-id="3bd52-p108">To remove a filter and display all of the records for a table or form in an Office Access 2007 database, you can use the **ShowAllRecords** action or the **Remove Filter/Sort** command on the **Records** menu. To remove a filter in an Access project (.adp), you can return to the Server Filter By Form window and remove all filter criteria and then click **Apply Server Filter** on the **Records** menu on the toolbar, or set the **ServerFilterByForm** property to **False** (0).</span></span>

<span data-ttu-id="3bd52-p109">Quando você salvar uma tabela ou um formulário, o Access salvará todo filtro definido no momento nesse projeto, mas não aplicará esses filtros automaticamente na próxima vez em que o objeto for aberto (apesar de que aplicará automaticamente qualquer classificação aplicada ao objeto antes de ser salvo). Se desejar aplicar um filtro automaticamente quando um formulário for aberto pela primeira vez, especifique uma macro que contenha a ação **AplicarFiltro** ou um procedimento de evento que contenha o método **ApplyFilter** do objeto **DoCmd** como sendo a configuração da propriedade de evento **AoAbrir** do formulário. Você também pode aplicar um filtro usando a ação **AbrirFormulário** ou **AbrirRelatório** ou seus métodos correspondentes. Para aplicar um filtro automaticamente quando uma tabela for aberta pela primeira vez, você pode abrir a tabela usando uma macro que contenha a ação **AbrirTabela**, seguida imediatamente pela ação **AplicarFiltro**.</span><span class="sxs-lookup"><span data-stu-id="3bd52-p109">When you save a table or form, Access saves any filter currently defined in that object, but won't apply the filter automatically the next time the object is opened (although it will automatically apply any sort you applied to the object before it was saved). If you want to apply a filter automatically when a form is first opened, specify a macro containing the **ApplyFilter** action or an event procedure containing the **ApplyFilter** method of the **DoCmd** object as the **OnOpen** event property setting of the form. You can also apply a filter by using the **OpenForm** or **OpenReport** action, or their corresponding methods. To apply a filter automatically when a table is first opened, you can open the table by using a macro containing the **OpenTable** action, followed immediately by the **ApplyFilter** action.</span></span>

## <a name="example"></a><span data-ttu-id="3bd52-142">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3bd52-142">Example</span></span>

<span data-ttu-id="3bd52-143">O exemplo a seguir mostra como usar a ação AplicarFiltro para filtrar o formulário frmFoods quando ele é aberto.</span><span class="sxs-lookup"><span data-stu-id="3bd52-143">The following example shows how to use the ApplyFilter action to filter the frmFoods form as it is opened.</span></span>

<span data-ttu-id="3bd52-144">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="3bd52-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    ApplyFilter
        Filter Name
        Where Condition=[display_name] Link "*cheese*"
        Control Name
```



