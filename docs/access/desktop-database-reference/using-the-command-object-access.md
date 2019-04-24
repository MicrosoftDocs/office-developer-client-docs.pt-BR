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
# <a name="using-the-command-object-access"></a><span data-ttu-id="f719c-102">Usando o objeto Command (Access)</span><span class="sxs-lookup"><span data-stu-id="f719c-102">Using the Command object (Access)</span></span>


<span data-ttu-id="f719c-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f719c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f719c-p101">Depois de se conectar a uma fonte de dados, você precisa executar as solicitações nela para obter os conjuntos de resultados. O ADO encapsula este tipo de funcionalidade de comando no objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="f719c-p101">After connecting to a data source, you need to execute requests against it to obtain result sets. ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="f719c-p102">Você pode usar o objeto **Command** para solicitar qualquer tipo de operação do provedor, considerando que o provedor pode interpretar a sequência do comando adequadamente. Uma operação comum para os provedores de dados é consultar um banco de dados e retornar os registros em um objeto **Recordset**. **Recordset**s serão abordados posteriormente neste e em outros capítulos; por enquanto, considere-os como ferramentas para manter e visualizar os conjuntos de resultados. Como com muitos objetos ADO, dependendo da funcionalidade do provedor, algumas propriedades, métodos e coleções do objeto **Command** podem gerar erros quando mencionados.</span><span class="sxs-lookup"><span data-stu-id="f719c-p102">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly. A common operation for data providers is to query a database and return records in a **Recordset** object. **Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets. As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="f719c-p103">Nem sempre é necessário criar um objeto **Command** para executar um comando em uma fonte de dados. Você pode usar o método **Execute** no objeto **Connection** ou o método **Open** no objeto **Recordset**. Contudo, você deveria usar um objeto **Command** se precisar usar novamente um comando em seu código ou se precisar transmitir informações detalhadas sobre o parâmetro com seu comando. Esses cenários são abordados em detalhes posteriormente neste capítulo.</span><span class="sxs-lookup"><span data-stu-id="f719c-p103">It is not always necessary to create a **Command** object to execute a command against a data source. You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object. However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command. These scenarios are covered in more detail later in this chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="f719c-114">Determinados Commands podem retornar um resultado como um fluxo binário ou como um único Record em vez de um Recordset se houver suporte para isso pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="f719c-114">Certain Commands can return a result set as a binary stream or as a single Record rather than as a Recordset, if this is supported by the provider.</span></span> <span data-ttu-id="f719c-115">Além disso, alguns Commands não são destinados a retornar qualquer conjunto de resultados (por exemplo, uma consulta SQL Update).</span><span class="sxs-lookup"><span data-stu-id="f719c-115">Also, some Commands are not intended to return any result set at all (for example, a SQL Update query).</span></span> <span data-ttu-id="f719c-116">Este capítulo abordará o cenário mais comum, contudo executando Commands que retornam resultados em um objeto Recordset.</span><span class="sxs-lookup"><span data-stu-id="f719c-116">This chapter will cover the most typical scenario, however: executing Commands that return results into a Recordset object.</span></span> <span data-ttu-id="f719c-117">Para obter mais informações sobre o retorno de resultados em  Records ou Streams, consulte [Capítulo 10: Records e Streams](chapter-10-records-and-streams.md).</span><span class="sxs-lookup"><span data-stu-id="f719c-117">For more information about returning results into Records or Streams, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

<span data-ttu-id="f719c-118">Esta seção inclui os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="f719c-118">This section includes the following topics:</span></span>

- [<span data-ttu-id="f719c-119">Visão geral do objeto Command</span><span class="sxs-lookup"><span data-stu-id="f719c-119">Command object overview</span></span>](command-object-overview.md)
- [<span data-ttu-id="f719c-120">Criação e execução de um comando simples</span><span class="sxs-lookup"><span data-stu-id="f719c-120">Creating and executing a simple command</span></span>](creating-and-executing-a-simple-command.md)
- [<span data-ttu-id="f719c-121">Parâmetros do objeto Command</span><span class="sxs-lookup"><span data-stu-id="f719c-121">Command object parameters</span></span>](command-object-parameters.md)
- [<span data-ttu-id="f719c-122">Chamada de um procedimento armazenado com um comando</span><span class="sxs-lookup"><span data-stu-id="f719c-122">Calling a stored procedure with a command</span></span>](calling-a-stored-procedure-with-a-command.md)
- [<span data-ttu-id="f719c-123">Comandos nomeados</span><span class="sxs-lookup"><span data-stu-id="f719c-123">Named commands</span></span>](named-commands.md)
