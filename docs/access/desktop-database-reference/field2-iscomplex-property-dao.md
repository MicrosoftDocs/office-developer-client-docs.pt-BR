---
title: Propriedade Campo2. isComplex (DAO)
TOCTitle: IsComplex Property
ms:assetid: ffc90e6e-e3ee-4f9b-ca6b-615199300d45
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837318(v=office.15)
ms:contentKeyID: 48548970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d24229a0fc3122cc8a9fb20b041fc9fadc5ccb0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292780"
---
# <a name="field2iscomplex-property-dao"></a><span data-ttu-id="83ba2-102">Propriedade Campo2. isComplex (DAO)</span><span class="sxs-lookup"><span data-stu-id="83ba2-102">Field2.IsComplex property (DAO)</span></span>

<span data-ttu-id="83ba2-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="83ba2-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="83ba2-104">Retorna um **Boolean** que indica se o campo especificado tem um tipo de dados de vários valores.</span><span class="sxs-lookup"><span data-stu-id="83ba2-104">Returns **Boolean** that indicates whether the specified field is a multi-valued data type.</span></span> <span data-ttu-id="83ba2-105">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="83ba2-105">Read-only.</span></span>

## <a name="version-information"></a><span data-ttu-id="83ba2-106">Informação da versão</span><span class="sxs-lookup"><span data-stu-id="83ba2-106">Version information</span></span>

<span data-ttu-id="83ba2-107">Versão adicionada: Access 2007</span><span class="sxs-lookup"><span data-stu-id="83ba2-107">Version added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="83ba2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83ba2-108">Syntax</span></span>

<span data-ttu-id="83ba2-109">*expressão* . IsComplex</span><span class="sxs-lookup"><span data-stu-id="83ba2-109">*expression* .IsComplex</span></span>

<span data-ttu-id="83ba2-110">*expressão* Uma variável que representa um objeto **campo2** .</span><span class="sxs-lookup"><span data-stu-id="83ba2-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="example"></a><span data-ttu-id="83ba2-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="83ba2-111">Example</span></span>

<span data-ttu-id="83ba2-112">O exemplo a seguir mostra como navegar em um Recordset que contém um campo de vários valores.</span><span class="sxs-lookup"><span data-stu-id="83ba2-112">The following example shows how to navigate a Recordset that contains a multi-value field.</span></span>

<span data-ttu-id="83ba2-113">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="83ba2-113">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub PrintStudentsAndClasses()
        Dim dbs As DAO.Database
        Dim rsStudents As DAO.Recordset2  'Recordset for students
        Dim rsClasses As DAO.Recordset2  'Recordset for classes
        Dim fld As DAO.Field2
    
        'open the database
        Set dbs = CurrentDb()
    
        'get the table of students
        Set rsStudents = dbs.OpenRecordset("tblStudents")
    
        'loop through the students
        Do While Not rsStudents.EOF
            
            'get the classes field
            Set fld = rsStudents("Classes")
    
            'get the classes Recordset
            'make sure the field is a multi-valued field before
            'getting a Recordset object
            If fld.IsComplex Then
                Set rsClasses = fld.Value
            End If
    
            'access all records in the Recordset
            If Not (rsClasses.BOF And rsClasses.EOF) Then
                rsClasses.MoveLast
                rsClasses.MoveFirst
            End If
    
            'print the student and number of classes
            Debug.Print rsStudents("FirstName") & " " & rsStudents("LastName"), _
                "Number of classes: " & rsClasses.RecordCount
    
            'print the classes for this student
            Do While Not rsClasses.EOF
                Debug.Print , rsClasses("Value")
                rsClasses.MoveNext
            Loop
    
            'close the Classes Recordset
            rsClasses.Close
    
            'get the next student
            rsStudents.MoveNext
    
        Loop
        
        'cleanup
        rsStudents.Close
    
        Set fld = Nothing
        Set rsStudents = Nothing
        Set dbs = Nothing
    
    End Sub
```
