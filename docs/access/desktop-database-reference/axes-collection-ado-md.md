---
title: Coleção Axes (ADO MD)
TOCTitle: Axes Collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2b078f2d8f1ea6562d6f82f90943923c7d92a07
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464498"
---
# <a name="axes-collection-ado-md"></a>Coleção Axes (ADO MD)


**Aplica-se a**: Access 2013 | Office 2013

Contém os objetos [Axis](axis-object-ado-md.md) que definem um conjunto de células.

## <a name="remarks"></a>Comentários

Um objeto [Cellset](cellset-object-ado-md.md) contém uma coleção **Axes**. Quando um **Cellset** está aberto, essa coleção conterá pelo menos um **Axis**. Consulte o objeto [Axis](axis-object-ado-md.md) para obter uma explicação mais detalhada sobre como usar os objetos **Axis**.


> [!NOTE]
> <P>[!OBSERVAçãO] O eixo de filtro de um <STRONG>Cellset</STRONG> não está contido na coleção <STRONG>Axes</STRONG>. Consulte a propriedade <A href="filteraxis-property-ado-md.md">FilterAxis</A> para obter mais informações.</P>



**Axes** é uma coleção padrão do ADO. Com as propriedades e os métodos de uma coleção, você pode executar os seguintes procedimentos:

  - Obter o número de objetos na coleção com a propriedade [Count](count-property-ado.md).

  - Retornar um objeto da coleção com a propriedade padrão [Item](item-property-ado.md).

  - Atualizar os objetos na coleção do provedor com o método [Refresh](refresh-method-ado.md).

