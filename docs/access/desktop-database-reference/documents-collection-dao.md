---
title: Coleção Documents (DAO)
TOCTitle: Documents Collection
ms:assetid: ae2fef58-34e7-eea6-ca51-d3903432c7f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821742(v=office.15)
ms:contentKeyID: 48547063
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92a9dc96b438a55401df95a63ea47b85d96b0f83
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465279"
---
# <a name="documents-collection-dao"></a>Coleção Documents (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Uma coleção **Documents** contém todos os objetos **Document** para um tipo específico de objeto (bancos de dados de mecanismo de banco de dados do Microsoft Access apenas).

## <a name="remarks"></a>Comentários

Cada objeto **Container** tem uma coleção **Documents** contendo objetos **Document** que descrevem instâncias de objetos internos do tipo especificado pelo **Container**.

Para fazer referência a um objeto **Document** em uma coleção por seu número ordinal ou por sua configuração de propriedade **Name**, use uma das seguintes formas de sintaxe:

  - **Documents**(0)

  - **Documentos** ("*nome*")

  - **Documentos**\!\[*nome*\]

## <a name="example"></a>Exemplo

Este exemplo enumera a coleção **Documents** do contêineer Tables e enumera a coleção **Properties** do primeiro objeto **Document** na coleção.

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```
