---
title: Método Fields.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: d08597d8-bad6-523b-a083-d824f85b64bc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834723(v=office.15)
ms:contentKeyID: 48547844
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09218fae470646ab04ecfb5427004e56183e46ca
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715666"
---
# <a name="fieldsrefresh-method-dao"></a>Método Fields.Refresh (DAO)


**Aplica-se a**: Access 2013, o Office 2013


Atualiza os objetos na coleção especificada para refletir o esquema atual do banco de dados.

## <a name="syntax"></a>Sintaxe

*expressão* . Atualizar

*expressão* Uma variável que representa um objeto **Fields** .

## <a name="remarks"></a>Comentários

Para determinar a posição que o mecanismo de banco de dados do Microsoft Access usa para os objetos **Field** na coleção **Fields** de um objeto **QueryDef**, **Recordset** ou **TableDef**, utilize a propriedade **OrdinalPosition** de cada objeto **Field**. Alterar a propriedade **OrdinalPosition** de um objeto **Field** pode não alterar a ordem dos objetos **Field** na coleção até que você use o método **Refresh**.

Use o método **Refresh** em um ambiente de vários usuários no qual outros usuários podem alterar o banco de dados. Você também pode precisar utilizá-lo em coleções que são indiretamente afetas pelas alterações no banco de dados. Por exemplo, se você alterar uma coleção **Users**, poderá precisar atualizar uma coleção **Groups** antes de utilizar a coleção **Groups**.

Uma coleção é preenchida com objetos quando ela se refere, pela primeira vez, a e não reflete automaticamente as alterações subsequentes feitas por outros usuários. Se provavelmente outro usuário alterou uma coleção, use o método Refresh na coleção imediatamente antes de executar qualquer tarefa no aplicativo que considera a presença ou a ausência de um objeto particular na coleção. Isso garante que a coleção seja atualizada assim que possível. Por outro lado, utilizar Refresh pode desnecessariamente reduzir o desempenho.

## <a name="example"></a>Exemplo

Este exemplo usa o método **Refresh** para atualizar a coleção **Fields** da tabela Categories com base nas alterações nos dados de **OrdinalPosition**. A ordem de **Fields** na coleção muda somente depois de o método **Refresh** ser usado.

```vb
    Sub RefreshX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Categories") 
     
     With tdfEmployees 
     ' Display original OrdinalPosition data and store it 
     ' in an array. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldLoop In .Fields 
     fldLoop.OrdinalPosition = _ 
     100 - fldLoop.OrdinalPosition 
     Next fldLoop 
     Set fldLoop = Nothing 
     
     ' Print new data. 
     Debug.Print "New OrdinalPosition data before Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     .Fields.Refresh 
     
     ' Print new data, showing how the field order has been 
     ' changed. 
     Debug.Print "New OrdinalPosition data after Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     ' Restore original OrdinalPosition data. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
