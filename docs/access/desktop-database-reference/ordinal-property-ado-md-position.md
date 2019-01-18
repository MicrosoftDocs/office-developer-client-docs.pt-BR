---
title: Propriedade Ordinal (Position do ADO MD)
TOCTitle: Ordinal property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e29b5c86e8f37d84116aa92432e93eb8943e29e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711739"
---
# <a name="ordinal-property-ado-md-position"></a>Propriedade Ordinal (Position do ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Identifica exclusivamente uma posição em um eixo.

## <a name="return-values"></a>Valores de retorno

Retorna um inteiro **Long** e é somente leitura.

## <a name="remarks"></a>Comentários

O **Ordinal** de um objeto [Position](position-object-ado-md.md) corresponde ao índice do **Position** na coleção [Positions](positions-collection-ado-md.md).

Uma célula pode ser recuperada rapidamente por meio do **Ordinal** do objeto **Position** em cada eixo com a propriedade [Item](item-property-ado-md-cellset.md) do objeto [Cellset](cellset-object-ado-md.md).

