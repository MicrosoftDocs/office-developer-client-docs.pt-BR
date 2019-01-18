---
title: Usando o objeto de Conexão (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d16b802140e2dcbbd85988bee316ae27236c3235
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706692"
---
# <a name="using-the-connection-object-access"></a><span data-ttu-id="2f5a2-102">Usando o objeto de Conexão (Access)</span><span class="sxs-lookup"><span data-stu-id="2f5a2-102">Using the Connection object (Access)</span></span>


<span data-ttu-id="2f5a2-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f5a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2f5a2-p101">Um objeto **Connection** representa uma única sessão com uma fonte de dados. No caso de um sistema de banco de dados cliente/servidor, pode ser equivalente a uma conexão de rede real ao servidor. Dependendo da funcionalidade suportada pelo provedor, algumas coleções, métodos ou propriedades de um objeto **Connection** pode não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-p101">A **Connection** object represents a unique session with a data source. In the case of a client/server database system, it can be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object might not be available.</span></span>

<span data-ttu-id="2f5a2-107">Antes de abrir um objeto **Connection**, você deve definir determinadas informações sobre a fonte de dados e o tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-107">Before opening a **Connection** object, you must define certain information about the data source and type of connection.</span></span> <span data-ttu-id="2f5a2-108">O parâmetro *ConnectionString* do método **Open** do objeto de **Conexão** — ou a propriedade **ConnectionString** no objeto de **Conexão** — geralmente contém a maioria dessas informações.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-108">The *ConnectionString* parameter of the **Connection** object **Open** method — or the **ConnectionString** property on the **Connection** object — usually contains most of this information.</span></span> <span data-ttu-id="2f5a2-109">Uma sequência de conexão é uma sequência de caracteres que define um número de variáveis de argumentos.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-109">A connection string is a string of characters that defines a variable number of arguments.</span></span> <span data-ttu-id="2f5a2-110">Os argumentos  alguns exigidos por ADO, mas outros específicos do provedor  contêm informações que o objeto **Connection** deve ter para executar este trabalho.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-110">The arguments — some required by ADO, but others provider-specific — contain information that the **Connection** object must have to carry out its work.</span></span> <span data-ttu-id="2f5a2-111">Os argumentos que compõem o parâmetro *ConnectionString* são separados por ponto e vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="2f5a2-111">The arguments that make up the *ConnectionString* parameter are separated with semicolons (;).</span></span>

> [!NOTE]
> <span data-ttu-id="2f5a2-p103">Você também pode especificar um Nome da fonte de dados (DSN) ODBC ou um arquivo Data Link (UDL) em uma sequência de conexão. Para obter mais informações sobre DSNs, consulte as Fontes de dados na Parte 1 da *Referência do Programador ODBC*. Para obter mais informações sobre UDLs, consulte a Visão geral da API do Data Link na *Referência do Programador OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-p103">You can also specify an ODBC Data Source Name (DSN) or a Data Link (UDL) file in a connection string. For more information about DSNs, see Data Sources in Part 1 of the *ODBC Programmer's Reference*. For more information about UDLs, see Data Link API Overview in the *OLE DB Programmer's Reference*.</span></span>

<span data-ttu-id="2f5a2-115">Esta seção inclui os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="2f5a2-115">This section includes the following topics:</span></span>

- [<span data-ttu-id="2f5a2-116">Criação da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="2f5a2-116">Creating the connection string</span></span>](creating-the-connection-string.md)
- [<span data-ttu-id="2f5a2-117">Controlando transações</span><span class="sxs-lookup"><span data-stu-id="2f5a2-117">Controlling transactions</span></span>](controlling-transactions.md)
