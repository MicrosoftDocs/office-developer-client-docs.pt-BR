---
title: Propriedade Type (ADO MD)
TOCTitle: Type property (ADO MD)
ms:assetid: 4aaa151e-1f02-aa7d-a9e5-e7019b200924
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249230(v=office.15)
ms:contentKeyID: 48544671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99b4e3e2c6930d8162c57d75978e9dba7b5af3e7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721924"
---
# <a name="type-property-ado-md"></a>Propriedade Type (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Indica o tipo do membro atual.

## <a name="return-values"></a>Valores de retorno

Retorna um valor [MemberTypeEnum](membertypeenum.md) e é somente leitura.

## <a name="remarks"></a>Comentários

Somente os objetos [Member](member-object-ado-md.md) pertencentes a um objeto [Level](level-object-ado-md.md) oferecem suporte a esta propriedade. Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).

