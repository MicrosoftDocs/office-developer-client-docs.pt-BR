---
title: Propriedade Description (ADO MD)
TOCTitle: Description property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f74532693f1054dd9d187757af840a3a00b451f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720615"
---
# <a name="description-property-ado-md"></a>Propriedade Description (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Retorna uma explicação do objeto atual.

## <a name="return-values"></a>Valores de retorno

Retorna um objeto **String** e é somente leitura.

## <a name="remarks"></a>Comentários

No caso de objetos [Member](member-object-ado-md.md), **Description** aplica-se somente a membros de medida e de fórmula. **Description** retorna uma sequência de caracteres vazia ("") para todos os outros tipos de membros. Para obter mais informações sobre os vários tipos de membros, consulte a propriedade [Type](type-property-ado-md.md).

Somente objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md) oferecem suporte a essa propriedade. Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).

