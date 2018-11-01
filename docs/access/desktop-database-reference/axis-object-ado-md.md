---
title: Objeto Axis (ADO MD)
TOCTitle: Axis Object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76fe2e0aa90397b32d95172318f3657741e1b1ec
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875018"
---
# <a name="axis-object-ado-md"></a>Objeto Axis (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Representa um eixo de posição ou de filtro de um conjunto de células, contendo membros selecionados de uma ou mais dimensões.

## <a name="remarks"></a>Comentários

Um objeto **Axis** pode estar contido em uma coleção [Axes](axes-collection-ado-md.md)ou retornado pela propriedade [FilterAxis](filteraxis-property-ado-md.md) de um [Cellset](cellset-object-ado-md.md).

Com as coleções e as propriedades de um objeto **Axis**, você pode fazer o que segue:

  - Identificar o **Eixo** com a propriedade [Name](name-property-ado-md.md).

  - Percorrer cada posição ao longo de um **Eixo** usando a coleção [Positions](positions-collection-ado-md.md).

  - Obter o número de dimensões no **Eixo** com a propriedade [DimensionCount](dimensioncount-property-ado-md.md).

  - Obter atributos específicos do provedor do **Eixo** com a coleção [Properties](properties-collection-ado.md) padrão do ADO.

