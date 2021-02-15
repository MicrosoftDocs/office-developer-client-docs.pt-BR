---
title: Ação da macro AbrirRelatório
TOCTitle: OpenReport macro action
ms:assetid: cd35faf2-190d-ac48-cf59-81c1599eb764
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834462(v=office.15)
ms:contentKeyID: 48547758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm188079
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cff57a185d226328792bef79072dfc46c6134f98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288347"
---
# <a name="openreport-macro-action"></a><span data-ttu-id="763bf-102">Ação da macro AbrirRelatório</span><span class="sxs-lookup"><span data-stu-id="763bf-102">OpenReport macro action</span></span>

<span data-ttu-id="763bf-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="763bf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="763bf-p101">Você pode usar a ação **AbrirRelatório** para abrir um relatório em modo Design ou Visualizar Impressão, ou para enviar o relatório diretamente para a impressora. Também pode restringir os registros impressos no relatório.</span><span class="sxs-lookup"><span data-stu-id="763bf-p101">You can use the **OpenReport** action to open a report in Design view or Print Preview, or to send the report directly to the printer. You can also restrict the records that are printed in the report.</span></span>

## <a name="setting"></a><span data-ttu-id="763bf-106">Setting</span><span class="sxs-lookup"><span data-stu-id="763bf-106">Setting</span></span>

