---
title: Microsoft OLE DB Provider for ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0098e646ea48656f44bd3ccd380ae41efc94ffba
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606932"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="43170-102">Microsoft OLE DB Provider for ODBC</span><span class="sxs-lookup"><span data-stu-id="43170-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="43170-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="43170-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="43170-p101">Para um programador de ADO ou RDS, o mundo ideal seria aquele em que todas as fontes de dados apresentassem uma interface OLE DB, de modo que as chamadas do ADO pudessem ser feitas diretamente na fonte de dados. Embora cada vez mais fornecedores de bancos de dados venham implementando interfaces OLE DB, algumas fontes de dados ainda não são expostas dessa maneira. Por outro lado, praticamente todos os sistemas DBMS em uso hoje em dia podem ser acessados por ODBC.</span><span class="sxs-lookup"><span data-stu-id="43170-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="43170-107">Já existem drivers ODBC disponíveis para todos os principais DBMS em uso atualmente, incluindo Microsoft SQL Server, Microsoft Access (mecanismo de banco de dados do Microsoft Jet) e Microsoft FoxPro, além de produtos de banco de dados produzidos por outro fornecedor, como a Oracle.</span><span class="sxs-lookup"><span data-stu-id="43170-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="43170-p102">Entretanto, o Microsoft ODBC Provider permite a conexão do ADO com qualquer fonte de dados ODBC. O provedor é de encadeamento livre e habilitado para Unicode.</span><span class="sxs-lookup"><span data-stu-id="43170-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="43170-p103">O provedor oferece suporte a transações, embora diferentes mecanismos DBMS ofereçam diferentes tipos de suporte a transações. Por exemplo, o Microsoft Access oferece suporte a transações aninhadas com até cinco níveis de profundidade.</span><span class="sxs-lookup"><span data-stu-id="43170-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="43170-112">Esse é o provedor padrão para o ADO, oferecendo suporte a todas propriedades e métodos do ADO dependentes de provedor.</span><span class="sxs-lookup"><span data-stu-id="43170-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="43170-113">Parâmetros da sequência de conexão</span><span class="sxs-lookup"><span data-stu-id="43170-113">Connection String Parameters</span></span>

<span data-ttu-id="43170-114">Para estabelecer uma conexão com esse provedor, defina o argumento **Provider=** da propriedade [ConnectionString](connectionstring-property-ado.md) como:</span><span class="sxs-lookup"><span data-stu-id="43170-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="43170-115">A leitura da propriedade [Provider](provider-property-ado.md) também retornará essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="43170-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="43170-116">Sequência de conexão típica</span><span class="sxs-lookup"><span data-stu-id="43170-116">Typical Connection String</span></span>

<span data-ttu-id="43170-117">Esta é uma sequência de conexão típica para esse provedor:</span><span class="sxs-lookup"><span data-stu-id="43170-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="43170-118">A cadeia de caracteres consiste nas seguintes palavras-chave:</span><span class="sxs-lookup"><span data-stu-id="43170-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43170-119">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="43170-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="43170-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="43170-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43170-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="43170-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="43170-122">Especifica o OLE DB Provider for ODBC.</span><span class="sxs-lookup"><span data-stu-id="43170-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="43170-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="43170-124">Especifica o nome da fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="43170-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="43170-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="43170-126">Especifica o nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="43170-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="43170-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="43170-128">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="43170-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="43170-129"><strong>URL</strong></span></span></p></td>
<span data-ttu-id="43170-130"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="43170-130"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="43170-131">Especifica a URL de um arquivo ou diretório publicado em uma pasta da Web.</span><span class="sxs-lookup"><span data-stu-id="43170-131">Specifies the URL of a file or directory published in a Web folder.</span></span></p></td>
=======
<td><p><span data-ttu-id="43170-132">Especifica a URL de um arquivo ou diretório publicado em uma pasta da web.</span><span class="sxs-lookup"><span data-stu-id="43170-132">Specifies the URL of a file or directory published in a web folder.</span></span></p></td><span data-ttu-id="43170-133">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="43170-133">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>


