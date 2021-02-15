---
title: Microsoft OLE DB Provider for ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f5ffae4880cadb90f47f1ac348ffc8b3ea58785
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288908"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="8d140-102">Provedor Microsoft OLE DB para ODBC</span><span class="sxs-lookup"><span data-stu-id="8d140-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="8d140-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d140-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d140-p101">Para um programador de ADO ou RDS, o mundo ideal seria aquele em que todas as fontes de dados apresentassem uma interface OLE DB, de modo que as chamadas do ADO pudessem ser feitas diretamente na fonte de dados. Embora cada vez mais fornecedores de bancos de dados venham implementando interfaces OLE DB, algumas fontes de dados ainda não são expostas dessa maneira. Por outro lado, praticamente todos os sistemas DBMS em uso hoje em dia podem ser acessados por ODBC.</span><span class="sxs-lookup"><span data-stu-id="8d140-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="8d140-107">Já existem drivers ODBC disponíveis para todos os principais DBMS em uso atualmente, incluindo Microsoft SQL Server, Microsoft Access (mecanismo de banco de dados do Microsoft Jet) e Microsoft FoxPro, além de produtos de banco de dados produzidos por outro fornecedor, como a Oracle.</span><span class="sxs-lookup"><span data-stu-id="8d140-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="8d140-p102">Entretanto, o Microsoft ODBC Provider permite a conexão do ADO com qualquer fonte de dados ODBC. O provedor é de encadeamento livre e habilitado para Unicode.</span><span class="sxs-lookup"><span data-stu-id="8d140-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="8d140-p103">O provedor oferece suporte a transações, embora diferentes mecanismos DBMS ofereçam diferentes tipos de suporte a transações. Por exemplo, o Microsoft Access oferece suporte a transações aninhadas com até cinco níveis de profundidade.</span><span class="sxs-lookup"><span data-stu-id="8d140-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="8d140-112">Esse é o provedor padrão para o ADO, oferecendo suporte a todas propriedades e métodos do ADO dependentes de provedor.</span><span class="sxs-lookup"><span data-stu-id="8d140-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="8d140-113">Parâmetros da sequência de conexão</span><span class="sxs-lookup"><span data-stu-id="8d140-113">Connection String Parameters</span></span>

<span data-ttu-id="8d140-114">Para estabelecer uma conexão com esse provedor, defina o argumento **Provider=** da propriedade [ConnectionString](connectionstring-property-ado.md) como:</span><span class="sxs-lookup"><span data-stu-id="8d140-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="8d140-115">A leitura da propriedade [Provider](provider-property-ado.md) também retornará essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8d140-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="8d140-116">Sequência de conexão típica</span><span class="sxs-lookup"><span data-stu-id="8d140-116">Typical Connection String</span></span>

