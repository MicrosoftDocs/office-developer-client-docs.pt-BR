---
title: Propriedade Recordset2. Bookmarkable (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 9c93d04d-ca10-acf5-122a-58625ed93424
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198125(v=office.15)
ms:contentKeyID: 48546601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052888
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 26b8b60255b4e50a2288dedb8e27906476926e8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307452"
---
# <a name="recordset2bookmarkable-property-dao"></a><span data-ttu-id="243f6-102">Propriedade Recordset2. Bookmarkable (DAO)</span><span class="sxs-lookup"><span data-stu-id="243f6-102">Recordset2.Bookmarkable property (DAO)</span></span>


<span data-ttu-id="243f6-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="243f6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="243f6-104">Retorna um valor que indica se um objeto **Recordset** suporta indicadores, que você pode definir usando a propriedade **[Bookmark](recordset2-bookmark-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="243f6-104">Returns a value that indicates whether a **Recordset** object supports bookmarks, which you can set by using the **[Bookmark](recordset2-bookmark-property-dao.md)** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="243f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="243f6-105">Syntax</span></span>

<span data-ttu-id="243f6-106">*expressão* . Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="243f6-106">*expression* .Bookmarkable</span></span>

<span data-ttu-id="243f6-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="243f6-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="243f6-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="243f6-108">Remarks</span></span>

<span data-ttu-id="243f6-109">Verifique a definição da propriedade **Bookmarkable** de um objeto **Recordset** antes de você tentar definir ou verificar a propriedade **Bookmark**.</span><span class="sxs-lookup"><span data-stu-id="243f6-109">Check the **Bookmarkable** property setting of a **Recordset** object before you attempt to set or check the **Bookmark** property.</span></span>

<span data-ttu-id="243f6-110">Para objetos **Recordset** com base em tabelas do mecanismo de banco de dados do Microsoft Access, o valor da propriedade **Bookmarkable** é true, e você pode usar indicadores.</span><span class="sxs-lookup"><span data-stu-id="243f6-110">For **Recordset** objects based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use bookmarks.</span></span> <span data-ttu-id="243f6-111">No entanto, outros produtos do banco de dados podem não oferecer suporte aos marcadores.</span><span class="sxs-lookup"><span data-stu-id="243f6-111">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="243f6-112">Por exemplo, não será possível usar os indicadores em qualquer objeto **Recordset** com base em uma tabela do Paradox vinculada que não tem chave primária.</span><span class="sxs-lookup"><span data-stu-id="243f6-112">For example, you can't use bookmarks in any **Recordset** object based on a linked Paradox table that has no primary key.</span></span>

## <a name="example"></a><span data-ttu-id="243f6-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="243f6-113">Example</span></span>

<span data-ttu-id="243f6-114">Este exemplo usa as propriedades **Bookmark** e **Bookmarkable** para permitir que o usuário sinalize um registro em um conjunto de registros e retorne mais tarde.</span><span class="sxs-lookup"><span data-stu-id="243f6-114">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a recordset and return to it later.</span></span>

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset2 
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
