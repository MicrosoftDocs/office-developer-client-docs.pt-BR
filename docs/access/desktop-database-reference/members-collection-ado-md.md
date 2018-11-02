---
title: Coleção Members (ADO MD)
TOCTitle: Members collection (ADO MD)
ms:assetid: 1389c554-e4f1-107d-22c6-7fe851d53d23
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248910(v=office.15)
ms:contentKeyID: 48543371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b5e27af7e1e1d4842e6a76fa8d5e649b3b351064
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922724"
---
# <a name="members-collection-ado-md"></a>Coleção Members (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Contém os objetos [Member](member-object-ado-md.md) de um nível ou uma posição em um eixo.

## <a name="remarks"></a>Comentários

Uma coleção **Members** é usada para conter os seguintes tipos de membros:

  - Os membros que constituem um nível em um cubo. Eles estão contidos em uma coleção **Members** de um objeto [Level](level-object-ado-md.md). Por exemplo, usando a amostra de [Visão geral de esquemas e dados multidimensionais](overview-of-multidimensional-schemas-and-data.md), os quatro membros do nível Países são Canadá, Estados Unidos, Reino Unido e Alemanha.

  - Os membros que são filhos de um membro específico dentro de uma hierarquia. Esses membros são retornados pela propriedade [Children](children-property-ado-md.md) do objeto **Member** pai. Por exemplo, usando novamente o mesmo exemplo, os dois filhos do membro Canada são Canada-East e Canada-West.

  - Os membros que definem uma posição específica ao longo de um eixo de um [conjunto de células](cellset-object-ado-md.md). Usando o conjunto de células de [Trabalhando com dados multidimensionais](working-with-multidimensional-data.md) como um exemplo, os dois membros da primeira posição no eixo x são Valentine e Seattle. Esses membros estão contidos na coleção **Members** de um objeto [Position](position-object-ado-md.md).

**Members** é uma coleção padrão do ADO. Com as propriedades e os métodos de uma coleção, você pode executar os seguintes procedimentos:

  - Obter o número de objetos na coleção com a propriedade [Count](count-property-ado.md).

  - Retornar um objeto da coleção com a propriedade padrão [Item](item-property-ado.md).

  - Atualizar os objetos na coleção do provedor com o método [Refresh](refresh-method-ado.md).

