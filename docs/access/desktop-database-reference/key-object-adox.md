---
title: Objeto Key (ADOX - referência de banco de dados da área de trabalho do Access)
TOCTitle: Key Object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c77e45f52994f14d79acf424da14b55b2cdd9814
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465470"
---
# <a name="key-object-adox"></a><span data-ttu-id="e6991-102">Objeto Key (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e6991-102">Key Object (ADOX)</span></span>


<span data-ttu-id="e6991-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6991-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e6991-104">Representa um campo de chave primária, estrangeira ou exclusiva de uma tabela de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e6991-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6991-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6991-105">Remarks</span></span>

<span data-ttu-id="e6991-106">O código a seguir criar uma nova **Chave**:</span><span class="sxs-lookup"><span data-stu-id="e6991-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="e6991-107">Com as propriedades e coleções de um objeto **Key**, você pode:</span><span class="sxs-lookup"><span data-stu-id="e6991-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="e6991-108">Identificar a chave com a propriedade [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e6991-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="e6991-109">Determinar se a chave é primária, externa ou exclusiva com a propriedade [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="e6991-109">Determine whether the key is primary, foreign, or unique with the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property.</span></span>

- <span data-ttu-id="e6991-110">Acessar as colunas do banco de dados da chave com a coleção [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e6991-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="e6991-111">Especificar o nome da tabela relacionada com a propriedade [RelatedTable](relatedtable-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e6991-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="e6991-112">Determinar a ação executada na exclusão ou atualização de uma chave primária com as propriedades [DeleteRule](deleterule-property-adox.md) e [UpdateRule](updaterule-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e6991-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>

