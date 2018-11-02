---
title: Objeto Table (ADOX)
TOCTitle: Table object (ADOX)
ms:assetid: 53a3e2f9-4ec0-8fed-d482-4f995921587b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249273(v=office.15)
ms:contentKeyID: 48544874
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 78f1248042c540df94c6f993d2498d46c8ca593f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923242"
---
# <a name="table-object-adox"></a><span data-ttu-id="13e70-102">Objeto Table (ADOX)</span><span class="sxs-lookup"><span data-stu-id="13e70-102">Table object (ADOX)</span></span>


<span data-ttu-id="13e70-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="13e70-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="13e70-104">Representa uma tabela de banco de dados, incluindo colunas, índices e chaves.</span><span class="sxs-lookup"><span data-stu-id="13e70-104">Represents a database table including columns, indexes, and keys.</span></span>

## <a name="remarks"></a><span data-ttu-id="13e70-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="13e70-105">Remarks</span></span>

<span data-ttu-id="13e70-106">O código a seguir criar uma nova **Tabela**:</span><span class="sxs-lookup"><span data-stu-id="13e70-106">The following code creates a new **Table**:</span></span>

`Dim obj As New Table`

<span data-ttu-id="13e70-107">Com as propriedades e coleções de um objeto **Table**, você pode:</span><span class="sxs-lookup"><span data-stu-id="13e70-107">With the properties and collections of a **Table** object, you can:</span></span>

  - <span data-ttu-id="13e70-108">Identificar a tabela com a propriedade [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="13e70-108">Identify the table with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="13e70-109">Determinar o tipo da tabela com a propriedade [Type](https://msdn.microsoft.com/library/jj250042\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="13e70-109">Determine the type of table with the [Type](https://msdn.microsoft.com/library/jj250042\(v=office.15\)) property.</span></span>

  - <span data-ttu-id="13e70-110">Acessar as colunas do banco de dados da tabela com a coleção [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="13e70-110">Access the database columns of the table with the [Columns](columns-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="13e70-111">Acessar os índices da tabela com a coleção [Indexes](indexes-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="13e70-111">Access the indexes of the table with the [Indexes](indexes-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="13e70-112">Acessar as chaves da tabela com a coleção [Keys](keys-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="13e70-112">Access the keys of the table with the [Keys](keys-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="13e70-113">Especificar o [Catálogo](catalog-object-adox.md) que contém a tabela com a propriedade [ParentCatalog](parentcatalog-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="13e70-113">Specify the [Catalog](catalog-object-adox.md) that owns the table with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

  - <span data-ttu-id="13e70-114">Retornar informações de data com as propriedades [DateCreated](datecreated-property-adox.md) e [DateModified](datemodified-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="13e70-114">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

  - <span data-ttu-id="13e70-115">Acessar propriedades de tabela específicas do provedor com a coleção [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="13e70-115">Access provider-specific table properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <P><span data-ttu-id="13e70-p101">[!OBSERVAçãO] Seu provedor de dados talvez não ofereça suporte para todas as propriedades dos objetos <STRONG>Table</STRONG>. Um erro ocorrerá se você tiver definido um valor para uma propriedade para a qual o provedor não oferece suporte. Para novos objetos <STRONG>Table</STRONG>, o erro ocorrerá quando o objeto for acrescentado à coleção. Para objetos existentes, o erro ocorrerá ao definir a propriedade.</span><span class="sxs-lookup"><span data-stu-id="13e70-p101">Your data provider may not support all properties of <STRONG>Table</STRONG> objects. An error will occur if you have set a value for a property that the provider does not support. For new <STRONG>Table</STRONG> objects, the error will occur when the object is appended to the collection. For existing objects, the error will occur when setting the property.</span></span></P>



<span data-ttu-id="13e70-p102">Ao criar objetos **Table**, a existência de um valor padrão apropriado para uma propriedade opcional não garante que seu provedor de dados ofereça suporte para a propriedade. Para obter mais informações sobre quais propriedades têm suporte do seu provedor, consulte a documentação do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="13e70-p102">When creating **Table** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property. For more information about which properties your provider supports, see your provider documentation.</span></span>

