---
title: Objeto Property (DAO)
TOCTitle: Property Object
ms:assetid: a1ecb0db-bb93-a7b5-23c3-0b73f275dfe0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820932(v=office.15)
ms:contentKeyID: 48546744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e26bc59221b4ff55c943b6a9a0c87ac5c0dd936b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301187"
---
# <a name="property-object-dao"></a>Objeto Property (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Um objeto **Property** representa uma característica interna ou definida pelo usuário de um objeto DAO.

## <a name="remarks"></a>Comentários

Cada objeto DAO exceto os objetos **Connection** e **Error** contém uma coleção **Properties** que tem objetos **Property** correspondentes para incorporar propriedades daquele objeto DAO. O usuário também pode definir objetos **Property** e acrescentá-los à coleção **Properties** de alguns objetos DAO. Esses objetos **Property** (que são normalmente chamados propriedades) caracterizam exclusivamente aquela instância do objeto.

Você pode criar propriedades definidas pelo usuário para os seguintes objetos:

- objetos **Database**, **Index**, **QueryDef** e **TableDef**

- objetos **Field** nas coleções **Fields** dos objetos **QueryDef** e **TableDef**

Para adicionar uma propriedade definida pelo usuário, use o método **CreateProperty** para criar um objeto **Property** com uma configuração exclusiva da propriedade **Name**. Defina as propriedades **Type** e **Value** do novo objeto **Property** e, em seguida, acrescente-o à coleção **Properties** do objeto apropriado. O objeto ao qual você está adicionando a propriedade definida pelo usuário já deve ter sido acrescentado a uma coleção. Fazer referência a um objeto **Property** definido pelo usuário que não foi acrescentado a uma coleção **Properties** causará um erro, à medida que acrescentar um objeto **Property** definido pelo usuário a uma coleção **Properties** contendo um objeto **Property** com o mesmo nome.

Você pode excluir propriedades definidas pelo usuário a partir da coleção **Properties**, mas não pode excluir propriedades incorporadas.

> [!NOTE]
> [!OBSERVAçãO] Um objeto **Property** definido pelo usuário é associado apenas à instância específica de um objeto. A propriedade não é definida para todas as instâncias de objetos do tipo selecionado.

Você pode usar a coleção **Properties** de um objeto para enumerar as propriedades incorporadas ao objeto e definidas pelo usuário. Não é necessário conhecer previamente quais propriedades existem ou quais as características (propriedades **Name** e **Type**) que devem manipulá-las. Entretanto, se você tentar ler uma propriedade somente gravação, como a propriedade **Password** de um objeto **Workspace**, ou tentar ler ou gravar uma propriedade em um contexto inapropriado, como a configuração da propriedade **Value** de um objeto **Field** na coleção **Fields** de um objeto **TableDef**, ocorrerá um erro.

O objeto **Property** também apresenta quatro propriedades incorporadas:

- A propriedade **Name**, uma **String** que identifica exclusivamente a propriedade.

- A propriedade **Type**, um **Integer** que especifica o tipo de dados da propriedade.

- A propriedade **Value**, uma **Variant** que contém a configuração de propriedade.

- A propriedade **Inherited**, um **Boolean** que indica se a propriedade é herdada de um outro objeto. Por exemplo, um objeto **Field** em uma coleção **Fields** de um objeto **Recordset** pode herdar propriedades do objeto base **TableDef** ou **QueryDef**.

Para referir-se a um objeto **Property** incorporado em uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:

- *object***. Propriedades**(0)

- *object***. Properties**("* name*")

- *object***. Nome das** \! \[* propriedades*\]

Para uma propriedade incorporada, você também pode usar esta sintaxe:

- *objeto*. *name*

> [!NOTE]
> Para uma propriedade definida pelo usuário, você deve usar o objeto *completo***. Sintaxe de** propriedades ("* nome*").

Com as mesmas formas de sintaxe, você também pode referir-se à propriedade **Value** de um objeto **Property**. O contexto da referência determinará se você está se referindo ao objeto **Property** propriamente dito ou à propriedade **Value** do objeto **Property**.

