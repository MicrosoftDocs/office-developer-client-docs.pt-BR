---
title: Objeto Catalog (ADO MD)
TOCTitle: Catalog Object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68af66ad00567e06649df6003eeac482eacd6686
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463759"
---
# <a name="catalog-object-ado-md"></a><span data-ttu-id="c653e-102">Objeto Catalog (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="c653e-102">Catalog Object (ADO MD)</span></span>


<span data-ttu-id="c653e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c653e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c653e-104">Contém informações de esquema multidimensionais (isto é, cubos e dimensões subjacentes, hierarquias, níveis e membros) específicos de um MDP (provedor de dados multidimensionais).</span><span class="sxs-lookup"><span data-stu-id="c653e-104">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</span></span>

## <a name="remarks"></a><span data-ttu-id="c653e-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="c653e-105">Remarks</span></span>

<span data-ttu-id="c653e-106">Com as coleções e as propriedades de um objeto **Catalog**, você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="c653e-106">With the collections and properties of a **Catalog** object, you can do the following:</span></span>

  - <span data-ttu-id="c653e-107">Abrir o catálogo definindo a propriedade [ActiveConnection](activeconnection-property-ado-md.md) para um objeto [Connection](connection-object-ado.md) do ADO padrão ou para uma sequência de conexão válida.</span><span class="sxs-lookup"><span data-stu-id="c653e-107">Open the catalog by setting the [ActiveConnection](activeconnection-property-ado-md.md) property to a standard ADO [Connection](connection-object-ado.md) object or to a valid connection string.</span></span>

  - <span data-ttu-id="c653e-108">Identificar o **Catálogo** com a propriedade [Name](name-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="c653e-108">Identify the **Catalog** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="c653e-109">Percorrer os cubos de um catálogo usando a coleção [CubeDefs](cubedefs-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="c653e-109">Iterate through the cubes in a catalog using the [CubeDefs](cubedefs-collection-ado-md.md) collection.</span></span>