<span data-ttu-id="43170-134">Como esse é o provedor padrão para o ADO, se você omitir o parâmetro **Provider=** na sequência de conexão, o ADO tentará estabelecer uma conexão com esse provedor.</span><span class="sxs-lookup"><span data-stu-id="43170-134">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="43170-p104">Embora não ofereça suporte a quaisquer parâmetros específicos de conexão além dos definidos pelo ADO, o provedor passará quaisquer parâmetros de conexão não-ADO para o gerenciador de driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="43170-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="43170-p105">Como é possível omitir o parâmetro **Provider**, você pode compor uma sequência de conexão ADO que seja idêntica a uma sequência de conexão ODBC para a mesma fonte de dados. Use os mesmos nomes de parâmetros (**DRIVER=**, **DATABASE=**, **DSN=**, e assim por diante), valores e sintaxe que você usaria para compor uma sequência de conexão ODBC. Você pode se conectar com ou sem um nome predefinido de fonte de dados (DSN) ou FileDSN.</span><span class="sxs-lookup"><span data-stu-id="43170-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="43170-140">**Sintaxe com um DSN ou FileDSN:**</span><span class="sxs-lookup"><span data-stu-id="43170-140">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="43170-141">**Sintaxe sem um DSN (conexão sem DSN):**</span><span class="sxs-lookup"><span data-stu-id="43170-141">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="43170-p106">Se você usar um **DSN** ou **FileDSN**, é necessário que ele seja definido com o Administrador de Fonte de Dados ODBC no Painel de Controle do Windows. No Microsoft Windows 2000, o Administrador ODBC está localizado nas Ferramentas Administrativas. Em versões anteriores do Windows, o ícone do Administrador ODBC era denominado **ODBC de 32 bits** ou simplesmente **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="43170-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="43170-145">Uma alternativa à definição de um **DSN** seria especificar o driver ODBC (**DRIVER=**), como "SQL Server;", o nome do servidor (**SERVER=**); e o nome do banco de dados (**DATABASE=**).</span><span class="sxs-lookup"><span data-stu-id="43170-145">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="43170-146">Você também pode especificar o nome de uma conta de usuário (**UID=**) e a senha dessa conta (**PWD=**) nos parâmetros específicos para ODBC ou nos parâmetros padrão *user* e *password* definidos pelo ADO.</span><span class="sxs-lookup"><span data-stu-id="43170-146">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="43170-147">Embora uma definição de **DSN** já especifica um banco de dados, você pode especificar *um* parâmetro de *banco de dados* , além de um **DSN** para se conectar a um banco de dados diferente.</span><span class="sxs-lookup"><span data-stu-id="43170-147">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="43170-148">É uma boa ideia sempre incluir *o* parâmetro de *banco de dados* quando você usa um **DSN**.</span><span class="sxs-lookup"><span data-stu-id="43170-148">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="43170-149">Isso garantirá a conexão com o banco de dados apropriado, mesmo que outro usuário tenha alterado o parâmetro referente do banco de dados padrão desde a última vez que você verificou a definição do **DSN**.</span><span class="sxs-lookup"><span data-stu-id="43170-149">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="43170-150">Parâmetros de conexão específicos para provedor</span><span class="sxs-lookup"><span data-stu-id="43170-150">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="43170-p108">O provedor OLE DB para ODBC adiciona várias propriedades à coleção [Properties](properties-collection-ado.md) do objeto **Connection**. A tabela abaixo lista essas propriedades, com o nome da propriedade do OLE DB correspondente entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="43170-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43170-153">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="43170-153">Property Name</span></span></p></th>
<th><p><span data-ttu-id="43170-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="43170-154">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43170-155">Accessible Procedures</span><span class="sxs-lookup"><span data-stu-id="43170-155">Accessible Procedures</span></span><br />
<span data-ttu-id="43170-156">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="43170-156">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="43170-157">Indica se o usuário tem acesso a procedimentos armazenados.</span><span class="sxs-lookup"><span data-stu-id="43170-157">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-158">Tabelas acessíveis</span><span class="sxs-lookup"><span data-stu-id="43170-158">Accessible Tables</span></span><br />
<span data-ttu-id="43170-159">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="43170-159">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="43170-160">Indica se o usuário tem permissão para executar instruções SELECT nas tabelas do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="43170-160">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-161">Instruções de ativas</span><span class="sxs-lookup"><span data-stu-id="43170-161">Active Statements</span></span><br />
<span data-ttu-id="43170-162">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="43170-162">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="43170-163">Indica o número de identificadores aos quais um driver ODBC pode oferecer suporte em uma conexão.</span><span class="sxs-lookup"><span data-stu-id="43170-163">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-164">Nome do driver</span><span class="sxs-lookup"><span data-stu-id="43170-164">Driver Name</span></span><br />
<span data-ttu-id="43170-165">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="43170-165">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="43170-166">Indica o nome do arquivo do driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="43170-166">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-167">Versão do driver ODBC</span><span class="sxs-lookup"><span data-stu-id="43170-167">Driver ODBC Version</span></span><br />
<span data-ttu-id="43170-168">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="43170-168">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="43170-169">Indica a versão do ODBC à qual o driver oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="43170-169">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-170">Uso de arquivos</span><span class="sxs-lookup"><span data-stu-id="43170-170">File Usage</span></span><br />
<span data-ttu-id="43170-171">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="43170-171">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="43170-172">Indica como o driver trata um arquivo em uma fonte de dados; como uma tabela ou como um catálogo.</span><span class="sxs-lookup"><span data-stu-id="43170-172">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-173">Escape cláusula LIKE</span><span class="sxs-lookup"><span data-stu-id="43170-173">Like Escape Clause</span></span><br />
<span data-ttu-id="43170-174">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="43170-174">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="43170-175">Indica se o driver oferece suporte à definição e utilização de um caractere de escape no lugar do caractere de porcentagem (%) e do caractere de sublinhado (_) no predicado LIKE de uma cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="43170-175">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-176">Máximo de colunas no grupo por</span><span class="sxs-lookup"><span data-stu-id="43170-176">Max Columns in Group By</span></span><br />
<span data-ttu-id="43170-177">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="43170-177">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="43170-178">Indica o número máximo de colunas que podem ser listadas na cláusula GROUP BY de uma instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="43170-178">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-179">Máximo de colunas no índice</span><span class="sxs-lookup"><span data-stu-id="43170-179">Max Columns in Index</span></span><br />
<span data-ttu-id="43170-180">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="43170-180">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="43170-181">Indica o número máximo de colunas que podem ser incluídas em um índice.</span><span class="sxs-lookup"><span data-stu-id="43170-181">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-182">Máximo de colunas por ordem</span><span class="sxs-lookup"><span data-stu-id="43170-182">Max Columns in Order By</span></span><br />
<span data-ttu-id="43170-183">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="43170-183">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="43170-184">Indica o número máximo de colunas que podem ser listadas na cláusula ORDER BY de uma instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="43170-184">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-185">Máximo de colunas em Select</span><span class="sxs-lookup"><span data-stu-id="43170-185">Max Columns in Select</span></span><br />
<span data-ttu-id="43170-186">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="43170-186">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="43170-187">Indica o número máximo de colunas que podem ser listadas na parte SELECT de uma instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="43170-187">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-188">Máximo de colunas na tabela</span><span class="sxs-lookup"><span data-stu-id="43170-188">Max Columns in Table</span></span><br />
<span data-ttu-id="43170-189">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="43170-189">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="43170-190">Indica o número máximo de colunas permitidas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="43170-190">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-191">Funções numéricas</span><span class="sxs-lookup"><span data-stu-id="43170-191">Numeric Functions</span></span><br />
<span data-ttu-id="43170-192">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="43170-192">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="43170-p109">Indica as funções numéricas às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</span><span class="sxs-lookup"><span data-stu-id="43170-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-195">Recursos de associação externa</span><span class="sxs-lookup"><span data-stu-id="43170-195">Outer Join Capabilities</span></span><br />
<span data-ttu-id="43170-196">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="43170-196">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="43170-197">Indica os tipos de junções externas (OUTER JOINs) aos quais o provedor oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="43170-197">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-198">Junções externas</span><span class="sxs-lookup"><span data-stu-id="43170-198">Outer Joins</span></span><br />
<span data-ttu-id="43170-199">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="43170-199">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="43170-200">Indica se o provedor oferece suporte a junções externas (OUTER JOINs).</span><span class="sxs-lookup"><span data-stu-id="43170-200">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-201">Caracteres especiais</span><span class="sxs-lookup"><span data-stu-id="43170-201">Special Characters</span></span><br />
<span data-ttu-id="43170-202">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="43170-202">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="43170-203">Indica quais caracteres têm um significado especial para o driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="43170-203">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-204">Procedimentos armazenados</span><span class="sxs-lookup"><span data-stu-id="43170-204">Stored Procedures</span></span><br />
<span data-ttu-id="43170-205">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="43170-205">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="43170-206">Indica se há procedimentos armazenados disponíveis para utilização com esse driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="43170-206">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-207">Funções de sequência</span><span class="sxs-lookup"><span data-stu-id="43170-207">String Functions</span></span><br />
<span data-ttu-id="43170-208">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="43170-208">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="43170-p110">Indica as funções de cadeia de caracteres às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</span><span class="sxs-lookup"><span data-stu-id="43170-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-211">Funções do sistema</span><span class="sxs-lookup"><span data-stu-id="43170-211">System Functions</span></span><br />
<span data-ttu-id="43170-212">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="43170-212">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="43170-p111">Indica as funções do sistema às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</span><span class="sxs-lookup"><span data-stu-id="43170-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-215">Funções de data/hora</span><span class="sxs-lookup"><span data-stu-id="43170-215">Time/Date Functions</span></span><br />
<span data-ttu-id="43170-216">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="43170-216">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="43170-p112">Indica as funções de hora e data às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</span><span class="sxs-lookup"><span data-stu-id="43170-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-219">Suporte a gramática SQL</span><span class="sxs-lookup"><span data-stu-id="43170-219">SQL Grammar Support</span></span><br />
<span data-ttu-id="43170-220">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="43170-220">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="43170-221">Indica a gramática SQL à qual o driver ODBC oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="43170-221">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="43170-222">Propriedades de Recordset e Command específicas para provedor</span><span class="sxs-lookup"><span data-stu-id="43170-222">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="43170-p113">O provedor OLE DB para ODBC adiciona várias propriedades à coleção **Properties** dos objetos **Recordset** e **Command**. A tabela abaixo lista essas propriedades com o nome da propriedade do OLE DB correspondente entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="43170-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43170-225">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="43170-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="43170-226">Descrição</span><span class="sxs-lookup"><span data-stu-id="43170-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43170-227">Consultas com base em exclui/atualizações/inserirá</span><span class="sxs-lookup"><span data-stu-id="43170-227">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="43170-228">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="43170-228">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="43170-229">Indica se atualizações, exclusões e inserções podem ser realizadas utilizando consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="43170-229">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-230">Tipo de simultaneidade ODBC</span><span class="sxs-lookup"><span data-stu-id="43170-230">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="43170-231">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="43170-231">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="43170-232">Indica o método utilizado para reduzir problemas potenciais que surgem quando dois usuários tentam acessar simultaneamente os mesmos dados na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="43170-232">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-233">Acessibilidade do BLOB no cursor somente de encaminhamento</span><span class="sxs-lookup"><span data-stu-id="43170-233">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="43170-234">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="43170-234">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="43170-235">Indica se <strong>Fields</strong> BLOB podem ser acessados quando um cursor somente de encaminhamento estiver sendo utilizado.</span><span class="sxs-lookup"><span data-stu-id="43170-235">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-236">Incluem valores SQL_FLOAT, SQL_DOUBLE e SQL_REAL em QBU WHERE cláusulas</span><span class="sxs-lookup"><span data-stu-id="43170-236">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="43170-237">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="43170-237">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="43170-238">Indica se valores SQL_FLOAT, SQL_DOUBLE e SQL_REAL podem ser incluídos em uma cláusula QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="43170-238">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-239">Posição na última linha, após inserir</span><span class="sxs-lookup"><span data-stu-id="43170-239">Position on the last row after insert</span></span><br />
<span data-ttu-id="43170-240">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="43170-240">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="43170-241">Indica que, após a inserção de um novo registro em uma tabela, a última linha da tabela passará a ser a linha atual.</span><span class="sxs-lookup"><span data-stu-id="43170-241">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-242">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="43170-242">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="43170-243">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="43170-243">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="43170-244">Indica se a interface <strong>IRowsetChange</strong> oferece suporte a informações estendidas.</span><span class="sxs-lookup"><span data-stu-id="43170-244">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-245">Tipo de Cursor ODBC</span><span class="sxs-lookup"><span data-stu-id="43170-245">ODBC Cursor Type</span></span><br />
<span data-ttu-id="43170-246">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="43170-246">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="43170-247">Indica o tipo de cursor utilizado pelo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="43170-247">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-248">Gerar um conjunto de linhas que pode ser empacotado.</span><span class="sxs-lookup"><span data-stu-id="43170-248">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="43170-249">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="43170-249">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="43170-250">Indica que o driver ODBC gera um conjunto de registros que pode ser empacotado.</span><span class="sxs-lookup"><span data-stu-id="43170-250">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="43170-251">Texto de comando</span><span class="sxs-lookup"><span data-stu-id="43170-251">Command Text</span></span>

