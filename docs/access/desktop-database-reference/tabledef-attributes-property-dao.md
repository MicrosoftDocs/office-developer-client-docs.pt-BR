---
title: Propriedade TableDef.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: d01588c3-e94e-06bd-6568-974873411f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834701(v=office.15)
ms:contentKeyID: 48547828
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abdb0d07f2293a53fccaf0d628c301750027acc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314389"
---
# <a name="tabledefattributes-property-dao"></a><span data-ttu-id="4f683-102">Propriedade TableDef.Attributes (DAO)</span><span class="sxs-lookup"><span data-stu-id="4f683-102">TableDef.Attributes property (DAO)</span></span>


<span data-ttu-id="4f683-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f683-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="4f683-104">Define ou retorna um valor que indica uma ou várias características de um objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="4f683-104">Sets or returns a value that indicates one or more characteristics of a **TableDef** object.</span></span> <span data-ttu-id="4f683-105">**Long** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4f683-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f683-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f683-106">Syntax</span></span>

<span data-ttu-id="4f683-107">*expressão* .Attributes</span><span class="sxs-lookup"><span data-stu-id="4f683-107">*expression* .Attributes</span></span>

<span data-ttu-id="4f683-108">*expressão* Uma variável que representa um objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="4f683-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f683-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f683-109">Remarks</span></span>

<span data-ttu-id="4f683-110">Para um objeto ainda não acrescentado a uma coleção, essa propriedade será leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4f683-110">For an object not yet appended to a collection, this property is read/write.</span></span>

## <a name="example"></a><span data-ttu-id="4f683-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4f683-111">Example</span></span>

<span data-ttu-id="4f683-112">Este exemplo exibe a propriedade **Attributes** dos objetos **Field**, **Relation** e **TableDef** no banco de dados Northwind.</span><span class="sxs-lookup"><span data-stu-id="4f683-112">This example displays the **Attributes** property for **Field**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

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

