---
title: Ação de macro ImportExportData
TOCTitle: ImportExportData Macro Action
ms:assetid: 2cbde873-8a3d-b15c-4aab-405cddf44cea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192107(v=office.15)
ms:contentKeyID: 48543961
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm51789
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d61d298da0e3b44895c8fce3ee1adc3b55d9a491
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464983"
---
# <a name="importexportdata-macro-action"></a>Ação de macro ImportExportData

**Aplica-se a**: Access 2013 | Office 2013

Você pode usar a ação **ImportExportData** para importar ou exportar dados entre o banco de dados atual do Access (.mdb ou .accdb) ou o projeto do Access (.adp) e outro banco de dados. Para bancos de dados do Microsoft Access, você também pode vincular uma tabela ao banco de dados atual do Access de outro banco de dados. Com uma tabela vinculada, você tem acesso aos dados da tabela enquanto a própria tabela permanece em outro banco de dados.

> [!NOTE]
> [!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.

## <a name="settings"></a>Configurações

A ação **ImportExportData** tem os argumentos a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Tipo de transferência</strong></p></td>
<td><p>O tipo de transferência que você deseja fazer. Selecione <strong>Importar</strong>, <strong>Exportar</strong> ou <strong>Vincular</strong> na caixa <strong>Tipo de Transferência</strong> na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. O padrão é <strong>Importar</strong>.  </p>

> [!NOTE]
> O tipo de transferência **Vincular** não tem suporte para projetos do Access (.adp).


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Tipo de Banco de Dados</strong></p></td>
<td><p>O tipo de banco de dados de onde será importado, para onde será exportado ou vinculado. Você pode selecionar o <strong>Microsoft Access</strong> ou um dos vários tipos de banco de dados na caixa <strong>Tipo de Banco de Dados</strong>. O padrão é <strong>Microsoft Access</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Nome do Banco de Dados</strong></p></td>
<td><p>O nome do banco de dados de onde será importado, para onde será exportado ou vinculado. Inclua o caminho completo. Esse é um argumento obrigatório. Para tipos de bancos de dados que usam arquivos separados para cada tabela, como FoxPro, Paradox e dBASE, insira o diretório que contém o arquivo. Insira o nome do arquivo no argumento <strong>Origem</strong> (para importar ou vincular) ou o argumento <strong>Destino</strong> (para exportar). Para bancos de dados ODBC, digite a cadeia de conexão completa ODBC (Open Database Connectivity).  </p>
<p>Para ver um exemplo de uma cadeia de conexão, vincule uma tabela externa ao Access:</p>
<ol>
<li><p>Na caixa de diálogo <strong>Obter Dados Externos</strong>, insira o caminho do seu banco de dados de origem na caixa <strong>Nome do arquivo</strong>.</p></li>
<li><p>Clique em <strong>Vincular à fonte de dados criando uma tabela vinculada</strong> e clique em <strong>OK</strong>.</p></li>
<li><p>Selecione uma tabela na caixa de diálogo <strong>Vincular Tabelas</strong> e clique em <strong>OK</strong>.</p></li>
</ol>
<p>Abra a tabela recentemente vinculada no modo Design e exiba as propriedades da tabela clicando em <strong>Folha de Propriedades</strong> na guia <strong>Design</strong>, em <strong>Ferramentas</strong>. O texto na configuração de propriedade <strong>Descrição</strong> é a cadeia de conexão para esta tabela.  </p>
<p>Para saber mais sobre as cadeias de conexão ODBC, consulte o arquivo da Ajuda ou outra documentação para o driver ODBC deste tipo de banco de dados ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tipo de Objeto</strong></p></td>
<td><p>O tipo de objeto a ser importado ou exportado. Se você selecionar <strong>Microsoft Access</strong> para o argumento <strong>Tipo de Banco de Dados</strong>, poderá selecionar <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Exibição de Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong>. O padrão é <strong>Tabela</strong>. Se você selecionar qualquer outro tipo de banco de dados ou se você selecionar <strong>Link</strong> na caixa <strong>Tipo de Transferência</strong>, esse argumento será ignorado. Se você estiver exportando uma consulta seleção para um banco de dados do Access, selecione <strong>Tabela</strong> nesse argumento para exportar o conjunto de resultados da consulta e selecione <strong>Consulta</strong> para exportar a própria consulta. Se você estiver exportando uma consulta seleção para outro tipo de banco de dados, esse argumento será ignorado e o conjunto de resultados da consulta será exportado.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Origem</strong></p></td>
<td><p>O nome da tabela, da consulta seleção ou do objeto do Access que você deseja importar, exportar ou vincular. Para alguns tipos de bancos de dados, como FoxPro, Paradox ou dBASE, esse é o nome do arquivo. Inclua a extensão do nome do arquivo (como .dbf) no nome do arquivo. Esse é um argumento obrigatório.</p></td>
</tr>
<tr class="even">
<td><p><strong>Destino</strong></p></td>
<td><p>O nome da tabela, consulta seleção ou objeto do Access importado, exportado ou vinculado no banco de dados de destino. Para alguns tipos de bancos de dados, como FoxPro, Paradox ou dBASE, é o nome do arquivo. Inclua o a extensão do nome do arquivo (como .dbf) no nome do arquivo. Esse é um argumento obrigatório. Se você selecionar <strong>Importar</strong> no argumento <strong>Tipo de Transferência</strong> e <strong>Tabela</strong> no argumento <strong>Tipo de Objeto</strong>. O Access cria uma nova tabela com os dados da tabela importada. Se você importar uma tabela ou outro objeto, o Access adiciona um número ao nome caso ele esteja em conflito com um nome existente. Por exemplo, se você importar Funcionários e Funcionários já existir, o Access renomeará a tabela ou outro objeto importado como Funcionários1. Se você exportar para um banco de dados do Access ou para outro banco de dados, o Access substituirá automaticamente qualquer tabela ou outro objeto existente com o mesmo nome.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Somente Estrutura</strong></p></td>
<td><p>Especifica se é necessário importar ou exportar somente a estrutura de uma tabela do banco de dados sem qualquer um desses dados. Selecione <strong>Sim</strong> ou <strong>Não</strong>. O padrão é <strong>Não</strong>.  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode importar e exportar tabelas entre o Access e outros tipos de bancos de dados. Também é possível exportar consultas seleção do Access para outros tipos de bancos de dados. O Access exporta o conjunto de resultados da consulta no formato de uma tabela. Você poderá importar e exportar qualquer objeto de banco de dados do Access caso ambos os bancos de dados sejam bancos de dados do Access.

Se você importar uma tabela de outro banco de dados do Access (.mdb ou .accdb) que seja uma tabela vinculada naquele banco de dados, ela ainda estará vinculada após a importação. Ou seja, o link é importado, e não a própria tabela.

Se o banco de dados que você está acessando exigir uma senha, será exibida uma caixa de diálogo quando você executar a macro. Digite a senha nessa caixa de diálogo.

A ação **ImportExportData** é semelhante aos comandos na guia **Dados Externos**, sob **Importar** ou **Exportar**. Você pode usar esses comandos para selecionar uma fonte de dados, como um banco de dados do Access ou outro tipo de banco de dados, uma planilha ou um arquivo de texto. Se você selecionar um banco de dados, uma ou mais caixas de diálogo aparecerão e você poderá selecionar o tipo de objeto a ser importado ou exportado (para bancos de dados do Access), o nome do objeto e outras opções, dependendo do banco de dados para o qual você esteja exportação ou vinculando. Os argumentos para a ação **ImportExportData** refletem as opções nessas caixas de diálogo.

Se você quiser fornecer informações de índice para uma tabela dBASE vinculada, primeiro vincule a tabela:

1.  Clique em **Arquivo dBASE**.

2.  Na caixa de diálogo **Obter Dados Externos**, insira o caminho para o arquivo dBASE na caixa **Nome do arquivo**.

3.  Clique em **Vincular à fonte de dados criando uma tabela vinculada** e, em seguida, clique em **OK**.

4.  Especifique os índices nas caixas de diálogo para este comando. O Access armazena as informações de índice em um arquivo de informações (.inf) especial, localizado na pasta do Microsoft Office.

5.  Então, você pode excluir o link para a tabela vinculada.

Na próxima vez em que você usar a ação **ImportExportData** para vincular esta tabela dBASE, o Access usará as informações de índice especificadas.

> [!NOTE]
> [!OBSERVAçãO] Se você consultar ou filtrar uma tabela vinculada, a consulta ou o filtro diferenciará maiúsculas de minúsculas.

Para executar a ação **ImportExportData** em um módulo do Visual Basic for Applications (VBA), use o método **TransferDatabase** do objeto **DoCmd**.

