---
title: Propriedade Recordset.NoMatch (DAO)
TOCTitle: NoMatch Property
ms:assetid: 47d03575-f570-89b5-a20f-a3bd8b8b5c6d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193226(v=office.15)
ms:contentKeyID: 48544606
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052889
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: e54f8c51787e51785bdaacaecd28a8d24e2cb5b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300424"
---
# <a name="recordsetnomatch-property-dao"></a><span data-ttu-id="e063e-102">Propriedade Recordset.NoMatch (DAO)</span><span class="sxs-lookup"><span data-stu-id="e063e-102">Recordset.NoMatch property (DAO)</span></span>

<span data-ttu-id="e063e-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e063e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e063e-104">Indica se um registro em particular foi localizado usando o método **[Seek](recordset-seek-method-dao.md)** ou um dos métodos **[Find](recordset-findfirst-method-dao.md)** (somente em espaços de trabalho do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="e063e-104">Indicates whether a particular record was found by using the **[Seek](recordset-seek-method-dao.md)** method or one of the **[Find](recordset-findfirst-method-dao.md)** methods (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="e063e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e063e-105">Syntax</span></span>

<span data-ttu-id="e063e-106">*expressão* .NoMatch</span><span class="sxs-lookup"><span data-stu-id="e063e-106">expression  . NoMatch</span></span>

<span data-ttu-id="e063e-107">*expressão* Uma variável que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e063e-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e063e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="e063e-108">Remarks</span></span>

<span data-ttu-id="e063e-109">Quando você abrir ou criar um objeto **[Recordset](recordset-object-dao.md)**, a propriedade **NoMatch** será definida como **False**.</span><span class="sxs-lookup"><span data-stu-id="e063e-109">When you open or create a **[Recordset](recordset-object-dao.md)** object, its **NoMatch** property is set to **False**.</span></span>

<span data-ttu-id="e063e-p101">Para localizar um registro, use o método **Seek** em um **Recordset** do tipo tabela ou um dos métodos **Find** em um objeto **Recordset** do tipo dynaset ou instantâneo. Verifique a definição da propriedade **NoMatch** para verificar se o registro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="e063e-p101">To locate a record, use the **Seek** method on a table-type **Recordset** object or one of the **Find** methods on a dynaset- or snapshot-type **Recordset** object. Check the **NoMatch** property setting to see whether the record was found.</span></span>

<span data-ttu-id="e063e-p102">Se o método **Seek** ou **Find** não for bem-sucedido e a propriedade **NoMatch** for **True**, o registro atual não será mais válido. Verifique se você obteve o indicador do registro atual antes de usar o método **Seek** ou o método **Find**, caso seja necessário retornar para esse registro.</span><span class="sxs-lookup"><span data-stu-id="e063e-p102">If the **Seek** or **Find** method is unsuccessful and the **NoMatch** property is **True**, the current record will no longer be valid. Be sure to obtain the current record's bookmark before using the **Seek** method or a **Find** method if you'll need to return to that record.</span></span>


> [!NOTE]
> <span data-ttu-id="e063e-114">O uso de qualquer um dos métodos **[Move](recordset-movefirst-method-dao.md)** em um objeto **Recordset** não afetará a definição da propriedade **NoMatch**.</span><span class="sxs-lookup"><span data-stu-id="e063e-114">Using any of the **[Move](recordset-movefirst-method-dao.md)** methods on a **Recordset** object won't affect its **NoMatch** property setting.</span></span>


## <a name="example"></a><span data-ttu-id="e063e-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e063e-115">Example</span></span>

<span data-ttu-id="e063e-p103">Este exemplo usa a propriedade **NoMatch** para determinar se um **Seek** e um **FindFirst** foram bem-sucedidos e, em caso negativo, para fornecer os comentários apropriados. Os procedimentos SeekMatch e FindMatch são exigidos para que esse procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="e063e-p103">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback. The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

```vb
    Sub NoMatchX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim rstCustomers As Recordset 
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
     
    Sub SeekMatch(rstTemp As Recordset, _ 
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

<br/>

<span data-ttu-id="e063e-118">O exemplo a seguir mostra como usar o método Seek para localizar um registro em uma tabela vinculada.</span><span class="sxs-lookup"><span data-stu-id="e063e-118">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="e063e-119">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="e063e-119">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
