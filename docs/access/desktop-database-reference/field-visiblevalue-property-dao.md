---
title: Propriedade Field.VisibleValue (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b3e1b6ec6cd34112f0ba1d84101390bbd400f82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292913"
---
# <a name="fieldvisiblevalue-property-dao"></a>Propriedade Field.VisibleValue (DAO)


**Aplica-se ao:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . VisibleValue

*expressão* Uma variável que representa um objeto de **Campo**.

## <a name="remarks"></a>Comentários

Essa propriedade contém o valor do campo atualmente no banco de dados do servidor. Durante uma atualização em lotes otimista, pode ocorrer uma colisão na qual um segundo cliente modificou o mesmo campo e registro no intervalo entre a recuperação de dados e a tentativa de atualização do primeiro cliente. Quando isso acontecer, o valor definido pelo segundo cliente será acessível por meio desta propriedade.

