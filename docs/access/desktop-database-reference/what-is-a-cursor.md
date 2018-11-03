---
title: O que é um Cursor?  (Referência de banco de dados da área de trabalho do access)
TOCTitle: What is a Cursor?
ms:assetid: cc70d941-05e0-9b14-1c5d-6b1a5802f546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250013(v=office.15)
ms:contentKeyID: 48547738
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0bedbeb041d919cd417ade215ac71b9eabbc4de2
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947592"
---
# <a name="what-is-a-cursor"></a><span data-ttu-id="a9496-103">O que é um cursor?</span><span class="sxs-lookup"><span data-stu-id="a9496-103">What is a cursor?</span></span>


<span data-ttu-id="a9496-104">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9496-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9496-p102">As operações em um banco de dados relacional agem em um conjunto completo de linhas. O conjunto de linha retornado por uma instrução SELECT é composto por todas as linhas que atendem às condições na cláusula WHERE da instrução. Esse conjunto completo de linhas retornado pela instrução é conhecido como o conjunto de resultados. Os aplicativos, especialmente aqueles que são interativos e estão online, nem sempre podem trabalhar de forma eficiente com um conjunto inteiro de resultados como uma unidade. Esses aplicativos precisam de um mecanismo para trabalharem com uma linha ou um pequeno bloco de linhas por vez. Os cursores são uma extensão dos conjuntos de resultados que fornecem esse mecanismo.</span><span class="sxs-lookup"><span data-stu-id="a9496-p102">Operations in a relational database act on a complete set of rows. The set of rows returned by a SELECT statement consists of all the rows that satisfy the conditions in the WHERE clause of the statement. This complete set of rows returned by the statement is known as the result set. Applications, especially those that are interactive and online, cannot always work effectively with the entire result set as a unit. These applications need a mechanism to work with one row or a small block of rows at a time. Cursors are an extension to result sets that provide that mechanism.</span></span>

<span data-ttu-id="a9496-p103">Um cursor é implementado por uma biblioteca de cursores. Esta é um software, normalmente implementado como uma parte do sistema de banco de dados ou uma API de acesso aos dados, utilizada para gerenciar atributos de dados retornados de uma fonte de dados (um conjunto de resultados). Esses atributos incluem gerenciamento simultâneo, posição no conjunto de resultados, número de linhas retornadas e se é possível ou não avançar e/ou voltar no conjunto de resultados (capacidade de navegação).</span><span class="sxs-lookup"><span data-stu-id="a9496-p103">A cursor is implemented by a cursor library. A cursor library is software, often implemented as a part of a database system or a data access API, that is used to manage attributes of data returned from a data source (a result set). These attributes include concurrency management, position in the result set, number of rows returned, and whether or not you can move forward and/or backward through the result set (scrollability).</span></span>

<span data-ttu-id="a9496-p104">Um cursor mantém o controle da posição no conjunto de resultados e permite que você execute várias operações, linha por linha em um conjunto de resultados, com ou sem o retorno para a tabela original. Em outras palavras, os cursores, por definição, retornam um conjunto de resultados com base nas tabelas dentro dos bancos de dados. O cursor é então nomeado porque ele indica a posição atual no conjunto de resultados, assim como o cursor em uma tela do computador indica a posição atual.</span><span class="sxs-lookup"><span data-stu-id="a9496-p104">A cursor keeps track of the position in the result set, and allows you to perform multiple operations row by row against a result set, with or without returning to the original table. In other words, cursors conceptually return a result set based on tables within the databases. The cursor is so named because it indicates the current position in the result set, just as the cursor on a computer screen indicates current position.</span></span>

<span data-ttu-id="a9496-117">É importante familiarizar-se com o conceito de cursores antes de seguir adiante para aprender as especificações de seu uso no ADO.</span><span class="sxs-lookup"><span data-stu-id="a9496-117">It is important to become familiar with the concept of cursors before moving on to learn the specifics of their usage in ADO.</span></span>