<span data-ttu-id="43170-252">A forma de utilização do objeto [Command](command-object-ado.md) depende em grande parte da fonte de dados e dos tipos de consultas e instruções de comando que ela aceita.</span><span class="sxs-lookup"><span data-stu-id="43170-252">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="43170-253">O ODBC fornece uma sintaxe específica para chamar procedimentos armazenados.</span><span class="sxs-lookup"><span data-stu-id="43170-253">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="43170-254">Para a propriedade [CommandText](commandtext-property-ado.md) do argumento *origem* para o método **Open** em um [Recordset](recordset-object-ado.md) , o argumento *CommandText* para o método **Execute** em um objeto de [Conexão](connection-object-ado.md) ou um objeto **Command** objeto, passa em uma cadeia de caracteres com esta sintaxe:</span><span class="sxs-lookup"><span data-stu-id="43170-254">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="43170-p115">Cada **?** faz referência a um objeto na coleção [Parameters](parameters-collection-ado.md). O primeiro **?** faz referência a **Parameters**(0), o segundo **?** a **Parameters**(1), e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="43170-p115">Each **?** references an object in the [Parameters](parameters-collection-ado.md) collection. The first **?** references **Parameters**(0), the next **?** references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="43170-p116">As referências a parâmetros são opcionais e dependem da estrutura do procedimento armazenado. Se você quiser chamar um procedimento armazenado que não define qualquer parâmetro, sua cadeia de caracteres será semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="43170-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="43170-262">Se você tiver dois parâmetros de consulta, sua cadeia de caracteres será semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="43170-262">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="43170-p117">Se o procedimento armazenado retornar um valor, esse valor de retorno será tratado como outro parâmetro. Se você não tiver parâmetros de consulta, mas tiver um valor de retorno, sua cadeia de caracteres será semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="43170-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="43170-265">Finalmente, se você tiver um valor de retorno e dois parâmetros de consulta, sua cadeia de caracteres será semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="43170-265">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="43170-266">Comportamento do Recordset</span><span class="sxs-lookup"><span data-stu-id="43170-266">Recordset Behavior</span></span>

