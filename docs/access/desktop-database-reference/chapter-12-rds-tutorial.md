---
title: 'Capítulo 12: Tutorial do RDS'
TOCTitle: 'Chapter 12: RDS Tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aec7c9a89ea078bfad9b05d664d373831491edc4
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860221"
---
# <a name="chapter-12-rds-tutorial"></a>Capítulo 12: Tutorial do RDS


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

Estas são as etapas neste tutorial:

- [Etapa 1: Especificar um programa do servidor (Tutorial do RDS)](step-1-specify-a-server-program-rds-tutorial.md)

- [Etapa 2: Chamar um programa do servidor (Tutorial do RDS)](step-2-invoke-the-server-program-rds-tutorial.md)

- [Etapa 3: O servidor obtém um conjunto de registros (Tutorial do RDS)](step-3-server-obtains-a-recordset-rds-tutorial.md)

- [Etapa 4: O servidor retorna um conjunto de registros (Tutorial do RDS)](step-4-server-returns-the-recordset-rds-tutorial.md)

- [Etapa 5: DataControl torna-se utilizável (Tutorial do RDS)](step-5-datacontrol-is-made-usable-rds-tutorial.md)

- [Etapa 6: As alterações são enviadas ao servidor (Tutorial do RDS)](step-6-changes-are-sent-to-the-server-rds-tutorial.md)

- [Tutorial do RDS (VBScript)](rds-tutorial-vbscript.md)

- [Tutorial RDS (Visual J++)](rds-tutorial-visual-j.md)