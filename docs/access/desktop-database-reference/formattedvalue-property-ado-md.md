---
title: Propriedade FormattedValue (ADO MD)
TOCTitle: FormattedValue property (ADO MD)
ms:assetid: ea7962f2-b08b-52c9-34e5-c5490c72662f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250189(v=office.15)
ms:contentKeyID: 48548464
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d750944cd42feb95b09f53382c54329ea0c32e1d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292311"
---
# <a name="formattedvalue-property-ado-md"></a>Propriedade FormattedValue (ADO MD)


**Aplica-se ao:** Access 2013, Office 2013

Indica a exibição formatada de um valor de célula.

## <a name="return-values"></a>Valor de retorno

Retorna **String** e é somente leitura.

## <a name="remarks"></a>Comentários

Use a propriedade **FormattedValue** para obter o valor de exibição formatado da propriedade [Value](value-property-ado-md.md) de um objeto [Cell](cell-object-ado-md.md). Por exemplo, se o valor de uma célula era 1056.87, e esse valor representava uma quantia em dólar, **FormattedValue** seria US$ 1.056,87.

