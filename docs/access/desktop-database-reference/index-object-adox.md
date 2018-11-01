---
title: Objeto Index (ADOX)
TOCTitle: Index Object (ADOX)
ms:assetid: fe368ab1-e396-4684-d930-18b0ba58a925
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250304(v=office.15)
ms:contentKeyID: 48548929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 682811352f1b218633cf4a925d4468322d9386d3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870636"
---
# <a name="index-object-adox"></a><span data-ttu-id="9f203-102">Objeto Index (ADOX)</span><span class="sxs-lookup"><span data-stu-id="9f203-102">Index Object (ADOX)</span></span>

<span data-ttu-id="9f203-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f203-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f203-104">Representa um índice de uma tabela de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9f203-104">Represents an index from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f203-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f203-105">Remarks</span></span>

<span data-ttu-id="9f203-106">O código a seguir criar um novo **Índice**:</span><span class="sxs-lookup"><span data-stu-id="9f203-106">The following code creates a new **Index**:</span></span>

`Dim obj As New Index`

<span data-ttu-id="9f203-107">Com as propriedades e coleções de um objeto **Index**, você pode:</span><span class="sxs-lookup"><span data-stu-id="9f203-107">With the properties and collections of an **Index** object, you can:</span></span>

  - <span data-ttu-id="9f203-108">Identificar o índice com a propriedade [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="9f203-108">Identify the index with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="9f203-109">Acessar as colunas do banco de dados do índice com a coleção [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="9f203-109">Access the database columns of the index with the [Columns](columns-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="9f203-110">Especificar se as chaves de índice devem ser exclusivas com a propriedade [Unique](unique-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="9f203-110">Specify whether the index keys must be unique with the [Unique](unique-property-adox.md) property.</span></span>

  - <span data-ttu-id="9f203-111">Especificar se o índice é a chave primária de uma tabela com a propriedade [PrimaryKey](primarykey-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="9f203-111">Specify whether the index is the primary key for a table with the [PrimaryKey](primarykey-property-adox.md) property.</span></span>

  - <span data-ttu-id="9f203-112">Especificar se os registros que têm valores nulos em seus campos de índice têm entradas de índice com a propriedade [IndexNulls](indexnulls-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="9f203-112">Specify whether records that have null values in their index fields have index entries with the [IndexNulls](indexnulls-property-adox.md) property.</span></span>

  - <span data-ttu-id="9f203-113">Especificar se o índice está agrupado com a propriedade [Clustered](clustered-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="9f203-113">Specify whether the index is clustered with the [Clustered](clustered-property-adox.md) property.</span></span>

  - <span data-ttu-id="9f203-114">Acessar propriedades de índice específicas do provedor com a coleção [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9f203-114">Access provider-specific index properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="9f203-115">[!OBSERVAçãO] Ocorrerá um erro ao anexar uma [Coluna](column-object-adox.md) à coleção **Columns** de um **Índice**, se a **Coluna** não existir em um objeto [Table](table-object-adox.md) já anexado à coleção [Tables](tables-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="9f203-115">An error will occur when appending a [Column](column-object-adox.md) to the **Columns** collection of an **Index** if the **Column** does not exist in a [Table](table-object-adox.md) object already appended to the [Tables](tables-collection-adox.md) collection.</span></span>

<span data-ttu-id="9f203-p101">Seu provedor de dados talvez não ofereça suporte para todas as propriedades dos objetos **Index**. Um erro ocorrerá se você tiver definido um valor para uma propriedade para a qual o provedor não oferece suporte. Para novos objetos **Index**, o erro ocorrerá quando o objeto for acrescentado à coleção. Para objetos existentes, o erro ocorrerá ao definir a propriedade.</span><span class="sxs-lookup"><span data-stu-id="9f203-p101">Your data provider may not support all properties of **Index** objects. An error will occur if you have set a value for a property that is not supported by the provider. For new **Index** objects, the error will occur when the object is appended to the collection. For existing objects, the error will occur when setting the property.</span></span>

<span data-ttu-id="9f203-p102">Ao criar objetos **Index**, a existência de um valor padrão apropriado para uma propriedade opcional não garante que seu provedor de dados ofereça suporte para a propriedade. Para obter mais informações sobre quais propriedades têm suporte do seu provedor, consulte a documentação do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="9f203-p102">When creating **Index** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property. For more information about which properties your provider supports, see your provider documentation.</span></span>

