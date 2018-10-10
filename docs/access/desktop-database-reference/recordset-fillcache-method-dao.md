---
title: Método Recordset.FillCache (DAO)
TOCTitle: FillCache Method
ms:assetid: d171b939-b904-c6bd-6217-68bc2814e282
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834751(v=office.15)
ms:contentKeyID: 48547861
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8fb7a662a061a7e98d3782d0c42badeda77ab3a8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463977"
---
# <a name="recordsetfillcache-method-dao"></a><span data-ttu-id="b57a6-102">Método Recordset.FillCache (DAO)</span><span class="sxs-lookup"><span data-stu-id="b57a6-102">Recordset.FillCache Method (DAO)</span></span>


<span data-ttu-id="b57a6-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b57a6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b57a6-104">Preenche parcial ou totalmente um cache local de um objeto **Recordset** que contém dados de uma fonte de dados ODBC conectada ao mecanismo de banco de dados do Microsoft Access (somente bancos de dados ODBC conectados ao mecanismo de banco de dados do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="b57a6-104">Fills all or a part of a local cache for a **Recordset** object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b57a6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b57a6-105">Syntax</span></span>

<span data-ttu-id="b57a6-106">*expressão* . FillCache (***linhas***, ***StartBookmark***)</span><span class="sxs-lookup"><span data-stu-id="b57a6-106">*expression* .FillCache(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="b57a6-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="b57a6-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="b57a6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b57a6-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b57a6-109">Nome</span><span class="sxs-lookup"><span data-stu-id="b57a6-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b57a6-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="b57a6-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b57a6-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b57a6-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b57a6-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b57a6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b57a6-113">Linhas</span><span class="sxs-lookup"><span data-stu-id="b57a6-113">Rows</span></span></p></td>
<td><p><span data-ttu-id="b57a6-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="b57a6-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="b57a6-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b57a6-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b57a6-p101">Um <strong>Variant</strong> (subtipo <strong>Integer</strong>) que especifica o número de linhas a ser armazenado no cache. Se você omitir esse argumento, o valor será determinado pela configuração da propriedade <strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="b57a6-p101">A <strong>Variant</strong> (<strong>Integer</strong> subtype) that specifies the number of rows to store in the cache. If you omit this argument, the value is determined by the <strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong> property setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b57a6-118">StartBookmark</span><span class="sxs-lookup"><span data-stu-id="b57a6-118">StartBookmark</span></span></p></td>
<td><p><span data-ttu-id="b57a6-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="b57a6-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="b57a6-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b57a6-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b57a6-p102">Um <strong>Variant</strong> (subtipo <strong>String</strong>) que especifica um indicador. O cache é preenchido começando pelo registro indicado por esse indicador. Se você omitir esse argumento, o cache será preenchido começando do registro indicado pela propriedade <strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="b57a6-p102">A <strong>Variant</strong> (<strong>String</strong> subtype) that specifies a bookmark. The cache is filled starting from the record indicated by this bookmark. If you omit this argument, the cache is filled starting from the record indicated by the <strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b57a6-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b57a6-124">Remarks</span></span>

<span data-ttu-id="b57a6-p103">Fazer cache melhora o desempenho de um aplicativo que recupera dados de um servidor remoto. Cache é um espaço na memória local que conserva os dados recuperados mais recentemente do servidor; isso pressupõe que os dados provavelmente serão solicitados de novo enquanto o aplicativo estiver sendo executado. Quando um usuário solicita dados, o mecanismo do banco de dados do Microsoft Access verifica os dados primeiramente no cache em vez de recuperá-los do servidor, o que leva mais tempo. O cache não salva dados que não sejam provenientes de uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="b57a6-p103">Caching improves the performance of an application that retrieves data from a remote server. A cache is space in local memory that holds the data most recently retrieved from the server; this assumes that the data will probably be requested again while the application is running. When a user requests data, the Microsoft Access database engine checks the cache for the data first rather than retrieving it from the server, which takes more time. The cache doesn't save data that doesn't come from an ODBC data source.</span></span>

<span data-ttu-id="b57a6-p104">Em vez de esperar que o cache seja preenchido com registros enquanto eles são recuperados, você pode usar o método **FillCache** para preencher explicitamente o cache a qualquer momento. Essa é uma maneira mais rápida de preencher o cache porque **FillCache** recupera vários registros de uma vez, e não um de cada vez. Por exemplo, enquanto você exibe cada tela de registros, seu aplicativo usa **FillCache** para recuperar a próxima tela de registros para exibição.</span><span class="sxs-lookup"><span data-stu-id="b57a6-p104">Rather than waiting for the cache to be filled with records as they are retrieved, you can use the **FillCache** method to explicitly fill the cache at any time. This is a faster way to fill the cache because **FillCache** retrieves several records at once instead of one at a time. For example, while you view each screenful of records, your application uses **FillCache** to retrieve the next screenful of records for viewing.</span></span>

<span data-ttu-id="b57a6-p105">Qualquer fonte de dados ODBC conectada ao mecanismo de banco de dados do Microsoft Access que você acessa com objetos **Recordset** pode ter um cache local. Para criar o cache, abra um objeto **Recordset** a partir da fonte de dados remota e, em seguida, defina as propriedades **CacheSize** e **CacheStart** do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b57a6-p105">Any Microsoft Access database engine-connected ODBC data source that you access with **Recordset** objects can have a local cache. To create the cache, open a **Recordset** object from the remote data source, and then set the **CacheSize** and **CacheStart** properties of the **Recordset**.</span></span>

<span data-ttu-id="b57a6-134">Se linhas e startbookmark criam um intervalo de registros que é parcialmente ou totalmente fora do intervalo dos registros especificados pelas propriedades **CacheSize** e **CacheStart** , a parte do recordset fora deste intervalo será ignorada e não será carregada para o cache.</span><span class="sxs-lookup"><span data-stu-id="b57a6-134">If rows and startbookmark create a range of records that is partially or entirely outside the range of records specified by the **CacheSize** and **CacheStart** properties, the portion of the recordset outside this range is ignored and will not be loaded into the cache.</span></span>

<span data-ttu-id="b57a6-135">Se **FillCache** solicitar mais registros do que o número restante na fonte de dados remota, o mecanismo de banco de dados do Microsoft Access recuperará apenas os registros restantes e não ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="b57a6-135">If **FillCache** requests more records than the number remaining in the remote data source, the Microsoft Access database engine retrieves only the remaining records, and no error occurs.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="b57a6-136">Registros recuperados do cache não refletem alterações concorrentes que outros usuários fazem nos dados de origem.</span><span class="sxs-lookup"><span data-stu-id="b57a6-136">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span></P>
> <LI>
> <P><span data-ttu-id="b57a6-p106"><STRONG>FillCache</STRONG> recupera apenas registros para os quais não foi feito cache. Para forçar uma atualização de todos os dados com cache, defina a propriedade <STRONG>CacheSize</STRONG> do <STRONG>Recordset</STRONG> para 0, redefina-a de acordo com o tamanho do cache que você originalmente solicitou e, em seguida, use <STRONG>FillCache</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b57a6-p106"><STRONG>FillCache</STRONG> only retrieves records not already cached. To force an update of all the cached data, set the <STRONG>CacheSize</STRONG> property of the <STRONG>Recordset</STRONG> to 0, reset it to the size of the cache you originally requested, and then use <STRONG>FillCache</STRONG>.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="b57a6-139">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b57a6-139">Example</span></span>

<span data-ttu-id="b57a6-p107">Este exemplo usa os métodos **CreateTableDef** e **FillCache** e as propriedades **CacheSize**, **CacheStart** e **SourceTableName** para enumerar os registros em uma tabela vinculada duas vezes. Em seguida, enumeram-se os registros duas vezes com um cache de 50 registros. O exemplo exibe então as estatísticas de desempenho das execuções sem cache e com cache por meio da tabela vinculada.</span><span class="sxs-lookup"><span data-stu-id="b57a6-p107">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

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
