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
# <a name="recordsettransactions-property-dao"></a><span data-ttu-id="aa1b1-102">Propriedade Recordset.Transactions (DAO)</span><span class="sxs-lookup"><span data-stu-id="aa1b1-102">Recordset.Transactions Property (DAO)</span></span>


<span data-ttu-id="aa1b1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa1b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aa1b1-p101">Retorna um valor que indica se um objeto aceita transactions. **Boolean** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="aa1b1-p101">Returns a value that indicates whether an object supports transactions. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa1b1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa1b1-106">Syntax</span></span>

<span data-ttu-id="aa1b1-107">*expressão* . Transações</span><span class="sxs-lookup"><span data-stu-id="aa1b1-107">*expression* .Transactions</span></span>

<span data-ttu-id="aa1b1-108">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="aa1b1-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa1b1-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa1b1-109">Remarks</span></span>

<span data-ttu-id="aa1b1-110">Em um espaço de trabalho do Microsoft Access, você também pode usar a propriedade **Transactions** com objetos **Recordset** do tipo dynaset ou tabela.</span><span class="sxs-lookup"><span data-stu-id="aa1b1-110">In a Microsoft Access workspace, you can also use the **Transactions** property with dynaset- or table-type **Recordset** objects.</span></span> <span data-ttu-id="aa1b1-111">Os objetos **[Recordset](recordset-object-dao.md)** e encaminhar – somente – tipo instantâneo sempre retornará **False**.</span><span class="sxs-lookup"><span data-stu-id="aa1b1-111">Snapshot- and forward–only–type **[Recordset](recordset-object-dao.md)** objects always return **False**.</span></span>

<span data-ttu-id="aa1b1-p103">Se um **Recordset** do tipo dynaset ou tabela estiver baseado em uma tabela do mecanismo de banco de dados do Microsoft Access, a propriedade **Transactions** será **True** e você poderá usar as transações. Outros mecanismos do banco de dados podem oferecer suporte para transações. Por exemplo, você não pode usar as transações de um objeto **Recordset** do tipo dynaset em uma tabela Paradox.</span><span class="sxs-lookup"><span data-stu-id="aa1b1-p103">If a dynaset- or table-type **Recordset** is based on a Microsoft Access database engine table, the **Transactions** property is **True** and you can use transactions. Other database engines may not support transactions. For example, you can't use transactions in a dynaset-type **Recordset** object based on a Paradox table.</span></span>

<span data-ttu-id="aa1b1-p104">Verifique a propriedade **Transactions** antes de usar o método **[BeginTrans](dbengine-begintrans-method-dao.md)** do objeto [**Workspace**](workspace-object-dao.md) do objeto **Recordset** para garantir que haverá suporte para as transações. O uso dos métodos **BeginTrans**, **CommitTrans** ou **Rollback** em um objeto que não ofereça suporte não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="aa1b1-p104">Check the **Transactions** property before using the **[BeginTrans](dbengine-begintrans-method-dao.md)** method on the **Recordset** object's **[Workspace](workspace-object-dao.md)** object to make sure that transactions are supported. Using the **BeginTrans**, **CommitTrans**, or **Rollback** methods on an unsupported object has no effect.</span></span>

## <a name="example"></a><span data-ttu-id="aa1b1-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="aa1b1-117">Example</span></span>

<span data-ttu-id="aa1b1-118">Este exemplo demonstra a propriedade **Transactions** nos espaços de trabalho do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="aa1b1-118">This example demonstrates the **Transactions** property in Microsoft Access workspaces.</span></span>

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