<span data-ttu-id="763bf-107">A ação **AbrirRelatório** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="763bf-107">The **OpenReport** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="763bf-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="763bf-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="763bf-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="763bf-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="763bf-110">Nome do relatório</span><span class="sxs-lookup"><span data-stu-id="763bf-110">Report Name</span></span></p></td>
<td><p><span data-ttu-id="763bf-111">O nome do relatório que será aberto.</span><span class="sxs-lookup"><span data-stu-id="763bf-111">The name of the report to open.</span></span> <span data-ttu-id="763bf-112">A <strong>caixa Nome do</strong> Relatório na seção <strong>Argumentos da</strong> Ação do painel Construtor de <strong>Macros</strong> mostra todos os relatórios no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="763bf-112">The <strong>Report Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane shows all reports in the current database.</span></span> <span data-ttu-id="763bf-113">Esse é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="763bf-113">This is a required argument.</span></span> <span data-ttu-id="763bf-114">Se você executar uma macro que contém a ação AbrirRelatório em um banco de dados biblioteca, o Microsoft Access procurará o relatório com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="763bf-114">If you run a macro containing the OpenReport action in a library database, Microsoft Access first looks for the report with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="763bf-115">Exibir</span><span class="sxs-lookup"><span data-stu-id="763bf-115">View</span></span></p></td>
<td><p><span data-ttu-id="763bf-p103">O modo de exibição no qual o relatório será aberto. Clique em <strong>Imprimir</strong> (imprimir o relatório imediatamente), <strong>Design</strong> ou <strong>Visualizar Impressão</strong> na caixa <strong>Modo de Exibição</strong>. O padrão é <strong>Imprimir</strong>.</span><span class="sxs-lookup"><span data-stu-id="763bf-p103">The view in which the report will open. Click <strong>Print</strong> (print the report immediately), <strong>Design</strong>, or <strong>Print Preview</strong> in the <strong>View</strong> box. The default is <strong>Print</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="763bf-119">Nome do Filtro</span><span class="sxs-lookup"><span data-stu-id="763bf-119">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="763bf-p104">Um filtro que restringe os registros do relatório. Você pode digitar o nome de uma consulta existente ou de um filtro que foi salvo como consulta. Entretanto, a consulta precisa incluir todos os campos no relatório que você está abrindo ou ter a propriedade <strong>SaídaTodosOsCampos</strong> definida como <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="763bf-p104">A filter that restricts the report's records. You can enter the name of either an existing query or a filter that was saved as a query. However, the query must include all the fields in the report you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="763bf-123">Condição Where</span><span class="sxs-lookup"><span data-stu-id="763bf-123">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="763bf-124">Uma cláusula SQL WHERE  (sem a palavra WHERE) válida ou expressão que o Access usa para selecionar registros da tabela ou consulta subjacente do relatório.</span><span class="sxs-lookup"><span data-stu-id="763bf-124">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the report's underlying table or query.</span></span> <span data-ttu-id="763bf-125">Se você selecionar um filtro com o argumento Nome do Filtro, o Access aplicará essa cláusula WHERE aos resultados do filtro.</span><span class="sxs-lookup"><span data-stu-id="763bf-125">If you select a filter with the Filter Name argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="763bf-126">Para abrir um relatório e restringir seus registros àqueles especificados pelo valor de um controle em um relatório, use a expressão a seguir:</span><span class="sxs-lookup"><span data-stu-id="763bf-126">To open a report and restrict its records to those specified by the value of a control on a form, use the following expression:</span></span><br /><span data-ttu-id="763bf-127">
<strong>[</strong><em>nome_do_campo</em><strong>] = Formulários![</strong><em>nome_do_formulário</em><strong>]![</strong><em>nome do controle em um formulário</em><strong>]</strong></span><span class="sxs-lookup"><span data-stu-id="763bf-127">
<strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on form</em><strong>]</strong></span></span><br />
<span data-ttu-id="763bf-128">Substitua <em>nome_do_campo</em> pelo nome de um campo na tabela ou consulta subjacente do relatório que será aberto.</span><span class="sxs-lookup"><span data-stu-id="763bf-128">Replace <em>fieldname</em> with the name of a field in the underlying table or query of the report you want to open.</span></span> <span data-ttu-id="763bf-129">Substitua <em>o nome do</em> formulário e o nome do controle no formulário pelo nome do formulário e o controle no formulário que contém o valor que você deseja que os registros do relatório sejam igualmente. <em></em></span><span class="sxs-lookup"><span data-stu-id="763bf-129">Replace <em>formname</em> and <em>controlname on form</em> with the name of the form and the control on the form that contains the value you want records in the report to match.</span></span></p>
<p><span data-ttu-id="763bf-130"><b>OBSERVAÇÃO:</b>o comprimento máximo do argumento Condição Where é de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="763bf-130"><b>NOTE</b>: The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="763bf-131">Se você precisar inserir uma cláusula SQL WHERE mais complexa e extensa do que essa, use o método <b>OpenReport</b> do objeto <b>DoCmd</b> em um módulo do VBA (Visual Basic for Applications).</span><span class="sxs-lookup"><span data-stu-id="763bf-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <b>OpenReport</b> method of the <b>DoCmd</b> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="763bf-132">É possível inserir instruções de cláusulas SQL WHERE de até 32.768 caracteres no VBA.</span><span class="sxs-lookup"><span data-stu-id="763bf-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="763bf-133">Modo Janela</span><span class="sxs-lookup"><span data-stu-id="763bf-133">Window Mode</span></span></p></td>
<td><p><span data-ttu-id="763bf-134">O modo no qual o relatório será aberto.</span><span class="sxs-lookup"><span data-stu-id="763bf-134">The mode in which the report will open.</span></span> <span data-ttu-id="763bf-135">Clique <strong>em Normal</strong>, <strong>Oculto</strong>, <strong>Ícone</strong>ou <strong>Caixa de</strong> Diálogo na caixa Modo <strong>janela.</strong></span><span class="sxs-lookup"><span data-stu-id="763bf-135">Click <strong>Normal</strong>, <strong>Hidden</strong>, <strong>Icon</strong>, or <strong>Dialog</strong> in the <strong>Window Mode</strong> box.</span></span> <span data-ttu-id="763bf-136">O padrão é <strong>Normal</strong>.</span><span class="sxs-lookup"><span data-stu-id="763bf-136">The default is <strong>Normal</strong>.</span></span></p>
<p><span data-ttu-id="763bf-137"><b>OBSERVAÇÃO:</b>algumas configurações de argumento do Modo Janela não se aplicam ao usar documentos com guias.</span><span class="sxs-lookup"><span data-stu-id="763bf-137"><b>NOTE</b>: Some Window Mode argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="763bf-138">Para alternar para janelas sobrepostas:</span><span class="sxs-lookup"><span data-stu-id="763bf-138">To switch to overlapping windows:</span></span>
<ol>
<li><p><span data-ttu-id="763bf-139">Clique em <strong>Opções</strong>.</span><span class="sxs-lookup"><span data-stu-id="763bf-139">Click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="763bf-140">Na caixa de diálogo <strong>Opções do Access</strong>, clique em <strong>Banco de Dados Atual</strong>.</span><span class="sxs-lookup"><span data-stu-id="763bf-140">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="763bf-141">Na seção <strong>Opções do Aplicativo</strong>, em <strong>Opções de Janela de Documento</strong>, clique em <strong>Janelas Sobrepostas</strong>.</span><span class="sxs-lookup"><span data-stu-id="763bf-141">In the <strong>Application Options</strong> section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="763bf-142">Clique <strong>em OK</strong>e feche e reabra o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="763bf-142">Click <strong>OK</strong>, and then close and reopen the database.</span></span></p></li>
</ol>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="763bf-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="763bf-143">Remarks</span></span>