<span data-ttu-id="a9496-118">Utilizando os cursores, você pode:</span><span class="sxs-lookup"><span data-stu-id="a9496-118">Using cursors, you can:</span></span>

  - <span data-ttu-id="a9496-119">Especificar o posicionamento em linhas específicas no conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="a9496-119">Specify positioning at specific rows in the result set.</span></span>

  - <span data-ttu-id="a9496-120">Recuperar uma linha ou um bloco de linha com base na posição atual do conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="a9496-120">Retrieve one row or a block of rows based on the current result set position.</span></span>

  - <span data-ttu-id="a9496-121">Modificar dados nas linhas, na posição atual, no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="a9496-121">Modify data in the rows at the current position in the result set.</span></span>

  - <span data-ttu-id="a9496-122">Definir diferentes níveis de importância para as alterações de dados feitas por outros usuários.</span><span class="sxs-lookup"><span data-stu-id="a9496-122">Define different levels of sensitivity to data changes made by other users.</span></span>

<span data-ttu-id="a9496-p105">Por exemplo, considere um aplicativo que mostre a um comprador potencial uma lista de produtos disponíveis. O comprador navega pela lista para ver os detalhes e o preço dos produtos e finalmente seleciona um produto para comprar. Navegação e seleção adicionais ocorrem no restante da lista. Para o comprador, os produtos aparecem um por vez, mas o aplicativo usa um cursor de rolagem para navegar para cima e para baixo no conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="a9496-p105">For example, consider an application that displays a list of available products to a potential buyer. The buyer scrolls through the list to see product details and cost, and finally selects a product for purchase. Additional scrolling and selection occurs for the remainder of the list. As far as the buyer is concerned, the products appear one at a time, but the application uses a scrollable cursor to browse up and down through the result set.</span></span>

<span data-ttu-id="a9496-127">Você pode usar cursores de várias formas:</span><span class="sxs-lookup"><span data-stu-id="a9496-127">You can use cursors in a variety of ways:</span></span>

  - <span data-ttu-id="a9496-128">Sem nenhuma linha.</span><span class="sxs-lookup"><span data-stu-id="a9496-128">With no rows at all.</span></span>

  - <span data-ttu-id="a9496-129">Com algumas ou todas as linhas em uma única tabela.</span><span class="sxs-lookup"><span data-stu-id="a9496-129">With some or all of the rows in a single table.</span></span>

  - <span data-ttu-id="a9496-130">Com algumas ou todas as linhas a partir de tabelas unidas de forma lógica.</span><span class="sxs-lookup"><span data-stu-id="a9496-130">With some or all of the rows from logically joined tables.</span></span>

  - <span data-ttu-id="a9496-131">Como somente-leitura ou atualizáveis no nível de cursor ou de campo.</span><span class="sxs-lookup"><span data-stu-id="a9496-131">As read-only or updateable at the cursor or field level.</span></span>

  - <span data-ttu-id="a9496-132">Como somente-avançar ou totalmente navegável.</span><span class="sxs-lookup"><span data-stu-id="a9496-132">As forward-only or fully scrollable.</span></span>

  - <span data-ttu-id="a9496-133">Com o conjunto de chaves do cursor localizado no servidor.</span><span class="sxs-lookup"><span data-stu-id="a9496-133">With the cursor keyset located on the server.</span></span>

  - <span data-ttu-id="a9496-134">Importante para as alterações em tabelas subjacentes causadas por outros aplicativos (como associação, classificação, inserções, atualizações e exclusões).</span><span class="sxs-lookup"><span data-stu-id="a9496-134">Sensitive to underlying table changes caused by other applications (such as membership, sort, inserts, updates, and deletes).</span></span>

  - <span data-ttu-id="a9496-135">Existente no servidor ou no cliente.</span><span class="sxs-lookup"><span data-stu-id="a9496-135">Existing on either the server or the client.</span></span>

<span data-ttu-id="a9496-p106">Os cursores somente-leitura ajudam os usuários a navegar pelo conjunto de resultados, e os cursores leitura/gravação podem implementar atualizações de linha individuais. Os cursores complexos podem ser definidos com os conjuntos de chaves que apontam de volta para as linhas da tabela de base. Enquanto alguns cursores são somente-leitura em uma direção progressiva, outros podem mover-se para frente e para trás e fornecer uma atualização dinâmica do conjunto de resultados com base nas alterações que outros aplicativos estão fazendo no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a9496-p106">Read-only cursors help users browse through the result set, and read/write cursors can implement individual row updates. Complex cursors can be defined with keysets that point back to base table rows. While some cursors are read-only in a forward direction, others can move back and forth and provide a dynamic refresh of the result set based on changes that other applications are making to the database.</span></span>

