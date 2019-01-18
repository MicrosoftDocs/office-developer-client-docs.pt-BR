---
title: Usar o Microsoft Access como um servidor DDE
TOCTitle: Use Microsoft Access as a DDE Server
description: O Microsoft Access dá suporte à DDE (troca dinâmica de dados) como um aplicativo de destino (cliente) ou um aplicativo de origem (servidor).
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0750bdce0e1cda383c48f9c16e62e00997fdfb0a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716373"
---
# <a name="use-microsoft-access-as-a-dde-server"></a>Usar o Microsoft Access como um servidor DDE

**Aplica-se a**: Access 2013, o Office 2013 

O Microsoft Access dá suporte à DDE (troca dinâmica de dados) como um aplicativo de destino (cliente) ou um aplicativo de origem (servidor). Por exemplo, um aplicativo como Microsoft Word, funcionando como um cliente, pode solicitar dados através da DDE de um banco de dados do Microsoft Access que esteja funcionando como servidor.

> [!TIP]
> [!DICA] Caso você precise manipular objetos do Microsoft Access a partir de outro aplicativo, convém considerar o uso da Automação.

Uma conversação DDE entre um cliente e servidor é estabelecida em um tópico específico. Um tópico pode ser um arquivo de dados em um formato com suporte do aplicativo servidor ou o tópico System, que fornece informações sobre o próprio aplicativo servidor. Depois de uma conversação iniciada em um tópico específico, somente um item de dados associado àquele tópico pode ser transferido.

Por exemplo, suponha que você esteja executando o Microsoft Word e queira inserir dados de um banco de dados específico do Microsoft Access em um documento. Comece uma conversação DDE com o Microsoft Access abrindo um canal DDE com a função **DDEInitiate** e especificando o nome do arquivo de banco de dados como o tópico. Em seguida, será transferir os dados daquele banco de dados para o Microsoft Word por meio desse canal.

Como um servidor DDE, o Microsoft Access dá suporte a estes tópicos:

- O tópico System

- O nome de um banco de dados (tópico *database*)

- O nome de uma tabela (tópico *tablename*)

- O nome de uma consulta (tópico *queryname*)

- Uma cadeia SQL do Microsoft Access (tópico *sqlstring*)

Depois que você estabelecer uma conversação DDE, você pode usar a instrução **DDEExecute** para enviar um comando do cliente para o aplicativo de servidor. Quando usado como um servidor DDE, o Microsoft Access reconhece qualquer um destes como comandos válidos:

- O nome de uma macro no banco de dados atual.

- Qualquer ação executável no Visual Basic através de um dos métodos do objeto **DoCmd**.

- As ações AbrirBancoDeDados e FecharBancoDeDados, usadas somente para operações DDE. (Um exemplo de como usar essas ações encontra-se adiante neste tópico).

> [!NOTE]
> [!OBSERVAçãO] Quando você especifica uma ação de macro como uma instrução **DDEExecute**, a ação e quaisquer argumentos seguem a sintaxe do objeto **DoCmd** e precisam vir entre colchetes ([ ]). No entanto, aplicativos que dão suporte à DDE não reconhecem constantes intrínsecas em operações DDE. Além disso, argumentos de cadeias de caracteres precisam vir entre aspas (" ") se a cadeia contiver uma vírgula. Senão, as aspas são desnecessárias.

O aplicativo cliente pode usar a função **DDERequest** para solicitar dados de texto do aplicativo servidor através de um canal DDE aberto. Outra alternativa é o cliente usar a instrução **DDEPoke** para enviar dados ao aplicativo servidor. Quando a transferência de dados for concluída, o cliente pode usar a instrução **DDETerminate** para fechar o canal DDE ou a instrução **DDETerminateAll** para fechar todos os canais abertos.

> [!NOTE]
> [!OBSERVAçãO] Quando o aplicativo cliente termina de receber dados através de um canal DDE, deve fechar aquele canal para poupar recursos de memória.

