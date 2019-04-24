---
title: Propriedade DefinedSize (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 121e81734fc5ecc0a761dae53942f1cbed98df2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294131"
---
# <a name="definedsize-property-ado"></a>Propriedade DefinedSize (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica a capacidade de dados de um objeto [Field](field-object-ado.md).

## <a name="return-value"></a>Valor de retorno

Retorna um valor **Long** que reflete o tamanho definido de um campo como um número de bytes.

## <a name="remarks"></a>Comentários

Use a propriedade **DefinedSize** para determinar a capacidade de dados de um objeto **Field**.

As propriedades **DefinedSize** e [ActualSize](actualsize-property-ado.md) são diferentes. Por exemplo, considere um objeto **Field** com um tipo declarado de **adVarChar** e um valor de propriedade **DefinedSize** de 50, contendo um único caractere. O valor da propriedade **ActualSize** retornado será a extensão em bytes deste único caractere.

