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
ms.openlocfilehash: ef0f4ad298e316cbae295bcf4f6c4c5349b18655
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998529"
---
# <a name="recordset2fillcache-method-dao"></a>Método Recordset2.FillCache (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Preenche parcial ou totalmente um cache local de um objeto **Recordset** que contém dados de uma fonte de dados ODBC conectada ao mecanismo de banco de dados do Microsoft Access (somente bancos de dados ODBC conectados ao mecanismo de banco de dados do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . FillCache (***linhas***, ***StartBookmark***)

*expressão* Uma variável que representa um objeto **Recordset2** .

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
<th><p>Obrigatório/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Rows</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um <strong>Variant</strong> (subtipo <strong>Integer</strong>) que especifica o número de linhas a ser armazenado no cache. Se você omitir esse argumento, o valor será determinado pela configuração da propriedade <strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>StartBookmark</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um <strong>Variant</strong> (subtipo <strong>String</strong>) que especifica um indicador. O cache é preenchido começando pelo registro indicado por esse indicador. Se você omitir esse argumento, o cache será preenchido começando do registro indicado pela propriedade <strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Fazer cache melhora o desempenho de um aplicativo que recupera dados de um servidor remoto. Cache é um espaço na memória local que conserva os dados recuperados mais recentemente do servidor; isso pressupõe que os dados provavelmente serão solicitados de novo enquanto o aplicativo estiver sendo executado. Quando um usuário solicita dados, o mecanismo do banco de dados do Microsoft Access verifica os dados primeiramente no cache em vez de recuperá-los do servidor, o que leva mais tempo. O cache não salva dados que não sejam provenientes de uma fonte de dados ODBC.

Em vez de esperar que o cache seja preenchido com registros enquanto eles são recuperados, você pode usar o método **FillCache** para preencher explicitamente o cache a qualquer momento. Essa é uma maneira mais rápida de preencher o cache porque **FillCache** recupera vários registros de uma vez, e não um de cada vez. Por exemplo, enquanto você exibe cada tela de registros, seu aplicativo usa **FillCache** para recuperar a próxima tela de registros para exibição.

Qualquer fonte de dados ODBC conectada ao mecanismo de banco de dados do Microsoft Access que você acessa com objetos **Recordset** pode ter um cache local. Para criar o cache, abra um objeto **Recordset** a partir da fonte de dados remota e, em seguida, defina as propriedades **CacheSize** e **CacheStart** do **Recordset**.

Se linhas e startbookmark criam um intervalo de registros que é parcialmente ou totalmente fora do intervalo dos registros especificados pelas propriedades **CacheSize** e **CacheStart** , a parte do recordset fora deste intervalo será ignorada e não será carregada para o cache.

Se **FillCache** solicitar mais registros do que o número restante na fonte de dados remota, o mecanismo de banco de dados do Microsoft Access recuperará apenas os registros restantes e não ocorrerá um erro.

> [!NOTE]
> - Registros recuperados do cache não refletem alterações concorrentes que outros usuários fazem nos dados de origem.
> - **FillCache** recupera apenas registros para os quais não foi feito cache. Para forçar uma atualização de todos os dados com cache, defina a propriedade **CacheSize** do **Recordset** para 0, redefina-a de acordo com o tamanho do cache que você originalmente solicitou e, em seguida, use **FillCache**.

## <a name="example"></a>Exemplo

Este exemplo usa os métodos **CreateTableDef** e **FillCache** e as propriedades **CacheSize**, **CacheStart** e **SourceTableName** para enumerar os registros em uma tabela vinculada duas vezes. Em seguida, enumeram-se os registros duas vezes com um cache de 50 registros. O exemplo exibe então as estatísticas de desempenho das execuções sem cache e com cache por meio da tabela vinculada.

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
