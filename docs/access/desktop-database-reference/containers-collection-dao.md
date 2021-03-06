---
title: Coleção Containers (DAO)
TOCTitle: Containers Object
ms:assetid: 4996ee39-ea13-f560-3069-dd7bc6022119
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193464(v=office.15)
ms:contentKeyID: 48544642
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9c874a1555fa6a6f5f948275176c57b5fb1c48bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295601"
---
# <a name="containers-collection-dao"></a>Coleção Containers (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Uma **coleção Containers** contém todos os objetos **Container** definidos em um banco de dados.

## <a name="remarks"></a>Comentários

Cada objeto **Database** tem uma coleção **Containers** que consiste em objetos **Container** incorporados. Alguns desses objetos **Container** são definidos pelo mecanismo de banco de dados do Microsoft Access enquanto outros podem ser definidos por outros aplicativos.

## <a name="example"></a>Exemplo

Este exemplo enumera a coleção **Containers** do banco de dados Northwind e a coleção **Properties** de cada objeto **Container** na coleção.

```vb
    Sub ContainerObjectX()
    
       Dim dbsNorthwind As Database
       Dim ctrLoop As Container
       Dim prpLoop As Property
    
       Set dbsNorthwind = OpenDatabase("Northwind.mdb")
    
       With dbsNorthwind
    
          ' Enumerate Containers collection.
          For Each ctrLoop In .Containers
             Debug.Print "Properties of " & ctrLoop.Name _
                & " container"
    
             ' Enumerate Properties collection of each
             ' Container object.
             For Each prpLoop In ctrLoop.Properties
                Debug.Print "  " & prpLoop.Name _
                   & " = " prpLoop
             Next prpLoop
    
          Next ctrLoop
    
          .Close
       End With
    
    End Sub
```
