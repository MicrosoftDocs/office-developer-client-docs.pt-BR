---
title: Propriedade Recordset.Transactions (DAO)
TOCTitle: Transactions Property
ms:assetid: 7830c056-8d6a-7942-7993-aa04b29cd77f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196110(v=office.15)
ms:contentKeyID: 48545746
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c3b34f8f027b2e70ada94c6d15584cf25a4aec1c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873284"
---
# <a name="recordsettransactions-property-dao"></a>Propriedade Recordset.Transactions (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna um valor que indica se um objeto aceita transactions. **Boolean** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . Transações

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

Em um espaço de trabalho do Microsoft Access, você também pode usar a propriedade **Transactions** com objetos **Recordset** do tipo dynaset ou tabela. Os objetos **[Recordset](recordset-object-dao.md)** e encaminhar – somente – tipo instantâneo sempre retornará **False**.

Se um **Recordset** do tipo dynaset ou tabela estiver baseado em uma tabela do mecanismo de banco de dados do Microsoft Access, a propriedade **Transactions** será **True** e você poderá usar as transações. Outros mecanismos do banco de dados podem oferecer suporte para transações. Por exemplo, você não pode usar as transações de um objeto **Recordset** do tipo dynaset em uma tabela Paradox.

Verifique a propriedade **Transactions** antes de usar o método **[BeginTrans](dbengine-begintrans-method-dao.md)** do objeto [**Workspace**](workspace-object-dao.md) do objeto **Recordset** para garantir que haverá suporte para as transações. O uso dos métodos **BeginTrans**, **CommitTrans** ou **Rollback** em um objeto que não ofereça suporte não terá efeito.

## <a name="example"></a>Exemplo

Este exemplo demonstra a propriedade **Transactions** nos espaços de trabalho do Microsoft Access.

```vb 
Sub TransactionsX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim conPubs As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Open two different Recordset objects and display the 
 ' Transactions property of each. 
 
 Debug.Print "Opening Microsoft Access table-type " & _ 
 "recordset..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "Employees", dbOpenTable) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 Debug.Print "Opening forward-only-type " & _ 
 "recordset where the source is an SQL statement..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "SELECT * FROM Employees", dbOpenForwardOnly) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 rstTemp.Close 
 dbsNorthwind.Close 
 conPubs.Close 
 wrkAcc.Close 
End Sub 
 
```