<span data-ttu-id="8d140-117">Esta é uma sequência de conexão típica para esse provedor:</span><span class="sxs-lookup"><span data-stu-id="8d140-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="8d140-118">A cadeia de caracteres consiste nas seguintes palavras-chave:</span><span class="sxs-lookup"><span data-stu-id="8d140-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d140-119">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="8d140-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="8d140-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d140-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d140-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="8d140-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="8d140-122">Especifica o OLE DB Provider for ODBC.</span><span class="sxs-lookup"><span data-stu-id="8d140-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="8d140-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="8d140-124">Especifica o nome da fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="8d140-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="8d140-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="8d140-126">Especifica o nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="8d140-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="8d140-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="8d140-128">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="8d140-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="8d140-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="8d140-130">Especifica a URL de um arquivo ou diretório publicado em uma pasta da Web.</span><span class="sxs-lookup"><span data-stu-id="8d140-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d140-131">Como esse é o provedor padrão para o ADO, se você omitir o parâmetro **Provider=** na sequência de conexão, o ADO tentará estabelecer uma conexão com esse provedor.</span><span class="sxs-lookup"><span data-stu-id="8d140-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="8d140-p104">Embora não ofereça suporte a quaisquer parâmetros específicos de conexão além dos definidos pelo ADO, o provedor passará quaisquer parâmetros de conexão não-ADO para o gerenciador de driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="8d140-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="8d140-p105">Como é possível omitir o parâmetro **Provider**, você pode compor uma sequência de conexão ADO que seja idêntica a uma sequência de conexão ODBC para a mesma fonte de dados. Use os mesmos nomes de parâmetros (**DRIVER=**, **DATABASE=**, **DSN=**, e assim por diante), valores e sintaxe que você usaria para compor uma sequência de conexão ODBC. Você pode se conectar com ou sem um nome predefinido de fonte de dados (DSN) ou FileDSN.</span><span class="sxs-lookup"><span data-stu-id="8d140-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="8d140-137">**Sintaxe com um DSN ou FileDSN:**</span><span class="sxs-lookup"><span data-stu-id="8d140-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="8d140-138">**Sintaxe sem um DSN (conexão sem DSN):**</span><span class="sxs-lookup"><span data-stu-id="8d140-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="8d140-p106">Se você usar um **DSN** ou **FileDSN**, é necessário que ele seja definido com o Administrador de Fonte de Dados ODBC no Painel de Controle do Windows. No Microsoft Windows 2000, o Administrador ODBC está localizado nas Ferramentas Administrativas. Em versões anteriores do Windows, o ícone do Administrador ODBC era denominado **ODBC de 32 bits** ou simplesmente **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="8d140-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="8d140-142">Uma alternativa à definição de um **DSN** seria especificar o driver ODBC (**DRIVER=**), como "SQL Server;", o nome do servidor (**SERVER=**); e o nome do banco de dados (**DATABASE=**).</span><span class="sxs-lookup"><span data-stu-id="8d140-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="8d140-143">Você também pode especificar o nome de uma conta de usuário (**UID=**) e a senha dessa conta (**PWD=**) nos parâmetros específicos para ODBC ou nos parâmetros padrão *user* e *password* definidos pelo ADO.</span><span class="sxs-lookup"><span data-stu-id="8d140-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="8d140-144">Embora uma **definição de DSN** já   especifique um banco de dados, você pode especificar um parâmetro de banco de dados além de um **DSN** para se conectar a um banco de dados diferente.</span><span class="sxs-lookup"><span data-stu-id="8d140-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="8d140-145">É uma boa ideia sempre incluir o *parâmetro* *de* banco de dados quando você usa um **DSN**.</span><span class="sxs-lookup"><span data-stu-id="8d140-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="8d140-146">Isso garantirá a conexão com o banco de dados apropriado, mesmo que outro usuário tenha alterado o parâmetro referente do banco de dados padrão desde a última vez que você verificou a definição do **DSN**.</span><span class="sxs-lookup"><span data-stu-id="8d140-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="8d140-147">Parâmetros de conexão específicos para provedor</span><span class="sxs-lookup"><span data-stu-id="8d140-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="8d140-p108">O provedor OLE DB para ODBC adiciona várias propriedades à coleção [Properties](properties-collection-ado.md) do objeto **Connection**. A tabela abaixo lista essas propriedades, com o nome da propriedade do OLE DB correspondente entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="8d140-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d140-150">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="8d140-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="8d140-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d140-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d140-152">Procedimentos acessíveis</span><span class="sxs-lookup"><span data-stu-id="8d140-152">Accessible Procedures</span></span><br />
<span data-ttu-id="8d140-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="8d140-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="8d140-154">Indica se o usuário tem acesso a procedimentos armazenados.</span><span class="sxs-lookup"><span data-stu-id="8d140-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-155">Tabelas Acessíveis</span><span class="sxs-lookup"><span data-stu-id="8d140-155">Accessible Tables</span></span><br />
<span data-ttu-id="8d140-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="8d140-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="8d140-157">Indica se o usuário tem permissão para executar instruções SELECT nas tabelas do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8d140-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-158">Instruções ativas</span><span class="sxs-lookup"><span data-stu-id="8d140-158">Active Statements</span></span><br />
<span data-ttu-id="8d140-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="8d140-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="8d140-160">Indica o número de identificadores aos quais um driver ODBC pode oferecer suporte em uma conexão.</span><span class="sxs-lookup"><span data-stu-id="8d140-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-161">Nome do driver</span><span class="sxs-lookup"><span data-stu-id="8d140-161">Driver Name</span></span><br />
<span data-ttu-id="8d140-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="8d140-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="8d140-163">Indica o nome do arquivo do driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="8d140-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-164">Driver ODBC Version</span><span class="sxs-lookup"><span data-stu-id="8d140-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="8d140-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="8d140-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="8d140-166">Indica a versão do ODBC à qual o driver oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="8d140-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-167">Uso do arquivo</span><span class="sxs-lookup"><span data-stu-id="8d140-167">File Usage</span></span><br />
<span data-ttu-id="8d140-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="8d140-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="8d140-169">Indica como o driver trata um arquivo em uma fonte de dados; como uma tabela ou como um catálogo.</span><span class="sxs-lookup"><span data-stu-id="8d140-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-170">Cláusula Like Escape</span><span class="sxs-lookup"><span data-stu-id="8d140-170">Like Escape Clause</span></span><br />
<span data-ttu-id="8d140-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="8d140-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="8d140-172">Indica se o driver oferece suporte à definição e utilização de um caractere de escape no lugar do caractere de porcentagem (%) e do caractere de sublinhado (_) no predicado LIKE de uma cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="8d140-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-173">Max Columns in Group By</span><span class="sxs-lookup"><span data-stu-id="8d140-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="8d140-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="8d140-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="8d140-175">Indica o número máximo de colunas que podem ser listadas na cláusula GROUP BY de uma instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="8d140-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-176">Max Columns in Index</span><span class="sxs-lookup"><span data-stu-id="8d140-176">Max Columns in Index</span></span><br />
<span data-ttu-id="8d140-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="8d140-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="8d140-178">Indica o número máximo de colunas que podem ser incluídas em um índice.</span><span class="sxs-lookup"><span data-stu-id="8d140-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-179">Max Columns in Order By</span><span class="sxs-lookup"><span data-stu-id="8d140-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="8d140-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="8d140-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="8d140-181">Indica o número máximo de colunas que podem ser listadas na cláusula ORDER BY de uma instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="8d140-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-182">Max Columns in Select</span><span class="sxs-lookup"><span data-stu-id="8d140-182">Max Columns in Select</span></span><br />
<span data-ttu-id="8d140-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="8d140-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="8d140-184">Indica o número máximo de colunas que podem ser listadas na parte SELECT de uma instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="8d140-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-185">Max Columns in Table</span><span class="sxs-lookup"><span data-stu-id="8d140-185">Max Columns in Table</span></span><br />
<span data-ttu-id="8d140-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="8d140-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="8d140-187">Indica o número máximo de colunas permitidas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="8d140-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-188">Funções numéricas</span><span class="sxs-lookup"><span data-stu-id="8d140-188">Numeric Functions</span></span><br />
<span data-ttu-id="8d140-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="8d140-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="8d140-p109">Indica as funções numéricas às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</span><span class="sxs-lookup"><span data-stu-id="8d140-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-192">Recursos de junção externa</span><span class="sxs-lookup"><span data-stu-id="8d140-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="8d140-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="8d140-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="8d140-194">Indica os tipos de junções externas (OUTER JOINs) aos quais o provedor oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="8d140-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-195">Junções externas</span><span class="sxs-lookup"><span data-stu-id="8d140-195">Outer Joins</span></span><br />
<span data-ttu-id="8d140-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="8d140-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="8d140-197">Indica se o provedor oferece suporte a junções externas (OUTER JOINs).</span><span class="sxs-lookup"><span data-stu-id="8d140-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-198">Caracteres especiais</span><span class="sxs-lookup"><span data-stu-id="8d140-198">Special Characters</span></span><br />
<span data-ttu-id="8d140-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="8d140-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="8d140-200">Indica quais caracteres têm um significado especial para o driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="8d140-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-201">Procedimentos armazenados</span><span class="sxs-lookup"><span data-stu-id="8d140-201">Stored Procedures</span></span><br />
<span data-ttu-id="8d140-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="8d140-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="8d140-203">Indica se há procedimentos armazenados disponíveis para utilização com esse driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="8d140-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-204">Funções de sequência</span><span class="sxs-lookup"><span data-stu-id="8d140-204">String Functions</span></span><br />
<span data-ttu-id="8d140-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="8d140-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="8d140-p110">Indica as funções de cadeia de caracteres às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</span><span class="sxs-lookup"><span data-stu-id="8d140-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-208">Funções do sistema</span><span class="sxs-lookup"><span data-stu-id="8d140-208">System Functions</span></span><br />
<span data-ttu-id="8d140-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="8d140-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="8d140-p111">Indica as funções do sistema às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</span><span class="sxs-lookup"><span data-stu-id="8d140-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-212">Funções Hora/Data</span><span class="sxs-lookup"><span data-stu-id="8d140-212">Time/Date Functions</span></span><br />
<span data-ttu-id="8d140-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="8d140-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="8d140-p112">Indica as funções de hora e data às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</span><span class="sxs-lookup"><span data-stu-id="8d140-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-216">Suporte a gramática SQL</span><span class="sxs-lookup"><span data-stu-id="8d140-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="8d140-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="8d140-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="8d140-218">Indica a gramática SQL à qual o driver ODBC oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="8d140-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="8d140-219">Propriedades de Recordset e Command específicas para provedor</span><span class="sxs-lookup"><span data-stu-id="8d140-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="8d140-p113">O provedor OLE DB para ODBC adiciona várias propriedades à coleção **Properties** dos objetos **Recordset** e **Command**. A tabela abaixo lista essas propriedades com o nome da propriedade do OLE DB correspondente entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="8d140-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d140-222">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="8d140-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="8d140-223">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d140-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d140-224">Atualizações/Exclusões/Inserções Baseadas em Consulta</span><span class="sxs-lookup"><span data-stu-id="8d140-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="8d140-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="8d140-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="8d140-226">Indica se atualizações, exclusões e inserções podem ser realizadas utilizando consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="8d140-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-227">Tipo de competência ODBC</span><span class="sxs-lookup"><span data-stu-id="8d140-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="8d140-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="8d140-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="8d140-229">Indica o método utilizado para reduzir problemas potenciais que surgem quando dois usuários tentam acessar simultaneamente os mesmos dados na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="8d140-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-230">Acessibilidade BLOB no Forward-Only cursor</span><span class="sxs-lookup"><span data-stu-id="8d140-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="8d140-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="8d140-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="8d140-232">Indica se <strong>Fields</strong> BLOB podem ser acessados quando um cursor somente de encaminhamento estiver sendo utilizado.</span><span class="sxs-lookup"><span data-stu-id="8d140-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-233">Incluir SQL_FLOAT, SQL_DOUBLE e SQL_REAL em cláusulas QBU WHERE</span><span class="sxs-lookup"><span data-stu-id="8d140-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="8d140-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="8d140-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="8d140-235">Indica se valores SQL_FLOAT, SQL_DOUBLE e SQL_REAL podem ser incluídos em uma cláusula QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="8d140-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-236">Posição na última linha após a inserção</span><span class="sxs-lookup"><span data-stu-id="8d140-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="8d140-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="8d140-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="8d140-238">Indica que, após a inserção de um novo registro em uma tabela, a última linha da tabela passará a ser a linha atual.</span><span class="sxs-lookup"><span data-stu-id="8d140-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="8d140-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="8d140-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="8d140-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="8d140-241">Indica se a interface <strong>IRowsetChange</strong> oferece suporte a informações estendidas.</span><span class="sxs-lookup"><span data-stu-id="8d140-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-242">Tipo de cursor ODBC</span><span class="sxs-lookup"><span data-stu-id="8d140-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="8d140-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="8d140-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="8d140-244">Indica o tipo de cursor utilizado pelo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="8d140-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-245">Gerar um rowset que pode ser empacotado</span><span class="sxs-lookup"><span data-stu-id="8d140-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="8d140-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="8d140-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="8d140-247">Indica que o driver ODBC gera um conjunto de registros que pode ser empacotado.</span><span class="sxs-lookup"><span data-stu-id="8d140-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="8d140-248">Texto de comando</span><span class="sxs-lookup"><span data-stu-id="8d140-248">Command Text</span></span>