O exemplo a seguir demonstra como criar um procedimento do Microsoft Word com Visual Basic que usa o Microsoft Access como um servidor DDE. (Para este exemplo funcionar, o Microsoft Access deve estar sendo executado).

```vb
    Sub AccessDDE() 
        Dim intChan1 As Integer, intChan2 As Integer 
        Dim strQueryData As String 
     
        ' Use System topic to open Northwind sample database. 
        ' Database must be open before using other DDE topics. 
        intChan1 = DDEInitiate("MSAccess", "System") 
        ' You may need to change this path to point to actual location 
        ' of Northwind sample database. 
        DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]" 
     
        ' Get all data from Ten Most Expensive Products query. 
        intChan2 = DDEInitiate("MSAccess", "Northwind.mdb;" _ 
            & "QUERY Ten Most Expensive Products") 
        strQueryData = DDERequest(intChan2, "All") 
        DDETerminate intChan2 
     
        ' Close database. 
        DDEExecute intChan1, "[CloseDatabase]" 
        DDETerminate intChan1 
     
        ' Print retrieved data to Debug Window. 
        Debug.Print strQueryData 
    End Sub
```

<br/>

As seções a seguir fornecem informações sobre os tópicos DDE válidos com suporte do Microsoft Access.

## <a name="the-system-topic"></a>O tópico System

O tópico System é um tópico padrão para todos os aplicativos Microsoft baseada no Windows. Ele fornece informações sobre os outros tópicos com suporte do aplicativo. Para acessar essa informação, seu código deve primeiro chamar a função **DDEInitiate** com o argumento *topic* e executar a instrução **DDERequest** com um dos seguintes fornecidos para o argumento *item* .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Item</p></th>
<th><p>Retorna</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SysItems</p></td>
<td><p>Uma lista de itens com suporte do tópico Sistema no Microsoft Access.</p></td>
</tr>
<tr class="even">
<td><p>Formats</p></td>
<td><p>Uma lista dos formatos que o Microsoft Access consegue copiar para a área de transferência.</p></td>
</tr>
<tr class="odd">
<td><p>Status</p></td>
<td><p>&quot;Ocupado&quot; ou &quot;pronto&quot;.</p></td>
</tr>
<tr class="even">
<td><p>Topics</p></td>
<td><p>Uma lista de todos os bancos de dados abertos.</p></td>
</tr>
</tbody>
</table>

<br/>

O exemplo a seguir demonstra o uso das funções **DDEInitiate** e **DDERequest** com o tópico System:

```vb
    ' In Visual Basic, initiate DDE conversation with Microsoft Access. 
    Dim intChan1 As Integer, strResults As String 
    intChan1 = DDEInitiate("MSAccess", "System") 
    ' Request list of topics supported by System topic. 
    strResults = DDERequest(intChan1, "SysItems") 
    ' Run OpenDatabase action to open Northwind.mdb. 
    ' You may need to change this path to point to actual location 
    ' of Northwind sample database. 
    DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]"
```

## <a name="the-database-topic"></a>O tópico de banco de dados

O tópico de *banco de dados* é o nome de arquivo do banco de dados existente. É possível digitar apenas o nome básico (Northwind) ou seu caminho e extensão. mdb (c:\\acesso\\amostras\\Northwind. mdb). Após iniciar uma conversação DDE com o banco de dados, você pode solicitar uma lista dos objetos naquele banco de dados.

> [!NOTE]
> [!OBSERVAçãO] Não é possível usar a DDE para consultar o arquivo de informações do grupo de trabalho do Microsoft Access.

