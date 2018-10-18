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
ms.openlocfilehash: 3110bd89b0dc56b13a42c7152465c0f9b39e3175
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25607043"
---
# <a name="dbengineopenconnection-method-dao"></a><span data-ttu-id="868ab-102">Método DBEngine.OpenConnection (DAO)</span><span class="sxs-lookup"><span data-stu-id="868ab-102">DBEngine.OpenConnection Method (DAO)</span></span>


<span data-ttu-id="868ab-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="868ab-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="868ab-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="868ab-104">Syntax</span></span>

<span data-ttu-id="868ab-105">*expressão* . OpenConnection (***nome***, ***Opções***, ***ReadOnly***, ***Conecte-se***)</span><span class="sxs-lookup"><span data-stu-id="868ab-105">*expression* .OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="868ab-106">*expressão* Uma variável que representa um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="868ab-106">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="868ab-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="868ab-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="868ab-108">Nome</span><span class="sxs-lookup"><span data-stu-id="868ab-108">Name</span></span></p></th>
<th><p><span data-ttu-id="868ab-109">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="868ab-109">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="868ab-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="868ab-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="868ab-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="868ab-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868ab-112">Name</span><span class="sxs-lookup"><span data-stu-id="868ab-112">Name</span></span></p></td>
<td><p><span data-ttu-id="868ab-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="868ab-113">Required</span></span></p></td>
<td><p><span data-ttu-id="868ab-114"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="868ab-114"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="868ab-p101">Uma expressão em sequência. Consulte a discussão em Comentários.</span><span class="sxs-lookup"><span data-stu-id="868ab-p101">A string expression. See the discussion under Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868ab-117">Opções</span><span class="sxs-lookup"><span data-stu-id="868ab-117">Options</span></span></p></td>
<td><p><span data-ttu-id="868ab-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="868ab-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="868ab-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="868ab-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="868ab-p102">Define as várias opções para a conexão, como especificado em Comentários. Com base nessa valor, o gerenciador do driver ODBC solicita ao usuário informações de conexão, como o DSN (Nome da fonte de dados), o nome do usuário e a senha.</span><span class="sxs-lookup"><span data-stu-id="868ab-p102">sets various options for the connection, as specified in Remarks. Based on this value, the ODBC driver manager prompts the user for connection information such as data source name (DSN), user name, and password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868ab-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="868ab-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="868ab-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="868ab-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="868ab-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="868ab-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="868ab-125"><strong>True</strong> se a conexão tiver que ser aberta para acesso somente leitura, e <strong>False</strong> se a conexão tiver que ser aberta para acesso de leitura/gravação (padrão).</span><span class="sxs-lookup"><span data-stu-id="868ab-125"><strong>True</strong> if the connection is to be opened for read-only access and <strong>False</strong> if the connection is to be opened for read/write access (default).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868ab-126">Connect</span><span class="sxs-lookup"><span data-stu-id="868ab-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="868ab-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="868ab-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="868ab-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="868ab-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="868ab-129">Uma cadeia de caracteres de conexão ODBC.</span><span class="sxs-lookup"><span data-stu-id="868ab-129">An ODBC connection string.</span></span> <span data-ttu-id="868ab-130">Consulte a propriedade <strong><a href="connection-connect-property-dao.md">Connect</a></strong> para os elementos específicos e a sintaxe dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="868ab-130">See the <strong><a href="connection-connect-property-dao.md">Connect</a></strong> property for the specific elements and syntax of this string.</span></span> <span data-ttu-id="868ab-131">Um antecedendo &quot;ODBC; &quot; é necessário.</span><span class="sxs-lookup"><span data-stu-id="868ab-131">A prepended &quot;ODBC;&quot; is required.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868ab-132"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="868ab-132"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="868ab-133">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="868ab-133">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="868ab-134">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="868ab-134">Return value</span></span>
>>>>>>> <span data-ttu-id="868ab-135">mestre</span><span class="sxs-lookup"><span data-stu-id="868ab-135">master</span></span>

<span data-ttu-id="868ab-136">Connection</span><span class="sxs-lookup"><span data-stu-id="868ab-136">Connection</span></span>

## <a name="remarks"></a><span data-ttu-id="868ab-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="868ab-137">Remarks</span></span>

<span data-ttu-id="868ab-p104">Use o método **OpenConnection** para estabelecer uma conexão com uma fonte de dados ODBC a partir de um espaço de trabalho ODBCDirect. O método **OpenConnection** é semelhante mas não igual a **OpenDatabase**. A principal diferença é que **OpenConnection** está disponível em um espaço de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="868ab-p104">Use the **OpenConnection** method to establish a connection to an ODBC data source from an ODBCDirect workspace. The **OpenConnection** method is similar but not equivalent to **OpenDatabase**. The main difference is that **OpenConnection** is available only in an ODBCDirect workspace.</span></span>

