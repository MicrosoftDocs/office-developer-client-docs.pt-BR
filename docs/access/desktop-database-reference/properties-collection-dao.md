---
title: Coleção Properties (DAO)
TOCTitle: Properties collection
ms:assetid: cd07184a-a261-29c9-542f-bc2eff6f4af6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834455(v=office.15)
ms:contentKeyID: 48547753
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 515d28f0d7d99359c36df79cf3b8769d8f71e06d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301278"
---
# <a name="properties-collection-dao"></a><span data-ttu-id="45f76-102">Coleção Properties (DAO)</span><span class="sxs-lookup"><span data-stu-id="45f76-102">Properties collection (DAO)</span></span>

<span data-ttu-id="45f76-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45f76-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45f76-104">Uma coleção **Properties** contém todos os objetos **[Property](property-object-dao.md)** de uma instância específica de um objeto.</span><span class="sxs-lookup"><span data-stu-id="45f76-104">A **Properties** collection contains all the **[Property](property-object-dao.md)** objects for a specific instance of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="45f76-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="45f76-105">Remarks</span></span>

<span data-ttu-id="45f76-p101">Todo objeto DAO, com exceção dos objetos **Connection** e **Error** contém uma coleção **Properties**, que tem certos objetos **Property** internos. Esses objetos **Property** (que geralmente são denominados apenas propriedades) caracterizam exclusivamente essa instância do objeto.</span><span class="sxs-lookup"><span data-stu-id="45f76-p101">Every DAO object except the **Connection** and **Error** objects contains a **Properties** collection, which has certain built-in **Property** objects. These **Property** objects (which are often just called properties) uniquely characterize that instance of the object.</span></span>

<span data-ttu-id="45f76-p102">Além das propriedades internas, você também poderá criar e adicionar suas próprias propriedades definidas pelo usuário. Para adicionar uma propriedade definida pelo usuário a uma instância existente de um objeto, defina primeiramente suas características com o método **CreateProperty**, em seguida adicione-a à coleção com o método **Append**. Uma referência a um objeto **Property** definido pelo usuário que não tenha sido acrescentado ainda a uma coleção **Properties** causará um erro, bem como o acréscimo de um objeto **Property** definido pelo usuário a uma coleção **Properties** que contenha um objeto **Property** de mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="45f76-p102">In addition to the built-in properties, you can also create and add your own user-defined properties. To add a user-defined property to an existing instance of an object, first define its characteristics with the **CreateProperty** method, then add it to the collection with the **Append** method. Referencing a user-defined **Property** object that has not yet been appended to a **Properties** collection will cause an error, as will appending a user-defined **Property** object to a **Properties** collection containing a **Property** object of the same name.</span></span>

<span data-ttu-id="45f76-111">É possível usar o método **Delete** para remover propriedades definidas pelo usuário da coleção **Properties**, mas não é possível remover propriedades internas.</span><span class="sxs-lookup"><span data-stu-id="45f76-111">You can use the **Delete** method to remove user-defined properties from the **Properties** collection, but you can't remove built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="45f76-p103">[!OBSERVAçãO] Um objeto **Property** definido pelo usuário está associado apenas à instância específica de um objeto. A propriedade não é definida para todas as instâncias de objetos do tipo selecionado.</span><span class="sxs-lookup"><span data-stu-id="45f76-p103">A user-defined **Property** object is associated only with the specific instance of an object. The property isn't defined for all instances of objects of the selected type.</span></span>

<span data-ttu-id="45f76-114">Para fazer referência a um objeto **Property** interno em uma coleção por seu número ordinal ou por sua configuração de propriedade **Name**, use uma das seguintes formas de sintaxe:</span><span class="sxs-lookup"><span data-stu-id="45f76-114">To refer to a built-in **Property** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="45f76-115">. **Propriedades**(0)</span><span class="sxs-lookup"><span data-stu-id="45f76-115">object.**Properties**(0)</span></span>

- <span data-ttu-id="45f76-116">. **Propriedades**("nome")</span><span class="sxs-lookup"><span data-stu-id="45f76-116">object.**Properties**("name")</span></span>

- <span data-ttu-id="45f76-117">.  \! Propriedades \[ name\]</span><span class="sxs-lookup"><span data-stu-id="45f76-117">object.**Properties**\!\[name\]</span></span>

<span data-ttu-id="45f76-118">Para uma propriedade interna, é possível usar esta sintaxe:</span><span class="sxs-lookup"><span data-stu-id="45f76-118">For a built-in property, you can also use this syntax:</span></span>

- <span data-ttu-id="45f76-119">object.name</span><span class="sxs-lookup"><span data-stu-id="45f76-119">object.name</span></span>

> [!NOTE]
> <span data-ttu-id="45f76-120">Para uma propriedade definida pelo usuário, você deve usar o objeto completo. **Sintaxe de** propriedades ("nome").</span><span class="sxs-lookup"><span data-stu-id="45f76-120">For a user-defined property, you must use the full object.**Properties**("name") syntax.</span></span>

<span data-ttu-id="45f76-p104">Com as mesmas formas de sintaxe, você também pode referir-se à propriedade **Value** de um objeto **Property**. O contexto da referência determinará se você está se referindo ao objeto **Property** propriamente dito ou à propriedade **Value** do objeto **Property**.</span><span class="sxs-lookup"><span data-stu-id="45f76-p104">With the same syntax forms, you can also refer to the **Value** property of a **Property** object. The context of the reference will determine whether you are referring to the **Property** object itself or the **Value** property of the **Property** object.</span></span>

## <a name="example"></a><span data-ttu-id="45f76-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="45f76-123">Example</span></span>

<span data-ttu-id="45f76-p105">Este exemplo cria uma propriedade definida pelo usuário para o banco de dados atual, define suas propriedades **Type** e **Value** e acrescenta-o à coleção **Properties** do banco de dados. Em seguida, são enumeradas no exemplo todas as propriedades do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="45f76-p105">This example creates a user-defined property for the current database, sets its **Type** and **Value** properties, and appends it to the **Properties** collection of the database. Then the example enumerates all properties in the database.</span></span>

```vb
    Sub PropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpNew As Property 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Create and append user-defined property. 
     Set prpNew = .CreateProperty() 
     prpNew.Name = "UserDefined" 
     prpNew.Type = dbText 
     prpNew.Value = "This is a user-defined property." 
     .Properties.Append prpNew 
     
     ' Enumerate all properties of current database. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     With prpLoop 
     Debug.Print " " & .Name 
     Debug.Print " Type: " & .Type 
     Debug.Print " Value: " & .Value 
     Debug.Print " Inherited: " & _ 
     .Inherited 
     End With 
     Next prpLoop 
     
     ' Delete new property because this is a 
     ' demonstration. 
     .Properties.Delete "UserDefined" 
     End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="45f76-p106">Este exemplo tenta definir o valor de uma propriedade definida pelo usuário. Se a propriedade não existir, será usado o método **CreateProperty** para criar e definir o valor da nova propriedade. O procedimento SetProperty é exigido para a execução deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="45f76-p106">This example tries to set the value of a user-defined property. If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property. The SetProperty procedure is required for this procedure to run.</span></span>

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
     If prpLoop <> "" Then Debug.Print " " & _ 
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
