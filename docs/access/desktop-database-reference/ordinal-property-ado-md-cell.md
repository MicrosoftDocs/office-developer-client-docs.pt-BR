---
title: Propriedade Ordinal (Cell do ADO MD)
TOCTitle: Ordinal Property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 284e2cac2c1a86d87e39d9913a262fbafb435ece
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462714"
---
# <a name="ordinal-property-ado-md-cell"></a>Propriedade Ordinal (Cell do ADO MD)


**Aplica-se a**: Access 2013 | Office 2013

Identifica exclusivamente uma célula pela sua posição em um conjunto de células.

## <a name="return-values"></a>Valores de retorno

Retorna um inteiro **Long** e é somente leitura.

## <a name="remarks"></a>Comentários

O valor ordinal da célula identifica a célula de maneira exclusiva em um conjunto de células. Conceitualmente, células são numeradas em um conjunto de células como se o conjunto de células fosse uma matriz de *p* dimensões, em que *p* é o número de [eixos](axes-collection-ado-md.md). Células são numeradas começando do zero e ordenadas por linha.

O valor ordinal da célula pode ser usado com a propriedade [Item](item-property-ado-md-cellset.md) do objeto [Cellset](cellset-object-ado-md.md) para recuperar rapidamente a [Célula](cell-object-ado-md.md).

