---
title: Propriedade Number (ADO)
TOCTitle: Number property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5eb46d6fbeb677e6d0fe73223d74ae2ea42d368
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288571"
---
# <a name="number-property-ado"></a>Propriedade Number (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica o número que identifica exclusivamente um objeto [Error](error-object-ado.md).

## <a name="return-value"></a>Valor de retorno

Retorna um valor **Long** que pode corresponder a uma das constantes [ErrorValueEnum](errorvalueenum.md).

## <a name="remarks"></a>Comentários

Use a propriedade **Number** para determinar qual erro ocorreu. O valor da propriedade é um número exclusivo que corresponde à condição de erro.

A coleção [Errors](errors-collection-ado.md) retorna um HRESULT no formato hexadecimal (por exemplo, 0x80004005) ou valor extenso (por exemplo, 2147467259). Esses HRESULTs podem ser causados por componentes de base, como o OLE DB ou o próprio OLE. Para obter mais informações sobre esses números, consulte o Capítulo 16 da *Referência do programador do OLE DB*.

