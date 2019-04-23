---
title: Propriedade PageCount (ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b37ccc0c9a61e00b3c2e8f5eb3367831e5ddea43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288116"
---
# <a name="pagecount-property-ado"></a>Propriedade PageCount (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica a quantidade de páginas de dados que o objeto [Recordset](recordset-object-ado.md) contém.

## <a name="return-value"></a>Valor de retorno

Retorna um valor **Long**, indicando a quantidade de páginas do **Recordset**.

## <a name="remarks"></a>Comentários

Utilize a propriedade **PageCount** para determinar a quantidade de páginas de dados contida no objeto **Recordset**. *As páginas * são grupos de registros cujo tamanho se iguala ao da definição da propriedade [PageSize](pagesize-property-ado.md). Mesmo que a última página esteja incompleta por conter menos registros que no valor **PageSize**, ela será considerada como uma página adicional no valor **PageCount**. Se o objeto **Recordset** não oferecer suporte a essa propriedade, o valor será -1, indicando que **PageCount** é indeterminável.

Consulte as propriedades **PageSize** e [AbsolutePage](absolutepage-property-ado.md) para obter mais informações sobre a funcionalidade da página.

