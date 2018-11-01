---
title: Coleção Connections (DAO)
TOCTitle: Connections Collection
ms:assetid: 65d073be-a84b-e3f2-cb43-b87ffa60e497
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195178(v=office.15)
ms:contentKeyID: 48545330
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b2f7fba059ba277de0fe494c845bbdbfcd27affa
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882781"
---
# <a name="connections-collection-dao"></a><span data-ttu-id="94c3b-102">Coleção Connections (DAO)</span><span class="sxs-lookup"><span data-stu-id="94c3b-102">Connections Collection (DAO)</span></span>


<span data-ttu-id="94c3b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="94c3b-103">**Applies to**: Access 2013, Office 2013</span></span>


> [!NOTE]
> <span data-ttu-id="94c3b-p101">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="94c3b-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>



<span data-ttu-id="94c3b-p102">Uma coleção **Connections** contém os objetos **Connection** atuais de um objeto **Workspace**. (espaços de trabalho do ODBCDirect apenas).</span><span class="sxs-lookup"><span data-stu-id="94c3b-p102">A **Connections** collection contains the current **Connection** objects of a **Workspace** object. (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="94c3b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="94c3b-108">Remarks</span></span>

<span data-ttu-id="94c3b-p103">Quando você abre um objeto **Connection**, ele é automaticamente acrescentado à coleção **Connections** do **Workspace**. Quando você fecha um objeto **Connection** com o método **[Close](connection-close-method-dao.md)**, ele é removido da coleção **Connections**. Você deve fechar todos os objetos **[Recordset](recordset-object-dao.md)** abertos no objeto **Connection** antes de fechá-lo.</span><span class="sxs-lookup"><span data-stu-id="94c3b-p103">When you open a **Connection** object, it is automatically appended to the **Connections** collection of the **Workspace**. When you close a **Connection** object with the **[Close](connection-close-method-dao.md)** method, it is removed from the **Connections** collection. You should close all open **[Recordset](recordset-object-dao.md)** objects within the **Connection** before closing it.</span></span>

<span data-ttu-id="94c3b-p104">Quando você abre um objeto **Connection**, um objeto **[Database](database-object-dao.md)** correspondente é criado e acrescentado à coleção **[Databases](databases-collection-dao.md)** no mesmo **Workspace** e vice-versa. Da mesma forma, quando você fecha o objeto **Connection**, o **Database** correspondente é excluído da coleção **Databases** e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="94c3b-p104">At the same time you open a **Connection** object, a corresponding **[Database](database-object-dao.md)** object is created and appended to the **[Databases](databases-collection-dao.md)** collection in the same **Workspace**, and vice versa. Similarly, when you close the **Connection**, the corresponding **Database** is deleted from the **Databases** collection, and so on.</span></span>

<span data-ttu-id="94c3b-p105">A configuração da propriedade **Name** de um objeto **Connection** é uma sequência de caracteres que especifica o caminho do arquivo do banco de dados. Para fazer referência a um objeto **Connection** em uma coleção por seu número ordinal ou por sua configuração de propriedade **Name**, use uma das seguintes formas de sintaxe:</span><span class="sxs-lookup"><span data-stu-id="94c3b-p105">The **Name** property setting of a **Connection** is a string that specifies the path of the database file. To refer to a **Connection** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

  - <span data-ttu-id="94c3b-116">**Connections**(0)</span><span class="sxs-lookup"><span data-stu-id="94c3b-116">**Connections**(0)</span></span>

  - <span data-ttu-id="94c3b-117">**Conexões** ("*nome*")</span><span class="sxs-lookup"><span data-stu-id="94c3b-117">**Connections**("*name*")</span></span>

  - <span data-ttu-id="94c3b-118">**Conexões**\!\[*nome*\]</span><span class="sxs-lookup"><span data-stu-id="94c3b-118">**Connections**\!\[*name*\]</span></span>


> [!NOTE]
> <span data-ttu-id="94c3b-p106">[!OBSERVAçãO] Você pode abrir a mesma fonte de dados mais de uma vez, criando nomes duplicados na coleção **Connections**. Você deve atribuir objetos **Connection** a variáveis de objeto e fazer referência a eles por nome de variável.</span><span class="sxs-lookup"><span data-stu-id="94c3b-p106">You can open the same data source more than once, creating duplicate names in the **Connections** collection. You should assign **Connection** objects to object variables and refer to them by variable name.</span></span>



## <a name="example"></a><span data-ttu-id="94c3b-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="94c3b-121">Example</span></span>

<span data-ttu-id="94c3b-122">Este exemplo demonstra o objeto **Connection** e a coleção **Connections** por meio da abertura de um objeto **Database** e dois objetos **Connection** do ODBCDirect e da listagem das propriedades disponíveis para cada objeto.</span><span class="sxs-lookup"><span data-stu-id="94c3b-122">This example demonstrates the **Connection** object and **Connections** collection by opening a **Database** object and two ODBCDirect **Connection** objects and listing the properties available to each object.</span></span>

```vb 
Sub ConnectionObjectX() 
 
   Dim wrkAcc as Workspace 
   Dim dbsNorthwind As Database 
   Dim wrkODBC As Workspace 
   Dim conPubs As Connection 
   Dim conPubs2 As Connection 
   Dim conLoop As Connection 
   Dim prpLoop As Property 
 
   ' Open a Database object. 
   Set wrkAcc = CreateWorkspace("NewWorkspace", _ 
      "admin", "", dbUseJet) 
   Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
   ' Create ODBCDirect Workspace object and open Connection 
   ' objects. 
   Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
      "admin", "", dbUseODBC) 
       
   ' Note: The DSNs referenced below must be configured to  
   '       use Microsoft Windows NT Authentication Mode to  
   '       authorize user access to the Microsoft SQL Server. 
   Set conPubs = wrkODBC.OpenConnection("Connection1", , , _ 
      "ODBC;DATABASE=pubs;DSN=Publishers") 
       
   Set conPubs2 = wrkODBC.OpenConnection("Connection2", , _ 
      True, "ODBC;DATABASE=pubs;DSN=Publishers") 
 
   Debug.Print "Database properties:" 
 
   With dbsNorthwind 
      ' Enumerate Properties collection of Database object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         Debug.Print "  " & prpLoop.Name & " = " & _ 
            prpLoop.Value 
         On Error GoTo 0 
      Next prpLoop 
   End With 
 
   ' Enumerate the Connections collection. 
   For Each conLoop In wrkODBC.Connections 
      Debug.Print "Connection properties for " & _ 
         conLoop.Name & ":" 
 
      With conLoop 
         ' Print property values by explicitly calling each 
         ' Property object; the Connection object does not 
         ' support a Properties collection. 
         Debug.Print "  Connect = " & .Connect 
         ' Property actually returns a Database object. 
         Debug.Print "  Database[.Name] = " & _ 
            .Database.Name 
         Debug.Print "  Name = " & .Name 
         Debug.Print "  QueryTimeout = " & .QueryTimeout 
         Debug.Print "  RecordsAffected = " & _ 
            .RecordsAffected 
         Debug.Print "  StillExecuting = " & _ 
            .StillExecuting 
         Debug.Print "  Transactions = " & .Transactions 
         Debug.Print "  Updatable = " & .Updatable 
      End With 
 
   Next conLoop 
 
   dbsNorthwind.Close 
   conPubs.Close 
   conPubs2.Close 
   wrkAcc.Close 
   wrkODBC.Close 
 
End Sub 
 
```

<span data-ttu-id="94c3b-123">Este exemplo usa o método **OpenConnection** com diferentes parâmetros para abrir três objetos **Connection** diferentes.</span><span class="sxs-lookup"><span data-stu-id="94c3b-123">This example uses the **OpenConnection** method with different parameters to open three different **Connection** objects.</span></span>

```vb 
Sub OpenConnectionX() 
 
   Dim wrkODBC As Workspace 
   Dim conPubs As Connection 
   Dim conPubs2 As Connection 
   Dim conPubs3 As Connection 
   Dim conLoop As Connection 
 
   ' Create ODBCDirect Workspace object. 
   Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
      "admin", "", dbUseODBC) 
 
   ' Open Connection object using supplied information in  
   ' the connect string. If this information were  
   ' insufficient, you could trap for an error rather than  
   ' go to an ODBC Driver Manager dialog box. 
   MsgBox "Opening Connection1..." 
       
    ' Note: The DSN referenced below must be set to  
    '       use Microsoft Windows NT Authentication Mode to  
    '       authorize user access to the Microsoft SQL Server. 
    Set conPubs = wrkODBC.OpenConnection("Connection1", _ 
       dbDriverNoPrompt, , _ 
       "ODBC;DATABASE=pubs;DSN=Publishers") 
 
   ' Open read-only Connection object based on information  
   ' you enter in the ODBC Driver Manager dialog box. 
   MsgBox "Opening Connection2..." 
   Set conPubs2 = wrkODBC.OpenConnection("Connection2", _ 
      dbDriverPrompt, True, "ODBC;DSN=Publishers;") 
 
   ' Open read-only Connection object by entering only the  
   ' missing information in the ODBC Driver Manager dialog  
   ' box. 
   MsgBox "Opening Connection3..." 
   Set conPubs3 = wrkODBC.OpenConnection("Connection3", _ 
      dbDriverCompleteRequired, True, _ 
      "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
   ' Enumerate the Connections collection. 
   For Each conLoop In wrkODBC.Connections 
      Debug.Print "Connection properties for " & _ 
         conLoop.Name & ":" 
 
      With conLoop 
         ' Print property values by explicitly calling each 
         ' Property object; the Connection object does not 
         ' support a Properties collection. 
         Debug.Print "  Connect = " & .Connect 
         ' Property actually returns a Database object. 
         Debug.Print "  Database[.Name] = " & _ 
            .Database.Name 
         Debug.Print "  Name = " & .Name 
         Debug.Print "  QueryTimeout = " & .QueryTimeout 
         Debug.Print "  RecordsAffected = " & _ 
            .RecordsAffected 
         Debug.Print "  StillExecuting = " & _ 
            .StillExecuting 
         Debug.Print "  Transactions = " & .Transactions 
         Debug.Print "  Updatable = " & .Updatable 
      End With 
 
   Next conLoop 
 
   conPubs.Close 
   conPubs2.Close 
   conPubs3.Close 
   wrkODBC.Close 
 
End Sub 
 
```

