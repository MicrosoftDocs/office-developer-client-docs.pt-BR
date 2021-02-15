---
title: Coleção Groups (ADOX)
TOCTitle: Groups collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 21f1880a9effca6e51bc1e8b52a58dce22ce1ea9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292073"
---
# <a name="groups-collection-adox"></a><span data-ttu-id="d421e-102">Coleção Groups (ADOX)</span><span class="sxs-lookup"><span data-stu-id="d421e-102">Groups collection (ADOX)</span></span>

<span data-ttu-id="d421e-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d421e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d421e-104">Contém todos os objetos [Group](group-object-adox.md) de um catálogo ou usuário.</span><span class="sxs-lookup"><span data-stu-id="d421e-104">Contains all stored [Group](group-object-adox.md) objects of a catalog or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="d421e-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d421e-105">Remarks</span></span>

<span data-ttu-id="d421e-p101">A coleção **Groups** de um [Catálogo](catalog-object-adox.md) representa todas as contas de grupo do catálogo. A coleção **Groups** de um [Usuário](user-object-adox.md) representa apenas o grupo ao qual o usuário pertence.</span><span class="sxs-lookup"><span data-stu-id="d421e-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="d421e-p102">O método [Append](append-method-adox-groups.md) de uma coleção **Groups** é exclusivo de ADOX. Você pode:</span><span class="sxs-lookup"><span data-stu-id="d421e-p102">The [Append](append-method-adox-groups.md) method for a **Groups** collection is unique for ADOX. You can:</span></span>

- <span data-ttu-id="d421e-110">Adicionar um novo grupo de segurança à coleção com o método **Append**.</span><span class="sxs-lookup"><span data-stu-id="d421e-110">Add a new security group to the collection with the **Append** method.</span></span>

<span data-ttu-id="d421e-p103">As propriedades e métodos restantes são padrão das coleções do ADO. Você pode:</span><span class="sxs-lookup"><span data-stu-id="d421e-p103">The remaining properties and methods are standard to ADO collections. You can:</span></span>

- <span data-ttu-id="d421e-113">Acessar um grupo na coleção com a propriedade [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d421e-113">Access a group in the collection with the [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="d421e-114">Retornar o número de grupos contidos na coleção com a propriedade [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d421e-114">Return the number of groups contained in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="d421e-115">Remover um grupo da coleção com o método [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="d421e-115">Remove a group from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

- <span data-ttu-id="d421e-116">Atualizar os objetos da coleção para refletir o atual esquema do banco de dados com o método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d421e-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

> [!NOTE]
> <span data-ttu-id="d421e-117">[!OBSERVAçãO] Antes de um objeto **Group** ser anexado à coleção **Groups** de um objeto **User**, na coleção **Groups** do [Catálogo](name-property-adox.md) já deve existir um objeto **Group** com o mesmo **Nome** daquele a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="d421e-117">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


