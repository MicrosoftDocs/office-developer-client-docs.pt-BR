---
title: Coleção Groups (ADOX)
TOCTitle: Groups Collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e7021d6dc485d4c0cfbeca4b9fe487817de715f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463965"
---
# <a name="groups-collection-adox"></a><span data-ttu-id="d39a2-102">Coleção Groups (ADOX)</span><span class="sxs-lookup"><span data-stu-id="d39a2-102">Groups Collection (ADOX)</span></span>


<span data-ttu-id="d39a2-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d39a2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d39a2-104">Contém todos os objetos [Group](group-object-adox.md) de um catálogo ou usuário.</span><span class="sxs-lookup"><span data-stu-id="d39a2-104">Contains all stored [Group](group-object-adox.md) objects of a catalog or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="d39a2-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d39a2-105">Remarks</span></span>

<span data-ttu-id="d39a2-p101">A coleção **Groups** de um [Catálogo](catalog-object-adox.md) representa todas as contas de grupo do catálogo. A coleção **Groups** de um [Usuário](user-object-adox.md) representa apenas o grupo ao qual o usuário pertence.</span><span class="sxs-lookup"><span data-stu-id="d39a2-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="d39a2-p102">O método [Append](append-method-adox-groups.md) de uma coleção **Groups** é exclusivo de ADOX. Você pode:</span><span class="sxs-lookup"><span data-stu-id="d39a2-p102">The [Append](append-method-adox-groups.md) method for a **Groups** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="d39a2-110">Adicionar um novo grupo de segurança à coleção com o método **Append**.</span><span class="sxs-lookup"><span data-stu-id="d39a2-110">Add a new security group to the collection with the **Append** method.</span></span>

<span data-ttu-id="d39a2-p103">As propriedades e métodos restantes são padrão das coleções do ADO. Você pode:</span><span class="sxs-lookup"><span data-stu-id="d39a2-p103">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="d39a2-113">Acessar um grupo na coleção com a propriedade [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d39a2-113">Access a group in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="d39a2-114">Retornar o número de grupos contidos na coleção com a propriedade [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d39a2-114">Return the number of groups contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="d39a2-115">Remover um grupo da coleção com o método [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="d39a2-115">Remove a group from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="d39a2-116">Atualizar os objetos da coleção para refletir o atual esquema do banco de dados com o método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d39a2-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d39a2-117">[!OBSERVAçãO] Antes de um objeto <STRONG>Group</STRONG> ser anexado à coleção <STRONG>Groups</STRONG> de um objeto <STRONG>User</STRONG>, na coleção <STRONG>Groups</STRONG> do <A href="name-property-adox.md">Catálogo</A> já deve existir um objeto <STRONG>Group</STRONG> com o mesmo <STRONG>Nome</STRONG> daquele a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="d39a2-117">Before appending a <STRONG>Group</STRONG> object to the <STRONG>Groups</STRONG> collection of a <STRONG>User</STRONG> object, a <STRONG>Group</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Groups</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


