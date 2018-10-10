---
title: Propriedade Type (ADO MD)
TOCTitle: Type Property (ADO MD)
ms:assetid: 4aaa151e-1f02-aa7d-a9e5-e7019b200924
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249230(v=office.15)
ms:contentKeyID: 48544671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f3ea67b96e24f01e167ca693dff356c595005904
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461978"
---
# <a name="type-property-ado-md"></a>Propriedade Type (ADO MD)


**Aplica-se a**: Access 2013 | Office 2013

Indica o tipo do membro atual.

## <a name="return-values"></a>Valores de retorno

Retorna um valor [MemberTypeEnum](membertypeenum.md) e é somente leitura.

## <a name="remarks"></a>Comentários

Somente os objetos [Member](member-object-ado-md.md) pertencentes a um objeto [Level](level-object-ado-md.md) oferecem suporte a esta propriedade. Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).

