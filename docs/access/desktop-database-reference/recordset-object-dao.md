---
title: Objeto Recordset (DAO)
TOCTitle: Recordset Object
ms:assetid: 9774232c-e6da-175b-fc7f-ed2ab7908fa0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197799(v=office.15)
ms:contentKeyID: 48546469
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3fb327b77a9b17ef83ef48cbe5f9e657f859687b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463006"
---
# <a name="recordset-object-dao"></a><span data-ttu-id="bf9f4-102">Objeto Recordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="bf9f4-102">Recordset Object (DAO)</span></span>

<span data-ttu-id="bf9f4-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf9f4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bf9f4-104">Um objeto **Recordset** representa os registros em uma tabela base ou os registros resultantes da execução de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-104">A **Recordset** object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf9f4-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf9f4-105">Remarks</span></span>

<span data-ttu-id="bf9f4-p101">Os objetos **Recordset** são usados para manipular dados em um banco de dados no nível do registro. Ao usar objetos de acesso a dados, manipula-se dados quase completamente usando os objetos **Recordset**. Todos os objetos **Recordset** são criados com registros (linhas) e campos (colunas). Há cinco tipos de objetos **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p101">You use **Recordset** objects to manipulate data in a database at the record level. When you use DAO objects, you manipulate data almost entirely using **Recordset** objects. All **Recordset** objects are constructed using records (rows) and fields (columns). There are five types of **Recordset** objects:</span></span>