<span data-ttu-id="43170-267">As tabelas abaixo listam os métodos e propriedades do ADO disponíveis em um objeto **Recordset** aberto com esse provedor.</span><span class="sxs-lookup"><span data-stu-id="43170-267">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="43170-268">Para obter informações mais detalhadas sobre o comportamento do **Recordset** na sua configuração de provedor, execute o método [Supports](supports-method-ado.md) e enumere a coleção **Properties** de **Recordset** para identificar se propriedades dinâmicas específicas para provedor estão presentes.</span><span class="sxs-lookup"><span data-stu-id="43170-268">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="43170-269">Disponibilidade das propriedades padrão do **Recordset** do ADO:</span><span class="sxs-lookup"><span data-stu-id="43170-269">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43170-270">Propriedade</span><span class="sxs-lookup"><span data-stu-id="43170-270">Property</span></span></p></th>
<th><p><span data-ttu-id="43170-271">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="43170-271">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="43170-272">Dinâmico</span><span class="sxs-lookup"><span data-stu-id="43170-272">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="43170-273">Conjunto de chaves</span><span class="sxs-lookup"><span data-stu-id="43170-273">Keyset</span></span></p></th>
<th><p><span data-ttu-id="43170-274">Estático</span><span class="sxs-lookup"><span data-stu-id="43170-274">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43170-275"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="43170-275"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="43170-276">não disponível</span><span class="sxs-lookup"><span data-stu-id="43170-276">not available</span></span></p></td>
<td><p><span data-ttu-id="43170-277">não disponível</span><span class="sxs-lookup"><span data-stu-id="43170-277">not available</span></span></p></td>
<td><p><span data-ttu-id="43170-278">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-278">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-279">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-279">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-280"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="43170-280"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="43170-281">não disponível</span><span class="sxs-lookup"><span data-stu-id="43170-281">not available</span></span></p></td>
<td><p><span data-ttu-id="43170-282">não disponível</span><span class="sxs-lookup"><span data-stu-id="43170-282">not available</span></span></p></td>
<td><p><span data-ttu-id="43170-283">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-284">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-284">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-285"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="43170-285"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="43170-286">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-286">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-287">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-287">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-288">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-288">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-289">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-289">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-290"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="43170-290"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="43170-291">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-291">read-only</span></span></p></td>
<td><p><span data-ttu-id="43170-292">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-292">read-only</span></span></p></td>
<td><p><span data-ttu-id="43170-293">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-293">read-only</span></span></p></td>
<td><p><span data-ttu-id="43170-294">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-294">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-295"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="43170-295"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="43170-296">não disponível</span><span class="sxs-lookup"><span data-stu-id="43170-296">not available</span></span></p></td>
<td><p><span data-ttu-id="43170-297">não disponível</span><span class="sxs-lookup"><span data-stu-id="43170-297">not available</span></span></p></td>
<td><p><span data-ttu-id="43170-298">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-299">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-299">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-300"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="43170-300"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="43170-301">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-301">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-302">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-302">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-303">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-304">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-304">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-305"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="43170-305"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="43170-306">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-306">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-307">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-307">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-308">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-309">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-309">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-310"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="43170-310"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="43170-311">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-311">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-312">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-312">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-313">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-313">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-314">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-314">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-315"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="43170-315"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="43170-316">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-316">read-only</span></span></p></td>
<td><p><span data-ttu-id="43170-317">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-317">read-only</span></span></p></td>
<td><p><span data-ttu-id="43170-318">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-318">read-only</span></span></p></td>
<td><p><span data-ttu-id="43170-319">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-319">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-320"><a href="filter-property-ado.md">Filtrar</a></span><span class="sxs-lookup"><span data-stu-id="43170-320"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="43170-321">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-321">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-322">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-322">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-323">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-324">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-324">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-325"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="43170-325"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="43170-326">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-326">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-327">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-327">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-328">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-329">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-329">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-330"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="43170-330"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="43170-331">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-331">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-332">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-332">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-333">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-334">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-334">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-335"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="43170-335"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="43170-336">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-336">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-337">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-337">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-338">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-339">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-339">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-340"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="43170-340"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="43170-341">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-341">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-342">não disponível</span><span class="sxs-lookup"><span data-stu-id="43170-342">not available</span></span></p></td>
<td><p><span data-ttu-id="43170-343">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-343">read-only</span></span></p></td>
<td><p><span data-ttu-id="43170-344">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-344">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-345"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="43170-345"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="43170-346">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-346">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-347">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-347">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-348">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-349">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-349">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-350"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="43170-350"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="43170-351">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-351">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-352">não disponível</span><span class="sxs-lookup"><span data-stu-id="43170-352">not available</span></span></p></td>
<td><p><span data-ttu-id="43170-353">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-353">read-only</span></span></p></td>
<td><p><span data-ttu-id="43170-354">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-354">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-355"><a href="source-property-ado-recordset.md">Origem</a></span><span class="sxs-lookup"><span data-stu-id="43170-355"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="43170-356">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-356">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-357">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-357">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-358">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-358">read/write</span></span></p></td>
<td><p><span data-ttu-id="43170-359">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43170-359">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-360"><a href="state-property-ado.md">Estado</a></span><span class="sxs-lookup"><span data-stu-id="43170-360"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="43170-361">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-361">read-only</span></span></p></td>
<td><p><span data-ttu-id="43170-362">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-362">read-only</span></span></p></td>
<td><p><span data-ttu-id="43170-363">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="43170-364">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-364">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-365"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="43170-365"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="43170-366">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-366">read-only</span></span></p></td>
<td><p><span data-ttu-id="43170-367">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-367">read-only</span></span></p></td>
<td><p><span data-ttu-id="43170-368">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-368">read-only</span></span></p></td>
<td><p><span data-ttu-id="43170-369">somente leitura</span><span class="sxs-lookup"><span data-stu-id="43170-369">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="43170-370">As propriedades [AbsolutePosition](absoluteposition-property-ado.md) e [AbsolutePage](absolutepage-property-ado.md) são somente leitura quando o ADO é utilizado com a versão 1.0 do Microsoft OLE DB Provider for ODBC.</span><span class="sxs-lookup"><span data-stu-id="43170-370">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="43170-371">Disponibilidade dos métodos padrão do **Recordset** do ADO:</span><span class="sxs-lookup"><span data-stu-id="43170-371">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43170-372">Método</span><span class="sxs-lookup"><span data-stu-id="43170-372">Method</span></span></p></th>
<th><p><span data-ttu-id="43170-373">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="43170-373">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="43170-374">Dinâmico</span><span class="sxs-lookup"><span data-stu-id="43170-374">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="43170-375">Conjunto de chaves</span><span class="sxs-lookup"><span data-stu-id="43170-375">Keyset</span></span></p></th>
<th><p><span data-ttu-id="43170-376">Estático</span><span class="sxs-lookup"><span data-stu-id="43170-376">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43170-377"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="43170-377"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="43170-378">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-378">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-379">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-379">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-380">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-381">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-381">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-382"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="43170-382"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="43170-383">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-383">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-384">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-384">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-385">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-386">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-386">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-387"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="43170-387"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="43170-388">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-388">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-389">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-389">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-390">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-391">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-391">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-392"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="43170-392"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="43170-393">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-393">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-394">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-394">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-395">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-395">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-396">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-396">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-397"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="43170-397"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="43170-398">Não</span><span class="sxs-lookup"><span data-stu-id="43170-398">No</span></span></p></td>
<td><p><span data-ttu-id="43170-399">Não</span><span class="sxs-lookup"><span data-stu-id="43170-399">No</span></span></p></td>
<td><p><span data-ttu-id="43170-400">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-401">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-401">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-402"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="43170-402"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="43170-403">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-403">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-404">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-404">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-405">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-406">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-406">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-407"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="43170-407"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="43170-408">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-408">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-409">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-409">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-410">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-411">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-411">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-412"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="43170-412"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="43170-413">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-413">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-414">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-414">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-415">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-416">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-416">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-417"><a href="move-method-ado.md">Mover</a></span><span class="sxs-lookup"><span data-stu-id="43170-417"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="43170-418">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-418">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-419">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-419">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-420">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-421">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-421">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-422"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Métodos MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="43170-422"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="43170-423">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-423">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-424">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-424">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-425">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-425">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-426">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-426">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-427"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="43170-427"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="43170-428">Não</span><span class="sxs-lookup"><span data-stu-id="43170-428">No</span></span></p></td>
<td><p><span data-ttu-id="43170-429">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-429">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-430">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-431">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-431">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-432"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="43170-432"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="43170-433">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-433">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-434">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-434">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-435">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-435">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-436">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-436">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-437"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="43170-437"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="43170-438">Não</span><span class="sxs-lookup"><span data-stu-id="43170-438">No</span></span></p></td>
<td><p><span data-ttu-id="43170-439">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-439">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-440">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-441">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-442"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="43170-442"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="43170-443">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-443">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-444">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-444">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-445">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-446">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-446">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-447"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="43170-447"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="43170-448">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-448">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-449">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-449">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-450">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-451">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-451">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-452"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="43170-452"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="43170-453">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-453">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-454">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-454">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-455">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-455">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-456">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-456">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-457"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="43170-457"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="43170-458">Não</span><span class="sxs-lookup"><span data-stu-id="43170-458">No</span></span></p></td>
<td><p><span data-ttu-id="43170-459">Não</span><span class="sxs-lookup"><span data-stu-id="43170-459">No</span></span></p></td>
<td><p><span data-ttu-id="43170-460">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-461">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-461">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-462"><a href="supports-method-ado.md">Suporta</a></span><span class="sxs-lookup"><span data-stu-id="43170-462"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="43170-463">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-463">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-464">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-464">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-465">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-466">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-466">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-467"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="43170-467"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="43170-468">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-468">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-469">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-469">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-470">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-471">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-471">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-472"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="43170-472"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="43170-473">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-473">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-474">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-474">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-475">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-475">Yes</span></span></p></td>
<td><p><span data-ttu-id="43170-476">Sim</span><span class="sxs-lookup"><span data-stu-id="43170-476">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="43170-477">\*Sem suporte em bancos de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="43170-477">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="43170-478">Propriedades dinâmicas</span><span class="sxs-lookup"><span data-stu-id="43170-478">Dynamic Properties</span></span>

