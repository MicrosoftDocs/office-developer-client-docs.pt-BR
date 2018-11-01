---
title: Objeto Document (DAO)
TOCTitle: Document Object
ms:assetid: b51d4545-b157-4c7c-fdbe-16a25afffdb3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822082(v=office.15)
ms:contentKeyID: 48547247
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 27caa87aa250b0604c163b347bb5202e1c9b994b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880772"
---
# <a name="document-object-dao"></a><span data-ttu-id="91c68-102">Objeto Document (DAO)</span><span class="sxs-lookup"><span data-stu-id="91c68-102">Document Object (DAO)</span></span>


<span data-ttu-id="91c68-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="91c68-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91c68-p101">O objeto **Document** inclui informações sobre uma instância de um objeto. O objeto pode ser um banco de dados, uma tabela, uma consulta ou uma relação salva (apenas bancos de dados do mecanismo de banco de dados do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="91c68-p101">A **Document** object includes information about one instance of an object. The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="91c68-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="91c68-106">Remarks</span></span>

<span data-ttu-id="91c68-p102">Cada objeto **Container** tem uma coleção **Documents** que contém objetos **Document** que descrevem instâncias de objetos incorporados do tipo especificado pelo **Container**. A tabela a seguir lista o tipo de objeto que cada **Document** descreve, o nome desse objeto **Container** e o tipo de informações que **Document** contém.</span><span class="sxs-lookup"><span data-stu-id="91c68-p102">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**. The following table lists the type of object each **Document** describes, the name of its **Container** object, and what type of information **Document** contains.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91c68-109">Document</span><span class="sxs-lookup"><span data-stu-id="91c68-109">Document</span></span></p></th>
<th><p><span data-ttu-id="91c68-110">Container</span><span class="sxs-lookup"><span data-stu-id="91c68-110">Container</span></span></p></th>
<th><p><span data-ttu-id="91c68-111">Contém informações sobre</span><span class="sxs-lookup"><span data-stu-id="91c68-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91c68-112">Banco de dados</span><span class="sxs-lookup"><span data-stu-id="91c68-112">Database</span></span></p></td>
<td><p><span data-ttu-id="91c68-113">Databases</span><span class="sxs-lookup"><span data-stu-id="91c68-113">Databases</span></span></p></td>
<td><p><span data-ttu-id="91c68-114">Banco de dados salvo</span><span class="sxs-lookup"><span data-stu-id="91c68-114">Saved database</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91c68-115">Tabela ou consulta</span><span class="sxs-lookup"><span data-stu-id="91c68-115">Table or query</span></span></p></td>
<td><p><span data-ttu-id="91c68-116">Tables</span><span class="sxs-lookup"><span data-stu-id="91c68-116">Tables</span></span></p></td>
<td><p><span data-ttu-id="91c68-117">Tabela ou consulta salva</span><span class="sxs-lookup"><span data-stu-id="91c68-117">Saved table or query</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91c68-118">Relação</span><span class="sxs-lookup"><span data-stu-id="91c68-118">Relationship</span></span></p></td>
<td><p><span data-ttu-id="91c68-119">Relations</span><span class="sxs-lookup"><span data-stu-id="91c68-119">Relations</span></span></p></td>
<td><p><span data-ttu-id="91c68-120">Relações salvas</span><span class="sxs-lookup"><span data-stu-id="91c68-120">Saved relationship</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="91c68-p103">[!OBSERVAçãO] Não confunda os objetos **Container** listados na tabela anterior com as coleções de mesmo nome. O objeto **Container** do banco de dados se refere a todos os objetos salvos do banco de dados, mas a coleção **Databases** se refere apenas aos objetos do banco de dados que estão abertos em um determinado espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="91c68-p103">Don't confuse the **Container** objects listed in the preceding table with the collections of the same name. The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.</span></span>



