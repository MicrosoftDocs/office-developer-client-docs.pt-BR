---
title: Objeto Field2 (DAO)
TOCTitle: Field2 Object
ms:assetid: 585aa163-402b-2c2b-d8d7-733a6d55d104
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194326(v=office.15)
ms:contentKeyID: 48544994
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 88c8b7ff347235bbdc29745e9f5383933d3d1dda
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713139"
---
# <a name="field2-object-dao"></a><span data-ttu-id="c5dc2-102">Objeto Field2 (DAO)</span><span class="sxs-lookup"><span data-stu-id="c5dc2-102">Field2 object (DAO)</span></span>

<span data-ttu-id="c5dc2-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5dc2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5dc2-104">Um objeto **Field2** representa uma coluna de dados com um tipo de dados comum e um conjunto comum de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-104">A **Field2** object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5dc2-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5dc2-105">Remarks</span></span>

<span data-ttu-id="c5dc2-p101">Um objeto **Field2** contém as mesmas propriedades e métodos que o objeto **[Field](field-object-dao.md)**. O objeto **Field2** contém várias propriedades e métodos novos que oferecem suporte a tipos de campo de vários valores. As novas propriedades e métodos são:</span><span class="sxs-lookup"><span data-stu-id="c5dc2-p101">A **Field2** object is contains all of the same properties and methods as the **[Field](field-object-dao.md)** object. The **Field2** object contains several new properties and methods that support multi-valued field types. The new properties and methods are:</span></span>