<span data-ttu-id="763bf-p110">A configuração **Imprimir** do argumento **Modo de Exibição** imprime o relatório imediatamente usando as configurações de impressora atuais, sem exibir a caixa de diálogo **Imprimir**. Você também pode usar a ação **AbrirRelatório** para abrir e configurar um relatório e usar a ação Imprimir para imprimi-lo. Por exemplo, convém modificar o relatório ou usar a ação **Imprimir** para alterar as configurações de impressora antes de imprimir.</span><span class="sxs-lookup"><span data-stu-id="763bf-p110">The **Print** setting for the **View** argument prints the report immediately by using the current printer settings, without bringing up the **Print** dialog box. You can also use the **OpenReport** action to open and set up a report and then use the PrintOut action to print it. For example, you may want to modify the report or use the **PrintOut** action to change the printer settings before you print.</span></span>

<span data-ttu-id="763bf-147">O filtro e a condição WHERE aplicados se tornam a configuração da propriedade **Filtro** do relatório.</span><span class="sxs-lookup"><span data-stu-id="763bf-147">The filter and WHERE condition you apply become the setting of the report's **Filter** property.</span></span>

<span data-ttu-id="763bf-148">A ação **AbrirRelatório** é semelhante a clicar duas vezes no relatório do Painel de Navegação ou a clicar com o botão direito do mouse no relatório do Painel de Navegação e selecionar um modo de exibição ou o comando **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="763bf-148">The **OpenReport** action is similar to double-clicking the report in the Navigation Pane, or right-clicking the report in the Navigation Pane and selecting a view or the **Print** command.</span></span>

> [!TIP] 
> - <span data-ttu-id="763bf-149">Para imprimir relatórios semelhantes para diferentes conjuntos de dados, use um filtro ou uma cláusula WHERE para restringir os registros impressos no relatório.</span><span class="sxs-lookup"><span data-stu-id="763bf-149">To print similar reports for different sets of data, use a filter or a WHERE clause to restrict the records printed in the report.</span></span> <span data-ttu-id="763bf-150">Edite a macro para aplicar um filtro diferente ou altere o argumento Condição Onde.</span><span class="sxs-lookup"><span data-stu-id="763bf-150">Then edit the macro to apply a different filter or change the Where Condition argument.</span></span>
> 
> - <span data-ttu-id="763bf-p112">Você pode arrastar um relatório do Painel de Navegação para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirRelatório** que abre o relatório em modo Relatório.</span><span class="sxs-lookup"><span data-stu-id="763bf-p112">You can drag a report from the Navigation Pane to a macro action row. This automatically creates an **OpenReport** action that opens the report in Report view.</span></span>

## <a name="example"></a><span data-ttu-id="763bf-153">Exemplo</span><span class="sxs-lookup"><span data-stu-id="763bf-153">Example</span></span>

<span data-ttu-id="763bf-154">O exemplo a seguir mostra como usar a ação Abrir Relatório para passar um parâmetro que filtra um relatório à medida que ele é aberto.</span><span class="sxs-lookup"><span data-stu-id="763bf-154">The following example shows how to use the OpenReport action to pass a parameter that filters a report as it is opened.</span></span> <span data-ttu-id="763bf-155">O **relatório rptChapters** exibe os registros do autor especificado passando o item selecionado na caixa de combinação **cboAuthors** para o parâmetro SelectedAuthor.</span><span class="sxs-lookup"><span data-stu-id="763bf-155">The **rptChapters** report displays the records for the specified author by passing the item selected in the **cboAuthors** combo box to the SelectedAuthor parameter.</span></span>

<span data-ttu-id="763bf-156">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="763bf-156">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenReport
        Report Name rptChapters
        View Report
        Filter Name
        Where Condition
        Window Mode Normal
    
    Parameters
        SelectedAuthor =[cboAuthor]
```