<span data-ttu-id="8d140-249">A forma de utilização do objeto [Command](command-object-ado.md) depende em grande parte da fonte de dados e dos tipos de consultas e instruções de comando que ela aceita.</span><span class="sxs-lookup"><span data-stu-id="8d140-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="8d140-p114">O ODBC fornece uma sintaxe específica para chamar procedimentos armazenados. Para a propriedade [CommandText](commandtext-property-ado.md) de um objeto **Command**, o argumento *CommandText* do método **Execute** em um objeto [Connection](connection-object-ado.md) ou o argumento *Source* do método **Open** em um objeto [Recordset](recordset-object-ado.md), deve-se passar uma cadeia de caracteres com a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="8d140-p114">ODBC provides a specific syntax for calling stored procedures. For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="8d140-252">Cada **?**</span><span class="sxs-lookup"><span data-stu-id="8d140-252">Each **?**</span></span> <span data-ttu-id="8d140-253">faz referência a um objeto na coleção [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8d140-253">references an object in the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="8d140-254">O primeiro **?**</span><span class="sxs-lookup"><span data-stu-id="8d140-254">The first **?**</span></span> <span data-ttu-id="8d140-255">parâmetros **de referência**(0), o **próximo?**</span><span class="sxs-lookup"><span data-stu-id="8d140-255">references **Parameters**(0), the next **?**</span></span> <span data-ttu-id="8d140-256">faz referência **a parâmetros**(1) e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8d140-256">references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="8d140-p116">As referências a parâmetros são opcionais e dependem da estrutura do procedimento armazenado. Se você quiser chamar um procedimento armazenado que não define qualquer parâmetro, sua cadeia de caracteres será semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="8d140-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="8d140-259">Se você tiver dois parâmetros de consulta, sua cadeia de caracteres será semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="8d140-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="8d140-p117">Se o procedimento armazenado retornar um valor, esse valor de retorno será tratado como outro parâmetro. Se você não tiver parâmetros de consulta, mas tiver um valor de retorno, sua cadeia de caracteres será semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="8d140-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="8d140-262">Finalmente, se você tiver um valor de retorno e dois parâmetros de consulta, sua cadeia de caracteres será semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="8d140-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="8d140-263">Comportamento do Recordset</span><span class="sxs-lookup"><span data-stu-id="8d140-263">Recordset Behavior</span></span>

