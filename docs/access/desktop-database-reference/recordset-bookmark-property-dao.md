---
title: Propriedade Recordset.Bookmark (DAO)
TOCTitle: Bookmark Property
ms:assetid: c4b1c2d9-668e-e365-544c-efb4ae4efcc9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823084(v=office.15)
ms:contentKeyID: 48547597
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052887
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 1ebf963695b2d754a4501077e2236c52280a9a2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300648"
---
# <a name="recordsetbookmark-property-dao"></a><span data-ttu-id="126eb-102">Propriedade Recordset.Bookmark (DAO)</span><span class="sxs-lookup"><span data-stu-id="126eb-102">Recordset.Bookmark property (DAO)</span></span>


<span data-ttu-id="126eb-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="126eb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="126eb-104">Define ou retorna um marcador que identifica exclusivamente o registro atual em um objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="126eb-104">Sets or returns a bookmark that uniquely identifies the current record in a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="126eb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="126eb-105">Syntax</span></span>

<span data-ttu-id="126eb-106">*expressão* .Bookmark</span><span class="sxs-lookup"><span data-stu-id="126eb-106">expression  . Bookmark</span></span>

<span data-ttu-id="126eb-107">*expressão* Uma variável que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="126eb-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="126eb-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="126eb-108">Remarks</span></span>

<span data-ttu-id="126eb-109">Para um objeto **Recordset** baseado totalmente em tabelas do mecanismo do banco de dados do Microsoft Access, o valor da propriedade **Bookmarkable** é True, e você usa a propriedade **Bookmark** com aquele **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="126eb-109">For a **Recordset** object based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is  **True**, and you can use the **Bookmark** property with that recordset.</span></span> <span data-ttu-id="126eb-110">No entanto, outros produtos do banco de dados podem não oferecer suporte aos marcadores.</span><span class="sxs-lookup"><span data-stu-id="126eb-110">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="126eb-111">Por exemplo, você não pode usar indicadores em nenhum objeto **Recordset** com base em uma tabela vinculada Paradox que não tenha nenhuma chave primária.</span><span class="sxs-lookup"><span data-stu-id="126eb-111">For example, you can't use bookmarks in any **Recordset** object based on a linked Paradox table that has no primary key.</span></span>

<span data-ttu-id="126eb-p102">Quando você criar ou abrir um objeto **Recordset**, cada um desses registros já possuirá um marcador exclusivo. Salve o marcador do registro atual pela atribuição do valor da propriedade **Bookmark** a uma variável. Para retornar rapidamente ao registro a qualquer momento depois de se mover para um registro diferente, defina a propriedade **Bookmark** do objeto **Recordset** como o valor dessa variável.</span><span class="sxs-lookup"><span data-stu-id="126eb-p102">When you create or open a **Recordset** object, each of its records already has a unique bookmark. You can save the bookmark for the current record by assigning the value of the **Bookmark** property to a variable. To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="126eb-p103">Não há limite para o número de marcadores que você pode estabelecer. Para criar um marcador de um registro diferente do registro atual, mova-se para o registro desejado e atribua o valor da propriedade **Bookmark** a uma variável **String** que identifique o registro.</span><span class="sxs-lookup"><span data-stu-id="126eb-p103">There is no limit to the number of bookmarks you can establish. To create a bookmark for a record other than the current record, move to the desired record and assign the value of the **Bookmark** property to a **String** variable that identifies the record.</span></span>

<span data-ttu-id="126eb-117">Para garantir que o objeto **Recordset** seja compatível com marcadores, verifique os valores de sua propriedade **[Bookmarkable](recordset-bookmarkable-property-dao.md)** antes de usar a propriedade **Bookmark**.</span><span class="sxs-lookup"><span data-stu-id="126eb-117">To make sure the **Recordset** object supports bookmarks, check the value of its **[Bookmarkable](recordset-bookmarkable-property-dao.md)** property before you use the **Bookmark** property.</span></span> <span data-ttu-id="126eb-118">Se a propriedade **Bookmarkable** for False, o objeto **Recordset** não oferecerá suporte aos marcadores e usará os resultados da propriedade **Bookmark** em um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="126eb-118">If the Bookmarkable property is  False, the Recordset object doesn't support bookmarks, and using the Bookmark property results in a trappable error.</span></span>

