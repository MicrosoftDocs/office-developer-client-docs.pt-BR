---
title: Método Database.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: f2039be9-5fd8-f673-dfbf-0a71540cdc98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836607(v=office.15)
ms:contentKeyID: 48548638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f966e041a6d2aff773f6c3849c0846ef362d1142
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294971"
---
# <a name="databasecreateproperty-method-dao"></a><span data-ttu-id="ab954-102">Método Database.CreateProperty (DAO)</span><span class="sxs-lookup"><span data-stu-id="ab954-102">Database.CreateProperty method (DAO)</span></span>

<span data-ttu-id="ab954-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab954-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab954-104">Cria um novo objeto **[Property](property-object-dao.md)** definido pelo usuário (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="ab954-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="ab954-105">.</span><span class="sxs-lookup"><span data-stu-id="ab954-105">.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab954-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab954-106">Syntax</span></span>

<span data-ttu-id="ab954-107">*expressão* . CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="ab954-107">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="ab954-108">*expressão* Uma variável que representa um objeto do **Banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="ab954-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ab954-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab954-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab954-110">Nome</span><span class="sxs-lookup"><span data-stu-id="ab954-110">Name</span></span></p></th>
<th><p><span data-ttu-id="ab954-111">Necessária/opcional</span><span class="sxs-lookup"><span data-stu-id="ab954-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="ab954-112">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ab954-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="ab954-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab954-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab954-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="ab954-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="ab954-115">Opcional</span><span class="sxs-lookup"><span data-stu-id="ab954-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="ab954-116"><strong>Variantes</strong></span><span class="sxs-lookup"><span data-stu-id="ab954-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ab954-117">Uma <strong>String</strong> que denomina exclusivamente o novo objeto <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab954-117">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object.</span></span> <span data-ttu-id="ab954-118">Consulte a propriedade <strong>Name</strong> para obter detalhes sobre nomes válidos de <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab954-118">See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab954-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="ab954-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="ab954-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="ab954-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="ab954-121"><strong>Variantes</strong></span><span class="sxs-lookup"><span data-stu-id="ab954-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ab954-122">Uma constante que define o tipo de dados do novo objeto <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab954-122">A constant that defines the data type of the new <strong>Property</strong> object.</span></span> <span data-ttu-id="ab954-123">Consulte a propriedade <strong><a href="field-type-property-dao.md">Type</a></strong> para obter tipos de dados válidos.</span><span class="sxs-lookup"><span data-stu-id="ab954-123">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab954-124"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="ab954-124"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="ab954-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="ab954-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="ab954-126"><strong>Variantes</strong></span><span class="sxs-lookup"><span data-stu-id="ab954-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ab954-127">Um <strong>Variant</strong> que contém o valor inicial da propriedade.</span><span class="sxs-lookup"><span data-stu-id="ab954-127">A <strong>Variant</strong> containing the initial property value.</span></span> <span data-ttu-id="ab954-128">Consulte a <strong><a href="field-value-property-dao.md">propriedade Value</a></strong> para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="ab954-128">See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab954-129"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="ab954-129"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="ab954-130">Opcional</span><span class="sxs-lookup"><span data-stu-id="ab954-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="ab954-131"><strong>Variantes</strong></span><span class="sxs-lookup"><span data-stu-id="ab954-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ab954-132">Um <strong>Variant</strong> (subtipo <strong>Boolean</strong>) que indica se <strong>Property</strong> é ou não um objeto DDL.</span><span class="sxs-lookup"><span data-stu-id="ab954-132">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="ab954-133">O padrão é False.</span><span class="sxs-lookup"><span data-stu-id="ab954-133">The default is False.</span></span> <span data-ttu-id="ab954-134">Se DDL for True, os usuários não poderão alterar ou excluir esse objeto <strong>Property,</strong> a menos que tenham permissão dbSecWriteDef.</span><span class="sxs-lookup"><span data-stu-id="ab954-134">If DDL is True, users can't change or delete this <strong>Property</strong> object unless they have dbSecWriteDef permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="ab954-135">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ab954-135">Return value</span></span>

<span data-ttu-id="ab954-136">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ab954-136">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="ab954-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab954-137">Remarks</span></span>

<span data-ttu-id="ab954-138">Você pode criar um objeto **Property** definido pelo usuário na coleção **[Properties](properties-collection-dao.md)** de um objeto que é persistente.</span><span class="sxs-lookup"><span data-stu-id="ab954-138">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="ab954-p106">Se você omitir uma ou mais das partes opcionais ao utilizar **CreateProperty**, poderá usar uma instruções de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto a uma coleção. Depois de acrescentar o objeto, você poderá alterar algumas, mas não todas, as configurações de propriedade. Consulte os tópicos de propriedade **Name**, **Type** e **Value** para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="ab954-p106">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="ab954-142">Se o nome se referir a um objeto que já é membro da coleção, ocorrerá um erro em tempo de executar quando você usar o **[método Append.](fields-append-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="ab954-142">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="ab954-143">Para remover um objeto **Property** definido pelo usuário da coleção, use o método **[Delete](fields-delete-method-dao.md)** na coleção **Properties**.</span><span class="sxs-lookup"><span data-stu-id="ab954-143">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection.</span></span> <span data-ttu-id="ab954-144">Não é possível excluir propriedades internas.</span><span class="sxs-lookup"><span data-stu-id="ab954-144">You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="ab954-145">Se você omitir o argumento DDL, ele será o padrão para False (não-DDL).</span><span class="sxs-lookup"><span data-stu-id="ab954-145">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="ab954-146">Como nenhuma propriedade DDL correspondente está exposta, você deve excluir e recriar o objeto **Property** que deseja alterar de DDL para não-DDL.</span><span class="sxs-lookup"><span data-stu-id="ab954-146">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


## <a name="example"></a><span data-ttu-id="ab954-147">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ab954-147">Example</span></span>

<span data-ttu-id="ab954-p109">Este exemplo tenta definir o valor de uma propriedade definida pelo usuário. Se a propriedade não existir, será usado o método **CreateProperty** para criar e definir o valor da nova propriedade. O procedimento SetProperty é exigido para a execução deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="ab954-p109">This example tries to set the value of a user-defined property. If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property. The SetProperty procedure is required for this procedure to run.</span></span>

```vb
    Sub CreatePropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Set the Archive property to True. 
       SetProperty dbsNorthwind, "Archive", True 
        
       With dbsNorthwind 
          Debug.Print "Properties of " & .Name 
           
          ' Enumerate Properties collection of the Northwind  
          ' database. 
          For Each prpLoop In .Properties 
             If prpLoop <> "" Then Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
          Next prpLoop 
     
          ' Delete the new property since this is a  
          ' demonstration. 
          .Properties.Delete "Archive" 
     
          .Close 
       End With 
     
    End Sub 
     
    Sub SetProperty(dbsTemp As Database, strName As String, _ 
       booTemp As Boolean) 
     
       Dim prpNew As Property 
       Dim errLoop As Error 
     
       ' Attempt to set the specified property. 
       On Error GoTo Err_Property 
       dbsTemp.Properties("strName") = booTemp 
       On Error GoTo 0 
     
       Exit Sub 
     
    Err_Property: 
     
       ' Error 3270 means that the property was not found. 
       If DBEngine.Errors(0).Number = 3270 Then 
          ' Create property, set its value, and append it to the  
          ' Properties collection. 
          Set prpNew = dbsTemp.CreateProperty(strName, _ 
             dbBoolean, booTemp) 
          dbsTemp.Properties.Append prpNew 
          Resume Next 
       Else 
          ' If different error has occurred, display message. 
          For Each errLoop In DBEngine.Errors 
             MsgBox "Error number: " & errLoop.Number & vbCr & _ 
                errLoop.Description 
          Next errLoop 
          End 
       End If 
     
    End Sub
```
