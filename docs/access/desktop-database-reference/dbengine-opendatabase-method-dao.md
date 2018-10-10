---
title: Método DBEngine.OpenDatabase (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: 49fca321-5955-3e69-64ea-da191536eadb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193474(v=office.15)
ms:contentKeyID: 48544654
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052979
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6999c003883675837ad333b6488820f3bb3a9f2e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465102"
---
# <a name="dbengineopendatabase-method-dao"></a><span data-ttu-id="6f0ec-102">Método DBEngine.OpenDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="6f0ec-102">DBEngine.OpenDatabase Method (DAO)</span></span>


<span data-ttu-id="6f0ec-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f0ec-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6f0ec-104">Abre um banco de dados especificado e retorna uma referência ao objeto **[Database](database-object-dao.md)** que o representa.</span><span class="sxs-lookup"><span data-stu-id="6f0ec-104">Opens a specified database and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f0ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f0ec-105">Syntax</span></span>

<span data-ttu-id="6f0ec-106">*expressão* . OpenDatabase (***nome***, ***Opções***, ***ReadOnly***, ***Conecte-se***)</span><span class="sxs-lookup"><span data-stu-id="6f0ec-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="6f0ec-107">*expressão* Uma variável que representa um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="6f0ec-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="6f0ec-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f0ec-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f0ec-109">Nome</span><span class="sxs-lookup"><span data-stu-id="6f0ec-109">Name</span></span></p></th>
<th><p><span data-ttu-id="6f0ec-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="6f0ec-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="6f0ec-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6f0ec-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="6f0ec-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f0ec-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f0ec-113">Name</span><span class="sxs-lookup"><span data-stu-id="6f0ec-113">Name</span></span></p></td>
<td><p><span data-ttu-id="6f0ec-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6f0ec-114">Required</span></span></p></td>
<td><p><span data-ttu-id="6f0ec-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="6f0ec-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6f0ec-p101">o nome de um arquivo de banco de dados existente do Microsoft Access ou o DSN (nome da fonte de dados) de uma fonte de dados ODBC. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter mais informações sobre como configurar esse valor.</span><span class="sxs-lookup"><span data-stu-id="6f0ec-p101">the name of an existing Microsoft Access database file, or the data source name (DSN) of an ODBC data source. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0ec-118">Options</span><span class="sxs-lookup"><span data-stu-id="6f0ec-118">Options</span></span></p></td>
<td><p><span data-ttu-id="6f0ec-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="6f0ec-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="6f0ec-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6f0ec-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6f0ec-121">Define as várias opções para o banco de dados, como especificado em Comentários.</span><span class="sxs-lookup"><span data-stu-id="6f0ec-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0ec-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6f0ec-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="6f0ec-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="6f0ec-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="6f0ec-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6f0ec-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6f0ec-125"><strong>True</strong> se você quiser abrir o banco de dados com acesso somente leitura, ou <strong>False</strong> (padrão) se você quiser abrir o banco de dados com acesso de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6f0ec-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0ec-126">Connect</span><span class="sxs-lookup"><span data-stu-id="6f0ec-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="6f0ec-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="6f0ec-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="6f0ec-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6f0ec-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6f0ec-129">Especifica várias informações de conexão, incluindo senhas.</span><span class="sxs-lookup"><span data-stu-id="6f0ec-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6f0ec-130">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6f0ec-130">Return Value</span></span>

<span data-ttu-id="6f0ec-131">Banco de dados</span><span class="sxs-lookup"><span data-stu-id="6f0ec-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="6f0ec-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f0ec-132">Remarks</span></span>

<span data-ttu-id="6f0ec-133">Você pode usar os valores a seguir para o argumento options.</span><span class="sxs-lookup"><span data-stu-id="6f0ec-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f0ec-134">Configuração</span><span class="sxs-lookup"><span data-stu-id="6f0ec-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="6f0ec-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f0ec-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f0ec-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="6f0ec-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="6f0ec-137">Abre o banco de dados no modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="6f0ec-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0ec-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="6f0ec-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="6f0ec-139">(Padrão) Abre o banco de dados no modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="6f0ec-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6f0ec-140">Quando você abre um banco de dados, ele é automaticamente adicionado à coleção **Databases**.</span><span class="sxs-lookup"><span data-stu-id="6f0ec-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="6f0ec-141">Algumas considerações se aplicam quando se usa dbname:</span><span class="sxs-lookup"><span data-stu-id="6f0ec-141">Some considerations apply when you use dbname:</span></span>

  - <span data-ttu-id="6f0ec-142">Se ela se referir a um banco de dados que já foi aberto para acesso por outro usuário, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="6f0ec-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

  - <span data-ttu-id="6f0ec-143">Se ela não se referir a um banco de dados existente ou validar o nome da fonte de dados ODBC, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="6f0ec-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

  - <span data-ttu-id="6f0ec-144">Se for uma cadeia de caracteres de comprimento zero ("") e *Conecte-se* for "ODBC;", uma caixa de diálogo listando todos os registrados nomes de fonte de dados ODBC é exibida para que o usuário possa selecionar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6f0ec-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="6f0ec-145">Para fechar um banco de dados e assim remover o objeto **Database** da coleção **Databases**, use o método **[Close](connection-close-method-dao.md)** no objeto.</span><span class="sxs-lookup"><span data-stu-id="6f0ec-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6f0ec-146">[!OBSERVAçãO] Ao acessar uma fonte de dados ODBC conectada a um mecanismo de banco de dados do Microsoft Access, você pode aprimorar o desempenho do seu aplicativo abrindo um objeto <STRONG>Database</STRONG> conectado à fonte de dados ODBC, em vez de vincular objetos <STRONG><A href="tabledef-object-dao.md">TableDef</A></STRONG> individuais a tabelas específicas na fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="6f0ec-146">When you access a Microsoft Access database engine-connected ODBC data source, you can improve your application's performance by opening a <STRONG>Database</STRONG> object connected to the ODBC data source, rather than by linking individual <STRONG><A href="tabledef-object-dao.md">TableDef</A></STRONG> objects to specific tables in the ODBC data source.</span></span></P>


