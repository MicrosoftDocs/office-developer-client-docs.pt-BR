---
title: Coleção Members (ADO MD)
TOCTitle: Members Collection (ADO MD)
ms:assetid: 1389c554-e4f1-107d-22c6-7fe851d53d23
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248910(v=office.15)
ms:contentKeyID: 48543371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd467335102351fc0412b5c77685d6434b0c20a8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463684"
---
# <a name="members-collection-ado-md"></a><span data-ttu-id="ade83-102">Coleção Members (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="ade83-102">Members Collection (ADO MD)</span></span>


<span data-ttu-id="ade83-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ade83-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ade83-104">Contém os objetos [Member](member-object-ado-md.md) de um nível ou uma posição em um eixo.</span><span class="sxs-lookup"><span data-stu-id="ade83-104">Contains the [Member](member-object-ado-md.md) objects from a level or a position along an axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="ade83-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="ade83-105">Remarks</span></span>

<span data-ttu-id="ade83-106">Uma coleção **Members** é usada para conter os seguintes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ade83-106">A **Members** collection is used to contain the following types of members:</span></span>

  - <span data-ttu-id="ade83-p101">Os membros que constituem um nível em um cubo. Eles estão contidos em uma coleção **Members** de um objeto [Level](level-object-ado-md.md). Por exemplo, usando a amostra de [Visão geral de esquemas e dados multidimensionais](overview-of-multidimensional-schemas-and-data.md), os quatro membros do nível Países são Canadá, Estados Unidos, Reino Unido e Alemanha.</span><span class="sxs-lookup"><span data-stu-id="ade83-p101">The members that make up a level in a cube. These are contained in the **Members** collection of a [Level](level-object-ado-md.md) object. For example, using the sample from [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md), the four members of the Countries level are Canada, USA, UK, and Germany.</span></span>

  - <span data-ttu-id="ade83-p102">Os membros que são filhos de um membro específico dentro de uma hierarquia. Esses membros são retornados pela propriedade [Children](children-property-ado-md.md) do objeto **Member** pai. Por exemplo, usando novamente o mesmo exemplo, os dois filhos do membro Canada são Canada-East e Canada-West.</span><span class="sxs-lookup"><span data-stu-id="ade83-p102">The members that are the children of a specific member within a hierarchy. These members are returned by the [Children](children-property-ado-md.md) property of the parent **Member** object. For example, again using the same sample, the two children of the Canada member are Canada-East and Canada-West.</span></span>

  - <span data-ttu-id="ade83-p103">Os membros que definem uma posição específica ao longo de um eixo de um [conjunto de células](cellset-object-ado-md.md). Usando o conjunto de células de [Trabalhando com dados multidimensionais](working-with-multidimensional-data.md) como um exemplo, os dois membros da primeira posição no eixo x são Valentine e Seattle. Esses membros estão contidos na coleção **Members** de um objeto [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="ade83-p103">The members that define a specific position along an axis of a [cellset](cellset-object-ado-md.md). Using the cellset from [Working with Multidimensional Data](working-with-multidimensional-data.md) as an example, the two members of the first position on the x-axis are Valentine and Seattle. These members are contained by the **Members** collection of a [Position](position-object-ado-md.md) object.</span></span>

<span data-ttu-id="ade83-p104">**Members** é uma coleção padrão do ADO. Com as propriedades e os métodos de uma coleção, você pode executar os seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="ade83-p104">**Members** is a standard ADO collection. With the properties and methods of a collection, you can do the following:</span></span>

  - <span data-ttu-id="ade83-118">Obter o número de objetos na coleção com a propriedade [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ade83-118">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="ade83-119">Retornar um objeto da coleção com a propriedade padrão [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ade83-119">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="ade83-120">Atualizar os objetos na coleção do provedor com o método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ade83-120">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

