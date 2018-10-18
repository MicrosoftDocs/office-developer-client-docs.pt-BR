---
title: Propriedade Description (ADO MD)
TOCTitle: Description Property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7dd66e0288e20bcf38adefc2fcc30f1856ebf3e6
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606868"
---
# <a name="description-property-ado-md"></a>Propriedade Description (ADO MD)


**Aplica-se a**: Access 2013 | Office 2013

Retorna uma explicação do objeto atual.

<<<<<<< Cabeça
## <a name="return-values"></a>Valores de retorno
=======
## <a name="return-values"></a>Valor de retorno
>>>>>>> mestre

Retorna um objeto **String** e é somente leitura.

## <a name="remarks"></a>Comentários

No caso de objetos [Member](member-object-ado-md.md), **Description** aplica-se somente a membros de medida e de fórmula. **Description** retorna uma sequência de caracteres vazia ("") para todos os outros tipos de membros. Para obter mais informações sobre os vários tipos de membros, consulte a propriedade [Type](type-property-ado-md.md).

Somente objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md) oferecem suporte a essa propriedade. Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).

