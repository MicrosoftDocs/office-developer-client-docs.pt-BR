---
title: Propriedade DefinedSize (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a0e67cfdbe60ebf2c49cb3e726311d2fa61bd3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868851"
---
# <a name="definedsize-property-ado"></a>Propriedade DefinedSize (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica a capacidade de dados de um objeto [Field](field-object-ado.md).

## <a name="return-value"></a>Valor de retorno

Retorna um valor **Long** que reflete o tamanho definido de um campo como um número de bytes.

## <a name="remarks"></a>Comentários

Use a propriedade **DefinedSize** para determinar a capacidade de dados de um objeto **Field**.

As propriedades **DefinedSize** e [ActualSize](actualsize-property-ado.md) são diferentes. Por exemplo, considere um objeto **Field** com um tipo declarado de **adVarChar** e um valor de propriedade **DefinedSize** de 50, contendo um único caractere. O valor da propriedade **ActualSize** retornado será a extensão em bytes deste único caractere.