- <span data-ttu-id="c5dc2-109">Propriedade **[AppendOnly](field2-appendonly-property-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="c5dc2-109">**[AppendOnly](field2-appendonly-property-dao.md)** property</span></span>

- <span data-ttu-id="c5dc2-110">Propriedade **[ComplexType](field2-complextype-property-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="c5dc2-110">**[ComplexType](field2-complextype-property-dao.md)** property</span></span>

- <span data-ttu-id="c5dc2-111">Propriedade **[IsComplex](field2-iscomplex-property-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="c5dc2-111">**[IsComplex](field2-iscomplex-property-dao.md)** property</span></span>

- <span data-ttu-id="c5dc2-112">Método **[LoadFromFile](field2-loadfromfile-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="c5dc2-112">**[LoadFromFile](field2-loadfromfile-method-dao.md)** method</span></span>

- <span data-ttu-id="c5dc2-113">Método **[SaveToFile](field2-savetofile-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="c5dc2-113">**[SaveToFile](field2-savetofile-method-dao.md)** method</span></span>

<span data-ttu-id="c5dc2-114">Para se referir a um objeto **Field2** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:</span><span class="sxs-lookup"><span data-stu-id="c5dc2-114">To refer to a **Field2** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="c5dc2-115">**Fields**(0)</span><span class="sxs-lookup"><span data-stu-id="c5dc2-115">**Fields**(0)</span></span>

<span data-ttu-id="c5dc2-116">**Campos** ("nome")</span><span class="sxs-lookup"><span data-stu-id="c5dc2-116">**Fields**("name")</span></span>

<span data-ttu-id="c5dc2-117">**Campos**\!\[nome\]</span><span class="sxs-lookup"><span data-stu-id="c5dc2-117">**Fields**\!\[name\]</span></span>

<span data-ttu-id="c5dc2-p102">Com as mesmas formas de sintaxe, você também pode se referir à propriedade **Value** de um objeto **Field2** criado e acrescentado à coleção **Fields**. O contexto da referência de campo determinará se você está se referindo ao objeto **Field2** ou à propriedade **Value** do objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-p102">With the same syntax forms, you can also refer to the **Value** property of a **Field2** object that you create and append to a **Fields** collection. The context of the field reference will determine whether you are referring to the **Field2** object or the **Value** property of the **Field** object.</span></span>

## <a name="example"></a><span data-ttu-id="c5dc2-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c5dc2-120">Example</span></span>

<span data-ttu-id="c5dc2-121">O exemplo a seguir mostra como navegar entre um Recordset que contém um campo de valor múltiplos.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-121">The following example shows how to navigate a Recordset that contains a multi-value field.</span></span>

<span data-ttu-id="c5dc2-122">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="c5dc2-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<br/>

<span data-ttu-id="c5dc2-123">O exemplo a seguir mostra como navegar entre os arquivos em um campo de anexo.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-123">The following example shows how to navigate the files in an attachment field.</span></span> <span data-ttu-id="c5dc2-124">O tipo de arquivo e o nome do arquivo de cada anexo é impresso na janela Immediate.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-124">The file type and filename of each attachment is printed in the Immediate window.</span></span>

```vb
    Sub ListAttachments()
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld As DAO.Field2
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Print the first and last name
            Debug.Print rst("FirstName") & " " & rst("LastName")
            
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Print all attachments in the field
            Do While Not rsA.EOF
                Debug.Print , rsA("FileType"), rsA("FileName")
                
                'Next attachment
                rsA.MoveNext
            Loop
            
            rsA.Close
            
            'Next record
            rst.MoveNext
        Loop
        
            
        rst.Close
        dbs.Close
        
        Set fld = Nothing
        Set rsA = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Sub
```

<br/>

<span data-ttu-id="c5dc2-125">O exemplo a seguir mostra como adicionar arquivos de um caminho de pasta especificado para um campo de anexo.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-125">The following example shows how to add files from a specified folder path to an attachment field.</span></span>

```vb
    Public Function LoadAttachments(strPath As String, Optional strPattern As String = "*.*") As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld  As DAO.Field2
        Dim strFile As String
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Load all attachments in the specified directory
            strFile = Dir(strPath & "\*.*")
            
            rst.Edit
            Do While Len(strFile) > 0
                'Add a new attachment that matches the pattern.
                'Pass "" to match all files.
                If strFile Like strPattern Then
                    rsA.AddNew
                    rsA("FileData").LoadFromFile strPath & "\" & strFile
                    rsA.Update
                    
                    'Increment the number of files added
                    LoadAttachments = LoadAttachments + 1
                End If
                strFile = Dir
            Loop
            rsA.Close
            
            rst.Update
            'Next record
            rst.MoveNext
        Loop
        
        rst.Close
        dbs.Close
        
        Set fld = Nothing
        Set rsA = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Function
```

<br/>

<span data-ttu-id="c5dc2-126">O exemplo a seguir mostra como salvar os arquivos armazenados em um campo de anexo no caminho da pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-126">The following example shows how to save the files stored in an attachment field to the specified folder path.</span></span>

```vb
    Public Function SaveAttachments(strPath As String, Optional strPattern As String = "*.*") As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld As DAO.Field2
        Dim strFullPath As String
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Save all attachments in the field
            Do While Not rsA.EOF
                If rsA("FileName") Like strPattern Then
                    strFullPath = strPath & "\" & rsA("FileName")
                    
                    'Make sure the file does not exist and save
                    If Dir(strFullPath) = "" Then
                        rsA("FileData").SaveToFile strFullPath
                    End If
                    
                    'Increment the number of files saved
                    SaveAttachments = SaveAttachments + 1
                End If
                
                'Next attachment
                rsA.MoveNext
            Loop
            rsA.Close
            
            'Next record
            rst.MoveNext
        Loop
        
        rst.Close
        dbs.Close
        
        Set fld = Nothing
        Set rsA = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Function
```

<br/>

<span data-ttu-id="c5dc2-127">O exemplo a seguir mostra como excluir um arquivo armazenado em um campo de anexo.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-127">The following example shows how to delete a file stored in an attachment field.</span></span>

```vb
    Function RemoveAttachment(strRemoveFile As String, Optional strFilter As String) As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld As DAO.Field2
        
        'Get the database
        Set dbs = CurrentDb
        
        'Open the recordset. If the strFilter is supplied, add it to the WHERE
        'clause for the recordset. Otherwise, any files matching strFileName
        'will be deleted
        If Len(strFilter) > 0 Then
            Set rst = dbs.OpenRecordset("SELECT * FROM tblAttachments WHERE " & strFilter)
        Else
            Set rst = dbs.OpenRecordset("tblAttachments")
        End If
        
        'Get the Attachment field
        Set fld = rst("Attachments")
        
        'Navigate through the recordset
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Walk the attachments and look for the file name to remove
            Do While Not rsA.EOF
                If rsA("FileName") Like strRemoveFile Then
                    rsA.Delete
                    
                    'Increment the number of files removed
                    RemoveAttachment = RemoveAttachment + 1
                End If
                rsA.MoveNext
            Loop
                    
            'Cleanup the Attachments recordset
            rsA.Close
            Set rsA = Nothing
            
            'Next record
            rst.MoveNext
        Loop
        
        rst.Close
        dbs.Close
        Set fld = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Function
```
