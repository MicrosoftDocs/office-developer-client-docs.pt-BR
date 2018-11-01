---
title: Propriedade Type (ADO MD)
TOCTitle: Type Property (ADO MD)
ms:assetid: 4aaa151e-1f02-aa7d-a9e5-e7019b200924
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249230(v=office.15)
ms:contentKeyID: 48544671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8f4a06956db9a051a130af0cbaa6f9090daa586b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889361"
---
# <a name="type-property-ado-md"></a>Propriedade Type (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Indica o tipo do membro atual.

## <a name="return-values"></a>Valor de retorno

Retorna um valor [MemberTypeEnum](membertypeenum.md) e é somente leitura.

## <a name="remarks"></a>Comentários

Somente os objetos [Member](member-object-ado-md.md) pertencentes a um objeto [Level](level-object-ado-md.md) oferecem suporte a esta propriedade. Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).

