---
title: Objeto Catalog (ADO MD)
TOCTitle: Catalog object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ee7d2e68df90c8eee4227f949f93ea074b7df97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296588"
---
# <a name="catalog-object-ado-md"></a><span data-ttu-id="9ad38-102">Objeto Catalog (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="9ad38-102">Catalog object (ADO MD)</span></span>


<span data-ttu-id="9ad38-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ad38-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ad38-104">Contém informações de esquema multidimensionais (isto é, cubos e dimensões subjacentes, hierarquias, níveis e membros) específicos de um MDP (provedor de dados multidimensionais).</span><span class="sxs-lookup"><span data-stu-id="9ad38-104">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ad38-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ad38-105">Remarks</span></span>

<span data-ttu-id="9ad38-106">Com as coleções e as propriedades de um objeto **Catalog**, você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="9ad38-106">With the collections and properties of a **Catalog** object, you can do the following:</span></span>

- <span data-ttu-id="9ad38-107">Abrir o catálogo definindo a propriedade [ActiveConnection](activeconnection-property-ado-md.md) para um objeto [Connection](connection-object-ado.md) do ADO padrão ou para uma sequência de conexão válida.</span><span class="sxs-lookup"><span data-stu-id="9ad38-107">Open the catalog by setting the [ActiveConnection](activeconnection-property-ado-md.md) property to a standard ADO [Connection](connection-object-ado.md) object or to a valid connection string.</span></span>

- <span data-ttu-id="9ad38-108">Identificar o **Catálogo** com a propriedade [Name](name-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="9ad38-108">Identify the **Catalog** with the [Name](name-property-ado-md.md) property.</span></span>

- <span data-ttu-id="9ad38-109">Percorrer os cubos de um catálogo usando a coleção [CubeDefs](cubedefs-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="9ad38-109">Iterate through the cubes in a catalog using the [CubeDefs](cubedefs-collection-ado-md.md) collection.</span></span>

