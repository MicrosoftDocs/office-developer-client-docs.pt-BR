---
title: Ação de Macro ImportExportText
TOCTitle: ImportExportText Macro Action
ms:assetid: 366fa095-6f09-7c22-e734-bfa585cfe79e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192475(v=office.15)
ms:contentKeyID: 48544171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168097
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c4ea6feeec4c8d4189b80354e41a01de61da4e30
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464363"
---
# <a name="importexporttext-macro-action"></a>Ação de Macro ImportExportText

**Aplica-se a**: Access 2013 | Office 2013

Você pode usar a ação **Importarexportartexto** para importar ou exportar texto entre o banco de dados Microsoft Access atual (. mdb ou. accdb) ou projeto do Access (. adp) e um arquivo de texto. Você também pode vincular os dados em um arquivo de texto para o banco de dados do Access atual. Com um arquivo de texto vinculado, você pode exibir os dados de texto com o Access enquanto ainda permite acesso completo aos dados do seu programa de processamento de palavras. Você também pode importar de, exportar para e vincular a uma tabela ou lista em um arquivo HTML (\*. HTML).

> [!NOTE]
> [!OBSERVAçãO] Se você vincular a dados de um arquivo de texto ou de um arquivo HTML, os dados ficarão somente leitura no Access.
> 
> [!OBSERVAçãO] This action will not be allowed if the database is not trusted. 

## <a name="setting"></a>Configuração

A ação **ImportExportText** tem os seguintes argumentos.

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
<td><p>O tipo de transferência que você deseja fazer. Você pode importar dados, exportar dados ou vincular a dados em arquivos de texto ou HTML delimitados e de largura fixa. também é possível exportar dados para um arquivo de dados de mala direta do Microsoft Word, que poderá então ser usado com o recurso de mala direta do Word para criar documentos mesclados, como cartas modelo e etiquetas de endereçamento. Selecione <strong>Importação Delimitada</strong>, <strong>Importar Largura Fixa</strong>, <strong>Importar HTML</strong>, <strong>Exportação Delimitada</strong>, <strong>Exportar Largura Fixa</strong>, <strong>Exportar HTML</strong>, <strong>Exportar mala direta do Word para Windows</strong>, <strong>Vínculo delimitado</strong>, <strong>Vínculo com largura fixa</strong> ou <strong>Vínculo HTML</strong> na caixa <strong>Tipo de Transferência</strong> na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. O padrão é <strong>Importação Delimitada</strong>.  </p>

