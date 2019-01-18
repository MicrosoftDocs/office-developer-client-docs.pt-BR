---
title: Método Field2.SaveToFile (DAO)
TOCTitle: SaveToFile Method
ms:assetid: 250f9596-1a03-471d-96f9-718cd57dc94f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191852(v=office.15)
ms:contentKeyID: 48543776
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101191
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 78b08575b1fde304dc47b8219c1143cda265baf8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706979"
---
# <a name="field2savetofile-method-dao"></a><span data-ttu-id="d5b51-102">Método Field2.SaveToFile (DAO)</span><span class="sxs-lookup"><span data-stu-id="d5b51-102">Field2.SaveToFile method (DAO)</span></span>

<span data-ttu-id="d5b51-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d5b51-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d5b51-104">Salva um anexo no disco.</span><span class="sxs-lookup"><span data-stu-id="d5b51-104">Saves an attachment to disk.</span></span>

## <a name="version-information"></a><span data-ttu-id="d5b51-105">Version information</span><span class="sxs-lookup"><span data-stu-id="d5b51-105">Version information</span></span>

<span data-ttu-id="d5b51-106">Versão adicionada: Access 2007</span><span class="sxs-lookup"><span data-stu-id="d5b51-106">Version added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="d5b51-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5b51-107">Syntax</span></span>

<span data-ttu-id="d5b51-108">*expressão* . SaveToFile (***FileName***)</span><span class="sxs-lookup"><span data-stu-id="d5b51-108">*expression* .SaveToFile(***FileName***)</span></span>

<span data-ttu-id="d5b51-109">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="d5b51-109">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5b51-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5b51-110">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d5b51-111">Nome</span><span class="sxs-lookup"><span data-stu-id="d5b51-111">Name</span></span></p></th>
<th><p><span data-ttu-id="d5b51-112">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="d5b51-112">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="d5b51-113">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d5b51-113">Data type</span></span></p></th>
<th><p><span data-ttu-id="d5b51-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5b51-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5b51-115"><em>FileName</em></span><span class="sxs-lookup"><span data-stu-id="d5b51-115"><em>FileName</em></span></span></p></td>
<td><p><span data-ttu-id="d5b51-116">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d5b51-116">Required</span></span></p></td>
<td><p><span data-ttu-id="d5b51-117"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="d5b51-117"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="d5b51-118">O caminho totalmente qualificado do arquivo no qual deseja salvar o anexo.</span><span class="sxs-lookup"><span data-stu-id="d5b51-118">The fully qualified path of the file to which you want to save the attachment.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="d5b51-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d5b51-119">Example</span></span>

<span data-ttu-id="d5b51-120">O trecho de código a seguir ilustra como usar o método **SaveToFile** para salvar todos os anexos de um funcionário específico no disco.</span><span class="sxs-lookup"><span data-stu-id="d5b51-120">The following code snippet illustrates how to use the **SaveToFile** method to save all of the attachments for a specific employee to disk.</span></span>

```vb
    '  Instantiate the parent recordset.  
       Set rsEmployees = db.OpenRecordset("Employees") 
      
       … Code to move to desired employee 
      
       ' Instantiate the child recordset. 
       Set rsPictures = rsEmployees.Fields("Pictures").Value  
     
       '  Loop through the attachments. 
       While Not rsPictures.EOF 
      
          '  Save current attachment to disk in the "My Documents" folder. 
          rsPictures.Fields("FileData").SaveToFile _ 
                      "C:\Documents and Settings\Username\My Documents" 
          rsPictures.MoveNext 
       Wend 
```

<br/>

<span data-ttu-id="d5b51-121">O exemplo a seguir mostra como salvar os arquivos armazenados em um campo de anexo no caminho da pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="d5b51-121">The following example shows how to save the files stored in an attachment field to the specified folder path.</span></span>

<span data-ttu-id="d5b51-122">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="d5b51-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
