---
title: Método Recordset2.FillCache (DAO)
TOCTitle: FillCache Method
ms:assetid: 28a70997-a8d4-73e6-171a-61286e3d3485
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192007(v=office.15)
ms:contentKeyID: 48543864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052942
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2098df82375ac47b7d5abe0bd63b0af2bb29ba40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309699"
---
# <a name="recordset2fillcache-method-dao"></a>Método Recordset2.FillCache (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Preenche todo ou uma parte do cache local para um objeto **Recordset** que contém dados de uma fonte de dados ODBC conectada ao mecanismo de banco de dados do Microsoft Access (apenas bancos de dados ODBC conectados ao mecanismo de banco de dados do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . FillCache(***Rows***, ***StartBookmark***)

*expressão* Uma variável que representa **um objeto Recordset2** .

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Necessária/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Linhas</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variantes</strong></p></td>
<td><p>Um <strong>Variant</strong> (subtipo <strong>Integer</strong>) que especifica o número de linhas a ser armazenado no cache. Se você omitir esse argumento, o valor será determinado pela configuração da propriedade <strong><a href="recordset2-cachesize-property-dao.md">CacheSize.</a></strong></p></td>
</tr>
<tr class="even">
<td><p><em>StartBookmark</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variantes</strong></p></td>
<td><p>Um <strong>Variant</strong> (subtipo <strong>String</strong>) que especifica um indicador. O cache é preenchido começando pelo registro indicado por esse indicador. Se você omitir esse argumento, o cache será preenchido começando pelo registro indicado pela <strong><a href="recordset2-cachestart-property-dao.md">propriedade CacheStart.</a></strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O armazenamento em cache aumenta o desempenho de um aplicativo que recupera dados de um servidor remoto. Um cache é o espaço na memória local que mantém os dados recuperados mais recentemente do servidor; isso indica que provavelmente os dados serão solicitados novamente durante a execução do aplicativo. Quando um usuário solicita dados, o mecanismo de banco de dados do Microsoft Access verifica esses dados no cache primeiro em vez de recuperá-los do servidor, o que leva mais tempo. O cache não salva dados que não são provenientes de uma fonte de dados ODBC.

Em vez de aguardar que o cache seja preenchido com registros à medida que eles são recuperados, você pode usar o método **FillCache** para preencher explicitamente o cache a qualquer momento. Esse é um modo mais rápido de preencher o cache porque **FillCache** recupera vários registros de uma vez, e não um por vez. Por exemplo, enquanto você exibe cada tecla cheia de registros, seu aplicativo usa **FillCache** para recuperar a próxima tela cheia de registros para exibição.

Qualquer fonte de dados ODBC conectada ao mecanismo de banco de dados do Microsoft Access que você acessa com os objetos **Recordset** pode ter um cache local. Para criar o cache, abra um objeto **Recordset** na fonte de dados remota e, em seguida, defina as propriedades **CacheSize** e **CacheStart** do **Recordset**.

Se as linhas e o startbookmark criarem um intervalo de registros parcial ou totalmente fora do intervalo de registros especificado pelas propriedades **CacheSize** e **CacheStart,** a parte do recordset fora desse intervalo será ignorada e não será carregada no cache.

Se **FillCache** solicitar mais registros do que o número restante na fonte de dados remota, o mecanismo do banco de dados do Microsoft Access irá recuperar somente os registros restantes, e não ocorrerá nenhum erro.

> [!NOTE]
> - Os registros recuperados do cache não refletem as alterações simultâneas que outros usuários fizeram na fonte de dados.
> - O **FillCache** recupera apenas os registros não armazenados em cache. Para forçar uma atualização de todos os dados em cache, defina a propriedade **CacheSize** do **Recordset** como 0, redefina-a para o tamanho do cache solicitado originalmente e use **FillCache**.

## <a name="example"></a>Exemplo

Este exemplo usa os métodos **CreateTableDef** e **FillCache** e as propriedades **CacheSize**, **CacheStart** e **SourceTableName** para enumerar os registros vinculados à tabela duas vezes. Em seguida, enumera os registros duas vezes com um cache de 50 registros. Depois, exemplo exibe as estatísticas de desempenho das execuções com cache e sem cache por meio da tabela vinculada.

```vb
    Sub ClientServerX3() 
     
       Dim dbsCurrent As Database 
       Dim tdfRoyalties As TableDef 
       Dim rstRemote As Recordset2 
       Dim sngStart As Single 
       Dim sngEnd As Single 
       Dim sngNoCache As Single 
       Dim sngCache As Single 
       Dim intLoop As Integer 
       Dim strTemp As String 
       Dim intRecords As Integer 
     
       ' Open a database to which a linked table can be  
       ' appended. 
       Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
       ' Create a linked table that connects to a Microsoft SQL 
       ' Server database. 
       Set tdfRoyalties = _ 
          dbsCurrent.CreateTableDef("Royalties") 
       ' Note: The DSN referenced below must be set to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
       tdfRoyalties.Connect = _ 
          "ODBC;DATABASE=pubs;DSN=Publishers" 
       tdfRoyalties.SourceTableName = "roysched" 
       dbsCurrent.TableDefs.Append tdfRoyalties 
       Set rstRemote = _ 
          dbsCurrent.OpenRecordset("Royalties") 
     
       With rstRemote 
          ' Enumerate the Recordset object twice and record 
          ' the elapsed time. 
          sngStart = Timer 
     
          For intLoop = 1 To 2 
             .MoveFirst 
             Do While Not .EOF 
                ' Execute a simple operation for the 
                ' performance test. 
                strTemp = !title_id 
                .MoveNext 
             Loop 
          Next intLoop 
     
          sngEnd = Timer 
          sngNoCache = sngEnd - sngStart 
     
          ' Cache the first 50 records. 
          .MoveFirst 
          .CacheSize = 50 
          .FillCache 
          sngStart = Timer 
     
          ' Enumerate the Recordset object twice and record 
          ' the elapsed time. 
          For intLoop = 1 To 2 
             intRecords = 0 
             .MoveFirst 
             Do While Not .EOF 
                ' Execute a simple operation for the 
                ' performance test. 
                strTemp = !title_id 
                ' Count the records. If the end of the 
                ' cache is reached, reset the cache to the 
                ' next 50 records. 
                intRecords = intRecords + 1 
                .MoveNext 
                If intRecords Mod 50 = 0 Then 
                   .CacheStart = .Bookmark 
                   .FillCache 
                End If 
             Loop 
          Next intLoop 
     
          sngEnd = Timer 
          sngCache = sngEnd - sngStart 
     
          ' Display performance results. 
          MsgBox "Caching Performance Results:" & vbCr & _ 
             "  No cache: " & Format(sngNoCache, _ 
             "##0.000") & " seconds" & vbCr & _ 
             "  50-record cache: " & Format(sngCache, _ 
             "##0.000") & " seconds" 
          .Close 
       End With 
     
       ' Delete linked table because this is a demonstration. 
       dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
       dbsCurrent.Close 
     
    End Sub
```
