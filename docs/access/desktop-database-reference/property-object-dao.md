---
title: Objeto Property (DAO)
TOCTitle: Property Object
ms:assetid: a1ecb0db-bb93-a7b5-23c3-0b73f275dfe0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820932(v=office.15)
ms:contentKeyID: 48546744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e26bc59221b4ff55c943b6a9a0c87ac5c0dd936b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718816"
---
# <a name="property-object-dao"></a><span data-ttu-id="af796-102">Objeto Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="af796-102">Property object (DAO)</span></span>

<span data-ttu-id="af796-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="af796-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="af796-104">Um objeto **Property** representa uma característica interna ou definida pelo usuário de um objeto DAO.</span><span class="sxs-lookup"><span data-stu-id="af796-104">A **Property** object represents a built-in or user-defined characteristic of a DAO object.</span></span>

## <a name="remarks"></a><span data-ttu-id="af796-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="af796-105">Remarks</span></span>

<span data-ttu-id="af796-p101">Cada objeto DAO exceto os objetos **Connection** e **Error** contém uma coleção **Properties** que tem objetos **Property** correspondentes para incorporar propriedades daquele objeto DAO. O usuário também pode definir objetos **Property** e acrescentá-los à coleção **Properties** de alguns objetos DAO. Esses objetos **Property** (que são normalmente chamados propriedades) caracterizam exclusivamente aquela instância do objeto.</span><span class="sxs-lookup"><span data-stu-id="af796-p101">Every DAO object except the **Connection** and **Error** objects contains a **Properties** collection which has **Property** objects corresponding to built-in properties of that DAO object. The user can also define **Property** objects and append them to the **Properties** collection of some DAO objects. These **Property** objects (which are often just called properties) uniquely characterize that instance of the object.</span></span>

<span data-ttu-id="af796-109">Você pode criar propriedades definidas pelo usuário para os seguintes objetos:</span><span class="sxs-lookup"><span data-stu-id="af796-109">You can create user-defined properties for the following objects:</span></span>

- <span data-ttu-id="af796-110">objetos **Database**, **Index**, **QueryDef** e **TableDef**</span><span class="sxs-lookup"><span data-stu-id="af796-110">**Database**, **Index**, **QueryDef**, and **TableDef** objects</span></span>

- <span data-ttu-id="af796-111">objetos **Field** nas coleções **Fields** dos objetos **QueryDef** e **TableDef**</span><span class="sxs-lookup"><span data-stu-id="af796-111">**Field** objects in **Fields** collections of **QueryDef** and **TableDef** objects</span></span>

<span data-ttu-id="af796-p102">Para adicionar uma propriedade definida pelo usuário, use o método **CreateProperty** para criar um objeto **Property** com uma configuração exclusiva da propriedade **Name**. Defina as propriedades **Type** e **Value** do novo objeto **Property** e, em seguida, acrescente-o à coleção **Properties** do objeto apropriado. O objeto ao qual você está adicionando a propriedade definida pelo usuário já deve ter sido acrescentado a uma coleção. Fazer referência a um objeto **Property** definido pelo usuário que não foi acrescentado a uma coleção **Properties** causará um erro, à medida que acrescentar um objeto **Property** definido pelo usuário a uma coleção **Properties** contendo um objeto **Property** com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="af796-p102">To add a user-defined property, use the **CreateProperty** method to create a **Property** object with a unique **Name** property setting. Set the **Type** and **Value** properties of the new **Property** object, and then append it to the **Properties** collection of the appropriate object. The object to which you are adding the user-defined property must already be appended to a collection. Referencing a user-defined **Property** object that has not yet been appended to a **Properties** collection will cause an error, as will appending a user-defined **Property** object to a **Properties** collection containing a **Property** object of the same name.</span></span>

<span data-ttu-id="af796-116">Você pode excluir propriedades definidas pelo usuário a partir da coleção **Properties**, mas não pode excluir propriedades incorporadas.</span><span class="sxs-lookup"><span data-stu-id="af796-116">You can delete user-defined properties from the **Properties** collection, but you can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="af796-p103">[!OBSERVAçãO] Um objeto **Property** definido pelo usuário é associado apenas à instância específica de um objeto. A propriedade não é definida para todas as instâncias de objetos do tipo selecionado.</span><span class="sxs-lookup"><span data-stu-id="af796-p103">A user-defined **Property** object is associated only with the specific instance of an object. The property isn't defined for all instances of objects of the selected type.</span></span>

