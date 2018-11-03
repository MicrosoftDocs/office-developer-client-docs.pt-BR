---
title: 'Capítulo 12: Tutorial RDS'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 276e8989b674c61414c42428bbff795bf700c6dc
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947676"
---
# <a name="chapter-12-rds-tutorial"></a><span data-ttu-id="3e700-102">Capítulo 12: Tutorial RDS</span><span class="sxs-lookup"><span data-stu-id="3e700-102">Chapter 12: RDS tutorial</span></span>

<span data-ttu-id="3e700-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e700-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e700-104">Este tutorial ilustra o uso do modelo de programação RDS para consultar e atualizar uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="3e700-104">This tutorial illustrates using the RDS programming model to query and update a data source.</span></span> <span data-ttu-id="3e700-105">Primeiramente, ele descreve as etapas necessárias para realizar essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="3e700-105">First, it describes the steps necessary to accomplish this task.</span></span> <span data-ttu-id="3e700-106">Em seguida, o tutorial é repetido no Microsoft Visual Basic Scripting Edition e Microsoft Visual J++, apresentando o ADO for Windows Foundation Classes (ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="3e700-106">Then the tutorial is repeated in Microsoft Visual Basic Scripting Edition and Microsoft Visual J++, featuring ADO for Windows Foundation Classes (ADO/WFC).</span></span>

<span data-ttu-id="3e700-107">Este tutorial é codificado em diferentes linguagens por dois motivos:</span><span class="sxs-lookup"><span data-stu-id="3e700-107">This tutorial is coded in different languages for two reasons:</span></span>

- <span data-ttu-id="3e700-p102">A documentação do RDS assume os códigos do leitor no Visual Basic. Isso torna a documentação conveniente para programadores do Visual Basic, mas menos útil para os programadores que utilizam outras linguagens.</span><span class="sxs-lookup"><span data-stu-id="3e700-p102">The documentation for RDS assumes the reader codes in Visual Basic. This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</span></span>

- <span data-ttu-id="3e700-110">Se você não estiver certo quanto a um determinado recurso RDS e conhecer um pouco de outra linguagem, pode conseguir resolver sua questão para o mesmo recurso expresso em outra linguagem.</span><span class="sxs-lookup"><span data-stu-id="3e700-110">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</span></span>

## <a name="how-the-tutorial-is-presented"></a><span data-ttu-id="3e700-111">Como o tutorial é apresentado</span><span class="sxs-lookup"><span data-stu-id="3e700-111">How the tutorial is presented</span></span>

<span data-ttu-id="3e700-p103">Esse tutorial é baseado no modelo de programação RDS. Ele discute cada etapa do modelo de programação individualmente. Além disso, ilustra cada etapa com um fragmento do código do Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3e700-p103">This tutorial is based on the RDS programming model. It discusses each step of the programming model individually. In addition, it illustrates each step with a fragment of Visual Basic code.</span></span>

<span data-ttu-id="3e700-p104">O exemplo do código é repetido em outras linguagens com a discussão mínima. Cada etapa em um determinado tutorial de linguagem de programação está marcado com a etapa correspondente no modelo de programação e tutorial descritivo. Utilize o número da etapa para se referir à discussão no tutorial descritivo.</span><span class="sxs-lookup"><span data-stu-id="3e700-p104">The code example is repeated in other languages with minimal discussion. Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial. Use the number of the step to refer to the discussion in the descriptive tutorial.</span></span>

<span data-ttu-id="3e700-p105">O modelo de programação RDS está indicado abaixo. Utilize-o como um roteiro conforme avança no tutorial.</span><span class="sxs-lookup"><span data-stu-id="3e700-p105">The RDS programming model is stated below. Use it as a roadmap as you proceed through the tutorial.</span></span>

## <a name="rds-programming-model-with-objects"></a><span data-ttu-id="3e700-120">Modelo de programação RDS com objetos</span><span class="sxs-lookup"><span data-stu-id="3e700-120">RDS programming model with objects</span></span>

- <span data-ttu-id="3e700-121">Especifique o programa a ser chamado no servidor e obtenha uma maneira (proxy) de se referir a ele a partir do cliente.</span><span class="sxs-lookup"><span data-stu-id="3e700-121">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</span></span>

- <span data-ttu-id="3e700-p106">Chame o programa do servidor. Transmita os parâmetros ao programa do servidor que identifica a fonte de dados e o comando a ser emitido.</span><span class="sxs-lookup"><span data-stu-id="3e700-p106">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue.</span></span>

- <span data-ttu-id="3e700-p107">O programa do servidor obtém um objeto [Recordset](recordset-object-ado.md) da fonte de dados, geralmente usando o ADO. Opcionalmente, o objeto **Recordset** é processado no servidor.</span><span class="sxs-lookup"><span data-stu-id="3e700-p107">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="3e700-126">O programa do servidor retorna o objeto **Recordset** final ao aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="3e700-126">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="3e700-127">No cliente, o objeto **Recordset** é colocado opcionalmente em um formulário que pode ser facilmente usado por controle visuais.</span><span class="sxs-lookup"><span data-stu-id="3e700-127">On the client, the **Recordset** object is optionally put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="3e700-128">As alterações ao objeto **Recordset** são enviadas de volta ao servidor e utilizadas para atualizar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="3e700-128">Changes to the **Recordset** object are sent back to the server and used to update the data source.</span></span>

<span data-ttu-id="3e700-129">Estas são as etapas neste tutorial:</span><span class="sxs-lookup"><span data-stu-id="3e700-129">Following are the steps in this tutorial:</span></span>

- [<span data-ttu-id="3e700-130">Etapa 1: Especificar um programa de servidor</span><span class="sxs-lookup"><span data-stu-id="3e700-130">Step 1: Specify a server program</span></span>](step-1-specify-a-server-program-rds-tutorial.md)
- [<span data-ttu-id="3e700-131">Etapa 2: Chamar o programa do servidor</span><span class="sxs-lookup"><span data-stu-id="3e700-131">Step 2: Invoke the server program</span></span>](step-2-invoke-the-server-program-rds-tutorial.md)
- [<span data-ttu-id="3e700-132">Etapa 3: O servidor obtém um Recordset</span><span class="sxs-lookup"><span data-stu-id="3e700-132">Step 3: Server obtains a Recordset</span></span>](step-3-server-obtains-a-recordset-rds-tutorial.md)
- [<span data-ttu-id="3e700-133">Etapa 4: Servidor retorna o Recordset</span><span class="sxs-lookup"><span data-stu-id="3e700-133">Step 4: Server returns the Recordset</span></span>](step-4-server-returns-the-recordset-rds-tutorial.md)
- [<span data-ttu-id="3e700-134">Etapa 5: DataControl torna-se disponível</span><span class="sxs-lookup"><span data-stu-id="3e700-134">Step 5: DataControl is made usable</span></span>](step-5-datacontrol-is-made-usable-rds-tutorial.md)
- [<span data-ttu-id="3e700-135">Etapa 6: As alterações são enviadas ao servidor</span><span class="sxs-lookup"><span data-stu-id="3e700-135">Step 6: Changes are sent to the server</span></span>](step-6-changes-are-sent-to-the-server-rds-tutorial.md)
- [<span data-ttu-id="3e700-136">Tutorial do RDS (VBScript)</span><span class="sxs-lookup"><span data-stu-id="3e700-136">RDS tutorial (VBScript)</span></span>](rds-tutorial-vbscript.md)
- [<span data-ttu-id="3e700-137">Tutorial do RDS (Visual J++)</span><span class="sxs-lookup"><span data-stu-id="3e700-137">RDS tutorial (Visual J++)</span></span>](rds-tutorial-visual-j.md)