<span data-ttu-id="8d140-264">As tabelas abaixo listam os métodos e propriedades do ADO disponíveis em um objeto **Recordset** aberto com esse provedor.</span><span class="sxs-lookup"><span data-stu-id="8d140-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="8d140-265">Para obter informações mais detalhadas sobre o comportamento do **Recordset** na sua configuração de provedor, execute o método [Supports](supports-method-ado.md) e enumere a coleção **Properties** de **Recordset** para identificar se propriedades dinâmicas específicas para provedor estão presentes.</span><span class="sxs-lookup"><span data-stu-id="8d140-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="8d140-266">Disponibilidade das propriedades padrão do **Recordset** do ADO:</span><span class="sxs-lookup"><span data-stu-id="8d140-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="8d140-267">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8d140-267">Property</span></span></p></th>
<th><p><span data-ttu-id="8d140-268">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="8d140-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="8d140-269">Dinâmica</span><span class="sxs-lookup"><span data-stu-id="8d140-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="8d140-270">Conjunto de chaves</span><span class="sxs-lookup"><span data-stu-id="8d140-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="8d140-271">Estático</span><span class="sxs-lookup"><span data-stu-id="8d140-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d140-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="8d140-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-273">não disponível</span><span class="sxs-lookup"><span data-stu-id="8d140-273">not available</span></span></p></td>
<td><p><span data-ttu-id="8d140-274">não disponível</span><span class="sxs-lookup"><span data-stu-id="8d140-274">not available</span></span></p></td>
<td><p><span data-ttu-id="8d140-275">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-276">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="8d140-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-278">não disponível</span><span class="sxs-lookup"><span data-stu-id="8d140-278">not available</span></span></p></td>
<td><p><span data-ttu-id="8d140-279">não disponível</span><span class="sxs-lookup"><span data-stu-id="8d140-279">not available</span></span></p></td>
<td><p><span data-ttu-id="8d140-280">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-281">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="8d140-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-283">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-284">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-285">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-286">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="8d140-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-288">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="8d140-289">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="8d140-290">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="8d140-291">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="8d140-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-293">não disponível</span><span class="sxs-lookup"><span data-stu-id="8d140-293">not available</span></span></p></td>
<td><p><span data-ttu-id="8d140-294">não disponível</span><span class="sxs-lookup"><span data-stu-id="8d140-294">not available</span></span></p></td>
<td><p><span data-ttu-id="8d140-295">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-296">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="8d140-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-298">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-299">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-300">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-301">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="8d140-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-303">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-304">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-305">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-306">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="8d140-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-308">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-309">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-310">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-311">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="8d140-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-313">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="8d140-314">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="8d140-315">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="8d140-316">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-317"><a href="filter-property-ado.md">Filtro</a></span><span class="sxs-lookup"><span data-stu-id="8d140-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-318">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-319">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-320">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-321">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-322"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="8d140-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-323">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-324">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-325">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-326">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="8d140-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-328">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-329">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-330">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-331">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="8d140-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-333">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-334">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-335">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-336">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="8d140-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-338">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-339">não disponível</span><span class="sxs-lookup"><span data-stu-id="8d140-339">not available</span></span></p></td>
<td><p><span data-ttu-id="8d140-340">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="8d140-341">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="8d140-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-343">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-344">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-345">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-346">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="8d140-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-348">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-349">não disponível</span><span class="sxs-lookup"><span data-stu-id="8d140-349">not available</span></span></p></td>
<td><p><span data-ttu-id="8d140-350">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="8d140-351">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-352"><a href="source-property-ado-recordset.md">Fonte</a></span><span class="sxs-lookup"><span data-stu-id="8d140-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-353">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-354">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-355">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="8d140-356">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8d140-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="8d140-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-358">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="8d140-359">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="8d140-360">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="8d140-361">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-362"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="8d140-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-363">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="8d140-364">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="8d140-365">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="8d140-366">somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d140-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d140-367">As propriedades [AbsolutePosition](absoluteposition-property-ado.md) e [AbsolutePage](absolutepage-property-ado.md) são somente leitura quando o ADO é utilizado com a versão 1.0 do Microsoft OLE DB Provider for ODBC.</span><span class="sxs-lookup"><span data-stu-id="8d140-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="8d140-368">Disponibilidade dos métodos padrão do **Recordset** do ADO:</span><span class="sxs-lookup"><span data-stu-id="8d140-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="8d140-369">Método</span><span class="sxs-lookup"><span data-stu-id="8d140-369">Method</span></span></p></th>
<th><p><span data-ttu-id="8d140-370">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="8d140-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="8d140-371">Dinâmica</span><span class="sxs-lookup"><span data-stu-id="8d140-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="8d140-372">Conjunto de chaves</span><span class="sxs-lookup"><span data-stu-id="8d140-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="8d140-373">Estático</span><span class="sxs-lookup"><span data-stu-id="8d140-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d140-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="8d140-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-375">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-376">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-377">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-378">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-379"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="8d140-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-380">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-381">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-382">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-383">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="8d140-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-385">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-386">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-387">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-388">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="8d140-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-390">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-391">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-392">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-393">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="8d140-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-395">Não</span><span class="sxs-lookup"><span data-stu-id="8d140-395">No</span></span></p></td>
<td><p><span data-ttu-id="8d140-396">Não</span><span class="sxs-lookup"><span data-stu-id="8d140-396">No</span></span></p></td>
<td><p><span data-ttu-id="8d140-397">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-398">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="8d140-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-400">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-401">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-402">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-403">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-404"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="8d140-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-405">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-406">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-407">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-408">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="8d140-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-410">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-411">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-412">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-413">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-414"><a href="move-method-ado.md">Mover</a></span><span class="sxs-lookup"><span data-stu-id="8d140-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-415">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-416">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-417">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-418">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="8d140-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-420">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-421">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-422">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-423">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="8d140-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-425">Não</span><span class="sxs-lookup"><span data-stu-id="8d140-425">No</span></span></p></td>
<td><p><span data-ttu-id="8d140-426">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-427">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-428">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="8d140-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-430">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-431">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-432">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-433">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="8d140-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-435">Não</span><span class="sxs-lookup"><span data-stu-id="8d140-435">No</span></span></p></td>
<td><p><span data-ttu-id="8d140-436">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-437">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-438">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="8d140-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="8d140-440">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-441">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-442">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-443">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="8d140-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-445">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-446">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-447">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-448">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="8d140-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-450">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-451">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-452">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-453">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-454"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="8d140-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-455">Não</span><span class="sxs-lookup"><span data-stu-id="8d140-455">No</span></span></p></td>
<td><p><span data-ttu-id="8d140-456">Não</span><span class="sxs-lookup"><span data-stu-id="8d140-456">No</span></span></p></td>
<td><p><span data-ttu-id="8d140-457">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-458">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-459"><a href="supports-method-ado.md">Oferece suporte</a></span><span class="sxs-lookup"><span data-stu-id="8d140-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-460">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-461">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-462">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-463">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-464"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="8d140-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-465">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-466">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-467">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-468">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="8d140-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="8d140-470">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-471">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-472">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="8d140-473">Sim</span><span class="sxs-lookup"><span data-stu-id="8d140-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d140-474">\*Sem suporte em bancos de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8d140-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="8d140-475">Propriedades dinâmicas</span><span class="sxs-lookup"><span data-stu-id="8d140-475">Dynamic Properties</span></span>