O tópico *database* oferece suporte aos seguintes itens.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Item</p></th>
<th><p>Retorna</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>TableList</p></td>
<td><p>Uma lista de tabelas</p></td>
</tr>
<tr class="even">
<td><p>QueryList</p></td>
<td><p>Uma lista de consultas</p></td>
</tr>
<tr class="odd">
<td><p>FormList</p></td>
<td><p>Uma lista de formulários</p></td>
</tr>
<tr class="even">
<td><p>ReportList</p></td>
<td><p>Uma lista de relatórios</p></td>
</tr>
<tr class="odd">
<td><p>MacroList</p></td>
<td><p>Uma lista de macros</p></td>
</tr>
<tr class="even">
<td><p>ModuleList</p></td>
<td><p>Uma lista dos módulos</p></td>
</tr>
<tr class="odd">
<td><p>ViewList</p></td>
<td><p>Uma lista de modos.</p></td>
</tr>
<tr class="even">
<td><p>StoredProcedureList</p></td>
<td><p>Uma lista de procedimentos armazenados.</p></td>
</tr>
<tr class="odd">
<td><p>DatabaseDiagramList</p></td>
<td><p>Uma lista de diagramas de bancos de dados.</p></td>
</tr>
</tbody>
</table>

<br/>

O exemplo a seguir mostra como abrir o formulário Employees no exemplo de banco de dados Northwind a partir de um procedimento do Visual Basic:

```vb
    ' In Visual Basic, initiate DDE conversation with 
    ' Northwind sample database. 
    ' Make sure database is open. 
    intChan2 = DDEInitiate("MSAccess", "Northwind") 
    ' Request list of forms in Northwind sample database. 
    strResponse = DDERequest(intChan2, "FormList") 
    ' Run OpenForm action and arguments to open Employees form. 
    DDEExecute intChan2, "[OpenForm Employees,0,,,1,0]"
```

## <a name="the-table-topic"></a>O tópico de tabela

Esses tópicos usam a seguinte sintaxe:

_databasename_ ; **Tabela** _TableName_

_databasename_ ; **Consulta** _queryname_

_databasename_ ; **SQL** [ _sqlstring_ ]

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parte</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>databasename</em></p></td>
<td><p>O nome do banco de dados em que está a tabela ou consulta ou a que se aplica o SQL, seguido de ponto-e-vírgula (;). O nome do banco de dados pode ser apenas o nome básico (Northwind) ou seu caminho e extensão .mdb completos (C:\Access\Exemplos\Northwind.mdb).</p></td>
</tr>
<tr class="even">
<td><p><em>tablename</em></p></td>
<td><p>O nome de uma tabela existente.</p></td>
</tr>
<tr class="odd">
<td><p><em>queryname</em></p></td>
<td><p>O nome de uma consulta existente.</p></td>
</tr>
<tr class="even">
<td><p><em>sqlstring</em></p></td>
<td><p>Uma instrução SQL válida até 256 caracteres e terminando com um ponto e vírgula. Para trocar mais de 256 caracteres, omitir esse argumento e, em vez disso, use sucessivas instruções <strong>DDEPoke</strong> para formar uma instrução SQL. Por exemplo, o seguinte código Visual Basic utiliza a instrução <strong>DDEPoke</strong> para formar uma instrução SQL e, em seguida, solicitar os resultados de uma consulta.</p></td>
</tr>
</tbody>
</table>

<br/>

