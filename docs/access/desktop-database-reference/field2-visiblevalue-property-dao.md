---
title: Propriedade Field2.VisibleValue (DAO)
TOCTitle: VisibleValue Property
ms:assetid: 1e023a1a-fd49-7570-42bd-2f4c06ac5e5e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845809(v=office.15)
ms:contentKeyID: 48543611
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101184
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9c901045f1f856142a628fb31806610e7d5dce43
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462348"
---
# <a name="field2visiblevalue-property-dao"></a>Propriedade Field2.VisibleValue (DAO)


**Aplica-se a**: Access 2013 | Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . VisibleValue

*expressão* Uma variável que representa um objeto **Field2** .

## <a name="remarks"></a>Comentários

Essa propriedade contém o valor do campo atualmente no banco de dados do servidor. Durante uma atualização em lotes otimista, pode ocorrer uma colisão na qual um segundo cliente modificou o mesmo campo e registro no intervalo entre a recuperação de dados e a tentativa de atualização do primeiro cliente. Quando isso acontecer, o valor definido pelo segundo cliente será acessível por meio desta propriedade.
