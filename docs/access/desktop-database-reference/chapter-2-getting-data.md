---
title: 'Capítulo 2: Obtenção de dados'
TOCTitle: 'Chapter 2: Getting data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f059e5dfe064442f10972fd36344e64f84fe7ea5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296441"
---
# <a name="chapter-2-getting-data"></a><span data-ttu-id="54395-102">Capítulo 2: Obtenção de dados</span><span class="sxs-lookup"><span data-stu-id="54395-102">Chapter 2: Getting data</span></span>

<span data-ttu-id="54395-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54395-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54395-p101">O capítulo anterior apresentou quatro operações principais envolvidas na criação de um aplicativo ADO: obtenção de dados, exame de dados, edição de dados e atualização de dados. Este capítulo se concentrará nos detalhes dos conceitos relevantes à primeira operação: obtenção de dados.</span><span class="sxs-lookup"><span data-stu-id="54395-p101">The preceding chapter introduced four primary operations involved in creating an ADO application: getting data, examining data, editing data, and updating data. This chapter will focus on the details of the concepts relevant to the first operation: getting data.</span></span>

<span data-ttu-id="54395-p102">Vários objetos do ADO podem desempenhar um papel nessa operação. Primeiro, você se conecta à fonte de dados usando um objeto **Connection** do ADO (que, às vezes, será criado de forma implícita). Em seguida, você passa instruções à fonte de dados sobre o que deseja fazer usando um objeto **Command** do ADO (que também pode ser criado de forma implícita). O resultado da passagem de um comando para uma fonte de dados e do recebimento de sua resposta normalmente será representado em um objeto **Recordset** do ADO.</span><span class="sxs-lookup"><span data-stu-id="54395-p102">Several ADO objects can play a role in this operation. First you connect to the data source using an ADO **Connection** object (which at times will be created implicitly). Then you pass instructions to the data source about what you want to do using an ADO **Command** object (which also can be created implicitly). The result of passing a command to a data source and receiving its response usually will be represented in an ADO **Recordset** object.</span></span>

<span data-ttu-id="54395-p103">Para obter dados, seu aplicativo deve se comunicar com uma fonte de dados, como um DBMS, um repositório de arquivos ou um arquivo de texto separado por vírgulas. Essa comunicação representa uma *conexão* — o ambiente necessário para o intercâmbio de dados.</span><span class="sxs-lookup"><span data-stu-id="54395-p103">To get data, your application must be in communication with a data source, such as a DBMS, a file store, or a comma-delimited text file. This communication represents a *connection* — the environment necessary for exchanging data.</span></span>

<span data-ttu-id="54395-p104">O modelo de objeto do ADO representa o conceito de uma conexão com o objeto **Connection**  a base sobre a qual grande parte da funcionalidade do ADO é criada. A finalidade de um objeto **Connection** é:</span><span class="sxs-lookup"><span data-stu-id="54395-p104">The ADO object model represents the concept of a connection with the **Connection** object — the foundation upon which much ADO functionality is built. The purpose of a **Connection** object is to:</span></span>

- <span data-ttu-id="54395-114">Definir as informações necessárias para que o ADO se comunique com as fontes de dados e crie sessões.</span><span class="sxs-lookup"><span data-stu-id="54395-114">Define the information ADO needs to communicate with data sources and create sessions.</span></span>

- <span data-ttu-id="54395-115">Definir os recursos transacionais da sessão.</span><span class="sxs-lookup"><span data-stu-id="54395-115">Define the transactional capabilities of the session.</span></span>

- <span data-ttu-id="54395-116">Permitir criar e executar comandos na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="54395-116">Allow you to create and execute commands against the data source.</span></span>

- <span data-ttu-id="54395-p105">Fornecer informações sobre o design da fonte de dados subjacente na forma de conjuntos de linhas de esquema. Para obter mais informações sobre conjuntos de linhas de esquema, consulte [Método OpenSchema](openschema-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="54395-p105">Provide information about the design of the underlying data source in the form of schema rowsets. For more information about schema rowsets, see [OpenSchema Method](openschema-method-ado.md).</span></span>

<span data-ttu-id="54395-119">Este capítulo aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="54395-119">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="54395-120">Criação de uma conexão</span><span class="sxs-lookup"><span data-stu-id="54395-120">Making a connection</span></span>](making-a-connection.md)
- [<span data-ttu-id="54395-121">Usando a referência de objeto de conexão (ADO)</span><span class="sxs-lookup"><span data-stu-id="54395-121">Using the connection object reference (ADO)</span></span>](using-the-connection-object-access.md)
- [<span data-ttu-id="54395-122">Usando a referência de objeto de comando (ADO)</span><span class="sxs-lookup"><span data-stu-id="54395-122">Using the command object reference (ADO)</span></span>](using-the-command-object-access.md)
- [<span data-ttu-id="54395-123">Adicionando dados a um Recordset (ADO)</span><span class="sxs-lookup"><span data-stu-id="54395-123">Adding data to a Recordset (ADO)</span></span>](adding-data-to-a-recordset.md)
