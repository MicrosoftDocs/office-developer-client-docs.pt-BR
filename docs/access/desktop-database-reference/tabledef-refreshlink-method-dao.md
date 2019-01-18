---
title: Método TableDef.RefreshLink (DAO)
TOCTitle: RefreshLink Method
ms:assetid: 9f0059c6-3b7b-57e3-7527-ef674ad9417d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198349(v=office.15)
ms:contentKeyID: 48546674
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052980
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ba9375da16cebd7db7a29fe20fca6f8b395a73a2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716464"
---
# <a name="tabledefrefreshlink-method-dao"></a><span data-ttu-id="6a039-102">Método TableDef.RefreshLink (DAO)</span><span class="sxs-lookup"><span data-stu-id="6a039-102">TableDef.RefreshLink method (DAO)</span></span>

<span data-ttu-id="6a039-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a039-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="6a039-104">Atualiza as informações de conexão para uma tabela vinculada (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6a039-104">Updates the connection information for a linked table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a039-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a039-105">Syntax</span></span>

<span data-ttu-id="6a039-106">*expressão* . RefreshLink</span><span class="sxs-lookup"><span data-stu-id="6a039-106">*expression* .RefreshLink</span></span>

<span data-ttu-id="6a039-107">*expressão* Uma variável que representa um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="6a039-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a039-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a039-108">Remarks</span></span>

<span data-ttu-id="6a039-p101">Para alterar as informações de conexão para uma tabela vinculada, redefina a propriedade **[Connect](connection-connect-property-dao.md)** do objeto **TableDef** correspondente e use o método **RefreshLink** para atualizar as informações. Utilizar o método **RefreshLink** não altera as propriedades da tabela vinculada nem os objetos **[Relation](relation-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="6a039-p101">To change the connection information for a linked table, reset the **[Connect](connection-connect-property-dao.md)** property of the corresponding **TableDef** object and then use the **RefreshLink** method to update the information. Using **RefreshLink** method doesn't change the linked table's properties and **[Relation](relation-object-dao.md)** objects.</span></span>

<span data-ttu-id="6a039-111">Para que essas informações de conexão existam em todas as coleções associadas ao objeto **TableDef** que representam a tabela vinculada, você deve usar o método **[Refresh](tabledefs-refresh-method-dao.md)** em cada coleção.</span><span class="sxs-lookup"><span data-stu-id="6a039-111">For this connection information to exist in all collections associated with the **TableDef** object that represents the linked table, you must use the **[Refresh](tabledefs-refresh-method-dao.md)** method on each collection.</span></span>

## <a name="example"></a><span data-ttu-id="6a039-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6a039-112">Example</span></span>

<span data-ttu-id="6a039-p102">Este exemplo usa o método **RefreshLink** para atualizar os dados em uma tabela vinculada depois que sua conexão é alterada de uma fonte de dados para outra. O procedimento RefreshLinkOutput é exigido para que este procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="6a039-p102">This example uses the **RefreshLink** method to refresh the data in a linked table after its connection has been changed from one data source to another. The RefreshLinkOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub RefreshLinkX() 
 
 Dim dbsCurrent As Database 
 Dim tdfLinked As TableDef 
 
 ' Open a database to which a linked table can be 
 ' appended. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a linked table that points to a Microsoft 
 ' SQL Server database. 
 Set tdfLinked = _ 
 dbsCurrent.CreateTableDef("AuthorsTable") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 tdfLinked.SourceTableName = "authors" 
 dbsCurrent.TableDefs.Append tdfLinked 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to first source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Change connection information for linked table and 
 ' refresh the connection in order to make the new data 
 ' available. 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=NewPublishers" 
 tdfLinked.RefreshLink 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to second source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Delete linked table because this is a demonstration. 
 dbsCurrent.TableDefs.Delete tdfLinked.Name 
 
 dbsCurrent.Close 
 
End Sub 
 
Sub RefreshLinkOutput(dbsTemp As Database) 
 
 Dim rstRemote As Recordset 
 Dim intCount As Integer 
 
 ' Open linked table. 
 Set rstRemote = _ 
 dbsTemp.OpenRecordset("AuthorsTable") 
 
 intCount = 0 
 
 ' Enumerate Recordset object, but stop at 50 records. 
 With rstRemote 
 Do While Not .EOF And intCount < 50 
 Debug.Print , .Fields(0), .Fields(1) 
 intCount = intCount + 1 
 .MoveNext 
 Loop 
 If Not .EOF Then Debug.Print , "[more records]" 
 .Close 
 End With 
 
End Sub 
 
```

