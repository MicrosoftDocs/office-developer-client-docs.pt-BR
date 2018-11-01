---
title: Coleção Recordsets (DAO)
TOCTitle: Recordsets Collection
ms:assetid: 246d9a78-4ce8-6393-982b-77ac00cd85bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191819(v=office.15)
ms:contentKeyID: 48543756
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1a32c52f60ed8c7bd68f32ed9986638bffcdec84
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868998"
---
# <a name="recordsets-collection-dao"></a>Coleção Recordsets (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Uma coleção **Recordsets** contém todos os objetos **Recordset** abertos em um objeto **Connection** ou **Database**.

## <a name="remarks"></a>Comentários

Ao usar objetos DAO, você manipula dados praticamente usando objetos **Recordset**.

Um novo objeto **Recordset** é automaticamente adicionado à coleção **Recordsets** quando você abre o objeto e é automaticamente removido quando você o fecha. **Recordset**

Você pode criar quantas variáveis de objeto **Recordset** forem necessárias. Diferentes objetos **Recordset** podem acessar as mesmas tabelas, consultas e campos sem entrar em conflito.

Para se referir a um objeto **Recordset** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:

- **Recordsets**(0)

- **Conjuntos de registros** ("nome")

- **Conjuntos de registros**\!\[nome\]

> [!NOTE]
> [!OBSERVAçãO] É possível abrir um objeto **Recordset** a partir do mesmo banco de dados ou fonte de dados mais de uma vez criando nomes duplicados na coleção **Recordsets**. Você deve atribuir objetos **Recordsets** para variáveis de objetos e referenciá-los por nome de variável.

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
