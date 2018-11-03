---
title: Botões de comando do catálogo de endereços
TOCTitle: Address Book command buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f586b92f309ffd330230bf732d0e477acf0a8ba9
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946921"
---
# <a name="address-book-command-buttons"></a><span data-ttu-id="08526-102">Botões de comando do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="08526-102">Address Book command buttons</span></span>


<span data-ttu-id="08526-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="08526-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="08526-104">O aplicativo de Catálogo de endereços inclui os seguintes botões de comando:</span><span class="sxs-lookup"><span data-stu-id="08526-104">The Address Book application includes the following command buttons:</span></span>

- <span data-ttu-id="08526-105">Um botão **Localizar** para enviar uma consulta ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="08526-105">A **Find** button to submit a query to the database.</span></span>

- <span data-ttu-id="08526-106">Um botão **Desmarcar** para desmarcar as caixas de texto antes de iniciar uma nova pesquisa.</span><span class="sxs-lookup"><span data-stu-id="08526-106">A **Clear** button to clear the text boxes before starting a new search.</span></span>

- <span data-ttu-id="08526-107">Um botão **Atualizar perfil** para salvar as alterações em um registro de funcionário.</span><span class="sxs-lookup"><span data-stu-id="08526-107">An **Update Profile** button to save changes to an employee record.</span></span>

- <span data-ttu-id="08526-108">Um botão **Cancelar alterações** para descartar as alterações.</span><span class="sxs-lookup"><span data-stu-id="08526-108">A **Cancel Changes** button to discard changes.</span></span>

## <a name="find-button"></a><span data-ttu-id="08526-109">Botão Localizar</span><span class="sxs-lookup"><span data-stu-id="08526-109">Find Button</span></span>

<span data-ttu-id="08526-110">Clicar no botão **Localizar** ativa o VBScript localizar\_procedimento Sub de OnClick, que cria e envia a consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="08526-110">Clicking the **Find** button activates the VBScript Find\_OnClick Sub procedure, which builds and sends the SQL query.</span></span> <span data-ttu-id="08526-111">Clicar nesse botão preenche a grade de dados.</span><span class="sxs-lookup"><span data-stu-id="08526-111">Clicking this button populates the data grid.</span></span>

## <a name="building-the-sql-query"></a><span data-ttu-id="08526-112">Criando a consulta SQL</span><span class="sxs-lookup"><span data-stu-id="08526-112">Building the SQL Query</span></span>

<span data-ttu-id="08526-113">A primeira parte do localizar\_procedimento OnClick Sub cria a consulta SQL, uma frase de cada vez, acrescentando cadeias de caracteres de texto para uma instrução de SQL SELECT global.</span><span class="sxs-lookup"><span data-stu-id="08526-113">The first part of the Find\_OnClick Sub procedure builds the SQL query, one phrase at a time, by appending text strings to a global SQL SELECT statement.</span></span> <span data-ttu-id="08526-114">Ele começa definindo-se a variável como uma instrução SQL que as solicitações de todas as linhas de dados da tabela da fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="08526-114">It begins by setting the variable to a SQL SELECT statement that requests all rows of data from the data source table.</span></span> <span data-ttu-id="08526-115">Em seguida, o procedimento Sub analisa cada uma das quatro caixas de entrada na página.</span><span class="sxs-lookup"><span data-stu-id="08526-115">Next, the Sub procedure scans each of the four input boxes on the page.</span></span>

<span data-ttu-id="08526-116">Como o programa usa a palavra na criação das instruções SQL, as consultas são pesquisas de subcadeia de caracteres em vez de correspondências exatas.</span><span class="sxs-lookup"><span data-stu-id="08526-116">Because the program uses the word in building the SQL statements, the queries are substring searches rather than exact matches.</span></span>

<span data-ttu-id="08526-117">Por exemplo, se a caixa **Último nome** continha a entrada "Berge" e a caixa **cargo** continha a entrada "Program Manager", a instrução SQL (valor) leria:</span><span class="sxs-lookup"><span data-stu-id="08526-117">For example, if the **Last Name** box contained the entry "Berge" and the **Title** box contained the entry "Program Manager", the SQL statement (value of ) would read:</span></span>

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

<span data-ttu-id="08526-118">Se a consulta foi bem-sucedida, todas as pessoas com o último nome contendo o texto "Berge" (como Berge e Berger) e com um cargo contendo as palavras "Program Manager" (por exemplo, Program Manager, Advanced Technologies) serão exibidas na grade de dados HTML.</span><span class="sxs-lookup"><span data-stu-id="08526-118">If the query was successful, all persons with a last name containing the text "Berge" (such as Berge and Berger) and with a title containing the words "Program Manager" (for example, Program Manager, Advanced Technologies) are displayed in the HTML data grid.</span></span>

