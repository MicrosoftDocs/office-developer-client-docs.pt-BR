---
title: Usando o objeto Command (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b89d292d86035e565ad18413062274dfbfc74db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312023"
---
# <a name="using-the-command-object-access"></a>Usando o objeto Command (Access)


**Aplica-se ao:** Access 2013, Office 2013

Depois de se conectar a uma fonte de dados, você precisa executar as solicitações nela para obter os conjuntos de resultados. O ADO encapsula este tipo de funcionalidade de comando no objeto **Command**.

Você pode usar o objeto **Command** para solicitar qualquer tipo de operação do provedor, considerando que o provedor pode interpretar a sequência do comando adequadamente. Uma operação comum para os provedores de dados é consultar um banco de dados e retornar os registros em um objeto **Recordset**. **Recordset**s serão abordados posteriormente neste e em outros capítulos; por enquanto, considere-os como ferramentas para manter e visualizar os conjuntos de resultados. Como com muitos objetos ADO, dependendo da funcionalidade do provedor, algumas propriedades, métodos e coleções do objeto **Command** podem gerar erros quando mencionados.

Nem sempre é necessário criar um objeto **Command** para executar um comando em uma fonte de dados. Você pode usar o método **Execute** no objeto **Connection** ou o método **Open** no objeto **Recordset**. Contudo, você deveria usar um objeto **Command** se precisar usar novamente um comando em seu código ou se precisar transmitir informações detalhadas sobre o parâmetro com seu comando. Esses cenários são abordados em detalhes posteriormente neste capítulo.

> [!NOTE]
> Determinados Commands podem retornar um resultado como um fluxo binário ou como um único Record em vez de um Recordset se houver suporte para isso pelo provedor. Além disso, alguns Commands não são destinados a retornar qualquer conjunto de resultados (por exemplo, uma consulta SQL Update). Este capítulo abordará o cenário mais comum, contudo executando Commands que retornam resultados em um objeto Recordset. Para obter mais informações sobre o retorno de resultados em  Records ou Streams, consulte [Capítulo 10: Records e Streams](chapter-10-records-and-streams.md).

Esta seção inclui os seguintes tópicos:

- [Visão geral do objeto Command](command-object-overview.md)
- [Criação e execução de um comando simples](creating-and-executing-a-simple-command.md)
- [Parâmetros do objeto Command](command-object-parameters.md)
- [Chamada de um procedimento armazenado com um comando](calling-a-stored-procedure-with-a-command.md)
- [Comandos nomeados](named-commands.md)
