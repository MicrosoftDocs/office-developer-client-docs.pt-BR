---
title: Ação da macro ImportarExportarPlanilha
TOCTitle: ImportExportSpreadsheet macro action
ms:assetid: 526aef41-8329-5335-9d16-4d332542a297
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193927(v=office.15)
ms:contentKeyID: 48544846
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm31446
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: f910393c6d7a64258e5afc7545641fc5c6778b03
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726005"
---
# <a name="importexportspreadsheet-macro-action"></a><span data-ttu-id="c2a44-102">Ação da macro ImportarExportarPlanilha</span><span class="sxs-lookup"><span data-stu-id="c2a44-102">ImportExportSpreadsheet macro action</span></span>

<span data-ttu-id="c2a44-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2a44-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2a44-p101">Você pode usar a ação **ImportExportSpreadsheet** para importar ou exportar dados entre o banco de dados atual do Access (.mdb ou .accdb) ou um arquivo de projeto do Access (.adp) e de planilha. Também é possível vincular os dados em uma planilha do Microsoft Excel ao banco de dados atual do Microsoft Access. Com uma planilha vinculada, você pode exibir e editar os dados da planilha com o Access e ainda permitir acesso completo aos dados do seu programa de planilha Excel. Você também pode vincular a dados em um arquivo de planilha do Lotus 1-2-3, mas esses dados são somente leitura no Access.</span><span class="sxs-lookup"><span data-stu-id="c2a44-p101">You can use the **ImportExportSpreadsheet** action to import or export data between the current Access database (.mdb or .accdb) or Access project (.adp) and a spreadsheet file. You can also link the data in a Microsoft Excel spreadsheet to the current Microsoft Access database. With a linked spreadsheet, you can view and edit the spreadsheet data with Access while still allowing complete access to the data from your Excel spreadsheet program. You can also link to data in a Lotus 1-2-3 spreadsheet file, but this data is read-only in Access.</span></span>

> [!NOTE]
> <span data-ttu-id="c2a44-108">Essa ação não será permitida se o banco de dados não for confiável.</span><span class="sxs-lookup"><span data-stu-id="c2a44-108">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="c2a44-109">Configuração</span><span class="sxs-lookup"><span data-stu-id="c2a44-109">Setting</span></span>

