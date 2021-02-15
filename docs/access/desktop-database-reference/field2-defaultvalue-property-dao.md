---
title: Propriedade Field2.DefaultValue (DAO)
TOCTitle: DefaultValue Property
ms:assetid: 709c9580-520e-46ce-7d70-e409872184bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195744(v=office.15)
ms:contentKeyID: 48545563
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053121
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 845a2e0c7ffa5d54d73c4fcec1a6c785468d734e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292829"
---
# <a name="field2defaultvalue-property-dao"></a><span data-ttu-id="80062-102">Propriedade Field2.DefaultValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="80062-102">Field2.DefaultValue property (DAO)</span></span>

<span data-ttu-id="80062-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80062-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80062-p101">Define ou retorna o valor padrão de um objeto **Field2**. Para um objeto **Field2** ainda não acrescentado à coleção **[Fields](fields-collection-dao.md)**, essa propriedade é de leitura/gravação (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="80062-p101">Sets or returns the default value of a **Field2** object. For a **Field2** object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="80062-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80062-106">Syntax</span></span>

<span data-ttu-id="80062-107">*expressão* . DefaultValue</span><span class="sxs-lookup"><span data-stu-id="80062-107">*expression* .DefaultValue</span></span>

<span data-ttu-id="80062-108">*expressão* Uma variável que representa um objeto **Field2**.</span><span class="sxs-lookup"><span data-stu-id="80062-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="80062-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="80062-109">Remarks</span></span>

<span data-ttu-id="80062-p102">A configuração ou o valor de retorno é um tipo de dados **String** que pode conter no máximo 255 caracteres. Ele pode conter texto ou uma expressão. Se a configuração da propriedade for uma expressão, ela não poderá conter funções definidas pelo usuário, funções agregadas do mecanismo de banco de dados do Microsoft Access SQL ou referência a consultas, formulários ou outros objetos **Field2**.</span><span class="sxs-lookup"><span data-stu-id="80062-p102">The setting or return value is a **String** data type that can contain a maximum of 255 characters. It can be either text or an expression. If the property setting is an expression, it can't contain user-defined functions, Microsoft Access database engine SQL aggregate functions, or references to queries, forms, or other **Field2** objects.</span></span>

> [!NOTE]
> <span data-ttu-id="80062-p103">[!OBSERVAçãO] Você também pode definir a propriedade **DefaultValue** de um objeto **Field2** em um objeto **TableDef** para um valor especial chamado "GenUniqueID( )". Isso faz com que um número aleatório seja atribuído a esse campo sempre que um novo registro é adicionado ou criado, fornecendo a cada registro um identificador exclusivo. A propriedade **Type** do campo de ver **Long**.</span><span class="sxs-lookup"><span data-stu-id="80062-p103">You can also set the **DefaultValue** property of a **Field2** object on a **TableDef** object to a special value called "GenUniqueID( )". This causes a random number to be assigned to this field whenever a new record is added or created, thereby giving each record a unique identifier. The field's **Type** property must be **Long**.</span></span>

<span data-ttu-id="80062-116">A disponibilidade da propriedade **DefaultValue** depende do objeto que contém a coleção **Fields**, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="80062-116">The availability of the **DefaultValue** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80062-117">Se a coleção Fields pertencer a</span><span class="sxs-lookup"><span data-stu-id="80062-117">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="80062-118">DefaultValue será</span><span class="sxs-lookup"><span data-stu-id="80062-118">Then DefaultValue is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80062-119">Objeto Index</span><span class="sxs-lookup"><span data-stu-id="80062-119">Index object</span></span></p></td>
<td><p><span data-ttu-id="80062-120">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="80062-120">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80062-121">Objeto QueryDef</span><span class="sxs-lookup"><span data-stu-id="80062-121">QueryDef object</span></span></p></td>
<td><p><span data-ttu-id="80062-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="80062-122">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80062-123">Objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="80062-123">Recordset object</span></span></p></td>
<td><p><span data-ttu-id="80062-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="80062-124">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80062-125">Objeto Relation</span><span class="sxs-lookup"><span data-stu-id="80062-125">Relation object</span></span></p></td>
<td><p><span data-ttu-id="80062-126">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="80062-126">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80062-127">Objeto TableDef</span><span class="sxs-lookup"><span data-stu-id="80062-127">TableDef object</span></span></p></td>
<td><p><span data-ttu-id="80062-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="80062-128">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="80062-p104">Quando um novo registro é criado, a configuração da propriedade **DefaultValue** é automaticamente inserida como o valor para o campo. Você pode alterar o valor de campo definindo sua propriedade **Value**.</span><span class="sxs-lookup"><span data-stu-id="80062-p104">When a new record is created, the **DefaultValue** property setting is automatically entered as the value for the field. You can change the field value by setting its **Value** property.</span></span>

<span data-ttu-id="80062-131">A propriedade **DefaultValue** não se aplica aos campos **AutoNumber** e **Long Binary**.</span><span class="sxs-lookup"><span data-stu-id="80062-131">The **DefaultValue** property doesn't apply to **AutoNumber** and **Long Binary** fields.</span></span>

## <a name="example"></a><span data-ttu-id="80062-132">Exemplo</span><span class="sxs-lookup"><span data-stu-id="80062-132">Example</span></span>

<span data-ttu-id="80062-p105">Este exemplo usa a propriedade **DefaultValue** para alertar o usuário de um valor normal de campo durante a solicitação de entrada. Além disso, ele demonstra como os novos registros serão preenchidos utilizando o **DefaultValue** na ausência de qualquer outra entrada. A função DefaultPrompt é exigida para que este procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="80062-p105">This example uses the **DefaultValue** property to alert the user of a field's normal value while prompting for input. In addition, it demonstrates how new records will be filled using **DefaultValue** in the absence of any other input. The DefaultPrompt function is required for this procedure to run.</span></span>

```vb
    Sub DefaultValueX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim strOldDefault As String 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strCode As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Store original DefaultValue information and set the 
     ' property to a new value. 
     strOldDefault = _ 
     tdfEmployees.Fields!PostalCode.DefaultValue 
     tdfEmployees.Fields!PostalCode.DefaultValue = "98052" 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Add a new record to the Recordset. 
     .AddNew 
     !FirstName = "Bruce" 
     !LastName = "Oberg" 
     
     ' Get user input. If user enters something, the field 
     ' will be filled with that data; otherwise, it will be 
     ' filled with the DefaultValue information. 
     strMessage = "Enter postal code for " & vbCr & _ 
     !FirstName & " " & !LastName & ":" 
     strCode = DefaultPrompt(strMessage, !PostalCode) 
     If strCode <> "" Then !PostalCode = strCode 
     .Update 
     
     ' Go to new record and print information. 
     .Bookmark = .LastModified 
     Debug.Print " FirstName = " & !FirstName 
     Debug.Print " LastName = " & !LastName 
     Debug.Print " PostalCode = " & !PostalCode 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     ' Restore original DefaultValue property because this is a 
     ' demonstration. 
     tdfEmployees.Fields!PostalCode.DefaultValue = _ 
     strOldDefault 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function DefaultPrompt(strPrompt As String, _ 
     fldTemp As Field2) As String 
     
     Dim strFullPrompt As String 
     
     ' Ask user for new DefaultValue setting for the specified 
     ' Field object. 
     strFullPrompt = strPrompt & vbCr & _ 
     "[Default = " & fldTemp.DefaultValue & _ 
     ", Cancel - use default]" 
     DefaultPrompt = InputBox(strFullPrompt) 
     
    End Function
```
