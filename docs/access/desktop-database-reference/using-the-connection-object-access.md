---
title: Usando o objeto de Conexão (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0ffc93c2d09c185ea7eaa4a9291ec87aaa72d5eb
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943567"
---
# <a name="using-the-connection-object-access"></a>Usando o objeto de Conexão (Access)


**Aplica-se a**: Access 2013, o Office 2013

Um objeto **Connection** representa uma única sessão com uma fonte de dados. No caso de um sistema de banco de dados cliente/servidor, pode ser equivalente a uma conexão de rede real ao servidor. Dependendo da funcionalidade suportada pelo provedor, algumas coleções, métodos ou propriedades de um objeto **Connection** pode não estar disponível.

Antes de abrir um objeto **Connection**, você deve definir determinadas informações sobre a fonte de dados e o tipo de conexão. O parâmetro *ConnectionString* do método **Open** do objeto de **Conexão** — ou a propriedade **ConnectionString** no objeto de **Conexão** — geralmente contém a maioria dessas informações. Uma sequência de conexão é uma sequência de caracteres que define um número de variáveis de argumentos. Os argumentos  alguns exigidos por ADO, mas outros específicos do provedor  contêm informações que o objeto **Connection** deve ter para executar este trabalho. Os argumentos que compõem o parâmetro *ConnectionString* são separados por ponto e vírgula (;).

> [!NOTE]
> Você também pode especificar um Nome da fonte de dados (DSN) ODBC ou um arquivo Data Link (UDL) em uma sequência de conexão. Para obter mais informações sobre DSNs, consulte as Fontes de dados na Parte 1 da *Referência do Programador ODBC*. Para obter mais informações sobre UDLs, consulte a Visão geral da API do Data Link na *Referência do Programador OLE DB*.

Esta seção inclui os seguintes tópicos:

- [Criação da cadeia de conexão](creating-the-connection-string.md)

- [Controlando transações](controlling-transactions.md)
