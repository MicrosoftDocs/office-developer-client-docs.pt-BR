---
title: Propriedade Field. AllowZeroLength (DAO)
TOCTitle: AllowZeroLength Property
ms:assetid: 5103a905-9258-e088-0210-857372f41c3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193832(v=office.15)
ms:contentKeyID: 48544807
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052962
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f1eb08c6079257a350a5bb92392871869e720f1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293158"
---
# <a name="fieldallowzerolength-property-dao"></a><span data-ttu-id="26e92-102">Propriedade Field. AllowZeroLength (DAO)</span><span class="sxs-lookup"><span data-stu-id="26e92-102">Field.AllowZeroLength property (DAO)</span></span>

<span data-ttu-id="26e92-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="26e92-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26e92-104">Define ou retorna um valor que indica que a sequência de comprimento zero ("") é uma configuração válida para a propriedade **[Value](field-value-property-dao.md)** do objeto **[Field](field-object-dao.md)** com um tipo de dados Texto ou Memorando (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="26e92-104">Sets or returns a value that indicates whether a zero-length string ("") is a valid setting for the **[Value](field-value-property-dao.md)** property of the **[Field](field-object-dao.md)** object with a Text or Memo data type (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="26e92-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26e92-105">Syntax</span></span>

<span data-ttu-id="26e92-106">*expressão* . AllowZeroLength</span><span class="sxs-lookup"><span data-stu-id="26e92-106">*expression* .AllowZeroLength</span></span>

<span data-ttu-id="26e92-107">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="26e92-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="26e92-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="26e92-108">Remarks</span></span>

<span data-ttu-id="26e92-109">Para um objeto ainda não acrescentado à coleção **Fields**, essa propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="26e92-109">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="26e92-110">Depois de acrescentado a uma coleção **Fields**, a disponibilidade da propriedade **AllowZeroLength** depende do objeto que contém a coleção **Fields**, como mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="26e92-110">Once appended to a **Fields** collection, the availability of the **AllowZeroLength** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26e92-111">Se a coleção Fields pertencer a</span><span class="sxs-lookup"><span data-stu-id="26e92-111">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="26e92-112">AllowZeroLength será</span><span class="sxs-lookup"><span data-stu-id="26e92-112">Then AllowZeroLength is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26e92-113">
						Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="26e92-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="26e92-114">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="26e92-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26e92-115">
						Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="26e92-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="26e92-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="26e92-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26e92-117">
						Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="26e92-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="26e92-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="26e92-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26e92-119">
						Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="26e92-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="26e92-120">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="26e92-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26e92-121">
						Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="26e92-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="26e92-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="26e92-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="26e92-123">Você pode usar essa propriedade junto com a propriedade **[Required](field-required-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)** ou **[ValidationRule](field-validationrule-property-dao.md)** para validar um valor em um campo.</span><span class="sxs-lookup"><span data-stu-id="26e92-123">You can use this property along with the **[Required](field-required-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to validate a value in a field.</span></span>

## <a name="example"></a><span data-ttu-id="26e92-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="26e92-124">Example</span></span>

<span data-ttu-id="26e92-p101">Neste exemplo, a propriedade **AllowZeroLength** permite que o usuário defina o valor de um **Field** para uma sequência vazia. Nessa situação, o usuário pode distinguir entre um registro em que os dados são desconhecidos e um registro em que dos dados não se aplicam.</span><span class="sxs-lookup"><span data-stu-id="26e92-p101">In this example, the **AllowZeroLength** property allows the user to set the value of a **Field** to an empty string. In this situation, the user can distinguish between a record where data is not known and a record where the data does not apply.</span></span>

```vb
    Sub AllowZeroLengthX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldTemp As Field 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strInput As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     ' Create a new Field object and append it to the Fields 
     ' collection of the Employees table. 
     Set fldTemp = tdfEmployees.CreateField("FaxPhone", _ 
     dbText, 24) 
     fldTemp.AllowZeroLength = True 
     tdfEmployees.Fields.Append fldTemp 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Get user input. 
     .Edit 
     strMessage = "Enter fax number for " & _ 
     !FirstName & " " & !LastName & "." & vbCr & _ 
     "[? - unknown, X - has no fax]" 
     strInput = UCase(InputBox(strMessage)) 
     If strInput <> "" Then 
     Select Case strInput 
     Case "?" 
     !FaxPhone = Null 
     Case "X" 
     !FaxPhone = "" 
     Case Else 
     !FaxPhone = strInput 
     End Select 
     
     .Update 
     
     ' Print report. 
     Debug.Print "Name - Fax number" 
     Debug.Print !FirstName & " " & !LastName & " - "; 
     
     If IsNull(!FaxPhone) Then 
     Debug.Print "[Unknown]" 
     Else 
     If !FaxPhone = "" Then 
     Debug.Print "[Has no fax]" 
     Else 
     Debug.Print !FaxPhone 
     End If 
     End If 
     
     Else 
     .CancelUpdate 
     End If 
     
     .Close 
     End With 
     
     ' Delete new field because this is a demonstration. 
     tdfEmployees.Fields.Delete fldTemp.Name 
     dbsNorthwind.Close 
     
    End Sub
```
