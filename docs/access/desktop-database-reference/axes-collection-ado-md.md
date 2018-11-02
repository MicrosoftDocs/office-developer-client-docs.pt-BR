---
title: Coleção Axes (ADO MD)
TOCTitle: Axes collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c88bf27f406a439d051112afb9abf94697a13b12
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922227"
---
# <a name="axes-collection-ado-md"></a>Coleção Axes (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Contém os objetos [Axis](axis-object-ado-md.md) que definem um conjunto de células.

## <a name="remarks"></a>Comentários

Um objeto [Cellset](cellset-object-ado-md.md) contém uma coleção **Axes**. Quando um **Cellset** está aberto, essa coleção conterá pelo menos um **Axis**. Consulte o objeto [Axis](axis-object-ado-md.md) para obter uma explicação mais detalhada sobre como usar os objetos **Axis**.


> [!NOTE]
> [!OBSERVAçãO] O eixo de filtro de um **Cellset** não está contido na coleção **Axes**. Consulte a propriedade [FilterAxis](filteraxis-property-ado-md.md) para obter mais informações.



**Axes** é uma coleção padrão do ADO. Com as propriedades e os métodos de uma coleção, você pode executar os seguintes procedimentos:

  - Obter o número de objetos na coleção com a propriedade [Count](count-property-ado.md).

  - Retornar um objeto da coleção com a propriedade padrão [Item](item-property-ado.md).

  - Atualizar os objetos na coleção do provedor com o método [Refresh](refresh-method-ado.md).