## <a name="preparing-and-sending-the-query"></a><span data-ttu-id="08526-119">Preparando e enviando a consulta</span><span class="sxs-lookup"><span data-stu-id="08526-119">Preparing and Sending the Query</span></span>

<span data-ttu-id="08526-120">A última parte da localizar\_procedimento OnClick Sub consiste em duas instruções.</span><span class="sxs-lookup"><span data-stu-id="08526-120">The last part of the Find\_OnClick Sub procedure consists of two statements.</span></span> <span data-ttu-id="08526-121">A primeira atribui a propriedade SQL do objeto RDS.DataControl à consulta SQL criada de forma dinâmica.</span><span class="sxs-lookup"><span data-stu-id="08526-121">The first statement assigns the SQL property of the RDS.DataControl object equal to the dynamically built SQL query.</span></span> <span data-ttu-id="08526-122">A segunda instrução faz com que o **RDS. DataControl** () para consultar o banco de dados de objeto e, em seguida, exiba os novos resultados da consulta na grade.</span><span class="sxs-lookup"><span data-stu-id="08526-122">The second statement causes the **RDS.DataControl** object () to query the database, and then display the new results of the query in the grid.</span></span>

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a><span data-ttu-id="08526-123">Botão Atualizar perfil</span><span class="sxs-lookup"><span data-stu-id="08526-123">Update Profile Button</span></span>

<span data-ttu-id="08526-124">Clicar no botão **Atualizar perfil** ativa a atualização do VBScript\_procedimento OnClick Sub, que executa o RDS. () SubmitChanges e Refresh métodos do objeto DataControl.</span><span class="sxs-lookup"><span data-stu-id="08526-124">Clicking the **Update Profile** button activates the VBScript Update\_OnClick Sub procedure, which executes the RDS.DataControl object's () SubmitChanges and Refresh methods.</span></span>

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

<span data-ttu-id="08526-125">Quando DC1. Executa SubmitChanges, o serviço de dados remotos todas as informações de atualização de pacotes e enviá-la para o servidor via HTTP.</span><span class="sxs-lookup"><span data-stu-id="08526-125">When DC1.SubmitChanges executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="08526-126">A atualização ocorre em tudo ou em nada; se uma parte da atualização não tiver sucesso, nenhuma das alterações será feita, e uma mensagem de status será retornada.</span><span class="sxs-lookup"><span data-stu-id="08526-126">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="08526-127">é executado, o Serviço de dados remoto cria pacote de todas as informações de atualização e os envia ao servidor via HTTP.</span><span class="sxs-lookup"><span data-stu-id="08526-127">executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="08526-128">A atualização ocorre em tudo ou em nada; se uma parte da atualização não tiver sucesso, nenhuma das alterações será feita, e uma mensagem de status será retornada.</span><span class="sxs-lookup"><span data-stu-id="08526-128">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="08526-129">DC1. A atualização não é necessária depois de **SubmitChanges** com o Remote Data Service, mas garante dados atualizados.</span><span class="sxs-lookup"><span data-stu-id="08526-129">DC1.Refresh isn't necessary after **SubmitChanges** with Remote Data Service, but it ensures fresh data.</span></span>

## <a name="cancel-changes-button"></a><span data-ttu-id="08526-130">Botão Cancelar alterações</span><span class="sxs-lookup"><span data-stu-id="08526-130">Cancel Changes Button</span></span>

<span data-ttu-id="08526-131">Clicar em **Cancelar alterações** ativa o cancelamento do VBScript\_procedimento OnClick Sub, que executa o RDS. Do objeto DataControl (método CancelUpdate.</span><span class="sxs-lookup"><span data-stu-id="08526-131">Clicking **Cancel Changes** activates the VBScript Cancel\_OnClick Sub procedure, which executes the RDS.DataControl object's ( CancelUpdate method.</span></span>

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

<span data-ttu-id="08526-132">Quando é executado, ele descarta todas as edições feitas por um usuário para um registro de funcionário na grade de dados desde a última consulta ou atualização.</span><span class="sxs-lookup"><span data-stu-id="08526-132">When executes, it discards any edits that a user has made to an employee record on the data grid since the last query or update.</span></span> <span data-ttu-id="08526-133">Ele restaura os valores originais.</span><span class="sxs-lookup"><span data-stu-id="08526-133">It restores the original values.</span></span>

