---
title: Objeto Cellset (ADO MD)
TOCTitle: Cellset Object (ADO MD)
ms:assetid: 28d4b3b9-f907-9ec0-00e1-9666c887cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249047(v=office.15)
ms:contentKeyID: 48543869
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a71e6989eca613a23b96e66816820ffa1e4742c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879554"
---
# <a name="cellset-object-ado-md"></a>Objeto Cellset (ADO MD)

**Aplica-se a**: Access 2013, o Office 2013

Representa os resultados de uma consulta multidimensional. É uma coleção das células selecionadas em cubos ou outros conjuntos de células.

## <a name="remarks"></a>Comentários

Dados em um **Conjunto de células** são recuperados usando-se acesso direto, na forma de matriz. Você pode "descer" até um membro específico para obter dados sobre o membro. Por exemplo, o código a seguir retorna a legenda do primeiro membro na primeira posição do primeiro eixo de um conjunto de células chamado cst:

`cst.Axes(0).Positions(0).Members(0).Caption`

Não existe uma noção de uma célula atual dentro de um conjunto de células. Em vez disso, a propriedade [Item](item-property-ado-md-cellset.md) recupera um objeto [Cell](cell-object-ado-md.md) específico do conjunto de células. Os argumentos da propriedade **Item** determinam qual célula é recuperada. Você pode especificar o valor ordinal único de uma célula. Você também pode recuperar células usando seus números de posição ao longo de cada eixo do conjunto de células. Para obter mais informações sobre recuperação de células, consulte a propriedade [Item](item-property-ado-md-cellset.md).

Com as coleções, os métodos e as propriedades de um objeto **Cellset**, você pode fazer o que segue:

  - Associar uma conexão aberta a um objeto **Cellset** definindo sua propriedade [ActiveConnection](activeconnection-property-ado-md.md).

  - Executar e recuperar resultados de uma consulta multidimensional com o método [Open](open-method-ado-md.md).

  - Recuperar uma **Célula** do **Conjunto de células** com a propriedade [Item](item-property-ado-md-cellset.md).

  - Retornar os objetos [Axis](axis-object-ado-md.md) que definem o **Conjunto de células** com a coleção [Axes](axes-collection-ado-md.md).

  - Recuperar informações sobre as dimensões usadas para filtrar os dados do **Conjunto de células** com a propriedade [FilterAxis](filteraxis-property-ado-md.md).

  - Retornar ou especificar a consulta usada para definir o **Conjunto de células** com a propriedade [Source](source-property-ado-md.md).

  - Retornar o estado atual do **Conjunto de células** (aberto, fechado, em execução ou em conexão) com a propriedade [State](state-property-ado-md.md).

  - Fechar um **Conjunto de células** aberto com o método [Close](close-method-ado-md.md).

  - Recuperar informações específicas do provedor sobre o **Conjunto de células** com a coleção [Properties](properties-collection-ado.md) padrão do ADO.