<span data-ttu-id="8d140-476">O Microsoft OLE DB Provider for ODBC insere várias propriedades dinâmicas na coleção **Properties** dos objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) e [Command](command-object-ado.md) não abertos.</span><span class="sxs-lookup"><span data-stu-id="8d140-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="8d140-p118">As tabelas abaixo são um índice cruzado dos nomes do ADO e do OLE DB de cada propriedade dinâmica. A Referência do programador do OLE DB diz respeito a um nome de propriedade do ADO de acordo com o termo, "Descrição." Você encontrará mais informações sobre essas propriedades na Referência do programador do OLE DB. Localize o nome da propriedade do OLE DB no Índice ou consulte o Apêndice C: propriedades do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="8d140-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="8d140-481">Propriedades dinâmicas de Connection</span><span class="sxs-lookup"><span data-stu-id="8d140-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="8d140-482">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="8d140-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d140-483">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="8d140-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="8d140-484">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="8d140-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d140-485">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="8d140-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="8d140-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="8d140-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-487">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="8d140-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="8d140-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="8d140-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-489">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="8d140-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="8d140-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="8d140-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-491">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="8d140-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="8d140-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="8d140-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-493">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="8d140-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="8d140-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="8d140-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-495">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="8d140-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="8d140-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="8d140-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-497">Column Definition</span><span class="sxs-lookup"><span data-stu-id="8d140-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="8d140-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="8d140-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-499">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="8d140-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="8d140-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="8d140-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-501">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="8d140-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="8d140-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="8d140-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-503">Data Source</span><span class="sxs-lookup"><span data-stu-id="8d140-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="8d140-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="8d140-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-505">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="8d140-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="8d140-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="8d140-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-507">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="8d140-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="8d140-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="8d140-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-509">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="8d140-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="8d140-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="8d140-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-511">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="8d140-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="8d140-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="8d140-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-513">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="8d140-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="8d140-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="8d140-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-515">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="8d140-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="8d140-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="8d140-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-517">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="8d140-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="8d140-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="8d140-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-519">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="8d140-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="8d140-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="8d140-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-521">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="8d140-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="8d140-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8d140-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-523">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="8d140-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="8d140-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="8d140-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-525">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="8d140-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="8d140-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="8d140-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-527">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="8d140-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="8d140-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="8d140-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-529">Localização</span><span class="sxs-lookup"><span data-stu-id="8d140-529">Location</span></span></p></td>
<td><p><span data-ttu-id="8d140-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="8d140-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-531">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="8d140-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="8d140-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="8d140-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-533">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="8d140-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="8d140-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="8d140-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-535">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="8d140-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="8d140-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="8d140-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-537">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="8d140-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="8d140-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="8d140-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-539">Modo</span><span class="sxs-lookup"><span data-stu-id="8d140-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="8d140-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="8d140-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-541">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="8d140-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="8d140-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="8d140-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-543">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="8d140-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="8d140-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="8d140-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-545">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="8d140-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="8d140-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="8d140-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-547">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="8d140-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="8d140-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="8d140-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-549">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="8d140-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="8d140-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="8d140-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-551">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="8d140-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="8d140-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="8d140-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-553">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="8d140-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="8d140-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="8d140-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-555">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="8d140-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="8d140-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="8d140-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-557">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="8d140-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="8d140-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="8d140-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-559">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="8d140-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="8d140-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="8d140-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-561">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="8d140-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="8d140-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="8d140-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-563">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="8d140-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="8d140-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="8d140-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-565">Password</span><span class="sxs-lookup"><span data-stu-id="8d140-565">Password</span></span></p></td>
<td><p><span data-ttu-id="8d140-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="8d140-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-567">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="8d140-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="8d140-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="8d140-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-569">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="8d140-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="8d140-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="8d140-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-571">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="8d140-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="8d140-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="8d140-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-573">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="8d140-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="8d140-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="8d140-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-575">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="8d140-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="8d140-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="8d140-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-577">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="8d140-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="8d140-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="8d140-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="8d140-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="8d140-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="8d140-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-581">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="8d140-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="8d140-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="8d140-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-583">Provider Name</span><span class="sxs-lookup"><span data-stu-id="8d140-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="8d140-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="8d140-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-585">Provider Version</span><span class="sxs-lookup"><span data-stu-id="8d140-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="8d140-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="8d140-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-587">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="8d140-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="8d140-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="8d140-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-589">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="8d140-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="8d140-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="8d140-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-591">Schema Term</span><span class="sxs-lookup"><span data-stu-id="8d140-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="8d140-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="8d140-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-593">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="8d140-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="8d140-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="8d140-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-595">SQL Support</span><span class="sxs-lookup"><span data-stu-id="8d140-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="8d140-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="8d140-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-597">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="8d140-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="8d140-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="8d140-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-599">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="8d140-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="8d140-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="8d140-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-601">Table Term</span><span class="sxs-lookup"><span data-stu-id="8d140-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="8d140-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="8d140-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-603">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="8d140-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="8d140-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="8d140-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-605">User ID</span><span class="sxs-lookup"><span data-stu-id="8d140-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="8d140-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="8d140-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-607">User Name</span><span class="sxs-lookup"><span data-stu-id="8d140-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="8d140-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="8d140-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-609">Window Handle</span><span class="sxs-lookup"><span data-stu-id="8d140-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="8d140-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="8d140-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="8d140-611">Propriedades dinâmicas do Recordset</span><span class="sxs-lookup"><span data-stu-id="8d140-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="8d140-612">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="8d140-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d140-613">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="8d140-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="8d140-614">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="8d140-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d140-615">Access Order</span><span class="sxs-lookup"><span data-stu-id="8d140-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="8d140-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="8d140-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-617">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="8d140-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="8d140-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="8d140-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-619">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="8d140-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="8d140-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="8d140-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="8d140-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="8d140-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="8d140-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-623">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="8d140-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="8d140-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="8d140-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-625">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="8d140-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="8d140-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="8d140-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-627">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="8d140-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-629">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="8d140-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="8d140-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="8d140-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-631">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="8d140-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="8d140-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="8d140-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-633">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="8d140-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="8d140-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="8d140-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="8d140-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="8d140-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="8d140-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="8d140-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="8d140-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="8d140-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="8d140-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="8d140-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="8d140-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="8d140-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="8d140-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="8d140-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="8d140-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="8d140-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="8d140-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-645">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="8d140-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="8d140-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="8d140-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="8d140-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="8d140-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="8d140-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="8d140-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="8d140-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="8d140-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="8d140-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="8d140-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="8d140-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="8d140-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="8d140-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="8d140-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="8d140-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="8d140-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="8d140-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="8d140-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="8d140-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="8d140-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="8d140-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="8d140-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="8d140-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="8d140-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="8d140-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="8d140-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="8d140-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-664">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="8d140-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8d140-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="8d140-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-666">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="8d140-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="8d140-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="8d140-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-668">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="8d140-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="8d140-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="8d140-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-670">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="8d140-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="8d140-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="8d140-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-672">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="8d140-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="8d140-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="8d140-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-674">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="8d140-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="8d140-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="8d140-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-676">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="8d140-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="8d140-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="8d140-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-678">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="8d140-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="8d140-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="8d140-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-680">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="8d140-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="8d140-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="8d140-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-682">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="8d140-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="8d140-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="8d140-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-684">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="8d140-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="8d140-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="8d140-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-686">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="8d140-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="8d140-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="8d140-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-688">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="8d140-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="8d140-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="8d140-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-690">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="8d140-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="8d140-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="8d140-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-692">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="8d140-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="8d140-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="8d140-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-694">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="8d140-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="8d140-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="8d140-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-696">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="8d140-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="8d140-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="8d140-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-698">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="8d140-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-700">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="8d140-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-702">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="8d140-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-704">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="8d140-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="8d140-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="8d140-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-706">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="8d140-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-708">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="8d140-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="8d140-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="8d140-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-710">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="8d140-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-712">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="8d140-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-714">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="8d140-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-716">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="8d140-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-718">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="8d140-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-720">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="8d140-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-722">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="8d140-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="8d140-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="8d140-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-724">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="8d140-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8d140-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="8d140-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-726">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="8d140-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="8d140-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="8d140-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-728">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="8d140-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="8d140-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="8d140-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-730">Updatability</span><span class="sxs-lookup"><span data-stu-id="8d140-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="8d140-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="8d140-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-732">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="8d140-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8d140-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="8d140-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="8d140-734">Propriedades dinâmicas do Command</span><span class="sxs-lookup"><span data-stu-id="8d140-734">Command Dynamic Properties</span></span>

