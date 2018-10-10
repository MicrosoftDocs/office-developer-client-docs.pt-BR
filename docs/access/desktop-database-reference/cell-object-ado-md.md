---
title: Objeto Cell (ADO MD)
TOCTitle: Cell Object (ADO MD)
ms:assetid: b9d00b71-1f40-5bd1-4b89-fbdb59c552ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249892(v=office.15)
ms:contentKeyID: 48547356
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f38de1adc48e7d63a3b67e45f242a8cc884633ac
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464457"
---
# <a name="cell-object-ado-md"></a><span data-ttu-id="df882-102">Objeto Cell (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="df882-102">Cell Object (ADO MD)</span></span>


<span data-ttu-id="df882-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="df882-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="df882-104">Representa os dados na interseção de coordenadas de eixo contidos em um conjunto de células.</span><span class="sxs-lookup"><span data-stu-id="df882-104">Represents the data at the intersection of axis coordinates contained in a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="df882-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="df882-105">Remarks</span></span>

<span data-ttu-id="df882-106">Um objeto **Cell** é retornado pela propriedade [Item](item-property-ado-md-cellset.md) de um objeto [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="df882-106">A **Cell** object is returned by the [Item](item-property-ado-md-cellset.md) property of a [Cellset](cellset-object-ado-md.md) object.</span></span>

<span data-ttu-id="df882-107">Com as coleções e as propriedades de um objeto **Cell**, você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="df882-107">With the collections and properties of a **Cell** object, you can do the following:</span></span>

  - <span data-ttu-id="df882-108">Retornar os dados da **Célula** com a propriedade [Value](value-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="df882-108">Return the data in the **Cell** with the [Value](value-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="df882-109">Retornar a cadeia de caracteres que representa a exibição formatada da propriedade **Value** com a propriedade [FormattedValue](formattedvalue-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="df882-109">Return the string representing the formatted display of the **Value** property with the [FormattedValue](formattedvalue-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="df882-110">Retornar o valor ordinal da **Célula** dentro do **Conjunto de células** com a propriedade [Ordinal](ordinal-property-ado-md-cell.md).</span><span class="sxs-lookup"><span data-stu-id="df882-110">Return the ordinal value of the **Cell** within the **Cellset** with the [Ordinal](ordinal-property-ado-md-cell.md) property.</span></span>

  - <span data-ttu-id="df882-111">Determinar a posição da **Célula** dentro de [CubeDef](cubedef-object-ado-md.md) com a coleção [Positions](positions-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="df882-111">Determine the position of the **Cell** within the [CubeDef](cubedef-object-ado-md.md) with the [Positions](positions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="df882-112">Recuperar outras informações sobre a **Célula** com a coleção [Properties](properties-collection-ado.md) do ADO padrão.</span><span class="sxs-lookup"><span data-stu-id="df882-112">Retrieve other information about the **Cell** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="df882-p101">A coleção **Properties** contém propriedades fornecidas pelo provedor. A tabela a seguir lista propriedades que talvez estejam disponíveis. A lista de propriedades verdadeira pode diferir, de acordo com a implementação do provedor. Consulte a documentação do seu provedor para obter uma lista mais completa de propriedades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="df882-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="df882-117">Nome</span><span class="sxs-lookup"><span data-stu-id="df882-117">Name</span></span></p></th>
<th><p><span data-ttu-id="df882-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="df882-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df882-119">BackColor</span><span class="sxs-lookup"><span data-stu-id="df882-119">BackColor</span></span></p></td>
<td><p><span data-ttu-id="df882-120">Cor de plano de fundo usada ao exibir a célula.</span><span class="sxs-lookup"><span data-stu-id="df882-120">Background color used when displaying the cell.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df882-121">FontFlags</span><span class="sxs-lookup"><span data-stu-id="df882-121">FontFlags</span></span></p></td>
<td><p><span data-ttu-id="df882-122">Bitmask que detalha efeitos da fonte.</span><span class="sxs-lookup"><span data-stu-id="df882-122">Bitmask detailing effects on the font.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df882-123">FontName</span><span class="sxs-lookup"><span data-stu-id="df882-123">FontName</span></span></p></td>
<td><p><span data-ttu-id="df882-124">Fonte usada para exibir o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="df882-124">Font used to display the cell value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df882-125">FontSize</span><span class="sxs-lookup"><span data-stu-id="df882-125">FontSize</span></span></p></td>
<td><p><span data-ttu-id="df882-126">Tamanho da fonte usada para exibir o valor da célula.</span><span class="sxs-lookup"><span data-stu-id="df882-126">Font size used to display the cell value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df882-127">ForeColor</span><span class="sxs-lookup"><span data-stu-id="df882-127">ForeColor</span></span></p></td>
<td><p><span data-ttu-id="df882-128">Cor de primeiro plano usada ao exibir a célula.</span><span class="sxs-lookup"><span data-stu-id="df882-128">Foreground color used when displaying the cell.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df882-129">FormatString</span><span class="sxs-lookup"><span data-stu-id="df882-129">FormatString</span></span></p></td>
<td><p><span data-ttu-id="df882-130">Valor em uma cadeia de caracteres formatada.</span><span class="sxs-lookup"><span data-stu-id="df882-130">Value in a formatted string.</span></span></p></td>
</tr>
</tbody>
</table>

