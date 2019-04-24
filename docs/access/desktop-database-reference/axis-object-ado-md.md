---
title: Objeto Axis (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23fdb0d9ba636ae58fa19b42d5a8a47cb01d4ab2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296896"
---
# <a name="axis-object-ado-md"></a>Objeto Axis (ADO MD)


**Aplica-se ao:** Access 2013, Office 2013

Representa um eixo de posição ou de filtro de um conjunto de células, contendo membros selecionados de uma ou mais dimensões.

## <a name="remarks"></a>Comentários

Um objeto **Axis** pode estar contido em uma coleção [Axes](axes-collection-ado-md.md)ou retornado pela propriedade [FilterAxis](filteraxis-property-ado-md.md) de um [Cellset](cellset-object-ado-md.md).

Com as coleções e as propriedades de um objeto **Axis**, você pode fazer o que segue:

- Identificar o **Eixo** com a propriedade [Name](name-property-ado-md.md).

- Percorrer cada posição ao longo de um **Eixo** usando a coleção [Positions](positions-collection-ado-md.md).

- Obter o número de dimensões no **Eixo** com a propriedade [DimensionCount](dimensioncount-property-ado-md.md).

- Obter atributos específicos do provedor do **Eixo** com a coleção [Properties](properties-collection-ado.md) padrão do ADO.

