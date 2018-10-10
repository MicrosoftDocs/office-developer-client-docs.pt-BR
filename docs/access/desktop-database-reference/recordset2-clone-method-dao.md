---
title: Método Recordset2.Clone (DAO)
TOCTitle: Clone Method
ms:assetid: f0d32cb1-03f6-395d-2509-b2139a5fdc68
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836567(v=office.15)
ms:contentKeyID: 48548614
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0e8356fe5a9f6d0a02fd63ca6664a03fb5e6bc77
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462317"
---
# <a name="recordset2clone-method-dao"></a><span data-ttu-id="e936f-102">Método Recordset2.Clone (DAO)</span><span class="sxs-lookup"><span data-stu-id="e936f-102">Recordset2.Clone Method (DAO)</span></span>


<span data-ttu-id="e936f-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e936f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e936f-104">Cria um objeto **[Recordset](recordset-object-dao.md)** duplicado que faz referência ao objeto **Recordset2** original.</span><span class="sxs-lookup"><span data-stu-id="e936f-104">Creates a duplicate **[Recordset](recordset-object-dao.md)** object that refers to the original **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e936f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e936f-105">Syntax</span></span>

<span data-ttu-id="e936f-106">*expressão* . Clone</span><span class="sxs-lookup"><span data-stu-id="e936f-106">*expression* .Clone</span></span>

<span data-ttu-id="e936f-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="e936f-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="return-value"></a><span data-ttu-id="e936f-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e936f-108">Return Value</span></span>

<span data-ttu-id="e936f-109">Recordset</span><span class="sxs-lookup"><span data-stu-id="e936f-109">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="e936f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e936f-110">Remarks</span></span>

<span data-ttu-id="e936f-p101">Use o método **Clone** para criar vários objetos **Recordset** duplicados. Cada conjunto de registros pode ter seu próprio registro atual. Usar **Clone** sozinho não altera os dados nos objetos ou em suas estruturas subjacentes. Quando você usa o método **Clone**, é possível compartilhar indicadores entre dois ou mais objetos **Recordset2** porque seus indicadores são intercambiáveis.</span><span class="sxs-lookup"><span data-stu-id="e936f-p101">Use the **Clone** method to create multiple, duplicate **Recordset** objects. Each recordset can have its own current record. Using **Clone** by itself doesn't change the data in the objects or in their underlying structures. When you use the **Clone** method, you can share bookmarks between two or more **Recordset2** objects because their bookmarks are interchangeable.</span></span>

<span data-ttu-id="e936f-p102">Você pode usar o método **Clone** quando desejar executar uma operação em um conjunto de registros que exige vários registros atuais. Isso é mais rápido e mais eficiente do que abrir um segundo conjunto de registros. Quando você cria um conjunto de registros com o método **Clone**, ele inicialmente não tem um registro atual. Para tornar um registro atual antes de usar o clone de conjunto de registros, você deve definir a propriedade **[Bookmark](recordset2-bookmark-property-dao.md)** ou usar um dos métodos **[Move](recordset-movefirst-method-dao.md)**, ou um dos métodos **[Find](recordset2-findfirst-method-dao.md)** ou o método **[Seek](recordset2-seek-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="e936f-p102">You can use the **Clone** method when you want to perform an operation on a recordset that requires multiple current records. This is faster and more efficient than opening a second recordset. When you create a recordset with the **Clone** method, it initially lacks a current record. To make a record current before you use the recordset clone, you must set the **[Bookmark](recordset2-bookmark-property-dao.md)** property or use one of the **[Move](recordset-movefirst-method-dao.md)** methods, one of the **[Find](recordset2-findfirst-method-dao.md)** methods, or the **[Seek](recordset2-seek-method-dao.md)** method.</span></span>

<span data-ttu-id="e936f-p103">Usar o método **[Close](connection-close-method-dao.md)** no objeto original ou duplicado não afeta o outro objeto. Por exemplo, usar **Close** no conjunto de registros original não fecha o clone.</span><span class="sxs-lookup"><span data-stu-id="e936f-p103">Using the **[Close](connection-close-method-dao.md)** method on either the original or duplicate object doesn't affect the other object. For example, using **Close** on the original recordset doesn't close the clone.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="e936f-121">Fechar um conjunto de registros clonado dentro de uma transação pendente provocará uma operação <STRONG>Rollback</STRONG> implícita.</span><span class="sxs-lookup"><span data-stu-id="e936f-121">Closing a clone recordset within a pending transaction will cause an implicit <STRONG>Rollback</STRONG> operation.</span></span></P>
> <LI>
> <P><span data-ttu-id="e936f-p104">Quando você clona um objeto <STRONG>Recordset</STRONG> do tipo tabela em um espaço de trabalho do Microsoft Access, a configuração da propriedade <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG> não é clonada na nova cópia do conjunto de registros. Você deve copiar a configuração da propriedade <STRONG>Index</STRONG> manualmente.</span><span class="sxs-lookup"><span data-stu-id="e936f-p104">When you clone a table-type <STRONG>Recordset</STRONG> object in a Microsoft Access workspace, the <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG> property setting is not cloned on the new copy of the recordset. You must copy the <STRONG>Index</STRONG> property setting manually.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="e936f-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e936f-124">Example</span></span>

<span data-ttu-id="e936f-125">Este exemplo usa o método **Clone** para criar cópias de um conjunto de registros e, em seguida, permite que o usuário posicione o ponteiro do registro de cada cópia de maneira independente.</span><span class="sxs-lookup"><span data-stu-id="e936f-125">This example uses the **Clone** method to create copies of a recordset and then lets the user position the record pointer of each copy independently.</span></span>

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
