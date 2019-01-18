---
title: Coleção Documents (DAO)
TOCTitle: Documents Collection
ms:assetid: ae2fef58-34e7-eea6-ca51-d3903432c7f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821742(v=office.15)
ms:contentKeyID: 48547063
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f6edd02c316fdff3f64b8a09c1504c46c9812a3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698831"
---
# <a name="documents-collection-dao"></a><span data-ttu-id="0a2ea-102">Coleção Documents (DAO)</span><span class="sxs-lookup"><span data-stu-id="0a2ea-102">Documents collection (DAO)</span></span>


<span data-ttu-id="0a2ea-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a2ea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0a2ea-104">Uma coleção **Documents** contém todos os objetos **Document** para um tipo específico de objeto (bancos de dados de mecanismo de banco de dados do Microsoft Access apenas).</span><span class="sxs-lookup"><span data-stu-id="0a2ea-104">A **Documents** collection contains all of the **Document** objects for a specific type of object (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="0a2ea-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a2ea-105">Remarks</span></span>

<span data-ttu-id="0a2ea-106">Cada objeto **Container** tem uma coleção **Documents** contendo objetos **Document** que descrevem instâncias de objetos internos do tipo especificado pelo **Container**.</span><span class="sxs-lookup"><span data-stu-id="0a2ea-106">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**.</span></span>

<span data-ttu-id="0a2ea-107">Para fazer referência a um objeto **Document** em uma coleção por seu número ordinal ou por sua configuração de propriedade **Name**, use uma das seguintes formas de sintaxe:</span><span class="sxs-lookup"><span data-stu-id="0a2ea-107">To refer to a **Document** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

  - <span data-ttu-id="0a2ea-108">**Documents**(0)</span><span class="sxs-lookup"><span data-stu-id="0a2ea-108">**Documents**(0)</span></span>

  - <span data-ttu-id="0a2ea-109">**Documentos** ("*nome*")</span><span class="sxs-lookup"><span data-stu-id="0a2ea-109">**Documents**("*name*")</span></span>

  - <span data-ttu-id="0a2ea-110">**Documentos**\!\[*nome*\]</span><span class="sxs-lookup"><span data-stu-id="0a2ea-110">**Documents**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="0a2ea-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0a2ea-111">Example</span></span>

<span data-ttu-id="0a2ea-112">Este exemplo enumera a coleção **Documents** do contêineer Tables e enumera a coleção **Properties** do primeiro objeto **Document** na coleção.</span><span class="sxs-lookup"><span data-stu-id="0a2ea-112">This example enumerates the **Documents** collection of the Tables container, and then enumerates the **Properties** collection of the first **Document** object in the collection.</span></span>

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

