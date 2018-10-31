---
title: 'Capítulo 2: Obtenção de dados'
TOCTitle: 'Chapter 2: Getting Data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 601d18373f5bcd0a9ed6777fa50c2a3ed631594a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860886"
---
# <a name="chapter-2-getting-data"></a>Capítulo 2: Obtenção de dados


**Aplica-se a**: Access 2013 | Office 2013

O capítulo anterior apresentou quatro operações principais envolvidas na criação de um aplicativo ADO: obtenção de dados, exame de dados, edição de dados e atualização de dados. Este capítulo se concentrará nos detalhes dos conceitos relevantes à primeira operação: obtenção de dados.

Vários objetos do ADO podem desempenhar um papel nessa operação. Primeiro, você se conecta à fonte de dados usando um objeto **Connection** do ADO (que, às vezes, será criado de forma implícita). Em seguida, você passa instruções à fonte de dados sobre o que deseja fazer usando um objeto **Command** do ADO (que também pode ser criado de forma implícita). O resultado da passagem de um comando para uma fonte de dados e do recebimento de sua resposta normalmente será representado em um objeto **Recordset** do ADO.

Para obter dados, seu aplicativo deve se comunicar com uma fonte de dados, como um DBMS, um repositório de arquivos ou um arquivo de texto separado por vírgulas. Essa comunicação representa uma *conexão* — o ambiente necessário para intercâmbio de dados.

O modelo de objeto do ADO representa o conceito de uma conexão com o objeto **Connection**  a base sobre a qual grande parte da funcionalidade do ADO é criada. A finalidade de um objeto **Connection** é:

  - Definir as informações necessárias para que o ADO se comunique com as fontes de dados e crie sessões.

  - Definir os recursos transacionais da sessão.

  - Permitir criar e executar comandos na fonte de dados.

  - Fornecer informações sobre o design da fonte de dados subjacente na forma de conjuntos de linhas de esquema. Para obter mais informações sobre conjuntos de linhas de esquema, consulte [Método OpenSchema](openschema-method-ado.md).

Este capítulo aborda os seguintes tópicos:

  - [Criação de uma conexão](making-a-connection.md)

  - [Usando a referência de objeto de Conexão (ADO)](using-the-connection-object-access.md)

  - [Usando a referência de objeto Command (ADO)](using-the-command-object-access.md)

  - [Adicionando dados a um Recordset (ADO)](adding-data-to-a-recordset.md)