<span data-ttu-id="43170-479">O Microsoft OLE DB Provider for ODBC insere várias propriedades dinâmicas na coleção **Properties** dos objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) e [Command](command-object-ado.md) não abertos.</span><span class="sxs-lookup"><span data-stu-id="43170-479">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="43170-p118">As tabelas abaixo são um índice cruzado dos nomes do ADO e do OLE DB de cada propriedade dinâmica. A Referência do programador do OLE DB diz respeito a um nome de propriedade do ADO de acordo com o termo, "Descrição." Você encontrará mais informações sobre essas propriedades na Referência do programador do OLE DB. Localize o nome da propriedade do OLE DB no Índice ou consulte o Apêndice C: propriedades do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="43170-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="43170-484">Propriedades dinâmicas de Connection</span><span class="sxs-lookup"><span data-stu-id="43170-484">Connection Dynamic Properties</span></span>

<span data-ttu-id="43170-485">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="43170-485">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43170-486">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="43170-486">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="43170-487">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="43170-487">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43170-488">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="43170-488">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="43170-489">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="43170-489">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-490">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="43170-490">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="43170-491">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="43170-491">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-492">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="43170-492">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="43170-493">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="43170-493">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-494">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="43170-494">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="43170-495">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="43170-495">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-496">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="43170-496">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="43170-497">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="43170-497">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-498">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="43170-498">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="43170-499">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="43170-499">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-500">Column Definition</span><span class="sxs-lookup"><span data-stu-id="43170-500">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="43170-501">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="43170-501">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-502">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="43170-502">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="43170-503">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="43170-503">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-504">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="43170-504">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="43170-505">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="43170-505">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-506">Data Source</span><span class="sxs-lookup"><span data-stu-id="43170-506">Data Source</span></span></p></td>
<td><p><span data-ttu-id="43170-507">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="43170-507">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-508">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="43170-508">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="43170-509">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="43170-509">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-510">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="43170-510">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="43170-511">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="43170-511">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-512">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="43170-512">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="43170-513">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="43170-513">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-514">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="43170-514">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="43170-515">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="43170-515">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-516">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="43170-516">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="43170-517">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="43170-517">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-518">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="43170-518">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="43170-519">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="43170-519">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-520">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="43170-520">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="43170-521">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="43170-521">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-522">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="43170-522">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="43170-523">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="43170-523">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-524">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="43170-524">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="43170-525">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="43170-525">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-526">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="43170-526">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="43170-527">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="43170-527">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-528">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="43170-528">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="43170-529">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="43170-529">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-530">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="43170-530">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="43170-531">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="43170-531">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-532">Location</span><span class="sxs-lookup"><span data-stu-id="43170-532">Location</span></span></p></td>
<td><p><span data-ttu-id="43170-533">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="43170-533">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-534">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="43170-534">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="43170-535">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="43170-535">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-536">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="43170-536">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="43170-537">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="43170-537">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-538">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="43170-538">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="43170-539">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="43170-539">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-540">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="43170-540">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="43170-541">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="43170-541">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-542">Mode</span><span class="sxs-lookup"><span data-stu-id="43170-542">Mode</span></span></p></td>
<td><p><span data-ttu-id="43170-543">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="43170-543">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-544">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="43170-544">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="43170-545">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="43170-545">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-546">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="43170-546">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="43170-547">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="43170-547">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-548">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="43170-548">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="43170-549">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="43170-549">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-550">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="43170-550">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="43170-551">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="43170-551">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-552">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="43170-552">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="43170-553">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="43170-553">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-554">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="43170-554">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="43170-555">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="43170-555">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-556">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="43170-556">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="43170-557">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="43170-557">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-558">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="43170-558">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="43170-559">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="43170-559">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-560">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="43170-560">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="43170-561">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="43170-561">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-562">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="43170-562">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="43170-563">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="43170-563">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-564">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="43170-564">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="43170-565">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="43170-565">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-566">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="43170-566">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="43170-567">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="43170-567">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-568">Password</span><span class="sxs-lookup"><span data-stu-id="43170-568">Password</span></span></p></td>
<td><p><span data-ttu-id="43170-569">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="43170-569">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-570">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="43170-570">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="43170-571">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="43170-571">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-572">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="43170-572">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="43170-573">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="43170-573">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-574">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="43170-574">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="43170-575">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="43170-575">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-576">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="43170-576">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="43170-577">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="43170-577">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-578">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="43170-578">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="43170-579">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="43170-579">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-580">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="43170-580">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="43170-581">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="43170-581">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-582">Prompt</span><span class="sxs-lookup"><span data-stu-id="43170-582">Prompt</span></span></p></td>
<td><p><span data-ttu-id="43170-583">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="43170-583">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-584">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="43170-584">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="43170-585">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="43170-585">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-586">Provider Name</span><span class="sxs-lookup"><span data-stu-id="43170-586">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="43170-587">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="43170-587">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-588">Provider Version</span><span class="sxs-lookup"><span data-stu-id="43170-588">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="43170-589">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="43170-589">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-590">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="43170-590">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="43170-591">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="43170-591">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-592">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="43170-592">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="43170-593">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="43170-593">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-594">Schema Term</span><span class="sxs-lookup"><span data-stu-id="43170-594">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="43170-595">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="43170-595">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-596">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="43170-596">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="43170-597">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="43170-597">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-598">SQL Support</span><span class="sxs-lookup"><span data-stu-id="43170-598">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="43170-599">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="43170-599">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-600">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="43170-600">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="43170-601">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="43170-601">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-602">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="43170-602">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="43170-603">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="43170-603">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-604">Table Term</span><span class="sxs-lookup"><span data-stu-id="43170-604">Table Term</span></span></p></td>
<td><p><span data-ttu-id="43170-605">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="43170-605">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-606">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="43170-606">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="43170-607">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="43170-607">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-608">User ID</span><span class="sxs-lookup"><span data-stu-id="43170-608">User ID</span></span></p></td>
<td><p><span data-ttu-id="43170-609">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="43170-609">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-610">User Name</span><span class="sxs-lookup"><span data-stu-id="43170-610">User Name</span></span></p></td>
<td><p><span data-ttu-id="43170-611">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="43170-611">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-612">Window Handle</span><span class="sxs-lookup"><span data-stu-id="43170-612">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="43170-613">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="43170-613">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="43170-614">Propriedades dinâmicas do Recordset</span><span class="sxs-lookup"><span data-stu-id="43170-614">Recordset Dynamic Properties</span></span>

