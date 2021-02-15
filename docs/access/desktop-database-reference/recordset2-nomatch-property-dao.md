---
title: Propriedade Recordset2.NoMatch (DAO)
TOCTitle: NoMatch Property
ms:assetid: 2d7a02ff-a2bf-5f0e-bd71-a6d42c25b13a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192114(v=office.15)
ms:contentKeyID: 48543972
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c3168dcce9fb13d057380e7a1a4ef89f8814e02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309391"
---
# <a name="recordset2nomatch-property-dao"></a><span data-ttu-id="3d849-102">Propriedade Recordset2.NoMatch (DAO)</span><span class="sxs-lookup"><span data-stu-id="3d849-102">Recordset2.NoMatch property (DAO)</span></span>

<span data-ttu-id="3d849-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d849-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d849-104">Indica se um registro em particular foi localizado usando o método **[Seek](recordset2-seek-method-dao.md)** ou um dos métodos **[Find](recordset2-findfirst-method-dao.md)** (somente em espaços de trabalho do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="3d849-104">Indicates whether a particular record was found by using the **[Seek](recordset2-seek-method-dao.md)** method or one of the **[Find](recordset2-findfirst-method-dao.md)** methods (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d849-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d849-105">Syntax</span></span>

<span data-ttu-id="3d849-106">*expressão* .NoMatch</span><span class="sxs-lookup"><span data-stu-id="3d849-106">*expression* .NoMatch</span></span>

<span data-ttu-id="3d849-107">*expressão* Uma variável que representa **um objeto Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="3d849-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d849-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d849-108">Remarks</span></span>

<span data-ttu-id="3d849-109">Quando você abrir ou criar um objeto **[Recordset](recordset-object-dao.md)**, a propriedade **NoMatch** será definida como **False**.</span><span class="sxs-lookup"><span data-stu-id="3d849-109">When you open or create a **[Recordset](recordset-object-dao.md)** object, its **NoMatch** property is set to **False**.</span></span>

<span data-ttu-id="3d849-p101">Para localizar um registro, use o método **Seek** em um **Recordset** do tipo tabela ou um dos métodos **Find** em um objeto **Recordset** do tipo dynaset ou instantâneo. Verifique a definição da propriedade **NoMatch** para verificar se o registro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="3d849-p101">To locate a record, use the **Seek** method on a table-type **Recordset** object or one of the **Find** methods on a dynaset- or snapshot-type **Recordset** object. Check the **NoMatch** property setting to see whether the record was found.</span></span>

<span data-ttu-id="3d849-p102">Se o método **Seek** ou **Find** não for bem-sucedido e a propriedade **NoMatch** for **True**, o registro atual não será mais válido. Verifique se você obteve o indicador do registro atual antes de usar o método **Seek** ou o método **Find**, caso seja necessário retornar para esse registro.</span><span class="sxs-lookup"><span data-stu-id="3d849-p102">If the **Seek** or **Find** method is unsuccessful and the **NoMatch** property is **True**, the current record will no longer be valid. Be sure to obtain the current record's bookmark before using the **Seek** method or a **Find** method if you'll need to return to that record.</span></span>

> [!NOTE]
> <span data-ttu-id="3d849-114">O uso de qualquer um dos métodos **[Move](recordset-movefirst-method-dao.md)** em um objeto **Recordset** não afetará a definição da propriedade **NoMatch**.</span><span class="sxs-lookup"><span data-stu-id="3d849-114">Using any of the **[Move](recordset-movefirst-method-dao.md)** methods on a **Recordset** object won't affect its **NoMatch** property setting.</span></span>

## <a name="example"></a><span data-ttu-id="3d849-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3d849-115">Example</span></span>

<span data-ttu-id="3d849-p103">Este exemplo usa a propriedade **NoMatch** para determinar se um **Seek** e um **FindFirst** foram bem-sucedidos e, em caso negativo, para fornecer os comentários apropriados. Os procedimentos SeekMatch e FindMatch são exigidos para que esse procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="3d849-p103">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback. The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

```vb
    Sub NoMatchX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim rstCustomers As Recordset2 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim strCountry As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Default is dbOpenTable; required if Index property will 
     ' be used. 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     With rstProducts 
     .Index = "PrimaryKey" 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with Seek method" & vbCr & _ 
     "Product ID: " & !ProductID & vbCr & _ 
     "Product Name: " & !ProductName & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter a product ID." 
     strSeek = InputBox(strMessage) 
     If strSeek = "" Then Exit Do 
     
     ' Call procedure that seeks for a record based on 
     ' the ID number supplied by the user. 
     SeekMatch rstProducts, Val(strSeek) 
     Loop 
     
     .Close 
     End With 
     
     Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
     "SELECT CompanyName, Country FROM Customers " & _ 
     "ORDER BY CompanyName", dbOpenSnapshot) 
     
     With rstCustomers 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with FindFirst method" & _ 
     vbCr & "Customer Name: " & !CompanyName & _ 
     vbCr & "Country: " & !Country & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter country on which to search." 
     strCountry = Trim(InputBox(strMessage)) 
     If strCountry = "" Then Exit Do 
     
     ' Call procedure that finds a record based on 
     ' the country name supplied by the user. 
     FindMatch rstCustomers, _ 
     "Country = '" & strCountry & "'" 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset2, _ 
     intSeek As Integer) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .Seek "=", intSeek 
     
     ' If Seek method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
     strFind As String) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .FindFirst strFind 
     
     ' If Find method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub
```
