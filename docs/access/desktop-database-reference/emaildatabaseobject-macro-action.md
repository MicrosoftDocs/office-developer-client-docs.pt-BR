---
title: Ação da macro EnviarObjetodeBancodeDadosporEMail
TOCTitle: EMailDatabaseObject macro action
ms:assetid: 7fd80596-5c08-dab9-5343-c0edc38a1af9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196469(v=office.15)
ms:contentKeyID: 48545915
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm24439
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 15cb7d6c422a9d7b0fae17ab649b6cfbc1b497a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293564"
---
# <a name="emaildatabaseobject-macro-action"></a><span data-ttu-id="f4677-102">Ação da macro EnviarObjetodeBancodeDadosporEMail</span><span class="sxs-lookup"><span data-stu-id="f4677-102">EMailDatabaseObject macro action</span></span>

<span data-ttu-id="f4677-103">**Se aplica ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4677-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="f4677-104">Você pode usar a ação **EMailDatabaseObject** para incluir a folha de dados especificada do Microsoft Access, o formulário, o relatório, o módulo ou a página de acesso a dados em uma mensagem eletrônica de email, onde ela possa ser visualizada e encaminhada.</span><span class="sxs-lookup"><span data-stu-id="f4677-104">You can use the **EMailDatabaseObject** action to include the specified Microsoft Access datasheet, form, report, module, or data access page in an electronic mail message, where it can be viewed and forwarded.</span></span>

> [!NOTE]
> <span data-ttu-id="f4677-105">[!OBSERVAçãO] This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="f4677-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="settings"></a><span data-ttu-id="f4677-106">Configurações</span><span class="sxs-lookup"><span data-stu-id="f4677-106">Settings</span></span>

