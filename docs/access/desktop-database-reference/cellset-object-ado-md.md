---
title: Objeto CellSet (ADO MD)
TOCTitle: Cellset object (ADO MD)
ms:assetid: 28d4b3b9-f907-9ec0-00e1-9666c887cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249047(v=office.15)
ms:contentKeyID: 48543869
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8cb75ad7277386cfe81b2edcffa234498318444
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296511"
---
# <a name="cellset-object-ado-md"></a><span data-ttu-id="eef50-102">Objeto CellSet (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="eef50-102">Cellset object (ADO MD)</span></span>

<span data-ttu-id="eef50-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eef50-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eef50-104">Representa os resultados de uma consulta multidimensional.</span><span class="sxs-lookup"><span data-stu-id="eef50-104">Represents the results of a multidimensional query.</span></span> <span data-ttu-id="eef50-105">É uma coleção das células selecionadas em cubos ou outros conjuntos de células.</span><span class="sxs-lookup"><span data-stu-id="eef50-105">It is a collection of cells selected from cubes or other cellsets.</span></span>

## <a name="remarks"></a><span data-ttu-id="eef50-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="eef50-106">Remarks</span></span>

<span data-ttu-id="eef50-p102">Dados em um **Conjunto de células** são recuperados usando-se acesso direto, na forma de matriz. Você pode "descer" até um membro específico para obter dados sobre o membro. Por exemplo, o código a seguir retorna a legenda do primeiro membro na primeira posição do primeiro eixo de um conjunto de células chamado cst:</span><span class="sxs-lookup"><span data-stu-id="eef50-p102">Data within a **Cellset** is retrieved using direct, array-like access. You can "drill down" to a specific member to obtain data about that member. For example, the following code returns the caption of the first member in the first position on the first axis of a cellset named cst:</span></span>

`cst.Axes(0).Positions(0).Members(0).Caption`

<span data-ttu-id="eef50-p103">Não existe uma noção de uma célula atual dentro de um conjunto de células. Em vez disso, a propriedade [Item](item-property-ado-md-cellset.md) recupera um objeto [Cell](cell-object-ado-md.md) específico do conjunto de células. Os argumentos da propriedade **Item** determinam qual célula é recuperada. Você pode especificar o valor ordinal único de uma célula. Você também pode recuperar células usando seus números de posição ao longo de cada eixo do conjunto de células. Para obter mais informações sobre recuperação de células, consulte a propriedade [Item](item-property-ado-md-cellset.md).</span><span class="sxs-lookup"><span data-stu-id="eef50-p103">There is no notion of a current cell within a cellset. Instead, the [Item](item-property-ado-md-cellset.md) property retrieves a specific [Cell](cell-object-ado-md.md) object from the cellset. The arguments of the **Item** property determine which cell is retrieved. You can specify the unique ordinal value of a cell. You can also retrieve cells by using their position numbers along each axis of the cellset. For more information about retrieving cells, see the [Item](item-property-ado-md-cellset.md) property.</span></span>

<span data-ttu-id="eef50-116">Com as coleções, os métodos e as propriedades de um objeto **Cellset**, você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="eef50-116">With the collections, methods, and properties of a **Cellset** object, you can do the following:</span></span>

  - <span data-ttu-id="eef50-117">Associar uma conexão aberta a um objeto **Cellset** definindo sua propriedade [ActiveConnection](activeconnection-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="eef50-117">Associate an open connection with a **Cellset** object by setting its [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="eef50-118">Executar e recuperar resultados de uma consulta multidimensional com o método [Open](open-method-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="eef50-118">Execute and retrieve the results of a multidimensional query with the [Open](open-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="eef50-119">Recuperar uma **Célula** do **Conjunto de células** com a propriedade [Item](item-property-ado-md-cellset.md).</span><span class="sxs-lookup"><span data-stu-id="eef50-119">Retrieve a **Cell** from the **Cellset** with the [Item](item-property-ado-md-cellset.md) property.</span></span>

  - <span data-ttu-id="eef50-120">Retornar os objetos [Axis](axis-object-ado-md.md) que definem o **Conjunto de células** com a coleção [Axes](axes-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="eef50-120">Return the [Axis](axis-object-ado-md.md) objects that define the **Cellset** with the [Axes](axes-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="eef50-121">Recuperar informações sobre as dimensões usadas para filtrar os dados do **Conjunto de células** com a propriedade [FilterAxis](filteraxis-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="eef50-121">Retrieve information about the dimensions used to filter the data in the **Cellset** with the [FilterAxis](filteraxis-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="eef50-122">Retornar ou especificar a consulta usada para definir o **Conjunto de células** com a propriedade [Source](source-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="eef50-122">Return or specify the query used to define the **Cellset** with the [Source](source-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="eef50-123">Retornar o estado atual do **Conjunto de células** (aberto, fechado, em execução ou em conexão) com a propriedade [State](state-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="eef50-123">Return the current state of the **Cellset** (open, closed, executing, or connecting) with the [State](state-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="eef50-124">Fechar um **Conjunto de células** aberto com o método [Close](close-method-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="eef50-124">Close an open **Cellset** with the [Close](close-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="eef50-125">Recuperar informações específicas do provedor sobre o **Conjunto de células** com a coleção [Properties](properties-collection-ado.md) padrão do ADO.</span><span class="sxs-lookup"><span data-stu-id="eef50-125">Retrieve provider-specific information about the **Cellset** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

