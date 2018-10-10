---
title: Propriedade TableDef.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: d01588c3-e94e-06bd-6568-974873411f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834701(v=office.15)
ms:contentKeyID: 48547828
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10c0c3211fe76b169f9c2ed634f8adb61c767cfc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465101"
---
# <a name="tabledefattributes-property-dao"></a>Propriedade TableDef.Attributes (DAO)


**Aplica-se a**: Access 2013 | Office 2013


Define ou retorna um valor que indica uma ou várias características de um objeto **TableDef**. **Long** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . Atributos

*expressão* Uma variável que representa um objeto **TableDef** .

## <a name="remarks"></a>Comentários

Para um objeto ainda não acrescentado a uma coleção, essa propriedade será leitura/gravação.

## <a name="example"></a>Exemplo

Este exemplo exibe a propriedade **Attributes** dos objetos **Field**, **Relation** e **TableDef** no banco de dados Northwind.

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```
