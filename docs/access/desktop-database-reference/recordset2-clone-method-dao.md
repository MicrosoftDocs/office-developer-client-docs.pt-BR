---
title: Método Recordset2.Clone (DAO)
TOCTitle: Clone Method
ms:assetid: f0d32cb1-03f6-395d-2509-b2139a5fdc68
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836567(v=office.15)
ms:contentKeyID: 48548614
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6780a27d573f5ff7ff41060074fb8abb9f8e2b80
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711319"
---
# <a name="recordset2clone-method-dao"></a><span data-ttu-id="7c597-102">Método Recordset2.Clone (DAO)</span><span class="sxs-lookup"><span data-stu-id="7c597-102">Recordset2.Clone method (DAO)</span></span>

<span data-ttu-id="7c597-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c597-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7c597-104">Cria um objeto **[Recordset](recordset-object-dao.md)** duplicado que faz referência ao objeto **Recordset2** original.</span><span class="sxs-lookup"><span data-stu-id="7c597-104">Creates a duplicate **[Recordset](recordset-object-dao.md)** object that refers to the original **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c597-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c597-105">Syntax</span></span>

<span data-ttu-id="7c597-106">*expressão* . Clone</span><span class="sxs-lookup"><span data-stu-id="7c597-106">*expression* .Clone</span></span>

<span data-ttu-id="7c597-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="7c597-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c597-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7c597-108">Return value</span></span>

<span data-ttu-id="7c597-109">Recordset</span><span class="sxs-lookup"><span data-stu-id="7c597-109">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="7c597-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c597-110">Remarks</span></span>

<span data-ttu-id="7c597-p101">Use o método **Clone** para criar vários objetos **Recordset** duplicados. Cada conjunto de registros pode ter seu próprio registro atual. Usar **Clone** sozinho não altera os dados nos objetos ou em suas estruturas subjacentes. Quando você usa o método **Clone**, é possível compartilhar indicadores entre dois ou mais objetos **Recordset2** porque seus indicadores são intercambiáveis.</span><span class="sxs-lookup"><span data-stu-id="7c597-p101">Use the **Clone** method to create multiple, duplicate **Recordset** objects. Each recordset can have its own current record. Using **Clone** by itself doesn't change the data in the objects or in their underlying structures. When you use the **Clone** method, you can share bookmarks between two or more **Recordset2** objects because their bookmarks are interchangeable.</span></span>

<span data-ttu-id="7c597-p102">Você pode usar o método **Clone** quando desejar executar uma operação em um conjunto de registros que exige vários registros atuais. Isso é mais rápido e mais eficiente do que abrir um segundo conjunto de registros. Quando você cria um conjunto de registros com o método **Clone**, ele inicialmente não tem um registro atual. Para tornar um registro atual antes de usar o clone de conjunto de registros, você deve definir a propriedade **[Bookmark](recordset2-bookmark-property-dao.md)** ou usar um dos métodos **[Move](recordset-movefirst-method-dao.md)**, ou um dos métodos **[Find](recordset2-findfirst-method-dao.md)** ou o método **[Seek](recordset2-seek-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="7c597-p102">You can use the **Clone** method when you want to perform an operation on a recordset that requires multiple current records. This is faster and more efficient than opening a second recordset. When you create a recordset with the **Clone** method, it initially lacks a current record. To make a record current before you use the recordset clone, you must set the **[Bookmark](recordset2-bookmark-property-dao.md)** property or use one of the **[Move](recordset-movefirst-method-dao.md)** methods, one of the **[Find](recordset2-findfirst-method-dao.md)** methods, or the **[Seek](recordset2-seek-method-dao.md)** method.</span></span>

<span data-ttu-id="7c597-p103">Usar o método **[Close](connection-close-method-dao.md)** no objeto original ou duplicado não afeta o outro objeto. Por exemplo, usar **Close** no conjunto de registros original não fecha o clone.</span><span class="sxs-lookup"><span data-stu-id="7c597-p103">Using the **[Close](connection-close-method-dao.md)** method on either the original or duplicate object doesn't affect the other object. For example, using **Close** on the original recordset doesn't close the clone.</span></span>

> [!NOTE]
> - <span data-ttu-id="7c597-121">Fechar um conjunto de registros clonado dentro de uma transação pendente provocará uma operação **Rollback** implícita.</span><span class="sxs-lookup"><span data-stu-id="7c597-121">Closing a clone recordset within a pending transaction will cause an implicit **Rollback** operation.</span></span>
> - <span data-ttu-id="7c597-p104">Quando você clona um objeto **Recordset** do tipo tabela em um espaço de trabalho do Microsoft Access, a configuração da propriedade **[Index](recordset2-index-property-dao.md)** não é clonada na nova cópia do conjunto de registros. Você deve copiar a configuração da propriedade **Index** manualmente.</span><span class="sxs-lookup"><span data-stu-id="7c597-p104">When you clone a table-type **Recordset** object in a Microsoft Access workspace, the **[Index](recordset2-index-property-dao.md)** property setting is not cloned on the new copy of the recordset. You must copy the **Index** property setting manually.</span></span>

## <a name="example"></a><span data-ttu-id="7c597-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7c597-124">Example</span></span>

<span data-ttu-id="7c597-125">Este exemplo usa o método **Clone** para criar cópias de um conjunto de registros e, em seguida, permite que o usuário posicione o ponteiro do registro de cada cópia de maneira independente.</span><span class="sxs-lookup"><span data-stu-id="7c597-125">This example uses the **Clone** method to create copies of a recordset and then lets the user position the record pointer of each copy independently.</span></span>

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset2 
       Dim intLoop As Integer 
       Dim strMessage As String 
       Dim strFind As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' If the following SQL statement will be used often,  
       ' creating a permanent QueryDef will result in better 
       ' performance. 
       Set arstProducts(1) = dbsNorthwind.OpenRecordset( _ 
          "SELECT ProductName FROM Products " & _ 
          "ORDER BY ProductName", dbOpenSnapshot) 
     
       ' Create two clones of the original Recordset. 
       Set arstProducts(2) = arstProducts(1).Clone 
       Set arstProducts(3) = arstProducts(1).Clone 
     
       Do While True 
     
          ' Loop through the array so that on each pass, the  
          ' user is searching a different copy of the same  
          ' Recordset. 
          For intLoop = 1 To 3 
     
             ' Ask for search string while showing where the 
             ' current record pointer is for each Recordset. 
             strMessage = _ 
                "Recordsets from Products table:" & vbCr & _ 
                "  1 - Original - Record pointer at " & _ 
                arstProducts(1)!ProductName & vbCr & _ 
                "  2 - Clone - Record pointer at " & _ 
                arstProducts(2)!ProductName & vbCr & _ 
                "  3 - Clone - Record pointer at " & _ 
                arstProducts(3)!ProductName & vbCr & _ 
                "Enter search string for #" & intLoop & ":" 
             strFind = Trim(InputBox(strMessage)) 
             If strFind = "" Then Exit Do 
     
             ' Find the search string; if there's no match, jump 
             ' to the last record. 
             With arstProducts(intLoop) 
                .FindFirst "ProductName >= '" & strFind & "'" 
                If .NoMatch Then .MoveLast 
             End With 
     
          Next intLoop 
     
       Loop 
     
       arstProducts(1).Close 
       arstProducts(2).Close 
       arstProducts(3).Close 
       dbsNorthwind.Close 
     
    End Sub
```
