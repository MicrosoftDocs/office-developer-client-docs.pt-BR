---
title: Propriedade FilterAxis (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b1f9c2bcc4ed4f3314a697d4a0eae8415bc4f62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292451"
---
# <a name="filteraxis-property-ado-md"></a>Propriedade FilterAxis (ADO MD)


**Aplica-se ao:** Access 2013, Office 2013

Indica informações de filtro sobre o conjunto de células atual.

## <a name="return-values"></a>Valor de retorno

Retorna um objeto [Axis](axis-object-ado-md.md) e é somente leitura.

## <a name="remarks"></a>Comentários

Use a propriedade **FilterAxis** para retornar informações sobre as dimensões que foram usadas para dividir os dados. A propriedade [DimensionCount](dimensioncount-property-ado-md.md) do **Axis** retorna o número de dimensões do slicer. Em geral, esse eixo tem apenas uma linha.

O **Axis** retornado pelo [FilterAxis](filteraxis-property-ado-md.md) não está contido na coleção [Axes](axes-collection-ado-md.md) de um objeto [Cellset](cellset-object-ado-md.md).

