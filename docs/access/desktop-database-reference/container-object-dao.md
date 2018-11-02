---
title: Objeto container (DAO)
TOCTitle: Container Object
ms:assetid: 22e487cd-e966-fe68-fff3-c680b460cbeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191764(v=office.15)
ms:contentKeyID: 48543720
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba9284e0d62c99ab9bcb631b29587e16a3d76bce
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919511"
---
# <a name="container-object-dao"></a><span data-ttu-id="3e2df-102">Objeto container (DAO)</span><span class="sxs-lookup"><span data-stu-id="3e2df-102">Container object (DAO)</span></span>

<span data-ttu-id="3e2df-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e2df-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e2df-104">Um objeto **Container** agrupa tipos semelhantes de objetos **Document**.</span><span class="sxs-lookup"><span data-stu-id="3e2df-104">A **Container** object groups similar types of **Document** objects together.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e2df-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e2df-105">Remarks</span></span>

<span data-ttu-id="3e2df-p101">Cada objeto **Database** tem uma coleção **Containers** que consiste em objetos **Container** incorporados. Os aplicativos podem definir seus próprios tipos de documentos e contêineres correspondentes (apenas bancos de dados do mecanismo de banco de dados do Microsoft Access); entretanto, esses objetos nem sempre são aceitos no DAO.</span><span class="sxs-lookup"><span data-stu-id="3e2df-p101">Each **Database** object has a **Containers** collection consisting of built-in **Container** objects. Applications can define their own document types and corresponding containers (Microsoft Access database engine databases only); however, these objects may not always be supported through DAO.</span></span>

<span data-ttu-id="3e2df-p102">Alguns desses objetos **Container** são definidos pelo mecanismo de banco de dados do Microsoft Access enquanto outros podem ser definidos por outros aplicativos. A tabela a seguir lista o nome de cada objeto **Container** definido pelo mecanismo de banco de dados do Microsoft Access e o tipo de informações que ele contém.</span><span class="sxs-lookup"><span data-stu-id="3e2df-p102">Some of these **Container** objects are defined by the Microsoft Access database engine while others may be defined by other applications. The following table lists the name of each **Container** object defined by the Microsoft Access database engine and what type of information it contains.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3e2df-110">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="3e2df-110">Container name</span></span></p></th>
<th><p><span data-ttu-id="3e2df-111">Contém informações sobre</span><span class="sxs-lookup"><span data-stu-id="3e2df-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e2df-112">Databases</span><span class="sxs-lookup"><span data-stu-id="3e2df-112">Databases</span></span></p></td>
<td><p><span data-ttu-id="3e2df-113">Bancos de dados salvos</span><span class="sxs-lookup"><span data-stu-id="3e2df-113">Saved databases</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e2df-114">Tables</span><span class="sxs-lookup"><span data-stu-id="3e2df-114">Tables</span></span></p></td>
<td><p><span data-ttu-id="3e2df-115">Tabelas e consultas salvas</span><span class="sxs-lookup"><span data-stu-id="3e2df-115">Saved tables and queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e2df-116">Relations</span><span class="sxs-lookup"><span data-stu-id="3e2df-116">Relations</span></span></p></td>
<td><p><span data-ttu-id="3e2df-117">Relações salvas</span><span class="sxs-lookup"><span data-stu-id="3e2df-117">Saved relationships</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="3e2df-p103">[!OBSERVAçãO] Não confunda os objetos **Container** listados na tabela anterior com as coleções de mesmo nome. O objeto **Container** do banco de dados se refere a todos os objetos salvos do banco de dados, mas a coleção **Databases** se refere apenas aos objetos do banco de dados que estão abertos em um determinado espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3e2df-p103">Don't confuse the **Container** objects listed in the preceding table with the collections of the same name. The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.</span></span>

