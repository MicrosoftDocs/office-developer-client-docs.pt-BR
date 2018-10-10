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
ms.openlocfilehash: 9627e5413e362baad505bfdf98092044499986c4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463373"
---
# <a name="connectiondatabase-property-dao"></a>Propriedade Connection.Database (DAO)


**Aplica-se a**: Access 2013 | Office 2013



## <a name="syntax"></a>Sintaxe

*expressão* . Banco de dados

*expressão* Uma variável que representa um objeto de **Conexão** .

## <a name="remarks"></a>Comentários

Em um objeto **[Connection](connection-object-dao.md)**, use a propriedade **Database** para obter uma referência a um objeto **Database** que corresponda ao **Connection**. No DAO, um objeto **Connection** e seus objetos **Database** correspondentes são simplesmente duas referências diferentes de variáveis de objeto para o mesmo objeto. A propriedade **Database** de um objeto **Connection** e a propriedade **[Connection](database-connection-property-dao.md)** de um objeto **Database** facilita a alteração das conexões para uma ODBC data source por meio do mecanismo de banco de dados do Microsoft Access a fim de usar o ODBCDirect.

## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **Database** para mostrar como o código utilizado para acessar os dados do ODBC por meio de mecanismo de banco de dados do Microsoft Access pode ser convertido para usar os objetos Connection do ODBCDirect.

O procedimento OldDatabaseCode utiliza uma fonte de dados conectada ao mecanismo de banco de dados do Microsoft Access para acessar um banco de dados do ODBC.

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

O exemplo NewDatabaseCode abre um objeto **Connection** em um espaço de trabalho ODBCDirect. Em seguida, ele atribui a propriedade **Database** do objeto **Connection** a uma variável de objeto com o mesmo nome da fonte de dados no procedimento antigo. Nenhum código subsequente tem que ser alterado enquanto ele não usa nenhum recurso específico dos espaços de trabalho do Microsoft Access.

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

