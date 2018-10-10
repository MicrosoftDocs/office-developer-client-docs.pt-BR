---
title: O que pode ser feito com o ADO
TOCTitle: What You Can Do With ADO
ms:assetid: 98246cb0-aec6-6a77-c953-85895ad83a5d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249681(v=office.15)
ms:contentKeyID: 48546483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d944d70e7aba054abb7e6f02933b1311bb90ee17
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462367"
---
# <a name="what-you-can-do-with-ado"></a><span data-ttu-id="cb54d-102">O que pode ser feito com o ADO</span><span class="sxs-lookup"><span data-stu-id="cb54d-102">What You Can Do With ADO</span></span>


<span data-ttu-id="cb54d-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb54d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cb54d-p101">O ADO foi projetado para fornecer aos desenvolvedores um modelo de objeto lógico e poderoso para acessar, editar e atualizar, de maneira programática, uma ampla variedade de fontes de dados pelas interfaces do sistema OLE DB. O uso mais comum do ADO é consultar uma ou mais tabelas em um banco de dados relacional, recuperar e exibir os resultados em um aplicativo e, talvez, permitir que os usuários fazer e salvem as alterações nos dados. Outras coisas que podem ser feitas de maneira programática com o ADO incluem:</span><span class="sxs-lookup"><span data-stu-id="cb54d-p101">ADO is designed to provide developers with a powerful, logical object model for programmatically accessing, editing, and updating a wide variety of data sources through OLE DB system interfaces. The most common usage of ADO is to query a table or tables in a relational database, retrieve and display the results in an application, and perhaps allow users to make and save changes to the data. Other things that can be done programmatically with ADO include:</span></span>

  - <span data-ttu-id="cb54d-107">Consultando um banco de dados usando o SQL e exibindo os resultados.</span><span class="sxs-lookup"><span data-stu-id="cb54d-107">Querying a database using SQL and displaying the results.</span></span>

  - <span data-ttu-id="cb54d-108">Acessando as informações em um repositório de arquivos pela Internet.</span><span class="sxs-lookup"><span data-stu-id="cb54d-108">Accessing information in a file store over the Internet.</span></span>

  - <span data-ttu-id="cb54d-109">Manipulando mensagens e pastas em um sistema de email.</span><span class="sxs-lookup"><span data-stu-id="cb54d-109">Manipulating messages and folders in an e-mail system.</span></span>

  - <span data-ttu-id="cb54d-110">Salvando dados de um banco de dados em um arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="cb54d-110">Saving data from a database into an XML file.</span></span>

  - <span data-ttu-id="cb54d-111">Permitindo que um usuário revise e faça alterações nos dados nas tabelas do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cb54d-111">Allowing a user to review and make changes to data in database tables.</span></span>

  - <span data-ttu-id="cb54d-112">Criando e usando novamente comandos parametrizados do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cb54d-112">Creating and reusing parameterized database commands.</span></span>

  - <span data-ttu-id="cb54d-113">Executando os procedimentos armazenados.</span><span class="sxs-lookup"><span data-stu-id="cb54d-113">Executing stored procedures.</span></span>

  - <span data-ttu-id="cb54d-114">Criando dinamicamente uma estrutura flexível, chamada **Recordset**, para manter, navegar e manipular os dados.</span><span class="sxs-lookup"><span data-stu-id="cb54d-114">Dynamically creating a flexible structure, called a **Recordset**, to hold, navigate, and manipulate data.</span></span>

  - <span data-ttu-id="cb54d-115">Executando operações do banco de dados transacional.</span><span class="sxs-lookup"><span data-stu-id="cb54d-115">Performing transactional database operations.</span></span>

  - <span data-ttu-id="cb54d-116">Filtrando e classificando cópias locais das informações do banco de dados com base nos critérios em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="cb54d-116">Filtering and sorting local copies of database information based on run-time criteria.</span></span>

  - <span data-ttu-id="cb54d-117">Criando e manipulando os resultados hierárquicos a partir dos bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="cb54d-117">Creating and manipulating hierarchical results from databases.</span></span>

  - <span data-ttu-id="cb54d-118">Vinculando os campos do banco de dados a componentes cientes de dados.</span><span class="sxs-lookup"><span data-stu-id="cb54d-118">Binding database fields to data-aware components.</span></span>

  - <span data-ttu-id="cb54d-119">Criando **Recordsets** remotos e desconectados.</span><span class="sxs-lookup"><span data-stu-id="cb54d-119">Creating remote, disconnected **Recordsets**.</span></span>

<span data-ttu-id="cb54d-p102">O ADO deve expor uma ampla variedade de opções e configurações para fornecer tal flexibilidade. Portanto, é importante fazer uma abordagem metódica para aprender a usar o ADO em um aplicativo, dividindo cada uma das suas metas em partes que podem ser gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="cb54d-p102">ADO must expose a wide variety of options and settings in order to provide such flexibility. Therefore it's important to take a methodical approach to learning how to use ADO in an application, breaking down each of your goals into manageable pieces.</span></span>

<span data-ttu-id="cb54d-p103">Quatro operações primárias estão envolvidas na maioria dos programas ADO: obtenção, análise, edição e atualização de dados. Os próximos quatro capítulos analisam cada uma dessas operações com mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="cb54d-p103">Four primary operations are involved in most ADO programs: getting data, examining data, editing data, and updating data. The next four chapters examine each of these operations in more detail.</span></span>

<span data-ttu-id="cb54d-p104">Antes de continuar, conheça os objetos no [HelloData: Um simples aplicativo ADO](hellodata-a-simple-ado-application.md). Este aplicativo é gravado no Visual Basic e executa cada uma das quatro operações ADO primárias.</span><span class="sxs-lookup"><span data-stu-id="cb54d-p104">Before proceeding, familiarize yourself with the objects in the ADO Object Model. Then review [HelloData: A Simple ADO Application](hellodata-a-simple-ado-application.md). This application is written in Visual Basic and performs each of the four primary ADO operations.</span></span>
