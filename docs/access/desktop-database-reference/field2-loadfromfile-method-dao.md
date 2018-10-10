---
title: Método Field2.LoadFromFile (DAO)
TOCTitle: LoadFromFile Method
ms:assetid: 8ffe4636-d4da-0579-f4b5-14f423647562
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197396(v=office.15)
ms:contentKeyID: 48546314
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101190
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c7780520f70b418b8fa6865ef3b85f50be132ee7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462932"
---
# <a name="field2loadfromfile-method-dao"></a><span data-ttu-id="1c4aa-102">Método Field2.LoadFromFile (DAO)</span><span class="sxs-lookup"><span data-stu-id="1c4aa-102">Field2.LoadFromFile Method (DAO)</span></span>

<span data-ttu-id="1c4aa-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c4aa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1c4aa-104">Carrega o arquivo especificado do disco.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-104">Loads the specified file from disk.</span></span>

## <a name="version-information"></a><span data-ttu-id="1c4aa-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="1c4aa-105">Version Information</span></span>

<span data-ttu-id="1c4aa-106">Version Added: Access 2007</span><span class="sxs-lookup"><span data-stu-id="1c4aa-106">Version Added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="1c4aa-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c4aa-107">Syntax</span></span>

<span data-ttu-id="1c4aa-108">*expressão* . LoadFromFile (***FileName***)</span><span class="sxs-lookup"><span data-stu-id="1c4aa-108">*expression* .LoadFromFile(***FileName***)</span></span>

<span data-ttu-id="1c4aa-109">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="1c4aa-109">*expression* A variable that represents a **Field2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="1c4aa-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c4aa-110">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c4aa-111">Nome</span><span class="sxs-lookup"><span data-stu-id="1c4aa-111">Name</span></span></p></th>
<th><p><span data-ttu-id="1c4aa-112">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="1c4aa-112">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="1c4aa-113">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1c4aa-113">Data Type</span></span></p></th>
<th><p><span data-ttu-id="1c4aa-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c4aa-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c4aa-115">FileName</span><span class="sxs-lookup"><span data-stu-id="1c4aa-115">FileName</span></span></p></td>
<td><p><span data-ttu-id="1c4aa-116">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1c4aa-116">Required</span></span></p></td>
<td><p><span data-ttu-id="1c4aa-117"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="1c4aa-117"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1c4aa-118">O caminho totalmente qualificado do arquivo a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-118">The fully qualified path of the file to that you want to load.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="1c4aa-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1c4aa-119">Example</span></span>

<span data-ttu-id="1c4aa-120">O trecho de código a seguir usa o método **LoadFromFile** para carregar a foto de um funcionário do disco.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-120">The following code snippet uses the **LoadFromFile** method to load an employee's picture from disk.</span></span>

```vb 
   '  Instantiate the parent recordset.  
   Set rsEmployees = db.OpenRecordset("Employees") 
  
   … Code to move to desired employee 
  
   ' Activate edit mode. 
   rsEmployees.Edit 
  
   ' Instantiate the child recordset. 
   Set rsPictures = rsEmployees.Fields("Pictures").Value  
  
   ' Add a new attachment. 
   rsPictures.AddNew 
   rsPictures.Fields("FileData").LoadFromFile "EmpPhoto39392.jpg" 
   rsPictures.Update 
  
   ' Update the parent record 
   rsEmployees.Update 
```

<br/>

<span data-ttu-id="1c4aa-121">O exemplo a seguir mostra como adicionar arquivos de um caminho de pasta especificado para um campo de anexo.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-121">The following example shows how to add files from a specified folder path to an attachment field.</span></span>

<span data-ttu-id="1c4aa-122">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="1c4aa-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