<span data-ttu-id="c2a44-110">A ação **TransferirPlanilha** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="c2a44-110">The **TransferSpreadsheet** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c2a44-111">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="c2a44-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c2a44-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2a44-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2a44-113"><strong>Tipo de transferência</strong></span><span class="sxs-lookup"><span data-stu-id="c2a44-113"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a44-p102">O tipo de transferência que você deseja fazer. Selecione <strong>Importar</strong>, <strong>Exportar</strong> ou <strong>Vincular</strong> na caixa <strong>Tipo de Transferência</strong> na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. O padrão é <strong>Importar</strong>.  </span><span class="sxs-lookup"><span data-stu-id="c2a44-p102">The type of transfer you want to make. Select <strong>Import</strong>, <strong>Export</strong>, or <strong>Link</strong> in the <strong>Transfer Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Import</strong>.</span></span></p><p><span data-ttu-id="c2a44-117"><strong>OBSERVAÇÃO</strong>: O tipo de <STRONG>Link</STRONG> de transferência não tem suporte para projetos do Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="c2a44-117">The <STRONG>Link</STRONG> transfer type is not supported for Access projects (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2a44-118"><strong>Tipo de planilha</strong></span><span class="sxs-lookup"><span data-stu-id="c2a44-118"><strong>Spreadsheet Type</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a44-p103">O tipo de planilha de onde importar, para onde exportar ou à qual vincular. Você pode selecionar um de vários tipos de planilha na caixa. O padrão é <strong>Pasta de Trabalho do Excel</strong>.  </span><span class="sxs-lookup"><span data-stu-id="c2a44-p103">The type of spreadsheet to import from, export to, or link to. You can select one of a number of spreadsheet types in the box. The default is <strong>Excel Workbook</strong>.</span></span></p><p><span data-ttu-id="c2a44-122"><strong>Observação</strong>: você pode importar de vincular (somente leitura) aos arquivos do Lotus. WK4, mas você não pode exportar dados do Access nesse formato de planilha.</span><span class="sxs-lookup"><span data-stu-id="c2a44-122"><strong>NOTE</strong>: You can import from and link (read-only) to Lotus .WK4 files, but you can't export Access data to this spreadsheet format.</span></span> <span data-ttu-id="c2a44-123">O Access também não oferece suporte para importar, exportar ou vincular dados do Lotus. WKS ou planilhas do Excel versão 2.0 com essa ação.</span><span class="sxs-lookup"><span data-stu-id="c2a44-123">Access also no longer supports importing, exporting, or linking data from Lotus .WKS or Excel version 2.0 spreadsheets with this action.</span></span> <span data-ttu-id="c2a44-124">Se você quiser importar ou vincular dados no Excel versão 2.0 ou o formato Lotus. WKS, converta os dados da planilha em uma versão mais recente do Excel ou do Lotus 1-2-3 antes de importar ou vincular os dados no Access.</span><span class="sxs-lookup"><span data-stu-id="c2a44-124">You can import from and link (read-only) to Lotus .WK4 files, but you can't export Access data to this spreadsheet format. Access also no longer supports importing, exporting, or linking data from Lotus .WKS or Excel version 2.0 spreadsheets with this action. If you want to import from or link to spreadsheet data in Excel version 2.0 or Lotus .WKS format, convert the spreadsheet data to a later version of Excel or Lotus 1-2-3 before importing or linking the data into Access.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2a44-125"><strong>Nome da Tabela</strong></span><span class="sxs-lookup"><span data-stu-id="c2a44-125"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a44-p105">O nome da tabela do Access para a qual os dados da planilha serão importados, de onde os dados da planilha serão exportados ou para onde os dados da planilha serão vinculados. Você também pode digitar o nome da consulta seleção do Access da qual você deseja exportar dados. Esse é um argumento obrigatório. Se você selecionar <strong>Import</strong> no argumento <strong>Transfer Type</strong>, o Access anexará os dados da planilha a essa tabela caso a tabela já exista. Caso contrário, o Access criará uma nova tabela com os dados da planilha. No Access, você não poderá usar uma instrução SQL para especificar dados a serem exportados quando estiver usando a ação <strong>ImportExportSpreadsheet</strong>. Em vez de usar uma instrução SQL, primeiro você deverá criar uma consulta e então especificar o nome da consulta no argumento <strong>Table Name</strong>.  </span><span class="sxs-lookup"><span data-stu-id="c2a44-p105">The name of the Access table to import spreadsheet data to, export spreadsheet data from, or link spreadsheet data to. You can also type the name of the Access select query you want to export data from. This is a required argument. If you select <strong>Import</strong> in the <strong>Transfer Type</strong> argument, Access appends the spreadsheet data to this table if the table already exists. Otherwise, Access creates a new table containing the spreadsheet data. In Access, you can't use an SQL statement to specify data to export when you are using the <strong>ImportExportSpreadsheet</strong> action. Instead of using an SQL statement, you must first create a query and then specify the name of the query in the <strong>Table Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2a44-133"><strong>Nome do arquivo</strong></span><span class="sxs-lookup"><span data-stu-id="c2a44-133"><strong>File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a44-p106">O nome do arquivo de planilha de onde importar, para onde exportar ou para onde vincular. Inclua o caminho completo. Esse é um argumento obrigatório. O Access criará uma nova planilha quando você exportar dados do Access. Se o nome do arquivo for igual ao nome de uma planilha existente, o Access substituirá a planilha existente, a menos que você esteja exportando para uma pasta de trabalho do Excel versão 5.0 ou posterior. Nesse caso, o Access copiará os dados exportados para a próxima planilha nova disponível na pasta de trabalho. Se você estiver importando de uma planilha do Excel versão 5.0 ou posterior ou vinculando dela, poderá especificar uma planilha em particular usando o argumento <strong>Intervalo</strong>.  </span><span class="sxs-lookup"><span data-stu-id="c2a44-p106">The name of the spreadsheet file to import from, export to, or link to. Include the full path. This is a required argument. Access creates a new spreadsheet when you export data from Access. If the file name is the same as the name of an existing spreadsheet, Access replaces the existing spreadsheet, unless you're exporting to an Excel version 5.0 or later workbook. In that case, Access copies the exported data to the next available new worksheet in the workbook. If you are importing from or linking to an Excel version 5.0 or later spreadsheet, you can specify a particular worksheet by using the <strong>Range</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2a44-141"><strong>Tem Nomes de Campo</strong></span><span class="sxs-lookup"><span data-stu-id="c2a44-141"><strong>Has Field Names</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a44-p107">Especifique se a primeira linha da planilha contém os nomes dos campos. Se você selecionar <strong>Sim</strong>, o Access usará os nomes dessa linha como nomes de campo na tabela do Access ao importar ou vincular os dados da planilha. Se você selecionar <strong>Não</strong>, o Access tratará a primeira linha como uma linha de dados normal. O padrão é <strong>Não</strong>. Quando você exporta uma tabela ou uma consulta seleção do Access para uma planilha, os nomes de campos serão inseridos na primeira linha da planilha, não importa o que estiver selecionado neste argumento.  </span><span class="sxs-lookup"><span data-stu-id="c2a44-p107">Specifies whether the first row of the spreadsheet contains the names of the fields. If you select <strong>Yes</strong>, Access uses the names in this row as field names in the Access table when you import or link the spreadsheet data. If you select <strong>No</strong>, Access treats the first row as a normal row of data. The default is <strong>No</strong>. When you export an Access table or select query to a spreadsheet, the field names are inserted into the first row of the spreadsheet no matter what you select in this argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2a44-147"><strong>Range</strong></span><span class="sxs-lookup"><span data-stu-id="c2a44-147"><strong>Range</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a44-p108">O intervalo de células a serem importadas ou vinculadas. Deixe esse argumento em branco para importar ou vincular a planilha inteira. Você pode digitar o nome de um intervalo da planilha ou especifique o intervalo de células a serem importadas ou vinculadas. Deixe esse argumento em branco para importar ou vincular a planilha inteira. Você pode digitar o nome de um intervalo na planilha ou especificar o intervalo de células a serem importadas ou vinculadas, como A1:E25 (observe que a sintaxe A1..E25 não funciona no Access 97 ou posterior). Se você estiver importando de uma planilha do Excel versão 5.0 ou posterior ou vinculando para uma, poderá usar o nome da planilha como prefixo e um ponto de exclamação; por exemplo, Orçamento!A1:C7.</span><span class="sxs-lookup"><span data-stu-id="c2a44-p108">The range of cells to import or link. Leave this argument blank to import or link the entire spreadsheet. You can type the name of a range in the spreadsheet or specify the range of cells to import or link, such as A1:E25 (note that the A1..E25 syntax does not work in Access 97 or later). If you are importing from or linking to an Excel version 5.0 or later spreadsheet, you can prefix the range with the name of the worksheet and an exclamation point; for example, Budget!A1:C7.</span></span></p><p><span data-ttu-id="c2a44-152"><strong>Observação</strong>: quando você exporta em uma planilha, você deve deixar esse argumento em branco.</span><span class="sxs-lookup"><span data-stu-id="c2a44-152">When you export to a spreadsheet, you must leave this argument blank. If you enter a range, the export will fail.</span></span> <span data-ttu-id="c2a44-153">Se você inserir um intervalo, a exportação falhará.</span><span class="sxs-lookup"><span data-stu-id="c2a44-153">When you export to a spreadsheet, you must leave this argument blank. If you enter a range, the export will fail.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c2a44-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2a44-154">Remarks</span></span>

<span data-ttu-id="c2a44-p110">Você pode exportar os dados em consultas seleção do Access para planilhas. O Access exporta o conjunto de resultados da consulta, tratando-o como uma tabela.</span><span class="sxs-lookup"><span data-stu-id="c2a44-p110">You can export the data in Access select queries to spreadsheets. Access exports the result set of the query, treating it just like a table.</span></span>

<span data-ttu-id="c2a44-157">Os dados da planilha que você anexa a uma tabela existente do Access devem ser compatíveis com a estrutura da tabela.</span><span class="sxs-lookup"><span data-stu-id="c2a44-157">Spreadsheet data that you append to an existing Access table must be compatible with the table's structure.</span></span>

- <span data-ttu-id="c2a44-158">Cada campo na planilha deve ser do mesmo tipo de dados que o campo correspondente na tabela.</span><span class="sxs-lookup"><span data-stu-id="c2a44-158">Each field in the spreadsheet must be of the same data type as the corresponding field in the table.</span></span>

- <span data-ttu-id="c2a44-159">Os campos deverão estar na mesma ordem (a menos que você defina o argumento **Tem Nomes de Campo** como **Sim**; nesse caso, os nomes de campo da planilha deverão corresponder aos nomes de campo na tabela).</span><span class="sxs-lookup"><span data-stu-id="c2a44-159">The fields must be in the same order (unless you set the **Has Field Names** argument to **Yes**, in which case the field names in the spreadsheet must match the field names in the table).</span></span>

<span data-ttu-id="c2a44-p111">Essa ação é semelhante a clicar na guia **Dados Externos** e clicar em **Excel** no grupo **Importar** ou **Exportar** ou clicar em **Mais** no grupo **Importar** ou **Exportar** e clicar em **Arquivo do Lotus 1-2-3**. Você pode usar esses comandos para selecionar uma fonte de dados, como o Access, ou digitar um banco de dados, de planilha ou de arquivo de texto. Se você selecionar uma planilha, será exibida uma série de caixas de diálogo ou um assistente do Access será executado, quando você selecionará o nome da planilha e outras opções. Os argumentos da ação **ImportExportSpreadsheet** refletem as opções nessas caixas de diálogo ou nos assistentes.</span><span class="sxs-lookup"><span data-stu-id="c2a44-p111">This action is similar to clicking the **External Data** tab and clicking **Excel** in the **Import** or **Export** group, or clicking **More** in the **Import** or **Export** group and clicking **Lotus 1-2-3 File**. You can use these commands to select a source of data, such as Access or a type of database, spreadsheet, or text file. If you select a spreadsheet, a series of dialog boxes appear, or an Access wizard runs, in which you select the name of the spreadsheet and other options. The arguments of the **ImportExportSpreadsheet** action reflect the options in these dialog boxes or in the wizards.</span></span>

> [!NOTE]
> <span data-ttu-id="c2a44-164">Se você consultar ou filtrar uma planilha vinculada, a consulta ou o filtro será sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c2a44-164">If you query or filter a linked spreadsheet, the query or filter is case-sensitive.</span></span>

<span data-ttu-id="c2a44-165">Se você vincular a uma planilha do Excel que esteja aberta em modo Editar, o Access aguardará até a planilha do Excel sair do modo Editar antes da conclusão da vinculação; não há tempo limite.</span><span class="sxs-lookup"><span data-stu-id="c2a44-165">If you link to an Excel spreadsheet that is open in Edit mode, Access will wait until the Excel spreadsheet is out of Edit mode before completing the link; there's no time-out.</span></span>

<span data-ttu-id="c2a44-166">Para executar a ação **ImportExportSpreadsheet** em um módulo do VBA (Visual Basic for Applications) module, use o método **TransferSpreadsheet** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="c2a44-166">To run the **ImportExportSpreadsheet** action in a Visual Basic for Applications (VBA) module, use the **TransferSpreadsheet** method of the **DoCmd** object.</span></span>