<span data-ttu-id="43170-615">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="43170-615">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43170-616">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="43170-616">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="43170-617">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="43170-617">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43170-618">Access Order</span><span class="sxs-lookup"><span data-stu-id="43170-618">Access Order</span></span></p></td>
<td><p><span data-ttu-id="43170-619">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="43170-619">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-620">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="43170-620">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="43170-621">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="43170-621">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-622">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="43170-622">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="43170-623">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="43170-623">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-624">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="43170-624">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="43170-625">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="43170-625">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-626">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="43170-626">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="43170-627">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="43170-627">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-628">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="43170-628">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="43170-629">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="43170-629">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-630">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="43170-630">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-631">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="43170-631">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-632">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="43170-632">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="43170-633">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="43170-633">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-634">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="43170-634">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="43170-635">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="43170-635">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-636">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="43170-636">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="43170-637">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="43170-637">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-638">IAccessor</span><span class="sxs-lookup"><span data-stu-id="43170-638">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="43170-639">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="43170-639">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-640">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="43170-640">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="43170-641">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="43170-641">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-642">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="43170-642">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="43170-643">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="43170-643">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-644">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="43170-644">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="43170-645">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="43170-645">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-646">IConvertType</span><span class="sxs-lookup"><span data-stu-id="43170-646">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="43170-647">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="43170-647">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-648">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="43170-648">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="43170-649">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="43170-649">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-650">IRowset</span><span class="sxs-lookup"><span data-stu-id="43170-650">IRowset</span></span></p></td>
<td><p><span data-ttu-id="43170-651">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="43170-651">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-652">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="43170-652">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="43170-653">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="43170-653">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-654">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="43170-654">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="43170-655">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="43170-655">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-656">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="43170-656">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="43170-657">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="43170-657">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-658">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="43170-658">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="43170-659">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="43170-659">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-660">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="43170-660">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-661">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="43170-661">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="43170-662">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="43170-662">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-663">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="43170-663">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="43170-664">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="43170-664">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-665">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="43170-665">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="43170-666">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="43170-666">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-667">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="43170-667">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="43170-668">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="43170-668">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-669">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="43170-669">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="43170-670">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="43170-670">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-671">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="43170-671">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="43170-672">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="43170-672">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-673">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="43170-673">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="43170-674">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="43170-674">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-675">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="43170-675">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="43170-676">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="43170-676">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-677">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="43170-677">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="43170-678">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="43170-678">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-679">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="43170-679">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="43170-680">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="43170-680">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-681">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="43170-681">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="43170-682">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="43170-682">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-683">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="43170-683">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="43170-684">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="43170-684">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-685">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="43170-685">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="43170-686">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="43170-686">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-687">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="43170-687">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="43170-688">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="43170-688">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-689">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="43170-689">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="43170-690">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="43170-690">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-691">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="43170-691">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="43170-692">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="43170-692">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-693">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="43170-693">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="43170-694">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="43170-694">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-695">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="43170-695">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="43170-696">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="43170-696">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-697">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="43170-697">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="43170-698">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="43170-698">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-699">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="43170-699">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="43170-700">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="43170-700">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-701">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="43170-701">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-702">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="43170-702">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-703">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="43170-703">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-704">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="43170-704">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-705">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="43170-705">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-706">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="43170-706">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-707">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="43170-707">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="43170-708">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="43170-708">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-709">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="43170-709">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-710">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="43170-710">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-711">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="43170-711">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="43170-712">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="43170-712">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-713">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="43170-713">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-714">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="43170-714">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-715">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="43170-715">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-716">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="43170-716">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-717">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="43170-717">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-718">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="43170-718">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-719">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="43170-719">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-720">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="43170-720">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-721">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="43170-721">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-722">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="43170-722">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-723">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="43170-723">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-724">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="43170-724">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-725">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="43170-725">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="43170-726">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="43170-726">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-727">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="43170-727">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="43170-728">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="43170-728">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-729">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="43170-729">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="43170-730">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="43170-730">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-731">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="43170-731">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="43170-732">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="43170-732">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-733">Updatability</span><span class="sxs-lookup"><span data-stu-id="43170-733">Updatability</span></span></p></td>
<td><p><span data-ttu-id="43170-734">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="43170-734">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-735">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="43170-735">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="43170-736">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="43170-736">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="43170-737">Propriedades dinâmicas do Command</span><span class="sxs-lookup"><span data-stu-id="43170-737">Command Dynamic Properties</span></span>

