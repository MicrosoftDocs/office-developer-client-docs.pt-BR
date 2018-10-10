---
title: Usando o objeto de Conexão (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd3e691258fe5950f40c36a1efcaed8e79810c7a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463162"
---
# <a name="using-the-connection-object-access"></a><span data-ttu-id="0c221-102">Usando o objeto de Conexão (Access)</span><span class="sxs-lookup"><span data-stu-id="0c221-102">Using the Connection Object (Access)</span></span>


<span data-ttu-id="0c221-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c221-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0c221-p101">Um objeto **Connection** representa uma única sessão com uma fonte de dados. No caso de um sistema de banco de dados cliente/servidor, pode ser equivalente a uma conexão de rede real ao servidor. Dependendo da funcionalidade suportada pelo provedor, algumas coleções, métodos ou propriedades de um objeto **Connection** pode não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="0c221-p101">A **Connection** object represents a unique session with a data source. In the case of a client/server database system, it can be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object might not be available.</span></span>

<span data-ttu-id="0c221-107">Antes de abrir um objeto **Connection**, você deve definir determinadas informações sobre a fonte de dados e o tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="0c221-107">Before opening a **Connection** object, you must define certain information about the data source and type of connection.</span></span> <span data-ttu-id="0c221-108">O parâmetro *ConnectionString* do método **Open** do objeto de **Conexão** — ou a propriedade **ConnectionString** no objeto de **Conexão** — geralmente contém a maioria dessas informações.</span><span class="sxs-lookup"><span data-stu-id="0c221-108">The *ConnectionString* parameter of the **Connection** object **Open** method — or the **ConnectionString** property on the **Connection** object — usually contains most of this information.</span></span> <span data-ttu-id="0c221-109">Uma sequência de conexão é uma sequência de caracteres que define um número de variáveis de argumentos.</span><span class="sxs-lookup"><span data-stu-id="0c221-109">A connection string is a string of characters that defines a variable number of arguments.</span></span> <span data-ttu-id="0c221-110">Os argumentos  alguns exigidos por ADO, mas outros específicos do provedor  contêm informações que o objeto **Connection** deve ter para executar este trabalho.</span><span class="sxs-lookup"><span data-stu-id="0c221-110">The arguments — some required by ADO, but others provider-specific — contain information that the **Connection** object must have to carry out its work.</span></span> <span data-ttu-id="0c221-111">Os argumentos que compõem o parâmetro *ConnectionString* são separados por ponto e vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="0c221-111">The arguments that make up the *ConnectionString* parameter are separated with semicolons (;).</span></span>


> [!NOTE]
> <P><span data-ttu-id="0c221-p103">Você também pode especificar um Nome da fonte de dados (DSN) ODBC ou um arquivo Data Link (UDL) em uma sequência de conexão. Para obter mais informações sobre DSNs, consulte as Fontes de dados na Parte 1 da <EM>Referência do Programador ODBC</EM>. Para obter mais informações sobre UDLs, consulte a Visão geral da API do Data Link na <EM>Referência do Programador OLE DB</EM>.</span><span class="sxs-lookup"><span data-stu-id="0c221-p103">You can also specify an ODBC Data Source Name (DSN) or a Data Link (UDL) file in a connection string. For more information about DSNs, see Data Sources in Part 1 of the <EM>ODBC Programmer's Reference</EM>. For more information about UDLs, see Data Link API Overview in the <EM>OLE DB Programmer's Reference</EM>.</span></span></P>


