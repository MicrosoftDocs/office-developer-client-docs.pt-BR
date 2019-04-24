---
title: Método Recordset. FillCache (DAO)
TOCTitle: FillCache Method
ms:assetid: d171b939-b904-c6bd-6217-68bc2814e282
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834751(v=office.15)
ms:contentKeyID: 48547861
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ef268a821d65732e0a54776872387f62c67e999
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300515"
---
# <a name="recordsetfillcache-method-dao"></a><span data-ttu-id="51e95-102">Método Recordset. FillCache (DAO)</span><span class="sxs-lookup"><span data-stu-id="51e95-102">Recordset.FillCache method (DAO)</span></span>

<span data-ttu-id="51e95-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51e95-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51e95-104">Preenche todo ou uma parte do cache local para um objeto **Recordset** que contém dados de uma fonte de dados ODBC conectada ao mecanismo de banco de dados do Microsoft Access (apenas bancos de dados ODBC conectados ao mecanismo de banco de dados do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="51e95-104">Fills all or a part of a local cache for a **Recordset** object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span>

## <a name="syntax"></a><span data-ttu-id="51e95-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51e95-105">Syntax</span></span>

<span data-ttu-id="51e95-106">*expressão* . FillCache (***linhas***, ***startbookmark criarem***)</span><span class="sxs-lookup"><span data-stu-id="51e95-106">*expression* .FillCache(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="51e95-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="51e95-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="51e95-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51e95-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51e95-109">Nome</span><span class="sxs-lookup"><span data-stu-id="51e95-109">Name</span></span></p></th>
<th><p><span data-ttu-id="51e95-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="51e95-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="51e95-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="51e95-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="51e95-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="51e95-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51e95-113"><em>Rows</em></span><span class="sxs-lookup"><span data-stu-id="51e95-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="51e95-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="51e95-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="51e95-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="51e95-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="51e95-116">Um <strong>Variant</strong> (subtipo <strong>Integer</strong>) que especifica o número de linhas a ser armazenado no cache.</span><span class="sxs-lookup"><span data-stu-id="51e95-116">A <strong>Variant</strong> (<strong>Integer</strong> subtype) that specifies the number of rows to store in the cache.</span></span> <span data-ttu-id="51e95-117">Se você omitir esse argumento, o valor será determinado pela <strong><a href="recordset-cachesize-property-dao.md"></a></strong> configuração da propriedade CacheSize.</span><span class="sxs-lookup"><span data-stu-id="51e95-117">If you omit this argument, the value is determined by the <strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong> property setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51e95-118"><em>Startbookmark criarem</em></span><span class="sxs-lookup"><span data-stu-id="51e95-118"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="51e95-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="51e95-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="51e95-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="51e95-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="51e95-121">Um <strong>Variant</strong> (subtipo <strong>String</strong>) que especifica um indicador.</span><span class="sxs-lookup"><span data-stu-id="51e95-121">A <strong>Variant</strong> (<strong>String</strong> subtype) that specifies a bookmark.</span></span> <span data-ttu-id="51e95-122">O cache é preenchido começando pelo registro indicado por esse indicador.</span><span class="sxs-lookup"><span data-stu-id="51e95-122">The cache is filled starting from the record indicated by this bookmark.</span></span> <span data-ttu-id="51e95-123">Se você omitir esse argumento, o cache será preenchido a partir do registro indicado pela propriedade <strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="51e95-123">If you omit this argument, the cache is filled starting from the record indicated by the <strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="51e95-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="51e95-124">Remarks</span></span>

<span data-ttu-id="51e95-p103">O armazenamento em cache aumenta o desempenho de um aplicativo que recupera dados de um servidor remoto. Um cache é o espaço na memória local que mantém os dados recuperados mais recentemente do servidor; isso indica que provavelmente os dados serão solicitados novamente durante a execução do aplicativo. Quando um usuário solicita dados, o mecanismo de banco de dados do Microsoft Access verifica esses dados no cache primeiro em vez de recuperá-los do servidor, o que leva mais tempo. O cache não salva dados que não são provenientes de uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="51e95-p103">Caching improves the performance of an application that retrieves data from a remote server. A cache is space in local memory that holds the data most recently retrieved from the server; this assumes that the data will probably be requested again while the application is running. When a user requests data, the Microsoft Access database engine checks the cache for the data first rather than retrieving it from the server, which takes more time. The cache doesn't save data that doesn't come from an ODBC data source.</span></span>

<span data-ttu-id="51e95-p104">Em vez de aguardar que o cache seja preenchido com registros à medida que eles são recuperados, você pode usar o método **FillCache** para preencher explicitamente o cache a qualquer momento. Esse é um modo mais rápido de preencher o cache porque **FillCache** recupera vários registros de uma vez, e não um por vez. Por exemplo, enquanto você exibe cada tecla cheia de registros, seu aplicativo usa **FillCache** para recuperar a próxima tela cheia de registros para exibição.</span><span class="sxs-lookup"><span data-stu-id="51e95-p104">Rather than waiting for the cache to be filled with records as they are retrieved, you can use the **FillCache** method to explicitly fill the cache at any time. This is a faster way to fill the cache because **FillCache** retrieves several records at once instead of one at a time. For example, while you view each screenful of records, your application uses **FillCache** to retrieve the next screenful of records for viewing.</span></span>

<span data-ttu-id="51e95-p105">Qualquer fonte de dados ODBC conectada ao mecanismo de banco de dados do Microsoft Access que você acessa com os objetos **Recordset** pode ter um cache local. Para criar o cache, abra um objeto **Recordset** na fonte de dados remota e, em seguida, defina as propriedades **CacheSize** e **CacheStart** do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="51e95-p105">Any Microsoft Access database engine-connected ODBC data source that you access with **Recordset** objects can have a local cache. To create the cache, open a **Recordset** object from the remote data source, and then set the **CacheSize** and **CacheStart** properties of the **Recordset**.</span></span>

<span data-ttu-id="51e95-134">Se Rows e startbookmark criarem criar um intervalo de registros que está parcialmente ou totalmente fora do intervalo de registros especificado pelas propriedades \*\*\*\* CacheSize e **CacheStart** , a parte do Recordset fora desse intervalo será ignorada e não será carregada no cache.</span><span class="sxs-lookup"><span data-stu-id="51e95-134">If rows and startbookmark create a range of records that is partially or entirely outside the range of records specified by the **CacheSize** and **CacheStart** properties, the portion of the recordset outside this range is ignored and will not be loaded into the cache.</span></span>

<span data-ttu-id="51e95-135">Se **FillCache** solicitar mais registros do que o número restante na fonte de dados remota, o mecanismo do banco de dados do Microsoft Access irá recuperar somente os registros restantes, e não ocorrerá nenhum erro.</span><span class="sxs-lookup"><span data-stu-id="51e95-135">If **FillCache** requests more records than the number remaining in the remote data source, the Microsoft Access database engine retrieves only the remaining records, and no error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="51e95-136">Os registros recuperados do cache não refletem as alterações simultâneas que outros usuários fizeram na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="51e95-136">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>
> - <span data-ttu-id="51e95-p106">O **FillCache** recupera apenas os registros não armazenados em cache. Para forçar uma atualização de todos os dados em cache, defina a propriedade **CacheSize** do **Recordset** como 0, redefina-a para o tamanho do cache solicitado originalmente e use **FillCache**.</span><span class="sxs-lookup"><span data-stu-id="51e95-p106">**FillCache** only retrieves records not already cached. To force an update of all the cached data, set the **CacheSize** property of the **Recordset** to 0, reset it to the size of the cache you originally requested, and then use **FillCache**.</span></span>

## <a name="example"></a><span data-ttu-id="51e95-139">Exemplo</span><span class="sxs-lookup"><span data-stu-id="51e95-139">Example</span></span>

<span data-ttu-id="51e95-p107">Este exemplo usa os métodos **CreateTableDef** e **FillCache** e as propriedades **CacheSize**, **CacheStart** e **SourceTableName** para enumerar os registros vinculados à tabela duas vezes. Em seguida, enumera os registros duas vezes com um cache de 50 registros. Depois, exemplo exibe as estatísticas de desempenho das execuções com cache e sem cache por meio da tabela vinculada.</span><span class="sxs-lookup"><span data-stu-id="51e95-p107">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

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