<span data-ttu-id="43170-738">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="43170-738">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43170-739">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="43170-739">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="43170-740">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="43170-740">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43170-741">Access Order</span><span class="sxs-lookup"><span data-stu-id="43170-741">Access Order</span></span></p></td>
<td><p><span data-ttu-id="43170-742">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="43170-742">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-743">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="43170-743">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="43170-744">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="43170-744">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-745">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="43170-745">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="43170-746">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="43170-746">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-747">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="43170-747">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="43170-748">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="43170-748">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-749">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="43170-749">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="43170-750">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="43170-750">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-751">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="43170-751">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="43170-752">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="43170-752">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-753">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="43170-753">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-754">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="43170-754">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-755">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="43170-755">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="43170-756">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="43170-756">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-757">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="43170-757">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="43170-758">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="43170-758">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-759">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="43170-759">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="43170-760">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="43170-760">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-761">IAccessor</span><span class="sxs-lookup"><span data-stu-id="43170-761">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="43170-762">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="43170-762">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-763">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="43170-763">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="43170-764">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="43170-764">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-765">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="43170-765">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="43170-766">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="43170-766">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-767">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="43170-767">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="43170-768">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="43170-768">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-769">IConvertType</span><span class="sxs-lookup"><span data-stu-id="43170-769">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="43170-770">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="43170-770">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-771">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="43170-771">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="43170-772">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="43170-772">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-773">IRowset</span><span class="sxs-lookup"><span data-stu-id="43170-773">IRowset</span></span></p></td>
<td><p><span data-ttu-id="43170-774">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="43170-774">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-775">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="43170-775">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="43170-776">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="43170-776">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-777">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="43170-777">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="43170-778">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="43170-778">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-779">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="43170-779">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="43170-780">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="43170-780">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-781">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="43170-781">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="43170-782">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="43170-782">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-783">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="43170-783">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-784">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="43170-784">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="43170-785">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="43170-785">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-786">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="43170-786">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="43170-787">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="43170-787">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-788">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="43170-788">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="43170-789">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="43170-789">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-790">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="43170-790">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="43170-791">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="43170-791">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-792">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="43170-792">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="43170-793">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="43170-793">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-794">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="43170-794">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="43170-795">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="43170-795">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-796">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="43170-796">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="43170-797">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="43170-797">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-798">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="43170-798">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="43170-799">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="43170-799">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-800">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="43170-800">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="43170-801">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="43170-801">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-802">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="43170-802">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="43170-803">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="43170-803">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-804">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="43170-804">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="43170-805">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="43170-805">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-806">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="43170-806">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="43170-807">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="43170-807">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-808">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="43170-808">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="43170-809">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="43170-809">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-810">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="43170-810">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="43170-811">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="43170-811">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-812">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="43170-812">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="43170-813">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="43170-813">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-814">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="43170-814">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="43170-815">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="43170-815">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-816">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="43170-816">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="43170-817">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="43170-817">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-818">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="43170-818">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="43170-819">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="43170-819">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-820">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="43170-820">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="43170-821">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="43170-821">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-822">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="43170-822">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="43170-823">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="43170-823">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-824">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="43170-824">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-825">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="43170-825">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-826">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="43170-826">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-827">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="43170-827">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-828">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="43170-828">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-829">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="43170-829">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-830">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="43170-830">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="43170-831">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="43170-831">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-832">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="43170-832">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-833">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="43170-833">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-834">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="43170-834">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="43170-835">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="43170-835">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-836">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="43170-836">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-837">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="43170-837">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-838">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="43170-838">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-839">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="43170-839">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-840">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="43170-840">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-841">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="43170-841">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-842">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="43170-842">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-843">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="43170-843">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-844">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="43170-844">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-845">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="43170-845">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-846">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="43170-846">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="43170-847">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="43170-847">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-848">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="43170-848">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="43170-849">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="43170-849">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-850">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="43170-850">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="43170-851">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="43170-851">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-852">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="43170-852">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="43170-853">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="43170-853">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43170-854">Updatability</span><span class="sxs-lookup"><span data-stu-id="43170-854">Updatability</span></span></p></td>
<td><p><span data-ttu-id="43170-855">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="43170-855">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43170-856">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="43170-856">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="43170-857">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="43170-857">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="43170-858">Confira também</span><span class="sxs-lookup"><span data-stu-id="43170-858">See also</span></span>

<span data-ttu-id="43170-859">Para obter detalhes sobre a implementação específica e informações funcionais sobre o Microsoft OLE DB Provider for ODBC, consulte o [Guia do programador do OLE DB do](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) ou visite a [Central de desenvolvedores de plataforma de dados](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="43170-859">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

