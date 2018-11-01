---
title: Ação de macro ExportarcomFormatação
TOCTitle: ExportWithFormatting Macro Action
ms:assetid: 8926dfa3-bf11-30ab-0f85-46f0a4961784
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197066(v=office.15)
ms:contentKeyID: 48546152
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm159503
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8a0ca9d2dde2ae5d39fb9159655f37b5140eee3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868012"
---
# <a name="exportwithformatting-macro-action"></a><span data-ttu-id="82e22-102">Ação de macro ExportarcomFormatação</span><span class="sxs-lookup"><span data-stu-id="82e22-102">ExportWithFormatting Macro Action</span></span>


<span data-ttu-id="82e22-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="82e22-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82e22-104">Você pode usar a ação **ExportarcomFormatação** para gerar a saída dos dados do objeto de banco de dados do Microsoft Access especificado (uma folha de dados, um formulário, um relatório, um módulo ou uma página de acesso a dados) para vários formatos de saída.</span><span class="sxs-lookup"><span data-stu-id="82e22-104">You can use the **ExportWithFormatting** action to output the data in the specified Microsoft Access database object (a datasheet, form, report, module, or data access page) to several output formats.</span></span>

## <a name="settings"></a><span data-ttu-id="82e22-105">Configurações</span><span class="sxs-lookup"><span data-stu-id="82e22-105">Settings</span></span>

