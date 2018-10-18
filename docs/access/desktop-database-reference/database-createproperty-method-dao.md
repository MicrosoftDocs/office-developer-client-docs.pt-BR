---
title: Método Database.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: f2039be9-5fd8-f673-dfbf-0a71540cdc98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836607(v=office.15)
ms:contentKeyID: 48548638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8da9145d41a2ae973e8d310d1286f3d7ed2594e
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602143"
---
# <a name="databasecreateproperty-method-dao"></a><span data-ttu-id="93d6a-102">Método Database.CreateProperty (DAO)</span><span class="sxs-lookup"><span data-stu-id="93d6a-102">Database.CreateProperty Method (DAO)</span></span>


<span data-ttu-id="93d6a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="93d6a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="93d6a-p101">Cria um novo objeto **[Property](property-object-dao.md)** definido pelo usuário (apenas espaços de trabalho do Microsoft Access). .</span><span class="sxs-lookup"><span data-stu-id="93d6a-p101">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="93d6a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93d6a-106">Syntax</span></span>

<span data-ttu-id="93d6a-107">*expressão* . CreateProperty (***nome***, ***tipo***, ***valor***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="93d6a-107">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="93d6a-108">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="93d6a-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="93d6a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93d6a-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93d6a-110">Nome</span><span class="sxs-lookup"><span data-stu-id="93d6a-110">Name</span></span></p></th>
<th><p><span data-ttu-id="93d6a-111">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="93d6a-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="93d6a-112">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="93d6a-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="93d6a-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="93d6a-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93d6a-114">Name</span><span class="sxs-lookup"><span data-stu-id="93d6a-114">Name</span></span></p></td>
<td><p><span data-ttu-id="93d6a-115">Opcional</span><span class="sxs-lookup"><span data-stu-id="93d6a-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="93d6a-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="93d6a-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="93d6a-p102">Uma <strong>String</strong> que denomina exclusivamente o novo objeto <strong>Property</strong>. Consulte a propriedade <strong>Name</strong> para obter detalhes sobre nomes válidos de <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="93d6a-p102">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93d6a-119">Type</span><span class="sxs-lookup"><span data-stu-id="93d6a-119">Type</span></span></p></td>
<td><p><span data-ttu-id="93d6a-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="93d6a-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="93d6a-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="93d6a-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="93d6a-p103">Uma constante que define o tipo de dados do novo objeto <strong>Property</strong>. Consulte a propriedade <strong><a href="field-type-property-dao.md">Type</a></strong> para obter tipos de dados válidos.</span><span class="sxs-lookup"><span data-stu-id="93d6a-p103">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93d6a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="93d6a-124">Value</span></span></p></td>
<td><p><span data-ttu-id="93d6a-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="93d6a-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="93d6a-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="93d6a-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="93d6a-p104">Um <strong>Variant</strong> que contém o valor inicial da propriedade. Consulte a propriedade <strong><a href="field-value-property-dao.md">Value</a></strong> para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="93d6a-p104">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93d6a-129">DDL</span><span class="sxs-lookup"><span data-stu-id="93d6a-129">DDL</span></span></p></td>
<td><p><span data-ttu-id="93d6a-130">Opcional</span><span class="sxs-lookup"><span data-stu-id="93d6a-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="93d6a-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="93d6a-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="93d6a-132">Um <strong>Variant</strong> (subtipo<strong>booleano</strong> ) que indica se é ou não a <strong>propriedade</strong> de um objeto DDL.</span><span class="sxs-lookup"><span data-stu-id="93d6a-132">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="93d6a-133">O padrão é False.</span><span class="sxs-lookup"><span data-stu-id="93d6a-133">The default is False.</span></span> <span data-ttu-id="93d6a-134">Se DDL for True, os usuários não podem alterar ou excluir esse objeto de <strong>propriedade</strong> , a menos que tenham permissão dbSecWriteDef.</span><span class="sxs-lookup"><span data-stu-id="93d6a-134">If DDL is True, users can't change or delete this <strong>Property</strong> object unless they have dbSecWriteDef permission.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93d6a-135"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="93d6a-135"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="93d6a-136">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="93d6a-136">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="93d6a-137">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="93d6a-137">Return value</span></span>
>>>>>>> <span data-ttu-id="93d6a-138">mestre</span><span class="sxs-lookup"><span data-stu-id="93d6a-138">master</span></span>

<span data-ttu-id="93d6a-139">Propriedade</span><span class="sxs-lookup"><span data-stu-id="93d6a-139">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="93d6a-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="93d6a-140">Remarks</span></span>

<span data-ttu-id="93d6a-141">Você pode criar um objeto **Property** definido pelo usuário somente na coleção **[Properties](properties-collection-dao.md)** de um objeto que é persistente.</span><span class="sxs-lookup"><span data-stu-id="93d6a-141">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="93d6a-p106">Se omitir uma ou mais dessas partes opcionais quando usar **CreateProperty**, você poderá usar uma instrução de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto à coleção. Depois de acrescentar o objeto, você poderá alterar algumas, mas não todas as configurações de propriedade. Consulte os tópicos de propriedade de **Name**, **Type** e **Value** para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="93d6a-p106">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="93d6a-145">Se name fizer referência a um objeto que já é um membro da coleção, ocorrerá um erro de tempo de execução quando você usa o método **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="93d6a-145">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="93d6a-p107">Para remover um objeto **Property** definido pelo usuário da coleção, use o método **[Delete](fields-delete-method-dao.md)** na coleção **Properties**. Não é possível excluir propriedades internas.</span><span class="sxs-lookup"><span data-stu-id="93d6a-p107">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection. You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="93d6a-148">Se você omitir o argumento DDL, o padrão é False (não-DDL).</span><span class="sxs-lookup"><span data-stu-id="93d6a-148">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="93d6a-149">Como nenhuma propriedade DDL correspondente está exposta, você deve excluir e recriar um objeto **Property** que deseja alterar de DDL para não-DDL.</span><span class="sxs-lookup"><span data-stu-id="93d6a-149">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


## <a name="example"></a><span data-ttu-id="93d6a-150">Exemplo</span><span class="sxs-lookup"><span data-stu-id="93d6a-150">Example</span></span>

<span data-ttu-id="93d6a-p109">Este exemplo tenta definir o valor de uma propriedade definida pelo usuário. Se a propriedade não existir, ele usará o método **CreateProperty** para criar e definir o valor da nova propriedade. O procedimento SetProperty é exigido para a execução deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="93d6a-p109">This example tries to set the value of a user-defined property. If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property. The SetProperty procedure is required for this procedure to run.</span></span>

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
