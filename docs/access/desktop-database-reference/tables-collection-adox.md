---
title: Coleção Tables (ADOX)
TOCTitle: Tables collection (ADOX)
ms:assetid: 07bc0541-c528-1c25-c8c4-05736836eda3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248821(v=office.15)
ms:contentKeyID: 48543082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e53cd4b6d4a61a226103eb443bac7f3b4f92d908
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314046"
---
# <a name="tables-collection-adox"></a><span data-ttu-id="3e11a-102">Coleção Tables (ADOX)</span><span class="sxs-lookup"><span data-stu-id="3e11a-102">Tables collection (ADOX)</span></span>


<span data-ttu-id="3e11a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e11a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e11a-104">Contém todos os objetos [Tabela](table-object-adox.md) de um catálogo.</span><span class="sxs-lookup"><span data-stu-id="3e11a-104">Contains all [Table](table-object-adox.md) objects of a catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e11a-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e11a-105">Remarks</span></span>

<span data-ttu-id="3e11a-p101">O método [Append](append-method-adox-tables.md) de uma coleção **Tables** é exclusivo de ADOX. Você pode:</span><span class="sxs-lookup"><span data-stu-id="3e11a-p101">The [Append](append-method-adox-tables.md) method for a **Tables** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="3e11a-108">Adicionar uma nova tabela à coleção com o método **Append**.</span><span class="sxs-lookup"><span data-stu-id="3e11a-108">Add a new table to the collection with the **Append** method.</span></span>

<span data-ttu-id="3e11a-p102">As propriedades e os métodos restantes são padrão das coleções do ADO. Você pode:</span><span class="sxs-lookup"><span data-stu-id="3e11a-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="3e11a-111">Acessar uma tabela na coleção com a propriedade [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3e11a-111">Access a table in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="3e11a-112">Retornar o número de tabelas contidas na coleção com a propriedade [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3e11a-112">Return the number of tables contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="3e11a-113">Remover uma tabela da coleção com o método [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="3e11a-113">Remove a table from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="3e11a-114">Atualizar os objetos da coleção para refletir o atual esquema do banco de dados com o método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3e11a-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

<span data-ttu-id="3e11a-p103">Alguns provedores podem retornar outros objetos de esquema, como modos de exibição, na coleção Tables. Portanto, algumas coleções ADOX podem conter referências ao mesmo objeto. Se você excluir o objeto de uma coleção, a alteração não será visível em outra coleção que faça referência ao objeto excluído até que o método Refresh seja acionado na coleção. Por exemplo, com o OLE DB Provider for Microsoft Jet, modos de exibição são retornados com a coleção Tables. Se cancelar um modo de exibição, você deverá atualizar a coleção Tables para que ela possa refletir a alteração.</span><span class="sxs-lookup"><span data-stu-id="3e11a-p103">Some providers may return other schema objects, such as a View, in the Tables collection. Therefore, some ADOX collections may contain references to the same object. Should you delete the object from one collection, the change will not be visible in another collection that references the deleted object until the Refresh method is called on the collection. For example, with the OLE DB Provider for Microsoft Jet, Views are returned with the Tables collection. If you drop a View, you must Refresh the Tables collection before the collection will reflect the change.</span></span>

