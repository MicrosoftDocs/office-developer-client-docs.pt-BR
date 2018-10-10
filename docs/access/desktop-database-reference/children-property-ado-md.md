---
title: Propriedade Children (ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e126b203e2282f96070f1f3eb14a9b926c04f432
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462540"
---
# <a name="children-property-ado-md"></a>Propriedade Children (ADO MD)


**Aplica-se a**: Access 2013 | Office 2013

Retorna uma coleção de [Members](members-collection-ado-md.md) dos quais o [Member](member-object-ado-md.md) atual é o pai na hierarquia.

## <a name="return-values"></a>Valores de retorno

Retorna uma coleção **Members** e é somente leitura.

## <a name="remarks"></a>Comentários

A propriedade **Children** contém uma coleção **Members** da qual o **Member** atual é o pai hierárquico. Os objetos **Member** no nível de folha não têm membros filho na coleção **Members**. Essa propriedade só é suportada em objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md). Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).

