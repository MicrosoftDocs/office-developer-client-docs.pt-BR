---
title: 'Capítulo 12: Tutorial RDS'
TOCTitle: 'Chapter 12: RDS Tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a482da49bb78a74cc68f589c928ffe13dd4a54ad
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464832"
---
# <a name="chapter-12-rds-tutorial"></a>Capítulo 12: Tutorial RDS


**Aplica-se a**: Access 2013 | Office 2013

Este tutorial ilustra o uso do modelo de programação RDS para consultar e atualizar uma fonte de dados. Primeiramente, ele descreve as etapas necessárias para realizar essa tarefa. Em seguida, o tutorial é repetido no Microsoft® Visual Basic Scripting Edition e Microsoft® Visual J++®, caracterizando o ADO para Windows Foundation Classes (ADO/WFC).

Este tutorial é codificado em diferentes linguagens por dois motivos:

  - A documentação do RDS assume os códigos do leitor no Visual Basic. Isso torna a documentação conveniente para programadores do Visual Basic, mas menos útil para os programadores que utilizam outras linguagens.

  - Se você não estiver certo quanto a um determinado recurso RDS e conhecer um pouco de outra linguagem, pode conseguir resolver sua questão para o mesmo recurso expresso em outra linguagem.

## <a name="how-the-tutorial-is-presented"></a>Como o tutorial é apresentado

Esse tutorial é baseado no modelo de programação RDS. Ele discute cada etapa do modelo de programação individualmente. Além disso, ilustra cada etapa com um fragmento do código do Visual Basic.

O exemplo do código é repetido em outras linguagens com a discussão mínima. Cada etapa em um determinado tutorial de linguagem de programação está marcado com a etapa correspondente no modelo de programação e tutorial descritivo. Utilize o número da etapa para se referir à discussão no tutorial descritivo.

O modelo de programação RDS está indicado abaixo. Utilize-o como um roteiro conforme avança no tutorial.

## <a name="rds-programming-model-with-objects"></a>Modelo de programação RDS com objetos

  - Especifique o programa a ser chamado no servidor e obtenha uma maneira (proxy) de se referir a ele a partir do cliente.

  - Chame o programa do servidor. Transmita os parâmetros ao programa do servidor que identifica a fonte de dados e o comando a ser emitido.

  - O programa do servidor obtém um objeto [Recordset](recordset-object-ado.md) da fonte de dados, geralmente usando o ADO. Opcionalmente, o objeto **Recordset** é processado no servidor.

  - O programa do servidor retorna o objeto **Recordset** final ao aplicativo cliente.

  - No cliente, o objeto **Recordset** é colocado opcionalmente em um formulário que pode ser facilmente usado por controle visuais.

  - As alterações ao objeto **Recordset** são enviadas de volta ao servidor e utilizadas para atualizar a fonte de dados.
