---
title: Coleção Columns (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13f9a17d7dfcd9e621e4f4b1f1fcc03e88b4d832
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464778"
---
# <a name="columns-collection-adox"></a><span data-ttu-id="e17fe-102">Coleção Columns (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e17fe-102">Columns Collection (ADOX)</span></span>


<span data-ttu-id="e17fe-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e17fe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e17fe-104">Contém todos os objetos [Column](column-object-adox.md) de uma tabela, índice ou chave.</span><span class="sxs-lookup"><span data-stu-id="e17fe-104">Contains all [Column](column-object-adox.md) objects of a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="e17fe-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="e17fe-105">Remarks</span></span>

<span data-ttu-id="e17fe-p101">O método [Append](append-method-adox-columns.md) de uma coleção **Columns** é exclusivo do ADOX. Você pode:</span><span class="sxs-lookup"><span data-stu-id="e17fe-p101">The [Append](append-method-adox-columns.md) method for a **Columns** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="e17fe-108">Adicionar uma nova coluna à coleção com o método **Append**.</span><span class="sxs-lookup"><span data-stu-id="e17fe-108">Add a new column to the collection with the **Append** method.</span></span>

<span data-ttu-id="e17fe-p102">As propriedades e métodos restantes são padrão das coleções do ADO. Você pode:</span><span class="sxs-lookup"><span data-stu-id="e17fe-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="e17fe-111">Acessar uma coluna na coleção com a propriedade [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e17fe-111">Access a column in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="e17fe-112">Retornar o número de colunas contidas na coleção com a propriedade [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e17fe-112">Return the number of columns contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="e17fe-113">Remover uma coluna da coleção com o método [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="e17fe-113">Remove a column from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="e17fe-114">Atualizar os objetos da coleção para refletir o atual esquema do banco de dados com o método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e17fe-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e17fe-115">[!OBSERVAçãO] Ocorrerá um erro ao anexar uma <STRONG>Coluna</STRONG> à coleção <STRONG>Columns</STRONG> de um <A href="index-object-adox.md">Índice</A>, se a <STRONG>Coluna</STRONG> não existir em uma <A href="table-object-adox.md">Tabela</A> que já esteja anexada à coleção <A href="tables-collection-adox.md">Tables</A>.</span><span class="sxs-lookup"><span data-stu-id="e17fe-115">An error will occur when appending a <STRONG>Column</STRONG> to the <STRONG>Columns</STRONG> collection of an <A href="index-object-adox.md">Index</A> if the <STRONG>Column</STRONG> does not exist in a <A href="table-object-adox.md">Table</A> that is already appended to the <A href="tables-collection-adox.md">Tables</A> collection.</span></span></P>


