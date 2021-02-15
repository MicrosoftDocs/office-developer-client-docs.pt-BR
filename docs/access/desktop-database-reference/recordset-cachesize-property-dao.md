---
title: Propriedade Recordset.CacheSize (DAO)
TOCTitle: CacheSize Property
ms:assetid: 8632f5fb-6e5d-5a3e-1bd7-81e1270e9531
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196807(v=office.15)
ms:contentKeyID: 48546079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 369ff9192bb592c96e17920c9771c10b70dc233b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300592"
---
# <a name="recordsetcachesize-property-dao"></a>Propriedade Recordset.CacheSize (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna vários registros recuperados de uma fonte de dados ODBC que serão armazenados em cache localmente. **Long** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . CacheSize

*expression* Uma variável que representa um objeto **Recordset**.

## <a name="remarks"></a>Comentários

O valor da propriedade **CacheSize** deve estar entre 5 e 1200, mas não deve ser maior que o permitido pela memória disponível. O valor típico é 100. A definição de 0 desativa o cache.

O cache de dados melhorará o desempenho, se você usar os objetos **Recordset** para recuperar dados de um servidor remoto. Um cache é um espaço na memória local que mantém os dados recuperados do servidor mais recentemente; isso será útil se os usuários solicitarem os dados novamente enquanto o aplicativo estiver em execução. Quando os usuários solicitarem os dados, o mecanismo do banco de dados do Microsoft Access verificará o cache dos dados solicitados primeiro em vez de recuperá-los do servidor, o que levará mais tempo. O cache salvará apenas os dados provenientes de uma fonte de dados ODBC.

Qualquer mecanismo de banco de dados do Microsoft Access conectado à fonte de dados ODBC, como uma tabela vinculada, pode ter um cache local. Para criar o cache, abra um objeto **Recordset** a partir da fonte de dados remota, defina as propriedades **CacheSize** e **[CacheStart](recordset-cachestart-property-dao.md)** e depois use o método **[FillCache](recordset-fillcache-method-dao.md)** ou consulte por etapas os registros usando os métodos **Move**.

Você pode basear a definição da propriedade **CacheSize** no número de registros que o aplicativo pode tratar de cada vez. Por exemplo, se você estiver usando um objeto **Recordset** como a fonte de dados que será exibida na tela, poderá definir a propriedade **CacheSize** como 20 para exibir 20 registros de cada vez.

O mecanismo do banco de dados do Microsoft Access solicita registros em um intervalo de cache a partir do cache e requisita registros de fora do intervalo de cache a partir do servidor.

Os registros recuperados do cache não refletem as alterações simultâneas que os outros usuários fizeram nos dados de origem.

Para forçar uma atualização em todos os dados armazenados, defina a propriedade **CacheSize** do objeto **Recordset** como 0, redefina-o para o tamanho de cache solicitado originalmente e depois use o método **FillCache**.

## <a name="example"></a>Exemplo

Este exemplo usa os métodos **CreateTableDef** e **FillCache** e as propriedades **CacheSize**, **CacheStart** e **SourceTableName** para enumerar os registros vinculados à tabela duas vezes. Em seguida, enumera os registros duas vezes com um cache de 50 registros. Depois, exemplo exibe as estatísticas de desempenho das execuções com cache e sem cache por meio da tabela vinculada.

```vb
    Sub ClientServerX3() 
     
     Dim dbsCurrent As Database 
     Dim tdfRoyalties As TableDef 
     Dim rstRemote As Recordset 
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
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
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
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```
