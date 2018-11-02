---
title: Propriedade Type (ADO MD)
TOCTitle: Type property (ADO MD)
ms:assetid: 4aaa151e-1f02-aa7d-a9e5-e7019b200924
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249230(v=office.15)
ms:contentKeyID: 48544671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3f5cffb5fb888298b23dad02d9593978e581aa6c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928744"
---
# <a name="type-property-ado-md"></a>Propriedade Type (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Indica o tipo do membro atual.

## <a name="return-values"></a>Valor de retorno

Retorna um valor [MemberTypeEnum](membertypeenum.md) e é somente leitura.

## <a name="remarks"></a>Comentários

Somente os objetos [Member](member-object-ado-md.md) pertencentes a um objeto [Level](level-object-ado-md.md) oferecem suporte a esta propriedade. Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).

