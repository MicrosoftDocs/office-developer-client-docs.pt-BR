---
title: Objeto Key (ADOX - referência de banco de dados da área de trabalho do Access)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7722130c76516eaa7dcaf0598a5e1c040e21ba25
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025942"
---
# <a name="key-object-adox"></a><span data-ttu-id="4facd-102">Objeto Key (ADOX)</span><span class="sxs-lookup"><span data-stu-id="4facd-102">Key object (ADOX)</span></span>


<span data-ttu-id="4facd-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4facd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4facd-104">Representa um campo de chave primária, estrangeira ou exclusiva de uma tabela de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4facd-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="4facd-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="4facd-105">Remarks</span></span>

<span data-ttu-id="4facd-106">O código a seguir criar uma nova **Chave**:</span><span class="sxs-lookup"><span data-stu-id="4facd-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="4facd-107">Com as propriedades e coleções de um objeto **Key**, você pode:</span><span class="sxs-lookup"><span data-stu-id="4facd-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="4facd-108">Identificar a chave com a propriedade [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="4facd-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="4facd-109">Determinar se a chave é primária, externa ou exclusiva com a propriedade [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox).</span><span class="sxs-lookup"><span data-stu-id="4facd-109">Determine whether the key is primary, foreign, or unique with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property.</span></span>

- <span data-ttu-id="4facd-110">Acessar as colunas do banco de dados da chave com a coleção [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="4facd-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="4facd-111">Especificar o nome da tabela relacionada com a propriedade [RelatedTable](relatedtable-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="4facd-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="4facd-112">Determinar a ação executada na exclusão ou atualização de uma chave primária com as propriedades [DeleteRule](deleterule-property-adox.md) e [UpdateRule](updaterule-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="4facd-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>

