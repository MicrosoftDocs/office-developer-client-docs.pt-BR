---
title: Propriedade Property.Inherited (DAO)
TOCTitle: Inherited Property
ms:assetid: 10e624db-2301-b9be-beca-6e8caccf7274
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845349(v=office.15)
ms:contentKeyID: 48543304
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052991
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cf3aef6d04c7d7cc573ec1d6efaca7d5238f5125
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709527"
---
# <a name="propertyinherited-property-dao"></a>Propriedade Property.Inherited (DAO)


**Aplica-se a**: Access 2013, o Office 2013 

Retorna um valor que indica se um objeto **[Property](property-object-dao.md)** foi herdado de um objeto base.

## <a name="syntax"></a>Sintaxe

*expressão* . Herdado

*expressão* Uma variável que representa um objeto **Property** .

## <a name="remarks"></a>Comentários

Para objetos **Property** internos que representam propriedades predefinidas, o único valor de retorno possível é **False**.

Use a propriedade **Inherited** para determinar se **Property** definido pelo usuário foi criado para o objeto ao qual se aplica ou se **Property** foi herdado de outro objeto. Por exemplo, suponha que você criou um novo **Property** para o objeto **[QueryDef](querydef-object-dao.md)** e depois abriu um objeto **[Recordset](recordset-object-dao.md)** a partir de um objeto **QueryDef**. Esse novo **Property** fará parte da coleção [**Properties**](properties-collection-dao.md) do objeto **Recordset** e sua propriedade **Inherited** será definida como **True** porque a propriedade foi criada a partir do objeto **QueryDef** e não do objeto **Recordset**.

## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **Inherited** para determinar se um objeto **Property** definido pelo usuário foi criado para um **Recordset** ou para algum objeto base.

```vb 
Sub InheritedX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfTest As TableDef 
 Dim rstTest As Recordset 
 Dim prpNew As Property 
 Dim prpLoop As Property 
 
 ' Create a new property for a saved TableDef object, then 
 ' open a recordset from that TableDef object. 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set tdfTest = dbsNorthwind.TableDefs(0) 
 Set prpNew = tdfTest.CreateProperty("NewProperty", _ 
 dbBoolean, True) 
 tdfTest.Properties.Append prpNew 
 Set rstTest = tdfTest.OpenRecordset(dbOpenForwardOnly) 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the TableDef. 
 Debug.Print "NewProperty of " & tdfTest.Name & _ 
 " TableDef:" 
 Debug.Print " Inherited = " & _ 
 tdfTest.Properties("NewProperty").Inherited 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the Recordset. 
 Debug.Print "NewProperty of " & rstTest.Name & _ 
 " Recordset:" 
 Debug.Print " Inherited = " & _ 
 rstTest.Properties("NewProperty").Inherited 
 
 ' Delete new TableDef because this is a demonstration. 
 tdfTest.Properties.Delete prpNew.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