> [!NOTE]
> <P>Somente os tipos de transferência <STRONG>Importação Delimitada</STRONG>, <STRONG>Importação com Largura Fixa</STRONG>, <STRONG>Exportação Delimitada</STRONG>, <STRONG>Exportação com Largura Fixa</STRONG> ou <STRONG>Exportar mala direta do Word para Windows</STRONG> têm suporte em um projeto do Access (.adp).</P>


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Nome da especificação</strong></p></td>
<td><p>O nome da especificação para o conjunto de opções que determina como um arquivo de texto será importando ou vinculado. Para um arquivo de texto de largura fixa, você especificará um argumento ou usará um arquivo schema.ini, que deve ser armazenado na mesma pasta que o arquivo de texto importado ou vinculado.  </p>
<p>Para criar uma especificação para importação ou vinculação de um arquivo de texto:</p>
<ol>
<li><p>Na caixa de diálogo <strong>Obter Dados Externos</strong>, insira o caminho do arquivo de texto de origem na caixa <strong>Nome do arquivo</strong>.</p></li>
<li><p>Clique na opção que você deseja para o armazenamento dos dados (importar, anexar ou vincular) e clique em <strong>OK</strong>.</p></li>
<li><p>Na caixa de diálogo <strong>Assistente de importação de texto</strong>, clique em <strong>Avançado</strong>.</p></li>
<li><p>Especifique as opções desejadas para esta especificação e, então, clique em <strong>Salvar como</strong>.</p></li>
<li><p>Insira o nome desejado para a especificação e, então, clique em <strong>OK</strong>.</p></li>
<li><p>Você pode gerenciar especificações existentes clicando em <strong>Especificações</strong> na caixa de diálogo de especificação.</p></li>
<li><p>Clique em <strong>OK</strong> para fechar a caixa de diálogo de especificação.</p></li>
</ol>
<p></p>
<p>Você poderá então digitar o nome da especificação nesse argumento sempre que quiser importar ou exportar o mesmo tipo de arquivo de texto. É possível importar, exportar ou vincular arquivos de texto delimitados sem digitar um nome de especificação para esse argumento. Nesse caso, o Access usa os padrões da caixa de diálogo do assistente. O Access usa um formato predeterminado para arquivos de dados de mala direta e, portanto, não será necessário nem mesmo digitar um nome de especificação para esse argumento quando esses tipos de arquivos forem exportados. Você pode usar especificações de importação/exportação com arquivos HTML, mas a única parte da especificação que se aplicarão será a especificação para a formatação do tipo de dados.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Nome da Tabela</strong></p></td>
<td><p>O nome da tabela do Access para a qual serão importados dados de texto, para a qual os dados de texto serão exportados ou à qual os dados de texto serão vinculados. Você também pode digitar o nome da consulta do Access da qual deseja exportar dados. É um argumento obrigatório. Se você clicar em <strong>Importação Delimitada</strong>, em <strong>Importação com Largura Fixa</strong> ou em <strong>Importação HTML</strong> na caixa <strong>Tipo de Transferência</strong>, anexará os dados de texto a essa tabela caso a tabela já exista. Caso contrário, o Access criará uma nova tabela com os dados de texto. Você não pode usar uma instrução SQL para especificar dados a serem exportados quando estiver usando a ação <strong>ImportExportText</strong>. Em vez de usar uma instrução SQL, primeiro será necessário criar uma consulta e então especificar o nome da consulta no argumento <strong>Nome da Tabela</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Nome do Arquivo</strong></p></td>
<td><p>O nome do arquivo de texto do qual importar, para o qual exportar ou ao qual vincular. Inclua o caminho completo. É um argumento obrigatório. O Access cria um novo arquivo de texto quando você exporta dados do Access. Se o nome do arquivo for igual ao nome de um arquivo de texto existente, o Access substituirá o arquivo de texto existente. Se quiser importar ou vincular uma tabela ou lista em particular em um arquivo HTML, você poderá usar o argumento <strong>Nome da Tabela HTML</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Tem Nomes de Campo</strong></p></td>
<td><p>Especifica se a primeira linha do arquivo de texto contém os nomes dos campos. Se você selecionar <strong>Sim</strong>, o Access usará os nomes dessa linha como nomes de campo na tabela do Access quando você importar ou vincular os dados de texto. Se você selecionar <strong>Não</strong>, o Access tratará a primeira linha como uma linha normal de dados. O padrão é <strong>Não</strong>. O Access ignora esse argumento para os arquivos de dados de mala direta do Word para Windows porque a primeira linha deve conter os nomes de campo. Quando você exporta uma tabela do Access ou uma consulta seleção para um arquivo de texto delimitado ou de largura fixa, o Access insere os nomes de campo de sua tabela ou consulta seleção na primeira linha do arquivo de texto caso você tenha selecionado <strong>Sim</strong> para esse argumento. Se você estiver importando ou vinculando um arquivo de texto de largura fixa e selecionar <strong>Sim</strong> nessa caixa, a primeira linha com os nomes de campo deverão usar o delimitador de campo definido na especificação de importação/exportação para separar os nomes de campo. Se você estiver exportando um arquivo de texto de largura fixa e selecionar <strong>Sim</strong> para esse argumento, o Access inserirá os nomes de campo na primeira linha do arquivo de texto com esse delimitador.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Nome de Tabela HTML</strong></p></td>
<td><p>O nome da tabela ou lista no arquivo HTML que você deseja importar ou vincular. Esse argumento será ignorado, a menos que o argumento <strong>Tipo de Transferência</strong> esteja definido como Importação HTML ou Vinculação HTML. Se você deixar esse argumento em branco, a primeira tabela ou lista no arquivo HTML será importada ou vinculada. O nome de tabela ou lista no arquivo HTML é determinado pelo texto especificado pelo &lt;legenda&gt; marcar, se houver um &lt;legenda&gt; marca. Se não houver nenhuma marca &lt;CAPTION&gt;, o nome será determinado pelo texto especificado pela marca &lt;TITLE&gt;. Se mais de uma tabela ou lista tiverem o mesmo nome, o Access as distinguirá adicionando um número ao final de cada nome; por exemplo, Funcionários1 e Funcionários2.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Página de Código</strong></p></td>
<td><p>O nome do conjunto de caracteres usados com o página de código.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode exportar os dados em consultas seleção do Access para arquivos de texto. O Access exporta o conjunto de resultados da consulta, tratando-o da mesma forma de uma tabela.

Os dados de texto que você anexa a uma tabela do Access existente devem ser compatíveis com a estrutura da tabela.

- Todos os campos no texto devem ter o mesmo tipo de dados que o campo correspondente na tabela.

- Os campos devem estar na mesma ordem (a menos que você defina o argumento **Tem Nomes de Campo** como **Sim**; nesse caso, os nomes de campo no texto deverão corresponder aos nomes de campo na tabela).

Essa ação é semelhante a clicar em **Arquivo de Texto** no grupo **Importar** ou **Exportar** na guia **Dados Externos**. Os argumentos da ação **ImportExportText** refletem as opções no assistente iniciado pelo comando **Arquivo de Texto**.

> [!TIP]
> [!DICA] Uma especificação de importação/exportação armazena as informações de que o Access precisa para importar, exportar ou vincular um arquivo de texto. Você pode usar especificações armazenadas para importar, exportar ou vincular dados de texto de ou para arquivos de texto semelhantes. Por exemplo, você poderia receber números de vendas semanais em um arquivo de texto de um computador mainframe. É possível criar e salvar uma especificação para esse tipo de dados e então usar a especificação sempre que você adicionar esses dados ao seu banco de dados do Access.

> [!NOTE]
> [!OBSERVAçãO] Se você consultar ou filtrar um arquivo de texto vinculado, a consulta ou o filtro diferenciará maiúsculas de minúsculas.

Para executar a ação **ImportExportText** em um módulo do Visual Basic for Applications (VBA), use o método **TransferText** do objeto **DoCmd**.

