---
title: Usando o objeto Command (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d55fd58daf13fa0f3995480f35da4ccc0f17ac5c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946682"
---
# <a name="using-the-command-object-access"></a><span data-ttu-id="6b693-102">Usando o objeto Command (Access)</span><span class="sxs-lookup"><span data-stu-id="6b693-102">Using the Command object (Access)</span></span>


<span data-ttu-id="6b693-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b693-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6b693-p101">Depois de se conectar a uma fonte de dados, você precisa executar as solicitações nela para obter os conjuntos de resultados. O ADO encapsula este tipo de funcionalidade de comando no objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="6b693-p101">After connecting to a data source, you need to execute requests against it to obtain result sets. ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="6b693-p102">Você pode usar o objeto **Command** para solicitar qualquer tipo de operação do provedor, considerando que o provedor pode interpretar a sequência do comando adequadamente. Uma operação comum para os provedores de dados é consultar um banco de dados e retornar os registros em um objeto **Recordset**. **Recordset**s serão abordados posteriormente neste e em outros capítulos; por enquanto, considere-os como ferramentas para manter e visualizar os conjuntos de resultados. Como com muitos objetos ADO, dependendo da funcionalidade do provedor, algumas propriedades, métodos e coleções do objeto **Command** podem gerar erros quando mencionados.</span><span class="sxs-lookup"><span data-stu-id="6b693-p102">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly. A common operation for data providers is to query a database and return records in a **Recordset** object. **Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets. As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="6b693-p103">Nem sempre é necessário criar um objeto **Command** para executar um comando em uma fonte de dados. Você pode usar o método **Execute** no objeto **Connection** ou o método **Open** no objeto **Recordset**. Contudo, você deveria usar um objeto **Command** se precisar usar novamente um comando em seu código ou se precisar transmitir informações detalhadas sobre o parâmetro com seu comando. Esses cenários são abordados em detalhes posteriormente neste capítulo.</span><span class="sxs-lookup"><span data-stu-id="6b693-p103">It is not always necessary to create a **Command** object to execute a command against a data source. You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object. However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command. These scenarios are covered in more detail later in this chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="6b693-114">Determinados comandos podem retornar um resultado definido como um fluxo binário ou como um único registro e não como um Recordset, se isso for suportado pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="6b693-114">Certain Commands can return a result set as a binary stream or as a single Record rather than as a Recordset, if this is supported by the provider.</span></span> <span data-ttu-id="6b693-115">Além disso, alguns comandos não visam retornar qualquer resultado definido em todos os (por exemplo, uma consulta SQL Update).</span><span class="sxs-lookup"><span data-stu-id="6b693-115">Also, some Commands are not intended to return any result set at all (for example, a SQL Update query).</span></span> <span data-ttu-id="6b693-116">Este capítulo abordará o cenário mais comum, no entanto: executar comandos que retornam resultados em um objeto Recordset.</span><span class="sxs-lookup"><span data-stu-id="6b693-116">This chapter will cover the most typical scenario, however: executing Commands that return results into a Recordset object.</span></span> <span data-ttu-id="6b693-117">Para obter mais informações sobre como retornar resultados em registros ou fluxos, consulte [Capítulo 10: Records e Streams](chapter-10-records-and-streams.md).</span><span class="sxs-lookup"><span data-stu-id="6b693-117">For more information about returning results into Records or Streams, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

<span data-ttu-id="6b693-118">Esta seção inclui os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="6b693-118">This section includes the following topics:</span></span>

- [<span data-ttu-id="6b693-119">Visão geral do objeto Command</span><span class="sxs-lookup"><span data-stu-id="6b693-119">Command Object Overview</span></span>](command-object-overview.md)

- [<span data-ttu-id="6b693-120">Criação e execução de um comando simples</span><span class="sxs-lookup"><span data-stu-id="6b693-120">Creating and Executing a Simple Command</span></span>](creating-and-executing-a-simple-command.md)

- [<span data-ttu-id="6b693-121">Parâmetros do objeto Command</span><span class="sxs-lookup"><span data-stu-id="6b693-121">Command Object Parameters</span></span>](command-object-parameters.md)

- [<span data-ttu-id="6b693-122">Chamada de um procedimento armazenado com um comando</span><span class="sxs-lookup"><span data-stu-id="6b693-122">Calling a Stored Procedure with a Command</span></span>](calling-a-stored-procedure-with-a-command.md)

- [<span data-ttu-id="6b693-123">Comandos nomeados</span><span class="sxs-lookup"><span data-stu-id="6b693-123">Named Commands</span></span>](named-commands.md)