- <span data-ttu-id="bf9f4-110">Recordset do tipo Tabela  representação em código de uma tabela base que pode ser usada para adicionar, alterar ou excluir registros de uma única tabela de banco de dados (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bf9f4-110">Table-type Recordset— representation in code of a base table that you can use to add, change, or delete records from a single database table (Microsoft Access workspaces only).</span></span>

- <span data-ttu-id="bf9f4-p102">Recordset do tipo Dynaset  o resultado de uma consulta que pode ter registros atualizáveis. Um objeto **Recordset** do tipo dynaset é um Recordset dinâmico que pode ser usado para adicionar, alterar ou excluir registros de uma tabela ou de tabelas de banco de dados subjacentes. Um objeto **Recordset** do tipo dynaset pode conter campos de uma ou mais tabelas em um banco de dados. Esse tipo corresponde a um cursor de conjunto de chaves ODBC.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p102">Dynaset-type Recordset— the result of a query that can have updatable records. A dynaset-type **Recordset** object is a dynamic set of records that you can use to add, change, or delete records from an underlying database table or tables. A dynaset-type **Recordset** object can contain fields from one or more tables in a database. This type corresponds to an ODBC keyset cursor.</span></span>

- <span data-ttu-id="bf9f4-p103">Recordset do tipo Instantâneo  uma cópia estática de um Recordset que pode ser usada para localizar dados ou gerar relatórios. Um objeto **Recordset** do tipo instantâneo pode conter campos de uma ou mais tabelas em um banco de dados, mas não pode ser atualizado. Esse tipo corresponde a um cursor estático ODBC.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p103">Snapshot-type Recordset— a static copy of a set of records that you can use to find data or generate reports. A snapshot-type **Recordset** object can contain fields from one or more tables in a database but can't be updated. This type corresponds to an ODBC static cursor.</span></span>

- <span data-ttu-id="bf9f4-p104">Recordset do tipo Somente Encaminhamento  idêntico a um instantâneo, exceto pelo fato de não fornecer cursor. Você pode simplesmente rolar para frente por meio dos registros. Isso melhora o desempenho em situações em que é preciso fazer uma única passagem por um conjunto de resultados. Esse tipo corresponde a um cursor somente encaminhamento ODBC.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p104">Forward-only-type Recordset— identical to a snapshot except that no cursor is provided. You can only scroll forward through records. This improves performance in situations where you only need to make a single pass through a result set. This type corresponds to an ODBC forward-only cursor.</span></span>

- <span data-ttu-id="bf9f4-p105">Recordset do tipo Dynamic  um conjunto de resultados de consulta de uma ou mais tabelas base nas quais você pode adicionar, alterar ou excluir registros de uma consulta de retorno de linha. Além disso, registros adicionados, alterados e editados por outros usuários nas tabelas base também aparecem no seu **Recordset**. Esse tipo corresponde a um cursor dinâmico ODBC (somente espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p105">Dynamic-type Recordset— a query result set from one or more base tables in which you can add, change, or delete records from a row-returning query. Further, records other users add, delete, or edit in the base tables also appear in your **Recordset**. This type corresponds to an ODBC dynamic cursor (ODBCDirect workspaces only).</span></span>

> [!NOTE]
> <span data-ttu-id="bf9f4-p106">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p106">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="bf9f4-127">Você pode escolher o tipo de objeto **Recordset** que você deseja criar usando o argumento type do método **OpenRecordset** .</span><span class="sxs-lookup"><span data-stu-id="bf9f4-127">You can choose the type of **Recordset** object you want to create using the type argument of the **OpenRecordset** method.</span></span>

<span data-ttu-id="bf9f4-128">Em um espaço de trabalho do Microsoft Access, se você não especificar um tipo de tentativas DAO para criar o tipo de **Recordset** com a maior funcionalidade disponível, iniciando com a tabela.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-128">In a Microsoft Access workspace, if you don't specify a type, DAO attempts to create the type of **Recordset** with the most functionality available, starting with table.</span></span> <span data-ttu-id="bf9f4-129">Se esse tipo não estiver disponível, o DAO tentará um dynaset, um instantâneo e, finalmente, um objeto **Recordset** de tipo somente encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-129">If this type isn't available, DAO attempts a dynaset, then a snapshot, and finally a forward-only type **Recordset** object.</span></span>

<span data-ttu-id="bf9f4-130">Em um espaço de trabalho do ODBCDirect, se você não especificar um tipo de DAO tenta criar o tipo de **Recordset** com a resposta mais rápida de consulta, começando com somente de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-130">In an ODBCDirect workspace, if you don't specify a type, DAO attempts to create the type of **Recordset** with the fastest query response, starting with forward-only.</span></span> <span data-ttu-id="bf9f4-131">Se esse tipo não estiver disponível, o DAO tentará um instantâneo, um dynaset e, finalmente, um objeto **Recordset** do tipo Dynamic.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-131">If this type isn't available, DAO attempts a snapshot, then a dynaset, and finally a dynamic- type **Recordset** object.</span></span>

<span data-ttu-id="bf9f4-p109">Ao criar um objeto **Recordset** usando um objeto **[TableDef](tabledef-object-dao.md)** não vinculado em um espaço de trabalho do Microsoft Access, objetos **Recordset** do tipo tabela serão criados. Somente objetos **Recordset** do tipo dynaset ou instantâneo podem ser criados com uma tabela ou tabelas vinculadas ao mecanismo de conexão do banco de dados ODBC ao banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p109">When creating a **Recordset** object using a non-linked **[TableDef](tabledef-object-dao.md)** object in a Microsoft Access workspace, table-type **Recordset** objects are created. Only dynaset-type or snapshot-type **Recordset** objects can be created with linked tables or tables in Microsoft Access database engine-connected ODBC databases.</span></span>

<span data-ttu-id="bf9f4-134">Um novo objeto **Recordset** é automaticamente adicionado à coleção **Recordsets** quando o objeto é aberto, e é automaticamente removido quando este é fechado.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-134">A new **Recordset** object is automatically added to the **Recordsets** collection when you open the object, and is automatically removed when you close it.</span></span>

> [!NOTE]
> <span data-ttu-id="bf9f4-p110">[!OBSERVAçãO] Se você usar variáveis para representar um objeto **Recordset** e um objeto **Database** contendo um **Recordset**, verifique se as variáveis têm o mesmo escopo, ou tempo de vida. Por exemplo, se você declarar uma variável pública que representa um objeto **Recordset**, certifique-se de que a variável que representa o **Database** que contém o **Recordset** também é pública, ou declarada em um procedimento **Sub** ou **Function** usando a palavra-chave **Static**.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p110">If you use variables to represent a **Recordset** object and the **Database** object that contains the **Recordset**, make sure the variables have the same scope, or lifetime. For example, if you declare a public variable that represents a **Recordset** object, make sure the variable that represents the **Database** containing the **Recordset** is also public, or is declared in a **Sub** or **Function** procedure using the **Static** keyword.</span></span>

<span data-ttu-id="bf9f4-p111">Você pode criar quantas variáveis de objeto **Recordset** precisar. Diferentes objetos **Recordset** podem acessar as mesmas tabelas, consultas e campos sem entrar em conflito.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p111">You can create as many **Recordset** object variables as needed. Different **Recordset** objects can access the same tables, queries, and fields without conflicting.</span></span>

<span data-ttu-id="bf9f4-139">Dynaset, instantâneo e objetos **Recordset** do tipo somente encaminhamento são armazenados na memória local.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-139">Dynaset–, snapshot–, and forward–only–type **Recordset** objects are stored in local memory.</span></span> <span data-ttu-id="bf9f4-140">Se não houver espaço suficiente na memória local para armazenar os dados, o mecanismo de banco de dados do Microsoft Access salvará os dados adicionais no espaço de disco Temporário.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-140">If there isn't enough space in local memory to store the data, the Microsoft Access database engine saves the additional data to TEMP disk space.</span></span> <span data-ttu-id="bf9f4-141">Se esse espaço estiver esgotado, ocorrerá um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-141">If this space is exhausted, a trappable error occurs.</span></span>

<span data-ttu-id="bf9f4-p113">A coleção padrão de um objeto **Recordset** é a coleção **Fields**, e a propriedade padrão de um objeto **[Field](field-object-dao.md)** é a propriedade **[Value](field-value-property-dao.md)**. Use os valores padrão para simplificar seu código.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p113">The default collection of a **Recordset** object is the **Fields** collection, and the default property of a **[Field](field-object-dao.md)** object is the **[Value](field-value-property-dao.md)** property. Use these defaults to simplify your code.</span></span>

<span data-ttu-id="bf9f4-p114">Ao criar um objeto **Recordset**, o registro atual é posicionado no primeiro registro, se houver algum registro. Se não houver registros, a configuração da propriedade **RecordCount** será 0 e as configurações das propriedades **BOF** e **EOF** serão **True**.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p114">When you create a **Recordset** object, the current record is positioned to the first record if there are any records. If there are no records, the **RecordCount** property setting is 0, and the **BOF** and **EOF** property settings are **True**.</span></span>

<span data-ttu-id="bf9f4-p115">É possível usar os métodos **MoveNext**, **MovePrevious**, **MoveFirst** e **MoveLast** para reposicionar o registro atual. objetos **Recordset** oferecem suporte somente para o método **MoveNext**. Ao usar o método Move para visitar cada registro (ou "percorrer" o **Recordset**), é possível usar as propriedades **BOF** e **EOF** para consultar o começo ou o fim de um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p115">You can use the **MoveNext**, **MovePrevious**, **MoveFirst**, and **MoveLast** methods to reposition the current record. Forward–only–type **Recordset** objects support only the **MoveNext** method. When using the Move methods to visit each record (or "walk" through the **Recordset**), you can use the **BOF** and **EOF** properties to check for the beginning or end of the **Recordset** object.</span></span>

<span data-ttu-id="bf9f4-p116">Com os objetos **Recordset** do tipo dynaset e instantâneo em um espaço de trabalho do Microsoft Access, é possível usar os métodos Find, como **FindFirst**, para localizar um registro específico com base em um critério. Se o registro não for localizado, a propriedade **NoMatch** é definida como **True**. Para objetos **Recordset** do tipo tabela, é possível examinar os registros usando o método **Seek**.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p116">With dynaset- and snapshot-type **Recordset** objects in a Microsoft Access workspace, you can also use the Find methods, such as **FindFirst**, to locate a specific record based on criteria. If the record isn't found, the **NoMatch** property is set to **True**. For table-type **Recordset** objects, you can scan records using the **Seek** method.</span></span>

<span data-ttu-id="bf9f4-152">A propriedade **Type** indica o tipo de objeto **Recordset** criado, e a propriedade **Updatable** indica se os registros do objeto podem ser alterados.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-152">The **Type** property indicates the type of **Recordset** object created, and the **Updatable** property indicates whether you can change the object's records.</span></span>

<span data-ttu-id="bf9f4-153">As informações sobre a estrutura de uma tabela base, como os nomes e tipos de dados de cada objeto **Field** e quaisquer objetos **Index**, estão armazenadas em um objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-153">Information about the structure of a base table, such as the names and data types of each **Field** object and any **Index** objects, is stored in a **TableDef** object.</span></span>

<span data-ttu-id="bf9f4-154">Para consultar um objeto **Recordset** em uma coleção de acordo com seu número ordinal ou sua configuração de propriedade **Name**, use qualquer um dos formulários de sintaxe a seguir:</span><span class="sxs-lookup"><span data-stu-id="bf9f4-154">To refer to a **Recordset** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="bf9f4-155">**Recordsets**(0)</span><span class="sxs-lookup"><span data-stu-id="bf9f4-155">**Recordsets**(0)</span></span>

- <span data-ttu-id="bf9f4-156">**Conjuntos de registros** ("nome")</span><span class="sxs-lookup"><span data-stu-id="bf9f4-156">**Recordsets**("name")</span></span>

- <span data-ttu-id="bf9f4-157">**Conjuntos de registros**\!\[nome\]</span><span class="sxs-lookup"><span data-stu-id="bf9f4-157">**Recordsets**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="bf9f4-p117">[!OBSERVAçãO] É possível abrir um objeto **Recordset** a partir do mesmo banco de dados ou fonte de dados mais de uma vez criando nomes duplicados na coleção **Recordsets**. Você deve atribuir objetos **Recordsets** para variáveis de objetos e referenciá-los por nome de variável.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p117">You can open a **Recordset** object from the same data source or database more than once, creating duplicate names in the **Recordsets** collection. You should assign **Recordset** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="bf9f4-160">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bf9f4-160">Example</span></span>

<span data-ttu-id="bf9f4-161">This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-161">This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.</span></span>

```vb
    Sub RecordsetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstTable As Recordset 
       Dim rstDynaset As Recordset 
       Dim rstSnapshot As Recordset 
       Dim rstForwardOnly As Recordset 
       Dim rstLoop As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
     
          ' Open one of each type of Recordset object. 
          Set rstTable = .OpenRecordset("Categories", _ 
             dbOpenTable) 
          Set rstDynaset = .OpenRecordset("Employees", _ 
             dbOpenDynaset) 
          Set rstSnapshot = .OpenRecordset("Shippers", _ 
             dbOpenSnapshot) 
          Set rstForwardOnly = .OpenRecordset _  
             ("Employees", dbOpenForwardOnly) 
     
          Debug.Print "Recordsets in Recordsets " & _ 
             "collection of dbsNorthwind" 
     
          ' Enumerate Recordsets collection. 
          For Each rstLoop In .Recordsets 
     
             With rstLoop 
                Debug.Print "  " & .Name 
     
                ' Enumerate Properties collection of each 
                ' Recordset object. Trap for any  
                ' properties whose values are invalid in  
                ' this context. 
                For Each prpLoop In .Properties 
                   On Error Resume Next 
                   If prpLoop <> "" Then Debug.Print _ 
                      "    " & prpLoop.Name & _ 
                      " = " & prpLoop 
                   On Error GoTo 0 
                Next prpLoop 
     
             End With 
     
          Next rstLoop 
     
          rstTable.Close 
          rstDynaset.Close 
          rstSnapshot.Close 
          rstForwardOnly.Close 
     
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="bf9f4-p118">Esse exemplo usa o método **OpenRecordset** para abrir cinco diferentes tipos de objetos **Recordset** e exibir seus conteúdos. O procedimento OpenRecordsetOutput é necessário para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p118">This example uses the **OpenRecordset** method to open five different **Recordset** objects and display their contents. The OpenRecordsetOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub OpenRecordsetX() 
     
       Dim wrkAcc As Workspace 
       Dim wrkODBC As Workspace 
       Dim dbsNorthwind As Database 
       Dim conPubs As Connection 
       Dim rstTemp As Recordset 
       Dim rstTemp2 As Recordset 
     
       ' Open Microsoft Access and ODBCDirect workspaces, Microsoft  
       ' Access database, and ODBCDirect connection. 
       Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
       Set wrkODBC = CreateWorkspace("", "admin", "", dbUseODBC) 
       Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
        
       ' Note: The DSN referenced below must be set to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
       Set conPubs = wrkODBC.OpenConnection("", , , _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
     
       ' Open five different Recordset objects and display the  
       ' contents of each. 
     
       Debug.Print "Opening forward-only-type recordset " & _ 
          "where the source is a QueryDef object..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "Ten Most Expensive Products", dbOpenForwardOnly) 
       OpenRecordsetOutput rstTemp 
     
       Debug.Print "Opening read-only dynaset-type " & _ 
          "recordset where the source is an SQL statement..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "SELECT * FROM Employees", dbOpenDynaset, dbReadOnly) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the Filter property to retrieve only certain  
       ' records with the next OpenRecordset call. 
       Debug.Print "Opening recordset from existing " & _ 
          "Recordset object to filter records..." 
       rstTemp.Filter = "LastName >= 'M'" 
       Set rstTemp2 = rstTemp.OpenRecordset() 
       OpenRecordsetOutput rstTemp2 
     
       Debug.Print "Opening dynamic-type recordset from " & _ 
          "an ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset( _ 
          "SELECT * FROM stores", dbOpenDynamic) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the StillExecuting property to determine when the  
       ' Recordset is ready for manipulation. 
       Debug.Print "Opening snapshot-type recordset based " & _ 
          "on asynchronous query to ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset("publishers", _ 
          dbOpenSnapshot, dbRunAsync) 
       Do While rstTemp.StillExecuting 
          Debug.Print "  [still executing...]" 
       Loop 
       OpenRecordsetOutput rstTemp 
     
       rstTemp.Close 
       dbsNorthwind.Close 
       conPubs.Close 
       wrkAcc.Close 
       wrkODBC.Close 
     
    End Sub 
     
    Sub OpenRecordsetOutput(rstOutput As Recordset) 
     
       ' Enumerate the specified Recordset object. 
       With rstOutput 
          Do While Not .EOF 
             Debug.Print , .Fields(0), .Fields(1) 
             .MoveNext 
          Loop 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="bf9f4-164">Este exemplo abre um objeto **Recordset** do tipo dynamic e enumera seus registros.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-164">This example opens a dynamic-type **Recordset** object and enumerates its records.</span></span>

```vb
    Sub dbOpenDynamicX() 
     
       Dim wrkMain As Workspace 
       Dim conMain As Connection 
       Dim qdfTemp As QueryDef 
       Dim rstTemp As Recordset 
       Dim strSQL As String 
       Dim intLoop As Integer 
     
       ' Create ODBC workspace and open connection to 
       ' SQL Server database. 
       Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
          "admin", "", dbUseODBC) 
           
       ' Note: The DSN referenced below must be configured to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server.     
       Set conMain = wrkMain.OpenConnection("Publishers", _ 
          dbDriverNoPrompt, False, _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
           
       ' Open dynamic-type recordset. 
       Set rstTemp = _ 
          conMain.OpenRecordset("authors", _ 
          dbOpenDynamic) 
     
       With rstTemp 
          Debug.Print "Dynamic-type recordset: " & .Name 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !au_lname & ", " & _ 
                !au_fname 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       conMain.Close 
       wrkMain.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="bf9f4-165">Este exemplo abre um objeto **Recordset** do tipo dynaset e mostra a extensão para a qual seus campos são atualizáveis.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-165">This example opens a dynaset-type **Recordset** and shows the extent to which its fields are updatable.</span></span>

```vb
    Sub dbOpenDynasetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstInvoices As Recordset 
       Dim fldLoop As Field 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstInvoices = _ 
          dbsNorthwind.OpenRecordset("Invoices", dbOpenDynaset) 
     
       With rstInvoices 
          Debug.Print "Dynaset-type recordset: " & .Name 
     
          If .Updatable Then 
             Debug.Print "  Updatable fields:" 
     
             ' Enumerate Fields collection of dynaset-type 
             ' Recordset object, print only updatable 
             ' fields. 
             For Each fldLoop In .Fields 
                If fldLoop.DataUpdatable Then 
                   Debug.Print "    " & fldLoop.Name 
                End If 
             Next fldLoop 
     
          End If 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="bf9f4-166">Este exemplo abre um objeto **Recordset** do tipo somente encaminhamento, demonstra suas características somente leitura e percorre o **Recordset** com o método **MoveNext**.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-166">This example opens a forward-only-type **Recordset**, demonstrates its read-only characteristics, and steps through the **Recordset** with the **MoveNext** method.</span></span>

```vb 
Sub dbOpenForwardOnlyX() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim fldLoop As Field 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   ' Open a forward-only-type Recordset object. Only the  
   ' MoveNext and Move methods may be used to navigate  
   ' through the recordset. 
   Set rstEmployees = _ 
      dbsNorthwind.OpenRecordset("Employees", _ 
      dbOpenForwardOnly) 
 
   With rstEmployees 
      Debug.Print "Forward-only-type recordset: " & _ 
         .Name & ", Updatable = " & .Updatable 
 
      Debug.Print "  Field - DataUpdatable" 
      ' Enumerate Fields collection, printing the Name and  
      ' DataUpdatable properties of each Field object. 
      For Each fldLoop In .Fields 
         Debug.Print "    " & _ 
            fldLoop.Name & " - " & fldLoop.DataUpdatable 
      Next fldLoop 
 
      Debug.Print "  Data" 
      ' Enumerate the recordset. 
      Do While Not .EOF 
         Debug.Print "    " & !FirstName & " " & _ 
            !LastName 
         .MoveNext 
      Loop 
 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
```

<br/>

<span data-ttu-id="bf9f4-167">Este exemplo abre um objeto **Recordset** do tipo instantâneo e demonstra suas características somente leitura.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-167">This example opens a snapshot-type **Recordset** and demonstrates its read-only characteristics.</span></span>

```vb
    Sub dbOpenSnapshotX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          Debug.Print "Snapshot-type recordset: " & _ 
             .Name 
     
          ' Enumerate the Properties collection of the 
          ' snapshot-type Recordset object, trapping for 
          ' any properties whose values are invalid in  
          ' this context. 
          For Each prpLoop In .Properties 
             On Error Resume Next 
             Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
             On Error Goto 0 
          Next prpLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="bf9f4-168">Este exemplo abre um objeto **Recordset**, define sua propriedade **Index** e enumera seus registros.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-168">This example opens a table-type **Recordset**, sets its **Index** property, and enumerates its records.</span></span>

```vb
    Sub dbOpenTableX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' dbOpenTable is default. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
     
       With rstEmployees 
          Debug.Print "Table-type recordset: " & .Name 
     
          ' Use predefined index. 
          .Index = "LastName" 
          Debug.Print "  Index = " & .Index 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !LastName & ", " & _ 
                !FirstName 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="bf9f4-169">O exemplo a seguir mostra como usar o método Seek para localizar um registro em uma tabela vinculada.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-169">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="bf9f4-170">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="bf9f4-170">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```

<br/>

<span data-ttu-id="bf9f4-171">O exemplo a seguir mostra como abrir um Recordset baseado em uma consulta de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-171">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

<span data-ttu-id="bf9f4-172">O exemplo a seguir mostra como abrir um Recordset baseado em uma tabela ou uma consulta.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-172">The following example shows how to open a Recordset based on a table or a query.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

<span data-ttu-id="bf9f4-173">O exemplo a seguir mostra como abrir um Recordset baseado em uma instrução SQL (Structured Query Language).</span><span class="sxs-lookup"><span data-stu-id="bf9f4-173">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

<span data-ttu-id="bf9f4-174">O exemplo a seguir mostra como usar os métodos FindFirst e FindNext para localizar um registro em um Recordset.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-174">The following example shows how to use the FindFirst and FindNext methods to find a record in a Recordset.</span></span>

```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="bf9f4-175">O exemplo a seguir mostra como copiar os resultados de uma consulta para uma planilha em uma nova pasta de trabalho do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-175">The following example shows how to copy the results of a query to a worksheet in a new Microsoft Excel workbook.</span></span>

```vb
    Public Sub CopyDataFromQuery( _
        xlApp As Excel.Application, _
        strQueryName As String)
    
        ' If the xlApp object exists
        If Not xlApp Is Nothing Then
        
            ' If the Workbook exists
            If xlApp.Workbooks.Count = 1 Then
            
                ' Create Recrodset Object from the Query
                Dim rsQuery As DAO.Recordset
                Set rsQuery = Application.CurrentDb.OpenRecordset(strQueryName)
                
                ' Get the Cells object
                Dim Cells As Object
                Set Cells = xlApp.Workbooks(1).ActiveSheet.Cells
                
                ' Copy the Data from the Query into the Sheet
                Cells.CopyFromRecordset rsQuery
                
            End If
        End If
    
    End Sub
```

