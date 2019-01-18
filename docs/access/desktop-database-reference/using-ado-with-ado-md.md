---
title: Usando o ADO com o ADO MD
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 80c87f57a96f98de704e3cfa9b7689a522e4a7af
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721932"
---
# <a name="using-ado-with-ado-md"></a>Usando o ADO com o ADO MD


**Aplica-se a**: Access 2013, o Office 2013

O ADO e o ADO MD são modelos de objeto relacionados, porém, separados. O ADO oferece objetos para conexão a fontes de dados, execução de comandos, recuperação de dados tabulares e metadados de esquema em um formato tabular e exibição de informações de erro do provedor. O ADO MD fornece objetos para recuperação de dados multidimensionais e exibição de metadados de esquemas multidimensionais.

Ao trabalhar com um MDP, você pode usar o ADO, o ADO MD ou ambos com seu aplicativo. Fazendo referência às duas bibliotecas do projeto, você terá acesso total à funcionalidade fornecida pelo MDP.

É sempre útil que os consumidores obtenham uma exibição plana e tabular de um conjunto de dados multidimensional. Para isso, basta usar o objeto [Recordset](recordset-object-ado.md) do ADO. Especifica a fonte para seu [conjunto de células](cellset-object-ado-md.md) , como o parâmetro ***Source*** do método [Open](open-method-ado-recordset.md) de um **Recordset**, e não como a origem para um **conjunto de células**do ADO MD.

Também pode ser útil exibir o metadados do esquema em um modo de exibição tabular, e não como uma hierarquia de objetos. O método [OpenSchema](openschema-method-ado.md) do ADO no objeto [Connection](connection-object-ado.md) permite que o usuário abra um **Recordset** que contém informações de esquema. O parâmetro ***QueryType*** do método **OpenSchema** tem vários valores de [SchemaEnum](schemaenum.md) relacionados especificamente ao MDPs. Estes são os valores:

  - **adSchemaCubes**

  - **adSchemaDimensions**

  - **adSchemaHierarchies**

  - **adSchemaLevels**

  - **adSchemaMeasures**

  - **adSchemaMembers**

Para usar os valores enumerados do ADO com as propriedades ou os métodos do ADO MD, seu projeto deve fazer referência às bibliotecas do ADO e do ADO MD. Por exemplo, você pode usar os valores enumerados **adState** do ADO com a propriedade [State](state-property-ado-md.md) do ADO MD. Para obter mais informações sobre como estabelecer referências a bibliotecas, consulte a documentação da ferramenta de desenvolvimento.

Para obter mais informações sobre os objetos e os métodos do ADO, consulte [Referência da API do ADO](ado-api-reference.md).