<span data-ttu-id="868ab-141">Se você especificar um nome registrado de fonte de dados do ODBC (DSN) no argumento conectar, em seguida, o argumento nome pode ser qualquer cadeia de caracteres válida e também fornecerá a propriedade **Name** para o objeto de **Conexão** .</span><span class="sxs-lookup"><span data-stu-id="868ab-141">If you specify a registered ODBC data source name (DSN) in the connect argument, then the name argument can be any valid string, and will also provide the **Name** property for the **Connection** object.</span></span> <span data-ttu-id="868ab-142">Se um DSN válido não está incluído no argumento conectar, em seguida, nome deve se referir a um DSN ODBC válido, que também será a propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="868ab-142">If a valid DSN is not included in the connect argument, then name must refer to a valid ODBC DSN, which will also be the **Name** property.</span></span> <span data-ttu-id="868ab-143">Se nem nome nem conectar contém um DSN válido, o Gerenciador de driver ODBC pode ser definido (via o argumento options) para solicitar ao usuário as informações de conexão necessárias.</span><span class="sxs-lookup"><span data-stu-id="868ab-143">If neither name nor connect contains a valid DSN, the ODBC driver manager can be set (via the options argument) to prompt the user for the required connection information.</span></span> <span data-ttu-id="868ab-144">O DSN é fornecido pela solicitação e depois fornece a propriedade **Name**.</span><span class="sxs-lookup"><span data-stu-id="868ab-144">The DSN supplied through the prompt then provides the **Name** property.</span></span>

<span data-ttu-id="868ab-p106">O argumento options determina se e quando solicitar que o usuário estabeleça a conexão e se a conexão será aberta de forma assíncrona ou não. Você pode usar uma das constantes a seguir.</span><span class="sxs-lookup"><span data-stu-id="868ab-p106">The options argument determines if and when to prompt the user to establish the connection, and whether or not to open the connection asynchronously. You can use one of the following constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="868ab-147">Constant</span><span class="sxs-lookup"><span data-stu-id="868ab-147">Constant</span></span></p></th>
<th><p><span data-ttu-id="868ab-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="868ab-148">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868ab-149"><strong>dbDriverNoPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="868ab-149"><strong>dbDriverNoPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="868ab-p107">O Gerenciador de Driver ODBC usa a cadeia de caracteres de conexão fornecida em <em>dbname</em> e <em>connect</em>. Se você não fornecer informações suficientes, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="868ab-p107">The ODBC Driver Manager uses the connection string provided in <em>dbname</em> and <em>connect</em>. If you don't provide sufficient information, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868ab-152"><strong>dbDriverPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="868ab-152"><strong>dbDriverPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="868ab-p108">O Gerenciador de driver ODBC exibe a caixa de diálogo <strong>Fontes de Dados ODBC</strong>, que mostra quaisquer informações relevantes fornecidas em <em>dbname</em> ou <em>connect</em>. A sequência de conexão é composta pelo DSN que o usuário seleciona via caixas de diálogo ou, se o usuário não especificar um DSN, pelo DSN padrão.</span><span class="sxs-lookup"><span data-stu-id="868ab-p108">The ODBC Driver Manager displays the <strong>ODBC Data Sources</strong> dialog box, which displays any relevant information supplied in <em>dbname</em> or <em>connect</em>. The connection string is made up of the DSN that the user selects via the dialog boxes, or, if the user doesn't specify a DSN, the default DSN is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868ab-155"><strong>dbDriverComplete</strong></span><span class="sxs-lookup"><span data-stu-id="868ab-155"><strong>dbDriverComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="868ab-p109">Padrão. Se o argumento <em>connect</em> incluir todas as informações necessárias para estabelecer a conexão,  o Gerenciador de driver ODBC utilizará a sequência em <em>connect</em>. Caso contrário, ele se comportará da mesma forma como quando você especifica <strong>dbDriverPrompt</strong>.</span><span class="sxs-lookup"><span data-stu-id="868ab-p109">Default. If the <em>connect</em> argument includes all the necessary information to complete a connection, the ODBC Driver Manager uses the string in <em>connect</em>. Otherwise it behaves as it does when you specify <strong>dbDriverPrompt</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868ab-159"><strong>dbDriverCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="868ab-159"><strong>dbDriverCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="868ab-160">Essa opção se comporta como <strong>dbDriverComplete</strong> exceto pelo fato de que o driver ODBC desabilita as solicitações para qualquer informação não exigida para estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="868ab-160">This option behaves like <strong>dbDriverComplete</strong> except the ODBC driver disables the prompts for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868ab-161"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="868ab-161"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="868ab-p110">Execute o método de modo assíncrono. Essa constante pode ser usada com quaisquer outras constantes <em>options</em>.</span><span class="sxs-lookup"><span data-stu-id="868ab-p110">Execute the method asynchronously. This constant may be used with any of the other <em>options</em> constants.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868ab-p111">**OpenConnection** retorna um objeto **Connection** que contém informações sobre a conexão. O objeto **Connection** é semelhante a um objeto **[Database](database-object-dao.md)**. A principal diferença é que um objeto **Database** geralmente representa um banco de dados, embora ele possa ser usado para representar uma conexão a uma fonte de dados ODBC a partir de um espaço de trabalho do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="868ab-p111">**OpenConnection** returns a **Connection** object which contains information about the connection. The **Connection** object is similar to a **[Database](database-object-dao.md)** object. The principal difference is that a **Database** object usually represents a database, although it can be used to represent a connection to an ODBC data source from a Microsoft Access workspace.</span></span>

