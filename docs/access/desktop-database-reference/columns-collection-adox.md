---
title: Coleção Columns (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a7abbf859162d527ac89c637022ce449219c235a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876523"
---
# <a name="columns-collection-adox"></a><span data-ttu-id="5bff3-102">Coleção Columns (ADOX)</span><span class="sxs-lookup"><span data-stu-id="5bff3-102">Columns Collection (ADOX)</span></span>


<span data-ttu-id="5bff3-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5bff3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5bff3-104">Contém todos os objetos [Column](column-object-adox.md) de uma tabela, índice ou chave.</span><span class="sxs-lookup"><span data-stu-id="5bff3-104">Contains all [Column](column-object-adox.md) objects of a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bff3-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bff3-105">Remarks</span></span>

<span data-ttu-id="5bff3-p101">O método [Append](append-method-adox-columns.md) de uma coleção **Columns** é exclusivo do ADOX. Você pode:</span><span class="sxs-lookup"><span data-stu-id="5bff3-p101">The [Append](append-method-adox-columns.md) method for a **Columns** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="5bff3-108">Adicionar uma nova coluna à coleção com o método **Append**.</span><span class="sxs-lookup"><span data-stu-id="5bff3-108">Add a new column to the collection with the **Append** method.</span></span>

<span data-ttu-id="5bff3-p102">As propriedades e métodos restantes são padrão das coleções do ADO. Você pode:</span><span class="sxs-lookup"><span data-stu-id="5bff3-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="5bff3-111">Acessar uma coluna na coleção com a propriedade [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5bff3-111">Access a column in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="5bff3-112">Retornar o número de colunas contidas na coleção com a propriedade [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5bff3-112">Return the number of columns contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="5bff3-113">Remover uma coluna da coleção com o método [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="5bff3-113">Remove a column from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="5bff3-114">Atualizar os objetos da coleção para refletir o atual esquema do banco de dados com o método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5bff3-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <span data-ttu-id="5bff3-115">[!OBSERVAçãO] Ocorrerá um erro ao anexar uma **Coluna** à coleção **Columns** de um [Índice](index-object-adox.md), se a **Coluna** não existir em uma [Tabela](table-object-adox.md) que já esteja anexada à coleção [Tables](tables-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5bff3-115">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


