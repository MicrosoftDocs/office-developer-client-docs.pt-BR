---
title: Coleção Columns (ADOX)
TOCTitle: Columns collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e8278e43ba04047225f54171782c6a745a579595
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922297"
---
# <a name="columns-collection-adox"></a><span data-ttu-id="84416-102">Coleção Columns (ADOX)</span><span class="sxs-lookup"><span data-stu-id="84416-102">Columns collection (ADOX)</span></span>


<span data-ttu-id="84416-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="84416-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="84416-104">Contém todos os objetos [Column](column-object-adox.md) de uma tabela, índice ou chave.</span><span class="sxs-lookup"><span data-stu-id="84416-104">Contains all [Column](column-object-adox.md) objects of a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="84416-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="84416-105">Remarks</span></span>

<span data-ttu-id="84416-p101">O método [Append](append-method-adox-columns.md) de uma coleção **Columns** é exclusivo do ADOX. Você pode:</span><span class="sxs-lookup"><span data-stu-id="84416-p101">The [Append](append-method-adox-columns.md) method for a **Columns** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="84416-108">Adicionar uma nova coluna à coleção com o método **Append**.</span><span class="sxs-lookup"><span data-stu-id="84416-108">Add a new column to the collection with the **Append** method.</span></span>

<span data-ttu-id="84416-p102">As propriedades e métodos restantes são padrão das coleções do ADO. Você pode:</span><span class="sxs-lookup"><span data-stu-id="84416-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="84416-111">Acessar uma coluna na coleção com a propriedade [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="84416-111">Access a column in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="84416-112">Retornar o número de colunas contidas na coleção com a propriedade [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="84416-112">Return the number of columns contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="84416-113">Remover uma coluna da coleção com o método [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="84416-113">Remove a column from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="84416-114">Atualizar os objetos da coleção para refletir o atual esquema do banco de dados com o método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="84416-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <span data-ttu-id="84416-115">[!OBSERVAçãO] Ocorrerá um erro ao anexar uma **Coluna** à coleção **Columns** de um [Índice](index-object-adox.md), se a **Coluna** não existir em uma [Tabela](table-object-adox.md) que já esteja anexada à coleção [Tables](tables-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="84416-115">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


