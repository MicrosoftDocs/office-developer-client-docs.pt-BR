---
title: Adição de dados a um conjunto de registros
TOCTitle: Adding data to a Recordset
ms:assetid: a3d121a8-f52f-66cd-8849-c3a75aeb276a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249761(v=office.15)
ms:contentKeyID: 48546797
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d16eb5871bfe55af58a89cc06b413e8404df8cb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701393"
---
# <a name="adding-data-to-a-recordset"></a>Adição de dados a um conjunto de registros

**Aplica-se a**: Access 2013, o Office 2013

É provável que o **Recordset** seja o objeto mais utilizado do ADO. No ADO, um **Recordset** é considerado como a combinação de um conjunto de resultados de uma fonte de dados com seus comportamentos de cursor associados. Portanto, você pode incluir dados em um **Recordset** e, em seguida, usar os métodos e as propriedades do **Recordset** para navegar pelas linhas de dados, exibir os valores das linhas e, de outro modo, manipular o conjunto de resultados.

Esta seção se concentrará na adição de dados ao **Recordset**. Para obter informações sobre como navegar pelos dados ou atualizá-los, consulte o [Capítulo 4: Editando dados](chapter-4-editing-data.md) e o [Capítulo 5: Atualizando e persistindo dados](chapter-5-updating-and-persisting-data.md). Nem sempre os recursos avançados de um objeto **Command** são necessários para adicionar o conjunto de resultados a um **Recordset**. Geralmente, você pode executar seu comando definindo a propriedade **Source** no **Recordset** ou passando um sequência de comandos ao método **Open** do objeto **Recordset**.

Há diversas maneiras de adicionar dados da fonte de dados a um **Recordset**. A técnica usada depende das necessidades do aplicativo e dos recursos do provedor.

