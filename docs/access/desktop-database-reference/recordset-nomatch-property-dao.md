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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702625"
---
# <a name="recordsetnomatch-property-dao"></a>Propriedade Recordset.NoMatch (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Indica se um registro específico foi encontrado usando o método **[Seek](recordset-seek-method-dao.md)** ou um dos métodos **[Find](recordset-findfirst-method-dao.md)** (somente em espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . NoMatch

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

Quando você abrir ou criar um objeto **[Recordset](recordset-object-dao.md)**, sua propriedade **NoMatch** será definida como **False**.

Para localizar um registro, use o método **Seek** em um **Recordset** do tipo tabela ou um dos métodos **Find** em um objeto **Recordset** do tipo dynaset ou instantâneo. Verifique a definição da propriedade **NoMatch** para verificar se o registro foi encontrado.

Se o método **Seek** ou **Find** não for bem-sucedido e a propriedade **NoMatch** for **True**, o registro atual não será mais válido. Verifique se você obteve o indicador do registro atual antes de usar o método **Seek** ou o método **Find**, caso seja necessário retornar para esse registro.


> [!NOTE]
> [!OBSERVAçãO] O uso de qualquer um dos métodos **[Move](recordset-movefirst-method-dao.md)** em um objeto **Recordset** não afetará a definição da propriedade **NoMatch**.


## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **NoMatch** para determinar se **Seek** e **FindFirst** foram bem-sucedidos e, se não foram, fornece os comentários adequados. Os procedimentos SeekMatch e FindMatch são necessários para executar esse procedimento.

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

O exemplo a seguir mostra como usar o método Seek para localizar um registro em uma tabela vinculada.

**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
