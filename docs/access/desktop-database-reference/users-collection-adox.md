---
title: Coleção Users (ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b44b7b858adca5672266eb1898213d8f28429f2e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931131"
---
# <a name="users-collection-adox"></a><span data-ttu-id="80e1f-102">Coleção Users (ADOX)</span><span class="sxs-lookup"><span data-stu-id="80e1f-102">Users collection (ADOX)</span></span>


<span data-ttu-id="80e1f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="80e1f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80e1f-104">Contém todos os objetos [User](user-object-adox.md) armazenados de um catálogo ou grupo.</span><span class="sxs-lookup"><span data-stu-id="80e1f-104">Contains all stored [User](user-object-adox.md) objects of a catalog or group.</span></span>

## <a name="remarks"></a><span data-ttu-id="80e1f-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="80e1f-105">Remarks</span></span>

<span data-ttu-id="80e1f-p101">A coleção **Users** de um objeto [Catalog](catalog-object-adox.md) representa todos os usuários do catálogo. A coleção **Users** de um objeto [Group](group-object-adox.md) representa apenas os usuários associados ao grupo específico.</span><span class="sxs-lookup"><span data-stu-id="80e1f-p101">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="80e1f-p102">O método [Append](append-method-adox-users.md) de uma coleção **Users** é exclusivo do ADOX. Você pode:</span><span class="sxs-lookup"><span data-stu-id="80e1f-p102">The [Append](append-method-adox-users.md) method for a **Users** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="80e1f-110">Adicionar um novo usuário à coleção com o método **Append**.</span><span class="sxs-lookup"><span data-stu-id="80e1f-110">Add a new user to the collection with the **Append** method.</span></span>

<span data-ttu-id="80e1f-p103">As propriedades e os métodos restantes são padrão das coleções do ADO. Você pode:</span><span class="sxs-lookup"><span data-stu-id="80e1f-p103">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="80e1f-113">Acessar um usuário na coleção com a propriedade [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="80e1f-113">Access a user in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="80e1f-114">Retornar o número de usuários contidos na coleção com a propriedade [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="80e1f-114">Return the number of users contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="80e1f-115">Remover um usuário da coleção com o método [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="80e1f-115">Remove a user from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="80e1f-116">Atualizar os objetos da coleção para refletir o atual esquema do banco de dados com o método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="80e1f-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="80e1f-117">[!OBSERVAçãO] Antes de um objeto <STRONG>User</STRONG> ser anexado à coleção <STRONG>Users</STRONG> de um objeto <STRONG>Group</STRONG>, na coleção <STRONG>Users</STRONG> do <A href="name-property-adox.md">Catálogo</A> já deve existir um objeto <STRONG>User</STRONG> com o mesmo <STRONG>Nome</STRONG> daquele a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="80e1f-117">Before appending a <STRONG>User</STRONG> object to the <STRONG>Users</STRONG> collection of a <STRONG>Group</STRONG> object, a <STRONG>User</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Users</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


