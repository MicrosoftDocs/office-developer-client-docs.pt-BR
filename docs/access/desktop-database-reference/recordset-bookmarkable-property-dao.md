---
title: Propriedade Recordset.Bookmarkable (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 6323f162-75c4-7cfe-c918-0b9454560f97
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194950(v=office.15)
ms:contentKeyID: 48545257
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2bd9b91f80c9411bb7cdf4e0be9e71ab055dc72f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699326"
---
# <a name="recordsetbookmarkable-property-dao"></a><span data-ttu-id="9ac42-102">Propriedade Recordset.Bookmarkable (DAO)</span><span class="sxs-lookup"><span data-stu-id="9ac42-102">Recordset.Bookmarkable property (DAO)</span></span>


<span data-ttu-id="9ac42-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ac42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ac42-104">Retorna um valor que indica se um objeto **Recordset** oferece suporte a indicadores, que você pode definir utilizando a propriedade **[Bookmark](recordset-bookmark-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="9ac42-104">Returns a value that indicates whether a **Recordset** object supports bookmarks, which you can set by using the **[Bookmark](recordset-bookmark-property-dao.md)** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ac42-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ac42-105">Syntax</span></span>

<span data-ttu-id="9ac42-106">*expressão* . Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="9ac42-106">*expression* .Bookmarkable</span></span>

<span data-ttu-id="9ac42-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="9ac42-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ac42-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ac42-108">Remarks</span></span>

<span data-ttu-id="9ac42-109">Verifique a configuração da propriedade **Bookmarkable** de um objeto **Recordset** antes de tentar definir ou verificar a propriedade **Bookmark**.</span><span class="sxs-lookup"><span data-stu-id="9ac42-109">Check the **Bookmarkable** property setting of a **Recordset** object before you attempt to set or check the **Bookmark** property.</span></span>

<span data-ttu-id="9ac42-110">Em objetos **Recordset** inteiramente baseado em tabelas de mecanismo de banco de dados do Microsoft Access, o valor da propriedade **Bookmarkable** é True e você pode usar indicadores.</span><span class="sxs-lookup"><span data-stu-id="9ac42-110">For **Recordset** objects based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use bookmarks.</span></span> <span data-ttu-id="9ac42-111">Entretanto, outros produtos de banco de dados podem não aceitar indicadores.</span><span class="sxs-lookup"><span data-stu-id="9ac42-111">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="9ac42-112">Por exemplo, você não pode usar indicadores em nenhum objeto **Recordset** com base em uma tabela vinculada Paradox que não tenha nenhuma chave primária.</span><span class="sxs-lookup"><span data-stu-id="9ac42-112">For example, you can't use bookmarks in any **Recordset** object based on a linked Paradox table that has no primary key.</span></span>

## <a name="example"></a><span data-ttu-id="9ac42-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9ac42-113">Example</span></span>

<span data-ttu-id="9ac42-114">Este exemplo utiliza as propriedades **Bookmark** e **Bookmarkable** para permitir que o usuário sinalize um registro no **Recordset** e volte a ele posteriormente.</span><span class="sxs-lookup"><span data-stu-id="9ac42-114">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a **Recordset** and return to it later.</span></span>

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
