---
title: Coleção Users (ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 24d7a5cab3260dac80b39e5134938c5f55175851
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312933"
---
# <a name="users-collection-adox"></a><span data-ttu-id="4dc44-102">Coleção Users (ADOX)</span><span class="sxs-lookup"><span data-stu-id="4dc44-102">Users collection (ADOX)</span></span>

<span data-ttu-id="4dc44-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4dc44-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4dc44-104">Contém todos os objetos [User](user-object-adox.md) armazenados de um catálogo ou grupo.</span><span class="sxs-lookup"><span data-stu-id="4dc44-104">Contains all stored [User](user-object-adox.md) objects of a catalog or group.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dc44-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="4dc44-105">Remarks</span></span>

<span data-ttu-id="4dc44-p101">A coleção **Users** de um objeto [Catalog](catalog-object-adox.md) representa todos os usuários do catálogo. A coleção **Users** de um objeto [Group](group-object-adox.md) representa apenas os usuários associados ao grupo específico.</span><span class="sxs-lookup"><span data-stu-id="4dc44-p101">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="4dc44-p102">O método [Append](append-method-adox-users.md) de uma coleção **Users** é exclusivo do ADOX. Você pode:</span><span class="sxs-lookup"><span data-stu-id="4dc44-p102">The [Append](append-method-adox-users.md) method for a **Users** collection is unique for ADOX. You can:</span></span>

- <span data-ttu-id="4dc44-110">Adicionar um novo usuário à coleção com o método **Append**.</span><span class="sxs-lookup"><span data-stu-id="4dc44-110">Add a new user to the collection with the **Append** method.</span></span>

<span data-ttu-id="4dc44-p103">As propriedades e os métodos restantes são padrão das coleções do ADO. Você pode:</span><span class="sxs-lookup"><span data-stu-id="4dc44-p103">The remaining properties and methods are standard to ADO collections. You can:</span></span>

- <span data-ttu-id="4dc44-113">Acessar um usuário na coleção com a propriedade [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4dc44-113">Access a user in the collection with the [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="4dc44-114">Retornar o número de usuários contidos na coleção com a propriedade [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4dc44-114">Return the number of users contained in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="4dc44-115">Remover um usuário da coleção com o método [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="4dc44-115">Remove a user from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

- <span data-ttu-id="4dc44-116">Atualizar os objetos da coleção para refletir o atual esquema do banco de dados com o método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4dc44-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

> [!NOTE]
> <span data-ttu-id="4dc44-117">[!OBSERVAçãO] Antes de um objeto **User** ser anexado à coleção **Users** de um objeto **Group**, na coleção **Users** do [Catálogo](name-property-adox.md) já deve existir um objeto **User** com o mesmo **Nome** daquele a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="4dc44-117">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>

