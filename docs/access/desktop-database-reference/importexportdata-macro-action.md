---
title: Ação da macro ImportarExportarDados
TOCTitle: ImportExportData macro action
ms:assetid: 2cbde873-8a3d-b15c-4aab-405cddf44cea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192107(v=office.15)
ms:contentKeyID: 48543961
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm51789
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 363945386233fd992390f1fbc4b6115e272dc923
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997613"
---
# <a name="importexportdata-macro-action"></a><span data-ttu-id="92e26-102">Ação da macro ImportarExportarDados</span><span class="sxs-lookup"><span data-stu-id="92e26-102">ImportExportData macro action</span></span>

<span data-ttu-id="92e26-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="92e26-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="92e26-p101">Você pode usar a ação **ImportExportData** para importar ou exportar dados entre o banco de dados atual do Access (.mdb ou .accdb) ou o projeto do Access (.adp) e outro banco de dados. Para bancos de dados do Microsoft Access, você também pode vincular uma tabela ao banco de dados atual do Access de outro banco de dados. Com uma tabela vinculada, você tem acesso aos dados da tabela enquanto a própria tabela permanece em outro banco de dados.</span><span class="sxs-lookup"><span data-stu-id="92e26-p101">You can use the **ImportExportData** action to import or export data between the current Access database (.mdb or .accdb) or Access project (.adp) and another database. For Microsoft Access databases, you can also link a table to the current Access database from another database. With a linked table, you have access to the table's data while the table itself remains in the other database.</span></span>

> [!NOTE]
> <span data-ttu-id="92e26-107">[!OBSERVAçãO] This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="92e26-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="settings"></a><span data-ttu-id="92e26-108">Configurações</span><span class="sxs-lookup"><span data-stu-id="92e26-108">Settings</span></span>