<span data-ttu-id="82e22-106">A ação **ExportarcomFormatação** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="82e22-106">The **ExportWithFormatting** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82e22-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="82e22-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="82e22-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="82e22-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82e22-109"><strong>Tipo de Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="82e22-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="82e22-p101">O tipo de objeto que contém os dados para gerar saída. Clique em <strong>Tabela</strong> (para uma folha de dados de tabela), <strong>Consulta</strong> (para uma folha de dados de consulta), <strong>Formulário</strong> (para um formulário ou uma folha de dados de formulário), <strong>Relatório</strong>, <strong>Módulo</strong>, <strong>Modo de Exibição de Servidor</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Não é possível gerar saída de uma macro. Se desejar gerar saída do objeto ativo, selecione seu tipo com este argumento, mas deixe o argumento <strong>Nome do Objeto</strong> em branco. Esse é um argumento obrigatório. O padrão é <strong>Tabela</strong>.  </span><span class="sxs-lookup"><span data-stu-id="82e22-p101">The type of object containing the data to output. Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can't output a macro. If you want to output the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank. This is a required argument. The default is <strong>Table</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82e22-116"><strong>Nome do Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="82e22-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="82e22-p102">O nome do objeto que contém os dados de saída. A caixa <strong>Nome do Objeto</strong> mostra todos os objetos no banco de dados do tipo selecionado pelo argumento <strong>Object Type</strong>. Se você executar uma macro que contém a ação <strong>ExportWithFormatting</strong> em um banco de dados biblioteca, o Access primeiro procurará o objeto com esse nome no banco de dados biblioteca e, em seguida, no banco de dados atual.  </span><span class="sxs-lookup"><span data-stu-id="82e22-p102">The name of the object containing the data to output. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you run a macro containing the <strong>ExportWithFormatting</strong> action in a library database, Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82e22-120"><strong>Formato de Saída</strong></span><span class="sxs-lookup"><span data-stu-id="82e22-120"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="82e22-121">O tipo de formato que será usado para gerar saída dos dados.</span><span class="sxs-lookup"><span data-stu-id="82e22-121">The type of format you want to use to output the data.</span></span> <span data-ttu-id="82e22-122">Você pode selecionar a <strong>Pasta de trabalho binária do Excel (*. xlsb)</strong>, <strong>do Excel 97 - pasta de trabalho do Excel 2003 (*. xls)</strong>, a <strong>Pasta de trabalho do Excel (*. xlsx)</strong>, <strong>HTML (*. htm; *. HTML)</strong>, <strong>Pasta de trabalho do Microsoft Excel 5.0/95 (*. xls)</strong>, <strong>Formato PDF (*. PDF)</strong>, <strong> Formato Rich Text (RTF)</strong>, <strong>arquivos de texto (*. txt)</strong>ou <strong>formato XPS (\*. XPS)</strong>.</span><span class="sxs-lookup"><span data-stu-id="82e22-122">You can select <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm; *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format (*.pdf)</strong>, <strong>Rich Text Format (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (*.xps)</strong>.</span></span> <span data-ttu-id="82e22-123">Se você deixar este argumento em branco, o Access solicitará o formato de saída.</span><span class="sxs-lookup"><span data-stu-id="82e22-123">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82e22-124"><strong>Arquivo de Saída</strong></span><span class="sxs-lookup"><span data-stu-id="82e22-124"><strong>Output File</strong></span></span></p></td>
<td><p><span data-ttu-id="82e22-p104">O arquivo no qual você deseja gerar saída dos dados, incluindo o caminho completo. É possível incluir a extensão de nome de arquivo padrão para o formato de saída selecionado com o argumento <strong>Formato de Saída</strong>, mas ela não é obrigatória. Se você deixar o argumento <strong>Arquivo de Saída</strong> em branco, o Access solicitará um nome de arquivo de saída.  </span><span class="sxs-lookup"><span data-stu-id="82e22-p104">The file to which you want to output the data, including the full path. You can include the standard file name extension for the output format you select with the <strong>Output Format</strong> argument, but it is not required. If you leave the <strong>Output File</strong> argument blank, Access prompts you for an output file name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82e22-128"><strong>AutoIniciar</strong></span><span class="sxs-lookup"><span data-stu-id="82e22-128"><strong>Auto Start</strong></span></span></p></td>
<td><p><span data-ttu-id="82e22-129">Especifica se o software apropriado deverá ser iniciado imediatamente após a execução da ação <strong>ExportarcomFormatação</strong>, com o arquivo especificado pelo argumento <strong>Arquivo de Saída</strong> aberto.</span><span class="sxs-lookup"><span data-stu-id="82e22-129">Specifies whether you want the appropriate software to start immediately after the <strong>ExportWithFormatting</strong> action runs, with the file specified by the <strong>Output File</strong> argument opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82e22-130"><strong>Arquivo de Modelo</strong></span><span class="sxs-lookup"><span data-stu-id="82e22-130"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="82e22-p105">O caminho e o nome de um arquivo que será usado como modelo para arquivos HTML. O arquivo modelo é um arquivo de texto que inclui marcas HTML e tokens que são exclusivos do Access.</span><span class="sxs-lookup"><span data-stu-id="82e22-p105">The path and file name of a file you want to use as a template for HTML files. The template file is a text file that includes HTML tags and tokens that are unique to Access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82e22-133"><strong>Codificação</strong></span><span class="sxs-lookup"><span data-stu-id="82e22-133"><strong>Encoding</strong></span></span></p></td>
<td><p><span data-ttu-id="82e22-p106">O tipo de formato de codificação de caracteres usado para gerar saída de texto ou de dados HTML. Você pode selecionar <strong>MS-DOS</strong>, <strong>Unicode</strong> ou <strong>Unicode (UTF-8)</strong>. A configuração de argumento <strong>MS-DOS</strong> está disponível somente para arquivos de texto. Se você deixar este argumento em branco, o Access gerará saída dos dados usando a codificação padrão do Windows para arquivos de texto e a codificação de sistema padrão para arquivos HTML.  </span><span class="sxs-lookup"><span data-stu-id="82e22-p106">The type of character encoding format you want used to output the text or HTML data. You can select <strong>MS-DOS</strong>, <strong>Unicode</strong>, or <strong>Unicode (UTF-8)</strong>. The <strong>MS-DOS</strong> argument setting is available only for text files. If you leave this argument blank, Access outputs the data by using the Windows default encoding for text files and the default system encoding for HTML files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82e22-138"><strong>Qualidade da Saída</strong></span><span class="sxs-lookup"><span data-stu-id="82e22-138"><strong>Output Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="82e22-139">Selecione <strong>Imprimir</strong> para otimizar a saída para impressão ou <strong>Tela</strong> para otimizar a saída para exibição em tela.</span><span class="sxs-lookup"><span data-stu-id="82e22-139">Select <strong>Print</strong> to optimize the output for printing, or <strong>Screen</strong> to optimize the output for display on a screen.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="82e22-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="82e22-140">Remarks</span></span>

<span data-ttu-id="82e22-p107">Os dados do Access têm saída no formato selecionado e podem ser lidos por qualquer programa que use o mesmo formato. Por exemplo, é possível gerar saída de um relatório do Access com sua formatação para um documento de Formato Rich Text e abrir o documento no Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="82e22-p107">The Access data is output in the selected format and can be read by any program that uses the same format. For example, you can output an Access report with its formatting to a Rich Text Format document and then open the document in Microsoft Word.</span></span>

<span data-ttu-id="82e22-p108">Se você gerar saída do objeto de banco de dados para o formato HTML, o Access criará um arquivo em formato HTML que contém os dados do objeto. Você pode usar o argumento **Arquivo Modelo** para especificar um arquivo que será usado como modelo para o arquivo .html.</span><span class="sxs-lookup"><span data-stu-id="82e22-p108">If you output the database object to HTML format, Access creates a file in HTML format containing the data from the object. You can use the **Template File** argument to specify a file to be used as a template for the .html file.</span></span>

<span data-ttu-id="82e22-145">As regras a seguir se aplicam ao usar a ação **ExportarcomFormatação** para gerar saída de um objeto de banco de dados para quaisquer dos formatos de saída:</span><span class="sxs-lookup"><span data-stu-id="82e22-145">The following rules apply when you use the **ExportWithFormatting** action to output a database object to any of the output formats:</span></span>

  - <span data-ttu-id="82e22-p109">É possível gerar saída dos dados em folhas de dados de tabela, de consulta e de formulário. No arquivo de saída, todos os campos da folha de dados aparecem da mesma maneira que no Access, com a exceção dos campos que contêm objetos OLE. As colunas dos campos de objetos OLE são incluídas no arquivo de saída, mas os campos ficam em branco.</span><span class="sxs-lookup"><span data-stu-id="82e22-p109">You can output data in table, query, and form datasheets. In the output file, all fields in the datasheet appear as they do in Access, with the exception of fields containing OLE objects. The columns for OLE object fields are included in the output file, but the fields are blank.</span></span>

  - <span data-ttu-id="82e22-149">Para um controle que está acoplado a um campo Sim/não (um botão de alternância, botão de opção ou caixa de seleção), o arquivo de saída exibe o valor – 1 (Sim) ou 0 (não).</span><span class="sxs-lookup"><span data-stu-id="82e22-149">For a control that is bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

  - <span data-ttu-id="82e22-150">Para uma caixa de texto ligada a um campo de hiperlink, o arquivo de saída exibe o hiperlink para todos os formatos de saída com exceção de texto MS-DOS (nesse caso, o hiperlink é exibido como texto normal).</span><span class="sxs-lookup"><span data-stu-id="82e22-150">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats with the exception of MS-DOS text (in this case, the hyperlink is displayed as normal text).</span></span>

  - <span data-ttu-id="82e22-151">Se você gerar saída dos dados de um formulário em modo Formulário, o arquivo de saída sempre conterá o modo Folha de Dados do formulário.</span><span class="sxs-lookup"><span data-stu-id="82e22-151">If you output the data in a form in Form view, the output file always contains the form's Datasheet view.</span></span>

  - <span data-ttu-id="82e22-p110">Quando é gerada saída de uma folha de dados, um formulário ou uma página de acesso a dados em formato HTML, um arquivo .html é criado. Quando é gerada saída de um relatório em formato HTML, um arquivo .html é criado para cada página do relatório.</span><span class="sxs-lookup"><span data-stu-id="82e22-p110">When you output a datasheet, form, or data access page in HTML format, one .html file is created. When you output a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="82e22-154">O resultado da execução da ação **ExportarcomFormatação** é semelhante a clicar em uma das opções do grupo **Exportar** da guia **Dados Externos**. Os argumentos da ação correspondem às configurações da caixa de diálogo **Exportar**.</span><span class="sxs-lookup"><span data-stu-id="82e22-154">The result of running the **ExportWithFormatting** action is similar to clicking one of the options in the **Export** group on the **External Data** tab. The action arguments correspond to the settings in the **Export** dialog box.</span></span>

<span data-ttu-id="82e22-155">Para executar a ação **ExportarcomFormatação** em um módulo do VBA (Visual Basic for Applications), use o método **SaídaPara** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="82e22-155">To run the **ExportWithFormatting** action in a Visual Basic for Applications (VBA) module, use the **OutputTo** method of the **DoCmd** object.</span></span>