<span data-ttu-id="8d140-735">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="8d140-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d140-736">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="8d140-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="8d140-737">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="8d140-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d140-738">Access Order</span><span class="sxs-lookup"><span data-stu-id="8d140-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="8d140-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="8d140-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-740">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="8d140-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="8d140-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="8d140-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-742">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="8d140-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="8d140-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="8d140-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="8d140-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="8d140-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="8d140-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-746">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="8d140-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="8d140-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="8d140-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-748">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="8d140-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="8d140-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="8d140-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-750">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="8d140-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-752">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="8d140-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="8d140-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="8d140-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-754">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="8d140-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="8d140-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="8d140-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-756">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="8d140-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="8d140-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="8d140-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="8d140-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="8d140-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="8d140-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="8d140-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="8d140-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="8d140-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="8d140-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="8d140-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="8d140-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="8d140-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="8d140-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="8d140-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="8d140-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="8d140-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="8d140-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-768">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="8d140-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="8d140-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="8d140-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="8d140-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="8d140-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="8d140-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="8d140-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="8d140-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="8d140-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="8d140-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="8d140-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="8d140-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="8d140-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="8d140-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="8d140-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="8d140-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="8d140-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="8d140-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="8d140-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="8d140-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="8d140-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="8d140-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="8d140-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="8d140-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="8d140-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="8d140-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="8d140-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="8d140-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-787">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="8d140-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8d140-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="8d140-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-789">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="8d140-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="8d140-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="8d140-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-791">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="8d140-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="8d140-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="8d140-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-793">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="8d140-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="8d140-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="8d140-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-795">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="8d140-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="8d140-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="8d140-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-797">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="8d140-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="8d140-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="8d140-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-799">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="8d140-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="8d140-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="8d140-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-801">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="8d140-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="8d140-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="8d140-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-803">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="8d140-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="8d140-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="8d140-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-805">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="8d140-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="8d140-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="8d140-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-807">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="8d140-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="8d140-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="8d140-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-809">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="8d140-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="8d140-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="8d140-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-811">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="8d140-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="8d140-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="8d140-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-813">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="8d140-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="8d140-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="8d140-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-815">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="8d140-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="8d140-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="8d140-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-817">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="8d140-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="8d140-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="8d140-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-819">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="8d140-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="8d140-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="8d140-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-821">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="8d140-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-823">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="8d140-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-825">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="8d140-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-827">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="8d140-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="8d140-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="8d140-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-829">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="8d140-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-831">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="8d140-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="8d140-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="8d140-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-833">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="8d140-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-835">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="8d140-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-837">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="8d140-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-839">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="8d140-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-841">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="8d140-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-843">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="8d140-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="8d140-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="8d140-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-845">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="8d140-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="8d140-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="8d140-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-847">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="8d140-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8d140-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="8d140-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-849">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="8d140-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="8d140-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="8d140-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d140-851">Updatability</span><span class="sxs-lookup"><span data-stu-id="8d140-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="8d140-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="8d140-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d140-853">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="8d140-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="8d140-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="8d140-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8d140-855">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d140-855">See also</span></span>

<span data-ttu-id="8d140-856">Para obter detalhes sobre a implementação específica e informações funcionais sobre o Microsoft OLE DB Provider for ODBC, consulte o Guia do Programador do [OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) ou visite a Central de Desenvolvedores da Plataforma de [Dados.](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017)</span><span class="sxs-lookup"><span data-stu-id="8d140-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