<span data-ttu-id="a9496-p107">Nem todos os aplicativos precisam utilizar cursores para acessar ou atualizar dados. Algumas consultas simplesmente não exigem atualização direta da linha com a utilização do cursor. Os cursores devem ser uma das últimas técnicas escolhidas para a recuperação de dados  em seguida, você deve escolher o cursor com o menor impacto possível. Quando você cria um conjunto de resultados utilizando um procedimento armazenado, o conjunto de resultados não é atualizável com os métodos Edit ou Update do cursor.</span><span class="sxs-lookup"><span data-stu-id="a9496-p107">Not all applications need to use cursors to access or update data. Some queries simply do not require direct row updating by using a cursor. Cursors should be one of the last techniques you choose to retrieve data — and then you should choose the lowest impact cursor possible. When you create a result set by using a stored procedure, the result set is not updateable using cursor edit or update methods.</span></span>

## <a name="concurrency"></a><span data-ttu-id="a9496-143">Simultaneidade</span><span class="sxs-lookup"><span data-stu-id="a9496-143">Concurrency</span></span>

<span data-ttu-id="a9496-p108">Em alguns aplicativos de vários usuários, é extremamente importante que os dados apresentados aos usuários sejam os mais atuais possíveis. Um exemplo clássico de tal sistema é um sistema de reserva de passagens aéreas, em que vários usuários podem estar concorrendo à mesma poltrona em um determinado voo (e, portanto, um único registro). Nesse casso, o design do aplicativo deve lidar com operações simultâneas em um único registro.</span><span class="sxs-lookup"><span data-stu-id="a9496-p108">In some multi-user applications it is vitally important for the data presented to the end user to be as current as possible. A classic example of such a system is an airline reservation system, where many users might be contending for the same seat on a given flight (and thus, a single record). In a case like this, the application design must handle concurrent operations on a single record.</span></span>

<span data-ttu-id="a9496-p109">Em outros aplicativos, a simultaneidade não é tão importante. Nesses casos, a despesa envolvida em manter os dados sempre atualizados não pode ser justificada.</span><span class="sxs-lookup"><span data-stu-id="a9496-p109">In other applications, concurrency is not as important. In such cases, the expense involved in keeping the data current at all times cannot be justified.</span></span>

## <a name="position"></a><span data-ttu-id="a9496-149">Posição</span><span class="sxs-lookup"><span data-stu-id="a9496-149">Position</span></span>

<span data-ttu-id="a9496-p110">Um cursor também mantém o controle da posição atual em um conjunto de resultados. Pense na posição do cursor como um ponteiro para o registro atual, semelhante ao modo como um índice de matriz aponta para o valor naquele determinado local na matriz.</span><span class="sxs-lookup"><span data-stu-id="a9496-p110">A cursor also keeps track of the current position in a result set. Think of the cursor position as a pointer to the current record, similar to the way an array index points to the value at that particular location in the array.</span></span>

## <a name="scrollability"></a><span data-ttu-id="a9496-152">Capacidade de navegação</span><span class="sxs-lookup"><span data-stu-id="a9496-152">Scrollability</span></span>

<span data-ttu-id="a9496-153">O tipo do cursor utilizado pelo aplicativo também afeta a capacidade de avançar e voltar nas linhas em um conjunto de resultados; isso normalmente é chamado de capacidade de navegação.</span><span class="sxs-lookup"><span data-stu-id="a9496-153">The type of cursor employed by your application also affects the ability to move forward and backward through the rows in a result set; this is sometimes called scrollability.</span></span> <span data-ttu-id="a9496-154">A capacidade de mover a frente *e* para trás ao longo de um conjunto de resultados aumenta a complexidade do cursor e, portanto, é mais cara implementar.</span><span class="sxs-lookup"><span data-stu-id="a9496-154">The ability to move forward *and* backward through a result set adds to the complexity of the cursor, and is therefore more expensive to implement.</span></span> <span data-ttu-id="a9496-155">Por essa razão, você deve solicitar um cursor com essa funcionalidade somente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="a9496-155">For this reason, you should ask for a cursor with this functionality only when necessary.</span></span>

