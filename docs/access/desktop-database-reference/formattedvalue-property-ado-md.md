---
title: Propriedade FormattedValue (ADO MD)
TOCTitle: FormattedValue property (ADO MD)
ms:assetid: ea7962f2-b08b-52c9-34e5-c5490c72662f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250189(v=office.15)
ms:contentKeyID: 48548464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 547feea04a7e6d103f30071094070650705789be
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922108"
---
# <a name="formattedvalue-property-ado-md"></a>Propriedade FormattedValue (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Indica a exibição formatada de um valor de célula.

## <a name="return-values"></a>Valor de retorno

Retorna um objeto **String** e é somente leitura.

## <a name="remarks"></a>Comentários

Use a propriedade **FormattedValue** para obter o valor de exibição formatado da propriedade [Value](value-property-ado-md.md) de um objeto [Cell](cell-object-ado-md.md). Por exemplo, se o valor de uma célula era 1056.87, e esse valor representava uma quantia em dólar, **FormattedValue** seria US$ 1.056,87.

