---
title: Coleção Recordsets (DAO)
TOCTitle: Recordsets Collection
ms:assetid: 246d9a78-4ce8-6393-982b-77ac00cd85bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191819(v=office.15)
ms:contentKeyID: 48543756
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b935e05264497c7ad09ada4a8c50c775845857b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309295"
---
# <a name="recordsets-collection-dao"></a>Coleção Recordsets (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Uma coleção **Recordsets** contém todos os objetos **Recordset** abertos em um objeto **Connection** ou **Database**.

## <a name="remarks"></a>Comentários

Ao usar objetos DAO, você manipula dados praticamente usando objetos **Recordset**.

Um novo objeto **Recordset** é automaticamente adicionado à coleção **Recordsets** quando você abre o objeto e é automaticamente removido quando você o fecha. **Recordset**

Você pode criar quantas variáveis de objeto **Recordset** forem necessárias. Diferentes objetos **Recordset** podem acessar as mesmas tabelas, consultas e campos sem entrar em conflito.

Para consultar um objeto **Recordset** em uma coleção de acordo com seu número ordinal ou sua configuração de propriedade **Name**, use qualquer um dos formulários de sintaxe a seguir:

- **Recordsets**(0)

- **Recordsets**(“nome”)

- **Recordsets**\!\[nome\]

> [!NOTE]
> É possível abrir um objeto **Recordset** a partir do mesmo banco de dados ou fonte de dados mais de uma vez criando nomes duplicados na coleção **Recordsets**. Você deve atribuir objetos **Recordsets** para variáveis de objetos e referenciá-los por nome de variável.

## <a name="example"></a>Exemplo

This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.

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
     Debug.Print " " & .Name 
     
     ' Enumerate Properties collection of each 
     ' Recordset object. Trap for any 
     ' properties whose values are invalid in 
     ' this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print _ 
     " " & prpLoop.Name & _ 
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
