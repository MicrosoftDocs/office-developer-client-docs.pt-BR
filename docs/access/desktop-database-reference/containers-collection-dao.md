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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703822"
---
# <a name="containers-collection-dao"></a><span data-ttu-id="48e38-102">Coleção Containers (DAO)</span><span class="sxs-lookup"><span data-stu-id="48e38-102">Containers collection (DAO)</span></span>

<span data-ttu-id="48e38-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="48e38-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="48e38-104">Uma coleção **Containers** contém todos os objetos de **contêiner** que são definidos em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="48e38-104">A **Containers** collection contains all of the **Container** objects that are defined in a database.</span></span>

## <a name="remarks"></a><span data-ttu-id="48e38-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="48e38-105">Remarks</span></span>

<span data-ttu-id="48e38-106">Cada objeto **Database** tem uma coleção **Containers** que consiste em objetos **Container** incorporados.</span><span class="sxs-lookup"><span data-stu-id="48e38-106">Each **Database** object has a **Containers** collection consisting of built-in **Container** objects.</span></span> <span data-ttu-id="48e38-107">Alguns desses objetos **Container** são definidos pelo mecanismo de banco de dados do Microsoft Access enquanto outros podem ser definidos por outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="48e38-107">Some of these **Container** objects are defined by the Microsoft Access database engine while others may be defined by other applications.</span></span>

## <a name="example"></a><span data-ttu-id="48e38-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="48e38-108">Example</span></span>

<span data-ttu-id="48e38-109">Este exemplo enumera a coleção **Containers** do banco de dados Northwind e a coleção **Properties** de cada objeto **Container** na coleção.</span><span class="sxs-lookup"><span data-stu-id="48e38-109">This example enumerates the **Containers** collection of the Northwind database and the **Properties** collection of each **Container** object in the collection.</span></span>

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