<span data-ttu-id="92e26-109">A ação **ImportExportData** tem os argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="92e26-109">The **ImportExportData** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="92e26-110">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="92e26-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="92e26-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="92e26-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92e26-112"><strong>Tipo de transferência</strong></span><span class="sxs-lookup"><span data-stu-id="92e26-112"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="92e26-p102">O tipo de transferência que você deseja fazer. Selecione <strong>Importar</strong>, <strong>Exportar</strong> ou <strong>Vincular</strong> na caixa <strong>Tipo de Transferência</strong> na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. O padrão é <strong>Importar</strong>.  </span><span class="sxs-lookup"><span data-stu-id="92e26-p102">The type of transfer you want to make. Select <strong>Import</strong>, <strong>Export</strong>, or <strong>Link</strong> in the <strong>Transfer Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Import</strong>.</span></span></p><p><span data-ttu-id="92e26-116"><strong>Observação</strong>: não há suporte para o tipo de transferência de <strong>Link</strong> para projetos do Access (. adp).</span><span class="sxs-lookup"><span data-stu-id="92e26-116"><strong>NOTE</strong>: The <strong>Link</strong> transfer type is not supported for Access projects (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92e26-117"><strong>Tipo de Banco de Dados</strong></span><span class="sxs-lookup"><span data-stu-id="92e26-117"><strong>Database Type</strong></span></span></p></td>
<td><p><span data-ttu-id="92e26-p103">O tipo de banco de dados de onde será importado, para onde será exportado ou vinculado. Você pode selecionar o <strong>Microsoft Access</strong> ou um dos vários tipos de banco de dados na caixa <strong>Tipo de Banco de Dados</strong>. O padrão é <strong>Microsoft Access</strong>.  </span><span class="sxs-lookup"><span data-stu-id="92e26-p103">The type of database to import from, export to, or link to. You can select <strong>Microsoft Access</strong> or one of a number of other database types in the <strong>Database Type</strong> box. The default is <strong>Microsoft Access</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92e26-121"><strong>Nome do Banco de Dados</strong></span><span class="sxs-lookup"><span data-stu-id="92e26-121"><strong>Database Name</strong></span></span></p></td>
<td><p><span data-ttu-id="92e26-p104">O nome do banco de dados de onde será importado, para onde será exportado ou vinculado. Inclua o caminho completo. Esse é um argumento obrigatório. Para tipos de bancos de dados que usam arquivos separados para cada tabela, como FoxPro, Paradox e dBASE, insira o diretório que contém o arquivo. Insira o nome do arquivo no argumento <strong>Origem</strong> (para importar ou vincular) ou o argumento <strong>Destino</strong> (para exportar). Para bancos de dados ODBC, digite a cadeia de conexão completa ODBC (Open Database Connectivity).  </span><span class="sxs-lookup"><span data-stu-id="92e26-p104">The name of the database to import from, export to, or link to. Include the full path. This is a required argument. For types of databases that use separate files for each table, such as FoxPro, Paradox, and dBASE, enter the directory containing the file. Enter the file name in the <strong>Source</strong> argument (to import or link) or the <strong>Destination</strong> argument (to export). For ODBC databases, type the full Open Database Connectivity (ODBC) connection string.</span></span></p>
<p><span data-ttu-id="92e26-128">Para ver um exemplo de uma cadeia de conexão, vincule uma tabela externa ao Access:</span><span class="sxs-lookup"><span data-stu-id="92e26-128">To see an example of a connection string, link an external table to Access:</span></span></p>
<ol>
<li><p><span data-ttu-id="92e26-129">Na caixa de diálogo <strong>Obter Dados Externos</strong>, insira o caminho do seu banco de dados de origem na caixa <strong>Nome do arquivo</strong>.</span><span class="sxs-lookup"><span data-stu-id="92e26-129">In the <strong>Get External Data</strong> dialog box, enter the path of your source database in the <strong>File name</strong> box.</span></span></p></li>
<li><p><span data-ttu-id="92e26-130">Clique em <strong>Vincular à fonte de dados criando uma tabela vinculada</strong> e clique em <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="92e26-130">Click <strong>Link to the data source by creating a linked table</strong>, and click <strong>OK</strong>.</span></span></p></li>
<li><p><span data-ttu-id="92e26-131">Selecione uma tabela na caixa de diálogo <strong>Vincular Tabelas</strong> e clique em <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="92e26-131">Select a table in the <strong>Link Tables</strong> dialog box, and click <strong>OK</strong>.</span></span></p></li>
</ol>
<p><span data-ttu-id="92e26-p105">Abra a tabela recentemente vinculada no modo Design e exiba as propriedades da tabela clicando em <strong>Folha de Propriedades</strong> na guia <strong>Design</strong>, em <strong>Ferramentas</strong>. O texto na configuração de propriedade <strong>Descrição</strong> é a cadeia de conexão para esta tabela.  </span><span class="sxs-lookup"><span data-stu-id="92e26-p105">Open the newly linked table in Design view and view the table properties by clicking <strong>Property Sheet</strong> on the <strong>Design</strong> tab, under <strong>Tools</strong>. The text in the <strong>Description</strong> property setting is the connection string for this table.</span></span></p>
<p><span data-ttu-id="92e26-134">Para obter mais informações sobre cadeias de caracteres de conexão ODBC, consulte o arquivo de Ajuda ou outra documentação para o driver ODBC desse tipo de banco de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="92e26-134">For more information about ODBC connection strings, see the Help file or other documentation for the ODBC driver of this type of ODBC database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92e26-135"><strong>Tipo de Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="92e26-135"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="92e26-p106">O tipo de objeto a ser importado ou exportado. Se você selecionar <strong>Microsoft Access</strong> para o argumento <strong>Tipo de Banco de Dados</strong>, poderá selecionar <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Exibição de Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong>. O padrão é <strong>Tabela</strong>. Se você selecionar qualquer outro tipo de banco de dados ou se você selecionar <strong>Link</strong> na caixa <strong>Tipo de Transferência</strong>, esse argumento será ignorado. Se você estiver exportando uma consulta seleção para um banco de dados do Access, selecione <strong>Tabela</strong> nesse argumento para exportar o conjunto de resultados da consulta e selecione <strong>Consulta</strong> para exportar a própria consulta. Se você estiver exportando uma consulta seleção para outro tipo de banco de dados, esse argumento será ignorado e o conjunto de resultados da consulta será exportado.  </span><span class="sxs-lookup"><span data-stu-id="92e26-p106">The type of object to import or export. If you select <strong>Microsoft Access</strong> for the <strong>Database Type</strong> argument, you can select <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box. The default is <strong>Table</strong>. If you select any other type of database, or if you select <strong>Link</strong> in the <strong>Transfer Type</strong> box, this argument is ignored. If you are exporting a select query to an Access database, select <strong>Table</strong> in this argument to export the result set of the query, and select <strong>Query</strong> to export the query itself. If you are exporting a select query to another type of database, this argument is ignored and the result set of the query is exported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92e26-142"><strong>Origem</strong></span><span class="sxs-lookup"><span data-stu-id="92e26-142"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="92e26-p107">O nome da tabela, da consulta seleção ou do objeto do Access que você deseja importar, exportar ou vincular. Para alguns tipos de bancos de dados, como FoxPro, Paradox ou dBASE, esse é o nome do arquivo. Inclua a extensão do nome do arquivo (como .dbf) no nome do arquivo. Esse é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="92e26-p107">The name of the table, select query, or Access object that you want to import, export, or link. For some types of databases, such as FoxPro, Paradox, or dBASE, this is a file name. Include the file name extension (such as .dbf) in the file name. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92e26-147"><strong>Destino</strong></span><span class="sxs-lookup"><span data-stu-id="92e26-147"><strong>Destination</strong></span></span></p></td>
<td><p><span data-ttu-id="92e26-p108">O nome da tabela, consulta seleção ou objeto do Access importado, exportado ou vinculado no banco de dados de destino. Para alguns tipos de bancos de dados, como FoxPro, Paradox ou dBASE, é o nome do arquivo. Inclua o a extensão do nome do arquivo (como .dbf) no nome do arquivo. Esse é um argumento obrigatório. Se você selecionar <strong>Importar</strong> no argumento <strong>Tipo de Transferência</strong> e <strong>Tabela</strong> no argumento <strong>Tipo de Objeto</strong>. O Access cria uma nova tabela com os dados da tabela importada. Se você importar uma tabela ou outro objeto, o Access adiciona um número ao nome caso ele esteja em conflito com um nome existente. Por exemplo, se você importar Funcionários e Funcionários já existir, o Access renomeará a tabela ou outro objeto importado como Funcionários1. Se você exportar para um banco de dados do Access ou para outro banco de dados, o Access substituirá automaticamente qualquer tabela ou outro objeto existente com o mesmo nome.  </span><span class="sxs-lookup"><span data-stu-id="92e26-p108">The name of the imported, exported, or linked table, select query, or Access object in the destination database. For some types of databases, such as FoxPro, Paradox, or dBASE, this is a file name. Include the file name extension (such as .dbf) in the file name. This is a required argument. If you select <strong>Import</strong> in the <strong>Transfer Type</strong> argument and <strong>Table</strong> in the <strong>Object Type</strong> argument, Access creates a new table containing the data in the imported table. If you import a table or other object, Access adds a number to the name if it conflicts with an existing name. For example, if you import Employees and Employees already exists, Access renames the imported table or other object Employees1. If you export to an Access database or another database, Access automatically replaces any existing table or other object that has the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92e26-156"><strong>Somente Estrutura</strong></span><span class="sxs-lookup"><span data-stu-id="92e26-156"><strong>Structure Only</strong></span></span></p></td>
<td><p><span data-ttu-id="92e26-p109">Especifica se é necessário importar ou exportar somente a estrutura de uma tabela do banco de dados sem qualquer um desses dados. Selecione <strong>Sim</strong> ou <strong>Não</strong>. O padrão é <strong>Não</strong>.  </span><span class="sxs-lookup"><span data-stu-id="92e26-p109">Specifies whether to import or export only the structure of a database table without any of its data. Select <strong>Yes</strong> or <strong>No</strong>. The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="92e26-160">Comentários</span><span class="sxs-lookup"><span data-stu-id="92e26-160">Remarks</span></span>

<span data-ttu-id="92e26-p110">Você pode importar e exportar tabelas entre o Access e outros tipos de bancos de dados. Também é possível exportar consultas seleção do Access para outros tipos de bancos de dados. O Access exporta o conjunto de resultados da consulta no formato de uma tabela. Você poderá importar e exportar qualquer objeto de banco de dados do Access caso ambos os bancos de dados sejam bancos de dados do Access.</span><span class="sxs-lookup"><span data-stu-id="92e26-p110">You can import and export tables between Access and other types of databases. You can also export Access select queries to other types of databases. Access exports the result set of the query in the form of a table. You can import and export any Access database object if both databases are Access databases.</span></span>

<span data-ttu-id="92e26-p111">Se você importar uma tabela de outro banco de dados do Access (.mdb ou .accdb) que seja uma tabela vinculada naquele banco de dados, ela ainda estará vinculada após a importação. Ou seja, o link é importado, e não a própria tabela.</span><span class="sxs-lookup"><span data-stu-id="92e26-p111">If you import a table from another Access database (.mdb or .accdb) that's a linked table in that database, it will still be linked after you import it. That is, the link is imported, not the table itself.</span></span>

<span data-ttu-id="92e26-p112">Se o banco de dados que você está acessando exigir uma senha, será exibida uma caixa de diálogo quando você executar a macro. Digite a senha nessa caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="92e26-p112">If the database you're accessing requires a password, a dialog box appears when you run the macro. Type the password in this dialog box.</span></span>

<span data-ttu-id="92e26-p113">A ação **ImportExportData** é semelhante aos comandos na guia **Dados Externos**, sob **Importar** ou **Exportar**. Você pode usar esses comandos para selecionar uma fonte de dados, como um banco de dados do Access ou outro tipo de banco de dados, uma planilha ou um arquivo de texto. Se você selecionar um banco de dados, uma ou mais caixas de diálogo aparecerão e você poderá selecionar o tipo de objeto a ser importado ou exportado (para bancos de dados do Access), o nome do objeto e outras opções, dependendo do banco de dados para o qual você esteja exportação ou vinculando. Os argumentos para a ação **ImportExportData** refletem as opções nessas caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="92e26-p113">The **ImportExportData** action is similar to the commands on the **External Data** tab, under **Import** or **Export**. You can use these commands to select a source of data, such as an Access database or another type of database, a spreadsheet, or a text file. If you select a database, one or more dialog boxes appear in which you select the type of object to import or export (for Access databases), the name of the object, and other options, depending on the database you are importing from or exporting or linking to. The arguments for the **ImportExportData** action reflect the options in these dialog boxes.</span></span>

<span data-ttu-id="92e26-173">Se você quiser fornecer informações de índice para uma tabela dBASE vinculada, primeiro vincule a tabela:</span><span class="sxs-lookup"><span data-stu-id="92e26-173">If you want to supply index information for a linked dBASE table, first link the table:</span></span>

1.  <span data-ttu-id="92e26-174">Clique em **Arquivo dBASE**.</span><span class="sxs-lookup"><span data-stu-id="92e26-174">Click **dBASE File**.</span></span>

2.  <span data-ttu-id="92e26-175">Na caixa de diálogo **Obter Dados Externos**, insira o caminho para o arquivo dBASE na caixa **Nome do arquivo**.</span><span class="sxs-lookup"><span data-stu-id="92e26-175">In the **Get External Data** dialog box, enter the path for the dBASE file in the **File name** box.</span></span>

3.  <span data-ttu-id="92e26-176">Clique em **Vincular à fonte de dados criando uma tabela vinculada** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="92e26-176">Click **Link to the data source by creating a linked table**, then click **OK**.</span></span>

4.  <span data-ttu-id="92e26-p114">Especifique os índices nas caixas de diálogo para este comando. O Access armazena as informações de índice em um arquivo de informações (.inf) especial, localizado na pasta do Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="92e26-p114">Specify the indexes in the dialog boxes for this command. Access stores the index information in a special information (.inf) file, located in the Microsoft Office folder.</span></span>

5.  <span data-ttu-id="92e26-179">Então, você pode excluir o link para a tabela vinculada.</span><span class="sxs-lookup"><span data-stu-id="92e26-179">You can then delete the link to the linked table.</span></span>

<span data-ttu-id="92e26-180">Na próxima vez em que você usar a ação **ImportExportData** para vincular esta tabela dBASE, o Access usará as informações de índice especificadas.</span><span class="sxs-lookup"><span data-stu-id="92e26-180">The next time you use the **ImportExportData** action to link this dBASE table, Access uses the index information that you've specified.</span></span>

> [!NOTE]
> <span data-ttu-id="92e26-181">[!OBSERVAçãO] Se você consultar ou filtrar uma tabela vinculada, a consulta ou o filtro diferenciará maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="92e26-181">If you query or filter a linked table, the query or filter is case-sensitive.</span></span>

<span data-ttu-id="92e26-182">Para executar a ação **ImportExportData** em um módulo do Visual Basic for Applications (VBA), use o método **TransferDatabase** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="92e26-182">To run the **ImportExportData** action in a Visual Basic for Applications (VBA) module, use the **TransferDatabase** method of the **DoCmd** object.</span></span>