<span data-ttu-id="af796-p104">Você pode usar a coleção **Properties** de um objeto para enumerar as propriedades incorporadas ao objeto e definidas pelo usuário. Não é necessário conhecer previamente quais propriedades existem ou quais as características (propriedades **Name** e **Type**) que devem manipulá-las. Entretanto, se você tentar ler uma propriedade somente gravação, como a propriedade **Password** de um objeto **Workspace**, ou tentar ler ou gravar uma propriedade em um contexto inapropriado, como a configuração da propriedade **Value** de um objeto **Field** na coleção **Fields** de um objeto **TableDef**, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="af796-p104">You can use the **Properties** collection of an object to enumerate the object's built-in and user-defined properties. You don't need to know beforehand exactly which properties exist or what their characteristics (**Name** and **Type** properties) are to manipulate them. However, if you try to read a write-only property, such as the **Password** property of a **Workspace** object, or try to read or write a property in an inappropriate context, such as the **Value** property setting of a **Field** object in the **Fields** collection of a **TableDef** object, an error occurs.</span></span>

<span data-ttu-id="af796-122">O objeto **Property** também apresenta quatro propriedades incorporadas:</span><span class="sxs-lookup"><span data-stu-id="af796-122">The **Property** object also has four built-in properties:</span></span>

- <span data-ttu-id="af796-123">A propriedade **Name**, uma **String** que identifica exclusivamente a propriedade.</span><span class="sxs-lookup"><span data-stu-id="af796-123">The **Name** property, a **String** that uniquely identifies the property.</span></span>

- <span data-ttu-id="af796-124">A propriedade **Type**, um **Integer** que especifica o tipo de dados da propriedade.</span><span class="sxs-lookup"><span data-stu-id="af796-124">The **Type** property, an **Integer** that specifies the property data type.</span></span>

- <span data-ttu-id="af796-125">A propriedade **Value**, uma **Variant** que contém a configuração de propriedade.</span><span class="sxs-lookup"><span data-stu-id="af796-125">The **Value** property, a **Variant** that contains the property setting.</span></span>

- <span data-ttu-id="af796-p105">A propriedade **Inherited**, um **Boolean** que indica se a propriedade é herdada de um outro objeto. Por exemplo, um objeto **Field** em uma coleção **Fields** de um objeto **Recordset** pode herdar propriedades do objeto base **TableDef** ou **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="af796-p105">The **Inherited** property, a **Boolean** that indicates whether the property is inherited from another object. For example, a **Field** object in a **Fields** collection of a **Recordset** object can inherit properties from the underlying **TableDef** or **QueryDef** object.</span></span>

<span data-ttu-id="af796-128">Para referir-se a um objeto **Property** incorporado em uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:</span><span class="sxs-lookup"><span data-stu-id="af796-128">To refer to a built-in **Property** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="af796-129">\* objeto \***. Propriedades**(0)</span><span class="sxs-lookup"><span data-stu-id="af796-129">\*object\***.Properties**(0)</span></span>

- <span data-ttu-id="af796-130">\*objeto \***. Propriedades**("\* nome \*")</span><span class="sxs-lookup"><span data-stu-id="af796-130">*object\***.Properties**("* name\*")</span></span>

- <span data-ttu-id="af796-131">\*objeto \***. Propriedades**\!\* nome \*\]</span><span class="sxs-lookup"><span data-stu-id="af796-131">*object\***.Properties**\!\[* name\*\]</span></span>

<span data-ttu-id="af796-132">Para uma propriedade incorporada, você também pode usar esta sintaxe:</span><span class="sxs-lookup"><span data-stu-id="af796-132">For a built-in property, you can also use this syntax:</span></span>

- <span data-ttu-id="af796-133">*objeto*. *nome*</span><span class="sxs-lookup"><span data-stu-id="af796-133">*object*.*name*</span></span>

> [!NOTE]
> <span data-ttu-id="af796-134">Para uma propriedade definida pelo usuário, você deve usar o objeto \*completo \***. Propriedades**("\* nome \*") sintaxe.</span><span class="sxs-lookup"><span data-stu-id="af796-134">For a user-defined property, you must use the full *object\***.Properties**("* name\*") syntax.</span></span>

<span data-ttu-id="af796-p106">Com as mesmas formas de sintaxe, você também pode referir-se à propriedade **Value** de um objeto **Property**. O contexto da referência determinará se você está se referindo ao objeto **Property** propriamente dito ou à propriedade **Value** do objeto **Property**.</span><span class="sxs-lookup"><span data-stu-id="af796-p106">With the same syntax forms, you can also refer to the **Value** property of a **Property** object. The context of the reference will determine whether you are referring to the **Property** object itself or the **Value** property of the **Property** object.</span></span>

