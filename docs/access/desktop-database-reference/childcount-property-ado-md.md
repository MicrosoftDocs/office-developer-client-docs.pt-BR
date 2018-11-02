---
title: Propriedade ChildCount (ADO MD)
TOCTitle: ChildCount property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8a55f54bfe796f9dfa0fc3ec157c8f7cfe9fa11
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925216"
---
# <a name="childcount-property-ado-md"></a>Propriedade ChildCount (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Indica o número de membros dos quais o objeto [Member](member-object-ado-md.md) atual é o pai em uma hierarquia.

## <a name="return-values"></a>Valor de retorno

Retorna um inteiro **Long** e é somente leitura.

## <a name="remarks"></a>Comentários

Use a propriedade **ChildCount** para retornar uma estimativa de quantos filhos pertencem a um **Member**. Os filhos reais de um **Member** podem ser retornados pela propriedade [Children](children-property-ado-md.md).

No caso de objetos **Member** de um objeto [Position](position-object-ado-md.md), o número máximo retornado é 65536. Se o número real de filhos exceder 65536, o valor retornado ainda será 65536. Portanto, o aplicativo deverá interpretar um **ChildCount** de 65536 como igual ou maior que o número de filhos de 65536.

No caso de objetos **Member** de um objeto [Level](level-object-ado-md.md), use a propriedade [Count](count-property-ado.md) da coleção ADO na coleção **Children** para determinar o número exato de filhos. A determinação desse número poderá ser lenta se ele for grande na coleção.

