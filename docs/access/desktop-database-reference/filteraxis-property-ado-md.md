---
title: Propriedade FilterAxis (ADO MD)
TOCTitle: FilterAxis Property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f298acf3a9250a0376ba31f5d3afc6b079ce0c78
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867703"
---
# <a name="filteraxis-property-ado-md"></a>Propriedade FilterAxis (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Indica informações de filtro sobre o conjunto de células atual.

## <a name="return-values"></a>Valor de retorno

Retorna um objeto [Axis](axis-object-ado-md.md) e é somente leitura.

## <a name="remarks"></a>Comentários

Use a propriedade **FilterAxis** para retornar informações sobre as dimensões que foram usadas para dividir os dados. A propriedade [DimensionCount](dimensioncount-property-ado-md.md) do **Axis** retorna o número de dimensões do slicer. Em geral, esse eixo tem apenas uma linha.

O **Axis** retornado pelo [FilterAxis](filteraxis-property-ado-md.md) não está contido na coleção [Axes](axes-collection-ado-md.md) de um objeto [Cellset](cellset-object-ado-md.md).

