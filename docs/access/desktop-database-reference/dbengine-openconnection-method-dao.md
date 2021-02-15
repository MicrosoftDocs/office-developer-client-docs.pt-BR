---
title: Método DBEngine.OpenConnection (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 778a581f-be42-94ee-e5c6-4cbc1843450d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196074(v=office.15)
ms:contentKeyID: 48545729
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053574
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 845c710954d83003f49a6cd9db21ae3f3bfab383
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294257"
---
# <a name="dbengineopenconnection-method-dao"></a><span data-ttu-id="d8c87-102">Método DBEngine.OpenConnection (DAO)</span><span class="sxs-lookup"><span data-stu-id="d8c87-102">DBEngine.OpenConnection method (DAO)</span></span>

<span data-ttu-id="d8c87-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8c87-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c87-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8c87-104">Syntax</span></span>

<span data-ttu-id="d8c87-105">*expressão* . OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span><span class="sxs-lookup"><span data-stu-id="d8c87-105">*expression* .OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="d8c87-106">*expressão* Uma variável que representa um objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="d8c87-106">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d8c87-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8c87-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8c87-108">Nome</span><span class="sxs-lookup"><span data-stu-id="d8c87-108">Name</span></span></p></th>
<th><p><span data-ttu-id="d8c87-109">Necessária/opcional</span><span class="sxs-lookup"><span data-stu-id="d8c87-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="d8c87-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d8c87-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="d8c87-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8c87-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8c87-112"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="d8c87-112"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="d8c87-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d8c87-113">Required</span></span></p></td>
<td><p><span data-ttu-id="d8c87-114"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="d8c87-114"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="d8c87-115">Uma expressão em sequência.</span><span class="sxs-lookup"><span data-stu-id="d8c87-115">A string expression.</span></span> <span data-ttu-id="d8c87-116">Consulte a discussão em Comentários.</span><span class="sxs-lookup"><span data-stu-id="d8c87-116">See the discussion under Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c87-117"><em>Opções</em></span><span class="sxs-lookup"><span data-stu-id="d8c87-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="d8c87-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="d8c87-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="d8c87-119"><strong>Variantes</strong></span><span class="sxs-lookup"><span data-stu-id="d8c87-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d8c87-p102">Define as várias opções para a conexão, como especificado em Comentários. Com base nessa valor, o gerenciador do driver ODBC solicita ao usuário informações de conexão, como o DSN (Nome da fonte de dados), o nome do usuário e a senha.</span><span class="sxs-lookup"><span data-stu-id="d8c87-p102">sets various options for the connection, as specified in Remarks. Based on this value, the ODBC driver manager prompts the user for connection information such as data source name (DSN), user name, and password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c87-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="d8c87-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="d8c87-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="d8c87-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="d8c87-124"><strong>Variantes</strong></span><span class="sxs-lookup"><span data-stu-id="d8c87-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d8c87-125"><strong>True</strong> se a conexão tiver que ser aberta para acesso somente leitura, e <strong>False</strong> se a conexão tiver que ser aberta para acesso de leitura/gravação (padrão).</span><span class="sxs-lookup"><span data-stu-id="d8c87-125"><strong>True</strong> if the connection is to be opened for read-only access and <strong>False</strong> if the connection is to be opened for read/write access (default).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c87-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="d8c87-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="d8c87-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="d8c87-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="d8c87-128"><strong>Variantes</strong></span><span class="sxs-lookup"><span data-stu-id="d8c87-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d8c87-129">Uma cadeia de caracteres de conexão ODBC.</span><span class="sxs-lookup"><span data-stu-id="d8c87-129">An ODBC connection string.</span></span> <span data-ttu-id="d8c87-130">Consulte a <strong><a href="connection-connect-property-dao.md">propriedade Connect</a></strong> para ver os elementos específicos e a sintaxe dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d8c87-130">See the <strong><a href="connection-connect-property-dao.md">Connect</a></strong> property for the specific elements and syntax of this string.</span></span> <span data-ttu-id="d8c87-131">Um &quot; ODBC anexado; &quot; é necessário.</span><span class="sxs-lookup"><span data-stu-id="d8c87-131">A prepended &quot;ODBC;&quot; is required.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="d8c87-132">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d8c87-132">Return value</span></span>

<span data-ttu-id="d8c87-133">Connection</span><span class="sxs-lookup"><span data-stu-id="d8c87-133">Connection</span></span>

## <a name="remarks"></a><span data-ttu-id="d8c87-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8c87-134">Remarks</span></span>

<span data-ttu-id="d8c87-p104">Use o método **OpenConnection** para estabelecer uma conexão com uma fonte de dados ODBC a partir de um espaço de trabalho ODBCDirect. O método **OpenConnection** é semelhante mas não igual a **OpenDatabase**. A principal diferença é que **OpenConnection** está disponível em um espaço de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="d8c87-p104">Use the **OpenConnection** method to establish a connection to an ODBC data source from an ODBCDirect workspace. The **OpenConnection** method is similar but not equivalent to **OpenDatabase**. The main difference is that **OpenConnection** is available only in an ODBCDirect workspace.</span></span>

<span data-ttu-id="d8c87-138">Se você especificar um DSN (nome de fonte de dados) ODBC registrado no argumento connect, o argumento name pode ser qualquer cadeia de caracteres válida e também fornecerá a propriedade **Name** para o objeto **Connection.**</span><span class="sxs-lookup"><span data-stu-id="d8c87-138">If you specify a registered ODBC data source name (DSN) in the connect argument, then the name argument can be any valid string, and will also provide the **Name** property for the **Connection** object.</span></span> <span data-ttu-id="d8c87-139">Se um DSN válido não for incluído no argumento connect, o nome deverá se referir a um DSN ODBC válido, que também será a **propriedade Name.**</span><span class="sxs-lookup"><span data-stu-id="d8c87-139">If a valid DSN is not included in the connect argument, then name must refer to a valid ODBC DSN, which will also be the **Name** property.</span></span> <span data-ttu-id="d8c87-140">Se nem o nome nem a conexão contiver um DSN válido, o gerenciador de driver ODBC poderá ser definido (por meio do argumento options) para solicitar ao usuário as informações de conexão necessárias.</span><span class="sxs-lookup"><span data-stu-id="d8c87-140">If neither name nor connect contains a valid DSN, the ODBC driver manager can be set (via the options argument) to prompt the user for the required connection information.</span></span> <span data-ttu-id="d8c87-141">O DSN é fornecido pela solicitação e depois fornece a propriedade **Name**.</span><span class="sxs-lookup"><span data-stu-id="d8c87-141">The DSN supplied through the prompt then provides the **Name** property.</span></span>

<span data-ttu-id="d8c87-142">O argumento options determina se e quando solicitar que o usuário estabeleça a conexão e se a conexão será aberta de forma assíncrona ou não.</span><span class="sxs-lookup"><span data-stu-id="d8c87-142">The options argument determines if and when to prompt the user to establish the connection, and whether or not to open the connection asynchronously.</span></span> <span data-ttu-id="d8c87-143">Você pode usar uma das constantes a seguir.</span><span class="sxs-lookup"><span data-stu-id="d8c87-143">You can use one of the following constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8c87-144">Constante</span><span class="sxs-lookup"><span data-stu-id="d8c87-144">Constant</span></span></p></th>
<th><p><span data-ttu-id="d8c87-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8c87-145">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8c87-146"><strong>dbDriverNoPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="d8c87-146"><strong>dbDriverNoPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="d8c87-147">O Gerenciador de Driver ODBC usa a cadeia de caracteres de conexão fornecida em <em>dbname</em> e <em>connect</em>.</span><span class="sxs-lookup"><span data-stu-id="d8c87-147">The ODBC Driver Manager uses the connection string provided in <em>dbname</em> and <em>connect</em>.</span></span> <span data-ttu-id="d8c87-148">Se você não fornecer informações suficientes, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d8c87-148">If you don't provide sufficient information, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c87-149"><strong>dbDriverPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="d8c87-149"><strong>dbDriverPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="d8c87-p108">O Gerenciador de Driver ODBC exibe a caixa de diálogo <strong>Fontes de Dados ODBC</strong>, que exibe quaisquer informações relevantes fornecidas em <em>dbname</em> ou <em>connect</em>. A cadeia de caracteres de conexão é formada pelo DSN que o usuário seleciona por meio das caixas de diálogo. Se o usuário não especificar um DSN, o DSN padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="d8c87-p108">The ODBC Driver Manager displays the <strong>ODBC Data Sources</strong> dialog box, which displays any relevant information supplied in <em>dbname</em> or <em>connect</em>. The connection string is made up of the DSN that the user selects via the dialog boxes, or, if the user doesn't specify a DSN, the default DSN is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c87-152"><strong>dbDriverComplete</strong></span><span class="sxs-lookup"><span data-stu-id="d8c87-152"><strong>dbDriverComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="d8c87-p109">Padrão. Se o argumento <em>connect</em> incluir todas as informações necessárias para estabelecer a conexão,  o Gerenciador de driver ODBC utilizará a sequência em <em>connect</em>. Caso contrário, ele se comportará da mesma forma como quando você especifica <strong>dbDriverPrompt</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c87-p109">Default. If the <em>connect</em> argument includes all the necessary information to complete a connection, the ODBC Driver Manager uses the string in <em>connect</em>. Otherwise it behaves as it does when you specify <strong>dbDriverPrompt</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c87-156"><strong>dbDriverCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="d8c87-156"><strong>dbDriverCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="d8c87-157">Essa opção se comporta como <strong>dbDriverComplete</strong> exceto pelo fato de que o driver ODBC desabilita as solicitações para qualquer informação não exigida para estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="d8c87-157">This option behaves like <strong>dbDriverComplete</strong> except the ODBC driver disables the prompts for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c87-158"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="d8c87-158"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="d8c87-159">Execute o método de modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="d8c87-159">Execute the method asynchronously.</span></span> <span data-ttu-id="d8c87-160">Essa constante pode ser usada com quaisquer outras constantes <em>options</em>.</span><span class="sxs-lookup"><span data-stu-id="d8c87-160">This constant may be used with any of the other <em>options</em> constants.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d8c87-p111">**OpenConnection** retorna um objeto **Connection** que contém informações sobre a conexão. O objeto **Connection** é semelhante a um objeto **[Database](database-object-dao.md)**. A principal diferença é que um objeto **Database** geralmente representa um banco de dados, embora ele possa ser usado para representar uma conexão a uma fonte de dados ODBC a partir de um espaço de trabalho do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="d8c87-p111">**OpenConnection** returns a **Connection** object which contains information about the connection. The **Connection** object is similar to a **[Database](database-object-dao.md)** object. The principal difference is that a **Database** object usually represents a database, although it can be used to represent a connection to an ODBC data source from a Microsoft Access workspace.</span></span>

