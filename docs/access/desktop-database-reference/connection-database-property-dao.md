---
title: Propriedade Connection.Database (DAO)
TOCTitle: Database Property
ms:assetid: cf871353-0ea4-f995-6e0e-812af443daf9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834675(v=office.15)
ms:contentKeyID: 48547809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053581
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 91b452eb70ecd93cf73650c68891fd00f2dfa267
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920036"
---
# <a name="connectiondatabase-property-dao"></a><span data-ttu-id="bcf23-102">Propriedade Connection.Database (DAO)</span><span class="sxs-lookup"><span data-stu-id="bcf23-102">Connection.Database property (DAO)</span></span>


<span data-ttu-id="bcf23-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="bcf23-103">**Applies to**: Access 2013, Office 2013</span></span>



## <a name="syntax"></a><span data-ttu-id="bcf23-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bcf23-104">Syntax</span></span>

<span data-ttu-id="bcf23-105">*expressão* . Banco de dados</span><span class="sxs-lookup"><span data-stu-id="bcf23-105">*expression* .Database</span></span>

<span data-ttu-id="bcf23-106">*expressão* Uma variável que representa um objeto de **Conexão** .</span><span class="sxs-lookup"><span data-stu-id="bcf23-106">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcf23-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="bcf23-107">Remarks</span></span>

<span data-ttu-id="bcf23-p101">Em um objeto **[Connection](connection-object-dao.md)**, use a propriedade **Database** para obter uma referência a um objeto **Database** que corresponda ao **Connection**. No DAO, um objeto **Connection** e seus objetos **Database** correspondentes são simplesmente duas referências diferentes de variáveis de objeto para o mesmo objeto. A propriedade **Database** de um objeto **Connection** e a propriedade **[Connection](database-connection-property-dao.md)** de um objeto **Database** facilita a alteração das conexões para uma ODBC data source por meio do mecanismo de banco de dados do Microsoft Access a fim de usar o ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="bcf23-p101">On a **[Connection](connection-object-dao.md)** object, use the **Database** property to obtain a reference to a **Database** object that corresponds to the **Connection**. In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object. The **Database** property of a **Connection** object and the **[Connection](database-connection-property-dao.md)** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

## <a name="example"></a><span data-ttu-id="bcf23-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bcf23-111">Example</span></span>

<span data-ttu-id="bcf23-112">Este exemplo usa a propriedade **Database** para mostrar como o código utilizado para acessar os dados do ODBC por meio de mecanismo de banco de dados do Microsoft Access pode ser convertido para usar os objetos Connection do ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="bcf23-112">This example uses the **Database** property to show how code that used to access ODBC data through the Microsoft Access database engine can be converted to use ODBCDirect Connection objects.</span></span>

<span data-ttu-id="bcf23-113">O procedimento OldDatabaseCode utiliza uma fonte de dados conectada ao mecanismo de banco de dados do Microsoft Access para acessar um banco de dados do ODBC.</span><span class="sxs-lookup"><span data-stu-id="bcf23-113">The OldDatabaseCode procedure uses a Microsoft Access database engine-connected data source to access an ODBC database.</span></span>

```vb
    Sub OldDatabaseCode() 
     
     Dim wrkMain As Workspace 
     Dim dbsPubs As Database 
     Dim prpLoop As Property 
     
     ' Create a Workspace object. 
     Set wrkMain = CreateWorkspace("", "admin", "", dbUseJet) 
     
     ' Open a Database object based on information in 
     ' the connect string. 
     
     'Note: The DSN referenced below must be configured to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set dbsPubs = wrkMain.OpenDatabase("Publishers", _ 
     dbDriverNoPrompt, False, _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     ' Enumerate the Properties collection of the Database 
     ' object. 
     With dbsPubs 
     Debug.Print "Database properties for " & _ 
     .Name & ":" 
     
     On Error Resume Next 
     For Each prpLoop In .Properties 
     If prpLoop.Name = "Connection" Then 
     ' Property actually returns a Connection object. 
     Debug.Print " Connection[.Name] = " & _ 
     .Connection.Name 
     Else 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop 
     End If 
     Next prpLoop 
     On Error GoTo 0 
     
     End With 
     
     dbsPubs.Close 
     wrkMain.Close 
     
    End Sub 
```

<span data-ttu-id="bcf23-p102">O exemplo NewDatabaseCode abre um objeto **Connection** em um espaço de trabalho ODBCDirect. Em seguida, ele atribui a propriedade **Database** do objeto **Connection** a uma variável de objeto com o mesmo nome da fonte de dados no procedimento antigo. Nenhum código subsequente tem que ser alterado enquanto ele não usa nenhum recurso específico dos espaços de trabalho do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bcf23-p102">The NewDatabaseCode example opens a **Connection** object in an ODBCDirect workspace. It then assigns the **Database** property of the **Connection** object to an object variable with the same name as the data source in the old procedure. None of the subsequent code has to be changed as long as it doesn't use any features specific to Microsoft Access workspaces.</span></span>

```vb 
Sub NewDatabaseCode() 
 
 Dim wrkMain As Workspace 
 Dim conPubs As Connection 
 Dim dbsPubs As Database 
 Dim prpLoop As Property 
 
 ' Create ODBCDirect Workspace object instead of Microsoft 
 ' Access Workspace object. 
 Set wrkMain = CreateWorkspace("", "admin", "", dbUseODBC) 
 
 ' Open Connection object based on information in 
 ' the connect string. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 ' Assign the Database property to the same object 
 ' variable as in the old code. 
 Set dbsPubs = conPubs.Database 
 
 ' Enumerate the Properties collection of the Database 
 ' object. From this point on, the code is the same as the 
 ' old example. 
 With dbsPubs 
 Debug.Print "Database properties for " & _ 
 .Name & ":" 
 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 If prpLoop.Name = "Connection" Then 
 ' Property actually returns a Connection object. 
 Debug.Print " Connection[.Name] = " & _ 
 .Connection.Name 
 Else 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 End If 
 Next prpLoop 
 On Error GoTo 0 
 
 End With 
 
 dbsPubs.Close 
 wrkMain.Close 
 
End Sub 
 
```