<span data-ttu-id="91c68-123">Com um objeto **Document**, você pode:</span><span class="sxs-lookup"><span data-stu-id="91c68-123">With a **Document** object, you can:</span></span>

  - <span data-ttu-id="91c68-124">Usar a propriedade **Name** para retornar o nome que um usuário ou mecanismo de banco de dados do Microsoft Access deu ao objeto quando ele foi criado.</span><span class="sxs-lookup"><span data-stu-id="91c68-124">Use the **Name** property to return the name that a user or the Microsoft Access database engine gave to the object when it was created.</span></span>

  - <span data-ttu-id="91c68-125">Usar a propriedade **Container** para retornar o nome do objeto **Container** que contém o objeto **Document**.</span><span class="sxs-lookup"><span data-stu-id="91c68-125">Use the **Container** property to return the name of the **Container** object that contains the **Document** object.</span></span>

  - <span data-ttu-id="91c68-p104">Usar a propriedade **Owner** para definir ou retornar o proprietário do objeto. Para definir a propriedade **Owner**, você deve ter permissão de gravação no objeto **Document** e definir a propriedade para o nome de um objeto **User** ou **Group** existente.</span><span class="sxs-lookup"><span data-stu-id="91c68-p104">Use the **Owner** property to set or return the owner of the object. To set the **Owner** property, you must have write permission for the **Document** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

  - <span data-ttu-id="91c68-p105">Usar as propriedades **UserName** ou **Permissions** para definir ou retornar as permissões de acesso de um usuário ou grupo para o objeto. Para definir essas propriedades, você deve ter permissão de gravação no objeto **Document** e definir a propriedade **UserName** para o nome de um objeto **User** ou **Group** existente.</span><span class="sxs-lookup"><span data-stu-id="91c68-p105">Use the **UserName** or **Permissions** properties to set or return the access permissions of a user or group for the object. To set these properties, you must have write permission for the **Document** object, and you must set the **UserName** property to the name of an existing **User** or **Group** object.</span></span>

  - <span data-ttu-id="91c68-130">Usar as propriedades **DateCreated** e **LastUpdated** para retornar a data e a hora em que o objeto **Document** foi criado e modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="91c68-130">Use the **DateCreated** and **LastUpdated** properties to return the date and time when the **Document** object was created and last modified.</span></span>

<span data-ttu-id="91c68-p106">Como um objeto **Document** corresponde a um objeto existente, você não poderá criar novos objetos **Document** nem excluir objetos existentes. Para referir-se a um objeto **Document** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:</span><span class="sxs-lookup"><span data-stu-id="91c68-p106">Because a **Document** object corresponds to an existing object, you can't create new **Document** objects or delete existing ones. To refer to a **Document** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

  - <span data-ttu-id="91c68-133">**Documents**(0)</span><span class="sxs-lookup"><span data-stu-id="91c68-133">**Documents**(0)</span></span>

  - <span data-ttu-id="91c68-134">**Documentos** ("*nome*")</span><span class="sxs-lookup"><span data-stu-id="91c68-134">**Documents**("*name*")</span></span>

  - <span data-ttu-id="91c68-135">**Documentos**\!\[*nome*\]</span><span class="sxs-lookup"><span data-stu-id="91c68-135">**Documents**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="91c68-136">Exemplo</span><span class="sxs-lookup"><span data-stu-id="91c68-136">Example</span></span>

<span data-ttu-id="91c68-137">Este exemplo enumera a coleção **Documents** do contêineer Tables e enumera a coleção **Properties** do primeiro objeto **Document** na coleção.</span><span class="sxs-lookup"><span data-stu-id="91c68-137">This example enumerates the **Documents** collection of the Tables container, and then enumerates the **Properties** collection of the first **Document** object in the collection.</span></span>

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

<span data-ttu-id="91c68-138">Este exemplo usa as propriedades **Owner** e **SystemDB** para mostrar os proprietários de uma variedade dos objetos **Document**.</span><span class="sxs-lookup"><span data-stu-id="91c68-138">This example uses the **Owner** and **SystemDB** properties to show the owners of a variety of **Document** objects.</span></span>

```vb 
Sub OwnerX() 
 
 ' Ensure that the Microsoft Access workgroup file is 
 ' available. 
 DBEngine.SystemDB = "system.mdw" 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 Debug.Print "Document owners:" 
 ' Enumerate Containers collection and show the owner 
 ' of the first Document in each container's Documents 
 ' collection. 
 For Each ctrLoop In .Containers 
 With ctrLoop 
 Debug.Print " [" & .Documents(0).Name & _ 
 "] in [" & .Name & _ 
 "] container owned by [" & _ 
 .Documents(0).Owner & "]" 
 End With 
 Next ctrLoop 
 
 .Close 
 End With 
 
End Sub 
 
```