<span data-ttu-id="3e2df-p104">Cada objeto **Container** tem uma coleção **Documents** que contém objetos **Document** que descrevem instâncias de objetos incorporados do tipo especificado pelo **Container**. Você normalmente usa um objeto **Container** como um link intermediário para as informações no objeto **Document**. Você também pode usar a coleção **Containers** para definir segurança em todos os objetos **Document** de um determinado tipo.</span><span class="sxs-lookup"><span data-stu-id="3e2df-p104">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**. You typically use a **Container** object as an intermediate link to the information in the **Document** object. You can also use the **Containers** collection to set security for all **Document** objects of a given type.</span></span>

<span data-ttu-id="3e2df-123">Com um objeto **Container** existente, você pode:</span><span class="sxs-lookup"><span data-stu-id="3e2df-123">With an existing **Container** object, you can:</span></span>

- <span data-ttu-id="3e2df-124">Usar a propriedade **Name** para retornar o nome predefinido do objeto **Container**.</span><span class="sxs-lookup"><span data-stu-id="3e2df-124">Use the **Name** property to return the predefined name of the **Container** object.</span></span>

- <span data-ttu-id="3e2df-p105">Usar a propriedade **Owner** para definir ou retornar o proprietário do objeto **Container**. Para definir a propriedade **Owner**, você deve ter permissão de gravação no objeto **Container** e definir a propriedade para o nome de um objeto **User** ou **Group** existente.</span><span class="sxs-lookup"><span data-stu-id="3e2df-p105">Use the **Owner** property to set or return the owner of the **Container** object. To set the **Owner** property, you must have write permission for the **Container** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="3e2df-127">Usar as propriedades **Permissions** e **UserName** para definir as permissões de acesso para o objeto **Container**; qualquer objeto **Document** criado na coleção **Documents** de um objeto **Container** herda essas configurações de permissão de acesso.</span><span class="sxs-lookup"><span data-stu-id="3e2df-127">Use the **Permissions** and **UserName** properties to set access permissions for the **Container** object; any **Document** object created in the **Documents** collection of a **Container** object inherits these access permission settings.</span></span>

<span data-ttu-id="3e2df-128">Como os objetos **Container** são incorporados, você não pode criar novos objetos **Container** nem excluir os existentes.</span><span class="sxs-lookup"><span data-stu-id="3e2df-128">Because **Container** objects are built-in, you can't create new **Container** objects or delete existing ones.</span></span>

<span data-ttu-id="3e2df-129">Para referir-se a um objeto **Container** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:</span><span class="sxs-lookup"><span data-stu-id="3e2df-129">To refer to a **Container** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="3e2df-130">**Containers**(0)</span><span class="sxs-lookup"><span data-stu-id="3e2df-130">**Containers**(0)</span></span>

- <span data-ttu-id="3e2df-131">**Contêineres** ("*nome*")</span><span class="sxs-lookup"><span data-stu-id="3e2df-131">**Containers**("*name*")</span></span>

- <span data-ttu-id="3e2df-132">**Contêineres**\!\[*nome*\]</span><span class="sxs-lookup"><span data-stu-id="3e2df-132">**Containers**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="3e2df-133">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3e2df-133">Example</span></span>

<span data-ttu-id="3e2df-134">Este exemplo enumera a coleção **Containers** do banco de dados Northwind e a coleção **Properties** de cada objeto **Container** na coleção.</span><span class="sxs-lookup"><span data-stu-id="3e2df-134">This example enumerates the **Containers** collection of the Northwind database and the **Properties** collection of each **Container** object in the collection.</span></span>

```vb
    Sub ContainerObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim ctrLoop As Container 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Enumerate Containers collection. 
     For Each ctrLoop In .Containers 
     Debug.Print "Properties of " & ctrLoop.Name _ 
     & " container" 
     
     ' Enumerate Properties collection of each 
     ' Container object. 
     For Each prpLoop In ctrLoop.Properties 
     Debug.Print " " & prpLoop.Name _ 
     & " = " prpLoop 
     Next prpLoop 
     
     Next ctrLoop 
     
     .Close 
     End With 
     
    End Sub
```