<span data-ttu-id="126eb-p105">Se você usar o método **[Clone](recordset-clone-method-dao.md)** para criar uma cópia de um objeto **Recordset**, as definições da propriedade **Bookmark** dos objetos **Recordset** original e duplicado serão idênticas e poderão ser usadas de forma permutável. No entanto, você não pode usar marcadores de objetos **Recordset** diferentes de forma permutável, mesmo que esses marcadores tenham sido criados usando o mesmo objeto ou a mesma instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="126eb-p105">If you use the **[Clone](recordset-clone-method-dao.md)** method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and can be used interchangeably. However, you can't use bookmarks from different **Recordset** objects interchangeably, even if they were created by using the same object or the same SQL statement.</span></span>

<span data-ttu-id="126eb-121">Se você definir a propriedade **Bookmark** como um valor que representa um registro excluído, ocorrerá um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="126eb-121">If you set the **Bookmark** property to a value that represents a deleted record, a trappable error occurs.</span></span>

<span data-ttu-id="126eb-122">O valor da propriedade **Bookmark**Bookmark não é o mesmo que um número de registro.</span><span class="sxs-lookup"><span data-stu-id="126eb-122">The value of the **Bookmark** property isn't the same as a record number.</span></span>

## <a name="example"></a><span data-ttu-id="126eb-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="126eb-123">Example</span></span>

<span data-ttu-id="126eb-124">Este exemplo usa as propriedades **Bookmark** e **Bookmarkable** para permitir que o usuário sinalize um registro em um **Recordset** para retornar a ele mais tarde.</span><span class="sxs-lookup"><span data-stu-id="126eb-124">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a **Recordset** and return to it later.</span></span>

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
     Dim strMessage As String 
     Dim intCommand As Integer 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenSnapshot) 
     
     With rstCategories 
     
     If .Bookmarkable = False Then 
     Debug.Print "Recordset is not Bookmarkable!" 
     Else 
     ' Populate Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show information about current record and get 
     ' user input. 
     strMessage = "Category: " & !CategoryName & _ 
     " (record " & (.AbsolutePosition + 1) & _ 
     " of " & .RecordCount & ")" & vbCr & _ 
     "Enter command:" & vbCr & _ 
     "[1 - next / 2 - previous /" & vbCr & _ 
     "3 - set bookmark / 4 - go to bookmark]" 
     intCommand = Val(InputBox(strMessage)) 
     
     Select Case intCommand 
     ' Move forward or backward, trapping for BOF 
     ' or EOF. 
     Case 1 
     .MoveNext 
     If .EOF Then .MoveLast 
     Case 2 
     .MovePrevious 
     If .BOF Then .MoveFirst 
     
     ' Store the bookmark of the current record. 
     Case 3 
     varBookmark = .Bookmark 
     
     ' Go to the record indicated by the stored 
     ' bookmark. 
     Case 4 
     If IsEmpty(varBookmark) Then 
     MsgBox "No Bookmark set!" 
     Else 
     .Bookmark = varBookmark 
     End If 
     
     Case Else 
     Exit Do 
     End Select 
     
     Loop 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="126eb-125">Este exemplo usa a propriedade **LastModified** para mover o ponteiro do registro atual para o registro modificado e para o registro recentemente criado.</span><span class="sxs-lookup"><span data-stu-id="126eb-125">This example uses the **LastModified** property to move the current record pointer to both a record that has been modified and a newly created record.</span></span>

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strFirst As String 
     Dim strLast As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Store current data. 
     strFirst = !FirstName 
     strLast = !LastName 
     ' Change data in current record. 
     .Edit 
     !FirstName = "Julie" 
     !LastName = "Warren" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after Edit: " & _ 
     !FirstName & " " & !LastName 
     
     ' Restore original data because this is a demonstration. 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     
     ' Add new record. 
     .AddNew 
     !FirstName = "Roger" 
     !LastName = "Harui" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after AddNew: " & _ 
     !FirstName & " " & !LastName 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
