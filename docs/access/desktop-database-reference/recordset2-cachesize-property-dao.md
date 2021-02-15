---
title: Propriedade Recordset2.CacheSize (DAO)
TOCTitle: CacheSize Property
ms:assetid: d8d195cc-6696-0583-31eb-b9988f8b7c6f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835090(v=office.15)
ms:contentKeyID: 48548042
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052927
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 94453b5bd8f5a405c5ad5b7c8a175468df2adfa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307424"
---
# <a name="recordset2cachesize-property-dao"></a><span data-ttu-id="8e134-102">Propriedade Recordset2.CacheSize (DAO)</span><span class="sxs-lookup"><span data-stu-id="8e134-102">Recordset2.CacheSize property (DAO)</span></span>


<span data-ttu-id="8e134-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e134-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e134-104">Define ou retorna vários registros recuperados de uma fonte de dados ODBC que serão armazenados em cache localmente.</span><span class="sxs-lookup"><span data-stu-id="8e134-104">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="8e134-105">**Long** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8e134-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e134-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e134-106">Syntax</span></span>

<span data-ttu-id="8e134-107">*expressão* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="8e134-107">*expression* .CacheSize</span></span>

<span data-ttu-id="8e134-108">*expressão* Uma variável que representa **um objeto Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="8e134-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e134-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e134-109">Remarks</span></span>

<span data-ttu-id="8e134-p102">O valor da propriedade **CacheSize** deve estar entre 5 e 1200, mas não deve ser maior que o permitido pela memória disponível. O valor típico é 100. A definição de 0 desativa o cache.</span><span class="sxs-lookup"><span data-stu-id="8e134-p102">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow. A typical value is 100. A setting of 0 turns off caching.</span></span>

<span data-ttu-id="8e134-p103">O cache de dados melhorará o desempenho, se você usar os objetos **Recordset** para recuperar dados de um servidor remoto. Um cache é um espaço na memória local que mantém os dados recuperados do servidor mais recentemente; isso será útil se os usuários solicitarem os dados novamente enquanto o aplicativo estiver em execução. Quando os usuários solicitarem os dados, o mecanismo do banco de dados do Microsoft Access verificará o cache dos dados solicitados primeiro em vez de recuperá-los do servidor, o que levará mais tempo. O cache salvará apenas os dados provenientes de uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="8e134-p103">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server. A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running. When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time. The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="8e134-p104">Qualquer mecanismo de banco de dados do Microsoft Access conectado à fonte de dados ODBC, como uma tabela vinculada, pode ter um cache local. Para criar o cache, abra um objeto **Recordset** a partir da fonte de dados remota, defina as propriedades **CacheSize** e **[CacheStart](recordset2-cachestart-property-dao.md)** e depois use o método **[FillCache](recordset2-fillcache-method-dao.md)** ou consulte por etapas os registros usando os métodos **Move**.</span><span class="sxs-lookup"><span data-stu-id="8e134-p104">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache. To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset2-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset2-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="8e134-p105">Você pode basear a definição da propriedade **CacheSize** no número de registros que o aplicativo pode tratar de cada vez. Por exemplo, se você estiver usando um objeto **Recordset** como a fonte de dados que será exibida na tela, poderá definir a propriedade **CacheSize** como 20 para exibir 20 registros de cada vez.</span><span class="sxs-lookup"><span data-stu-id="8e134-p105">You can base the **CacheSize** property setting on the number of records your application can handle at one time. For example, if you're using a **Recordset** object as the source of the data to be displayed on screen, you could set its **CacheSize** property to 20 to display 20 records at one time.</span></span>

<span data-ttu-id="8e134-121">O mecanismo do banco de dados do Microsoft Access solicita registros em um intervalo de cache a partir do cache e requisita registros de fora do intervalo de cache a partir do servidor.</span><span class="sxs-lookup"><span data-stu-id="8e134-121">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="8e134-122">Os registros recuperados do cache não refletem as alterações simultâneas que os outros usuários fizeram nos dados de origem.</span><span class="sxs-lookup"><span data-stu-id="8e134-122">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

<span data-ttu-id="8e134-123">Para forçar uma atualização em todos os dados armazenados, defina a propriedade **CacheSize** do objeto **Recordset** como 0, redefina-o para o tamanho de cache solicitado originalmente e depois use o método **FillCache**.</span><span class="sxs-lookup"><span data-stu-id="8e134-123">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

## <a name="example"></a><span data-ttu-id="8e134-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8e134-124">Example</span></span>

<span data-ttu-id="8e134-p106">Este exemplo usa os métodos **CreateTableDef** e **FillCache** e as propriedades **CacheSize**, **CacheStart** e **SourceTableName** para enumerar os registros vinculados à tabela duas vezes. Em seguida, enumera os registros duas vezes com um cache de 50 registros. Depois, exemplo exibe as estatísticas de desempenho das execuções com cache e sem cache por meio da tabela vinculada.</span><span class="sxs-lookup"><span data-stu-id="8e134-p106">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

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