A tabela a seguir lista os itens válidos para os tópicos TABELA *tablename*, CONSULTA *queryname* e SQL *sqlstring*.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Item</p></th>
<th><p>Retorna</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>All</p></td>
<td><p>Todos os dados na tabela, incluindo nomes de campos.</p></td>
</tr>
<tr class="even">
<td><p>Data</p></td>
<td><p>Todas as linhas de dados, sem nomes de campos.</p></td>
</tr>
<tr class="odd">
<td><p>FieldNames</p></td>
<td><p>Uma lista de linha única de nomes de campos.</p></td>
</tr>
<tr class="even">
<td><p>FieldNames; T</p></td>
<td><p>Uma lista de duas linhas de nomes de campos (primeira linha) e seus tipos de dados (segunda linha).</p>
<p>Estes são os valores retornados:</p>
<p>Valor</p>
<p><ul>
<li>0</li>
<li>1</li>
<li>2</li>
<li>3</li>
<li>4</li>
<li>5</li>
<li>6</li>
<li>7</li>
<li>8</li>
<li>9</li>
<li>10</li>
<li>11</li>
<li>12</li>
</ul>
</p>
</td>
</tr>
<tr class="even">
<td><p>NextRow</p></td>
<td><p>Os dados na próxima linha da tabela ou consulta. Quando você abre um canal, NextRow retorna os dados da primeira linha. Se a linha atual for o último registro e você executar NextRow, a solicitação falhará.</p></td>
</tr>
<tr class="odd">
<td><p>PrevRow</p></td>
<td><p>Os dados na linha anterior da tabela ou consulta. Se PrevRow for a primeira solicitação em um novo canal, os dados na última linha da tabela ou consulta serão retornados. Se o primeiro registro for a linha atual, a solicitação a PrevRow falhará.</p></td>
</tr>
<tr class="even">
<td><p>FirstRow</p></td>
<td><p>Os dados na primeira linha da tabela ou consulta.</p></td>
</tr>
<tr class="odd">
<td><p>LastRow</p></td>
<td><p>Os dados na última linha da tabela ou consulta.</p></td>
</tr>
<tr class="even">
<td><p>FieldCount</p></td>
<td><p>O número de campos na tabela ou consulta.</p></td>
</tr>
<tr class="odd">
<td><p>SQLText</p></td>
<td><p>Uma instrução SQL que representa a tabela ou consulta. Para tabelas, esse item retorna uma instrução SQL no formato &quot;selecione `*` da <em>tabela</em>; &quot;.</p></td>
</tr>
<tr class="even">
<td><p>SQLText;<em>n</em></p></td>
<td><p>Uma instrução SQL, em que <em>n</em>-partes, representando a tabela ou consulta, onde <em>n</em> é um inteiro de até 256 de caractere. Por exemplo, suponhamos que uma consulta é representada pela seguinte instrução SQL: O item &quot;SQLText; 7&quot; retorna os seguintes blocos de delimitado por tabulação: O item &quot;SQLText; 7&quot; retorna os seguintes blocos de delimitado por tabulações:</p></td>
</tr>
</tbody>
</table>

<br/>

O exemplo a seguir mostra como usar DDE em um procedimento do Visual Basic para solicitar dados de uma tabela no exemplo de banco de dados Northwind e inserir os dados em um arquivo de texto:

```vb
    Sub NorthwindDDE 
        Dim intChan1 As Integer, intChan2 As Integer, intChan3 As Integer 
        Dim strResp1 As Variant, strResp2 As Variant, strResp3 As Variant 
     
        ' In a Visual Basic module, get data from Categories table, 
        ' Catalog query, and Orders table in Northwind.mdb. 
        ' Make sure database is open first. 
        intChan1 = DDEInitiate("MSAccess", "Northwind;TABLE Shippers") 
        intChan2 = DDEInitiate("MSAccess", "Northwind;QUERY Catalog") 
        intChan3 = DDEInitiate("MSAccess", "Northwind;SQL SELECT * " _ 
            & "FROM Orders " _ 
            & "WHERE OrderID > 10050;") 
     
        strResp1 = DDERequest(intChan1, "All") 
        strResp2 = DDERequest(intChan2, "FieldNames;T") 
        strResp3 = DDERequest(intChan3, "FieldNames;T") 
        DDETerminate intChan1 
        DDETerminate intChan2 
        DDETerminate intChan3 
     
        ' Insert data into text file. 
        Open "C:\DATA.TXT" For Append As #1 
        Print #1, strResp1 
        Print #1, strResp2 
        Print #1, strResp3 
        Close #1 
    End Sub
```