<span data-ttu-id="f4677-107">A ação **EnviarObjetodeBancodeDadosporEMail** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="f4677-107">The **EMailDatabaseObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4677-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="f4677-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f4677-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4677-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4677-110"><strong>Tipo de Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="f4677-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="f4677-p101">O tipo de objeto a ser incluído na mensagem de email. Clique em <strong>Tabela</strong> (para obter uma folha de dados da tabela), <strong>Consulta</strong> (para obter uma folha de dados da consulta), <strong>Formulário</strong> (para obter um formulário ou uma folha de dados do formulário), <strong>Relatório</strong>, <strong>Módulo</strong> ou <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Procedimentos Armazenados</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong>, na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Não é possível enviar uma macro. Se quiser incluir o objeto ativo, selecione o respectivo tipo com esse argumento, mas deixe em branco o argumento <strong>Nome do objeto</strong>.  </span><span class="sxs-lookup"><span data-stu-id="f4677-p101">The type of object to include in the mail message. Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, or <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Stored Procedures</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can't send a macro. If you want to include the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4677-115"><strong>Nome do objeto</strong></span><span class="sxs-lookup"><span data-stu-id="f4677-115"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f4677-p102">O nome do objeto para incluir na mensagem de email. A caixa <strong>Nome do Objeto</strong> mostra todos os objetos no banco de dados do tipo selecionado pelo argumento <strong>Object Type</strong>. Se você deixar os argumentos <strong>Object Type</strong> e o <strong>Object Name</strong> em branco, o Access enviará uma mensagem ao aplicativo de email sem nenhum objeto banco de dados. Se você executar uma macro que contém a ação ￼ <strong>EMailDatabaseObject</strong> em um banco de dados da biblioteca, o Access primeiro procurará o objeto com esse nome no banco de dados biblioteca e, em seguida, no banco de dados atual.  </span><span class="sxs-lookup"><span data-stu-id="f4677-p102">The name of the object to include in the mail message. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave both the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, Access sends a message to the mail application without any database object. If you run a macro containing the <strong>EMailDatabaseObject</strong> action in a library database, Access looks for the object with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4677-120"><strong>Formato de Saída</strong></span><span class="sxs-lookup"><span data-stu-id="f4677-120"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="f4677-121">O tipo de formato que você deseja usar para o objeto incluído.</span><span class="sxs-lookup"><span data-stu-id="f4677-121">The type of format you want used for the included object.</span></span> <span data-ttu-id="f4677-122">A lista de formatos que você pode selecionar mudará dependendo do que você selecionar para o argumento <strong>Tipo de</strong> Objeto.</span><span class="sxs-lookup"><span data-stu-id="f4677-122">The list of formats you can select from will change depending on what you select for the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="f4677-123">Os formatos disponíveis podem incluir <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm, *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format</strong>, Rich <strong>Text Fomat (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>ou <strong>XPS Format (\*.xps)</strong>.</span><span class="sxs-lookup"><span data-stu-id="f4677-123">Available formats may include <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm, *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format</strong>, <strong>Rich Text Fomat (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (\*.xps)</strong>.</span></span> <span data-ttu-id="f4677-124">na caixa <strong>Formato de</strong> Saída.</span><span class="sxs-lookup"><span data-stu-id="f4677-124">in the <strong>Output Format</strong> box.</span></span> <span data-ttu-id="f4677-125">Os módulos só podem ser enviados em formato de texto.</span><span class="sxs-lookup"><span data-stu-id="f4677-125">Modules can be sent only in text format.</span></span> <span data-ttu-id="f4677-126">As páginas de acesso a dados só podem ser enviadas em formato HTML.</span><span class="sxs-lookup"><span data-stu-id="f4677-126">Data access pages can only be sent in HTML format.</span></span> <span data-ttu-id="f4677-127">Se você deixar este argumento em branco, o Access solicitará o formato de saída.</span><span class="sxs-lookup"><span data-stu-id="f4677-127">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4677-128"><strong>To</strong></span><span class="sxs-lookup"><span data-stu-id="f4677-128"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="f4677-p104">Os destinatários cujos nomes você deseja inserir na linha <strong>Para</strong> da mensagem de email. Se você deixar este argumento em branco, o Access solicitará os nomes dos destinatários. Separe os nomes dos destinatários especificados nesse argumento (e nos argumentos <strong>Cc</strong> e <strong>Cco</strong>) usando um ponto e vírgula (;) ou com o separador de lista definido na guia <strong>Número</strong> da caixa de diálogo <strong>Propriedades das Configurações Regionais</strong> no <strong>Painel de Controle</strong> do Windows. Se o aplicativo de email não identificar os nomes dos destinatários, a mensagem não será enviada e ocorrerá um erro.  </span><span class="sxs-lookup"><span data-stu-id="f4677-p104">The recipients of the message whose names you want to put on the <strong>To</strong> line in the mail message. If you leave this argument blank, Access prompts you for the recipients' names. Separate the recipients' names you specify in this argument (and in the <strong>Cc</strong> and <strong>Bcc</strong> arguments) with a semicolon (;) or with the list separator set on the <strong>Number</strong> tab of the <strong>Regional Settings Properties</strong> dialog box in Microsoft Windows <strong>Control Panel</strong>. If the mail application can't identify the recipients' names, the message isn't sent and an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4677-133"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="f4677-133"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="f4677-134">Os destinatários da mensagem cujos nomes você deseja colocar na linha <strong>Cc</strong> (cópia &quot; &quot; carbono) da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="f4677-134">The message recipients whose names you want to put on the <strong>Cc</strong> (&quot;carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="f4677-135">Se você deixar este argumento em branco, a linha <strong>Cc</strong> da mensagem de email ficará em branco.</span><span class="sxs-lookup"><span data-stu-id="f4677-135">If you leave this argument blank, the <strong>Cc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4677-136"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="f4677-136"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="f4677-137">Os destinatários da mensagem cujos nomes você deseja colocar na linha <strong>Cc</strong> ( &quot; cópia &quot; carbono) da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="f4677-137">The message recipients whose names you want to put on the <strong>Bcc</strong> (&quot;blind carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="f4677-138">Se você deixar este argumento em branco, a linha <strong>Cco</strong> ficará em branco.</span><span class="sxs-lookup"><span data-stu-id="f4677-138">If you leave this argument blank, the <strong>Bcc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4677-139"><strong>Assunto</strong></span><span class="sxs-lookup"><span data-stu-id="f4677-139"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="f4677-p107">O assunto da mensagem. Esse texto aparece na linha <strong>Assunto</strong> da mensagem de email. Se você deixar este argumento em branco, a linha <strong>Assunto</strong> ficará em branco.  </span><span class="sxs-lookup"><span data-stu-id="f4677-p107">The subject of the message. This text appears on the <strong>Subject</strong> line in the mail message. If you leave this argument blank, the <strong>Subject</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4677-143"><strong>Texto da mensagem</strong></span><span class="sxs-lookup"><span data-stu-id="f4677-143"><strong>Message Text</strong></span></span></p></td>
<td><p><span data-ttu-id="f4677-p108">Qualquer texto que você quiser incluir na mensagem, adicionalmente ao objeto de banco de dados. Esse texto aparece no corpo principal da mensagem de email, depois do objeto. Se você deixar este argumento em branco, nenhum texto adicional será incluído na mensagem de email. Se deixar em branco os argumentos <strong>Tipo de objeto</strong> e <strong>Nome do objeto</strong>, você poderá usar este argumento para enviar uma mensagem de email sem um objeto de banco de dados.  </span><span class="sxs-lookup"><span data-stu-id="f4677-p108">Any text you want to include in the message in addition to the database object. This text appears in the main body of the mail message, after the object. If you leave this argument blank, no additional text is included in the mail message. If you leave the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, you can use this argument to send a mail message without a database object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4677-148"><strong>Editar mensagem</strong></span><span class="sxs-lookup"><span data-stu-id="f4677-148"><strong>Edit Message</strong></span></span></p></td>
<td><p><span data-ttu-id="f4677-p109">Especifica se a mensagem pode ser editada antes do envio. Se você selecionar <strong>Sim</strong>, o aplicativo de email será iniciado automaticamente e a mensagem poderá ser editada. Se escolher <strong>Não</strong>, a mensagem será enviada sem que o usuário tenha a oportunidade de editá-la. O padrão é <strong>Sim</strong>.  </span><span class="sxs-lookup"><span data-stu-id="f4677-p109">Specifies whether the message can be edited before it's sent. If you select <strong>Yes</strong>, the electronic mail application starts automatically, and the message can be edited. If you select <strong>No</strong>, the message is sent without the user having a chance to edit the message. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4677-153"><strong>Arquivo de Modelo</strong></span><span class="sxs-lookup"><span data-stu-id="f4677-153"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="f4677-p110">O caminho e o nome do arquivo que você deseja usar como modelo para um arquivo HTML. O arquivo de modelo contém marcas HTML.</span><span class="sxs-lookup"><span data-stu-id="f4677-p110">The path and file name of a file you want to use as a template for an HTML file. The template file is a file containing HTML tags.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f4677-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4677-156">Remarks</span></span>

<span data-ttu-id="f4677-p111">O objeto na mensagem de email está no formato de saída selecionado. Quando você clica duas vezes no objeto, o software adequado é iniciado com o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="f4677-p111">The object in the mail message is in the selected output format. When you double-click the object, the appropriate software starts with the object opened.</span></span>

<span data-ttu-id="f4677-159">As regras a seguir são aplicáveis quando você usa a ação **EnviarObjetodeBancodeDadosporEMail** para incluir um objeto de banco de dados em uma mensagem de email:</span><span class="sxs-lookup"><span data-stu-id="f4677-159">The following rules apply when you use the **EMailDatabaseObject** action to include a database object in a mail message:</span></span>

- <span data-ttu-id="f4677-p112">Você pode enviar uma tabela, uma consulta e folhas de dados de formulário. No objeto incluído, todos os campos da folha de dados mantêm a mesma aparência do Access, exceto os campos que contêm objetos OLE. As colunas desses campos estão incluídas no objeto, mas os campos estão em branco.</span><span class="sxs-lookup"><span data-stu-id="f4677-p112">You can send table, query, and form datasheets. In the included object, all fields in the datasheet look as they do in Access, except fields containing OLE objects. The columns for these fields are included in the object, but the fields are blank.</span></span>

- <span data-ttu-id="f4677-163">Para um controle acoplado a um campo Sim/Não (um botão de alternância, um botão de opção ou uma caixa de seleção), o arquivo de saída exibe o valor –1 (Sim) ou 0 (Não).</span><span class="sxs-lookup"><span data-stu-id="f4677-163">For a control bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

- <span data-ttu-id="f4677-164">Para uma caixa de texto acoplada a um campo Hiperlink, o arquivo de saída exibe o hiperlink para todos os formatos de saída, exceto o texto MS-DOS (nesse caso, o hiperlink é exibido apenas como texto normal).</span><span class="sxs-lookup"><span data-stu-id="f4677-164">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats except MS-DOS text (in this case, the hyperlink is just displayed as normal text).</span></span>

- <span data-ttu-id="f4677-165">Se você enviar um formulário no modo Formulário, o objeto incluído sempre conterá o modo Folha de Dados do formulário.</span><span class="sxs-lookup"><span data-stu-id="f4677-165">If you send a form in Form view, the included object always contains the form's Datasheet view.</span></span>

- <span data-ttu-id="f4677-p113">Se você enviar um relatório, os únicos controles incluídos no objeto serão caixas de texto e, em alguns casos, rótulos. Todos os outros controles serão ignorados. As informações de cabeçalho e rodapé também não serão incluídas. A única exceção é que, quando você envia um relatório no formato Excel, uma caixa de texto em um rodapé de grupo, contendo uma expressão com a função **Soma**, é incluída no objeto. Nenhum outro controle em um cabeçalho ou em um rodapé (e nenhuma outra função de agregação além de **Soma**) será incluído no objeto.</span><span class="sxs-lookup"><span data-stu-id="f4677-p113">If you send a report, the only controls that are included in the object are text boxes and (in some cases) labels. All other controls are ignored. Header and footer information is also not included. The only exception to this is that when you send a report in Excel format, a text box in a group footer containing an expression with the **Sum** function is included in the object. No other control in a header or footer (and no aggregate function other than **Sum**) is included in the object.</span></span>

- <span data-ttu-id="f4677-171">Os sub-relatórios estão incluídos no objeto.</span><span class="sxs-lookup"><span data-stu-id="f4677-171">Subreports are included in the object.</span></span>

- <span data-ttu-id="f4677-p114">Quando você enviar uma folha de dados, um formulário ou uma página de acesso a dados no formato HTML, será criado um arquivo .html. Quando enviar um relatório no formato HTML, será criado um arquivo .html para cada página do relatório.</span><span class="sxs-lookup"><span data-stu-id="f4677-p114">When you send a datasheet, form, or data access page in HTML format, one .html file is created. When you send a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="f4677-174">Para executar a ação **EnviarObjetodeBancodeDadosporEMail** em um módulo do VBA (Visual Basic for Applications), use o método **EnviarObjeto** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="f4677-174">To run the **EMailDatabaseObject** action in a Visual Basic for Applications (VBA) module, use the **SendObject** method of the **DoCmd** object.</span></span>

### <a name="about-the-contributor"></a><span data-ttu-id="f4677-175">Sobre o colaborador</span><span class="sxs-lookup"><span data-stu-id="f4677-175">About the contributor</span></span>

<span data-ttu-id="f4677-176">**Link fornecido por** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), o fundador e presidente da FMS, Inc., um provedor líder de soluções de banco de dados personalizadas e ferramentas de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="f4677-176">**Link provided by** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), the founder and president of FMS, Inc., a leading provider of custom database solutions and developer tools.</span></span>

- [<span data-ttu-id="f4677-177">Recursos e limites do uso do Método SendObject para envio</span><span class="sxs-lookup"><span data-stu-id="f4677-177">Features and Limits of Using the SendObject Method to Send</span></span>](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





