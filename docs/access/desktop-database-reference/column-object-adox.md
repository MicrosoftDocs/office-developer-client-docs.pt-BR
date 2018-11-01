---
title: Objeto Column (ADOX)
TOCTitle: Column Object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28ae0f69303db5569b97799d8a77ca66828e2035
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879617"
---
# <a name="column-object-adox"></a><span data-ttu-id="aec41-102">Objeto Column (ADOX)</span><span class="sxs-lookup"><span data-stu-id="aec41-102">Column Object (ADOX)</span></span>


<span data-ttu-id="aec41-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="aec41-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aec41-104">Representa uma coluna de uma tabela, um índice ou uma chave.</span><span class="sxs-lookup"><span data-stu-id="aec41-104">Represents a column from a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="aec41-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="aec41-105">Remarks</span></span>

<span data-ttu-id="aec41-106">O código a seguir cria uma nova **Coluna**:</span><span class="sxs-lookup"><span data-stu-id="aec41-106">The following code creates a new **Column**:</span></span>

`Dim obj As New Column`

<span data-ttu-id="aec41-107">Com as propriedades e coleções de um objeto **Column**, você pode:</span><span class="sxs-lookup"><span data-stu-id="aec41-107">With the properties and collections of a **Column** object, you can:</span></span>

  - <span data-ttu-id="aec41-108">Identificar a coluna com a propriedade [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="aec41-108">Identify the column with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="aec41-109">Especificar os tipos de dados da coluna com a propriedade [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="aec41-109">Specify the data type of the column with the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property.</span></span>

  - <span data-ttu-id="aec41-110">Determinar se a coluna tem tamanho fixo ou se ela pode conter valores nulos com a propriedade [Attributes](attributes-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="aec41-110">Determine if the column is fixed-length, or if it can contain null values with the [Attributes](attributes-property-adox.md) property.</span></span>

  - <span data-ttu-id="aec41-111">Especificar o tamanho máximo da coluna com a propriedade [DefinedSize](definedsize-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="aec41-111">Specify the maximum size of the column with the [DefinedSize](definedsize-property-adox.md) property.</span></span>

  - <span data-ttu-id="aec41-112">Para valores de dados numéricos, especificar a escala com a propriedade [NumericScale](numericscale-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="aec41-112">For numeric data values, specify the scale with the [NumericScale](numericscale-property-adox.md) property.</span></span>

  - <span data-ttu-id="aec41-113">Para valores de dados numéricos, especificar a precisão máxima com a propriedade [Precision](precision-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="aec41-113">For numeric data value, specify the maximum precision with the [Precision](precision-property-adox.md) property.</span></span>

  - <span data-ttu-id="aec41-114">Especificar o [Catálogo](catalog-object-adox.md) que contém a coluna com a propriedade [ParentCatalog](parentcatalog-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="aec41-114">Specify the [Catalog](catalog-object-adox.md) that owns the column with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

  - <span data-ttu-id="aec41-115">Para colunas-chave, especificar o nome da coluna relacionada na tabela relacionada com a propriedade [RelatedColumn](relatedcolumn-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="aec41-115">For key columns, specify the name of the related column in the related table with the [RelatedColumn](relatedcolumn-property-adox.md) property.</span></span>

  - <span data-ttu-id="aec41-116">Para colunas de índice, especificar se a ordem de classificação é ascendente ou descendente com a propriedade [SortOrder](sortorder-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="aec41-116">For index columns, specify whether the sort order is ascending or descending with the [SortOrder](sortorder-property-adox.md) property.</span></span>

  - <span data-ttu-id="aec41-117">Acessar propriedades específicas do provedor com a coleção [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="aec41-117">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="aec41-p101">[!OBSERVAçãO] Seu provedor de dados talvez não ofereça suporte para todas as propriedades dos objetos **Column**. Um erro ocorrerá se você tiver definido um valor para uma propriedade para a qual o provedor não oferece suporte. Para novos objetos **Column**, o erro ocorrerá quando o objeto for acrescentado à coleção. Para objetos existentes, o erro ocorrerá ao definir a propriedade.</span><span class="sxs-lookup"><span data-stu-id="aec41-p101">Not all properties of **Column** objects may be supported by your data provider. An error will occur if you have set a value for a property that the provider does not support. For new **Column** objects, the error will occur when the object is appended to the collection. For existing objects, the error will occur when setting the property.</span></span>
> 
> <span data-ttu-id="aec41-p102">Ao criar objetos **Column**, a existência de um valor padrão apropriado para uma propriedade opcional não garante que seu provedor de dados ofereça suporte para a propriedade. Para obter mais informações sobre quais propriedades têm suporte do seu provedor, consulte a documentação do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="aec41-p102">When creating **Column** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property. For more information about which properties your provider supports, see your provider documentation.</span></span>

