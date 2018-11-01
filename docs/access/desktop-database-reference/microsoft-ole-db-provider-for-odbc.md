---
title: Microsoft OLE DB Provider for ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66ef27165e6f5823cc97a295643dfc2ae5c205c2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883180"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="dcfdb-102">Microsoft OLE DB Provider for ODBC</span><span class="sxs-lookup"><span data-stu-id="dcfdb-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="dcfdb-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="dcfdb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dcfdb-p101">Para um programador de ADO ou RDS, o mundo ideal seria aquele em que todas as fontes de dados apresentassem uma interface OLE DB, de modo que as chamadas do ADO pudessem ser feitas diretamente na fonte de dados. Embora cada vez mais fornecedores de bancos de dados venham implementando interfaces OLE DB, algumas fontes de dados ainda não são expostas dessa maneira. Por outro lado, praticamente todos os sistemas DBMS em uso hoje em dia podem ser acessados por ODBC.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="dcfdb-107">Já existem drivers ODBC disponíveis para todos os principais DBMS em uso atualmente, incluindo Microsoft SQL Server, Microsoft Access (mecanismo de banco de dados do Microsoft Jet) e Microsoft FoxPro, além de produtos de banco de dados produzidos por outro fornecedor, como a Oracle.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="dcfdb-p102">Entretanto, o Microsoft ODBC Provider permite a conexão do ADO com qualquer fonte de dados ODBC. O provedor é de encadeamento livre e habilitado para Unicode.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="dcfdb-p103">O provedor oferece suporte a transações, embora diferentes mecanismos DBMS ofereçam diferentes tipos de suporte a transações. Por exemplo, o Microsoft Access oferece suporte a transações aninhadas com até cinco níveis de profundidade.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="dcfdb-112">Esse é o provedor padrão para o ADO, oferecendo suporte a todas propriedades e métodos do ADO dependentes de provedor.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="dcfdb-113">Parâmetros da sequência de conexão</span><span class="sxs-lookup"><span data-stu-id="dcfdb-113">Connection String Parameters</span></span>

<span data-ttu-id="dcfdb-114">Para estabelecer uma conexão com esse provedor, defina o argumento **Provider=** da propriedade [ConnectionString](connectionstring-property-ado.md) como:</span><span class="sxs-lookup"><span data-stu-id="dcfdb-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="dcfdb-115">A leitura da propriedade [Provider](provider-property-ado.md) também retornará essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="dcfdb-116">Sequência de conexão típica</span><span class="sxs-lookup"><span data-stu-id="dcfdb-116">Typical Connection String</span></span>

<span data-ttu-id="dcfdb-117">Esta é uma sequência de conexão típica para esse provedor:</span><span class="sxs-lookup"><span data-stu-id="dcfdb-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="dcfdb-118">A cadeia de caracteres consiste nas seguintes palavras-chave:</span><span class="sxs-lookup"><span data-stu-id="dcfdb-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dcfdb-119">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="dcfdb-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="dcfdb-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="dcfdb-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="dcfdb-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-122">Especifica o OLE DB Provider for ODBC.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="dcfdb-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-124">Especifica o nome da fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="dcfdb-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-126">Especifica o nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="dcfdb-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-128">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="dcfdb-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-130">Especifica a URL de um arquivo ou diretório publicado em uma pasta da web.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dcfdb-131">Como esse é o provedor padrão para o ADO, se você omitir o parâmetro **Provider=** na sequência de conexão, o ADO tentará estabelecer uma conexão com esse provedor.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="dcfdb-p104">Embora não ofereça suporte a quaisquer parâmetros específicos de conexão além dos definidos pelo ADO, o provedor passará quaisquer parâmetros de conexão não-ADO para o gerenciador de driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="dcfdb-p105">Como é possível omitir o parâmetro **Provider**, você pode compor uma sequência de conexão ADO que seja idêntica a uma sequência de conexão ODBC para a mesma fonte de dados. Use os mesmos nomes de parâmetros (**DRIVER=**, **DATABASE=**, **DSN=**, e assim por diante), valores e sintaxe que você usaria para compor uma sequência de conexão ODBC. Você pode se conectar com ou sem um nome predefinido de fonte de dados (DSN) ou FileDSN.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="dcfdb-137">**Sintaxe com um DSN ou FileDSN:**</span><span class="sxs-lookup"><span data-stu-id="dcfdb-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="dcfdb-138">**Sintaxe sem um DSN (conexão sem DSN):**</span><span class="sxs-lookup"><span data-stu-id="dcfdb-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="dcfdb-p106">Se você usar um **DSN** ou **FileDSN**, é necessário que ele seja definido com o Administrador de Fonte de Dados ODBC no Painel de Controle do Windows. No Microsoft Windows 2000, o Administrador ODBC está localizado nas Ferramentas Administrativas. Em versões anteriores do Windows, o ícone do Administrador ODBC era denominado **ODBC de 32 bits** ou simplesmente **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="dcfdb-142">Uma alternativa à definição de um **DSN** seria especificar o driver ODBC (**DRIVER=**), como "SQL Server;", o nome do servidor (**SERVER=**); e o nome do banco de dados (**DATABASE=**).</span><span class="sxs-lookup"><span data-stu-id="dcfdb-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="dcfdb-143">Você também pode especificar o nome de uma conta de usuário (**UID=**) e a senha dessa conta (**PWD=**) nos parâmetros específicos para ODBC ou nos parâmetros padrão *user* e *password* definidos pelo ADO.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="dcfdb-144">Embora uma definição de **DSN** já especifica um banco de dados, você pode especificar *um* parâmetro de *banco de dados* , além de um **DSN** para se conectar a um banco de dados diferente.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="dcfdb-145">É uma boa ideia sempre incluir *o* parâmetro de *banco de dados* quando você usa um **DSN**.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="dcfdb-146">Isso garantirá a conexão com o banco de dados apropriado, mesmo que outro usuário tenha alterado o parâmetro referente do banco de dados padrão desde a última vez que você verificou a definição do **DSN**.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="dcfdb-147">Parâmetros de conexão específicos para provedor</span><span class="sxs-lookup"><span data-stu-id="dcfdb-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="dcfdb-p108">O provedor OLE DB para ODBC adiciona várias propriedades à coleção [Properties](properties-collection-ado.md) do objeto **Connection**. A tabela abaixo lista essas propriedades, com o nome da propriedade do OLE DB correspondente entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dcfdb-150">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="dcfdb-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="dcfdb-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="dcfdb-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-152">Accessible Procedures</span><span class="sxs-lookup"><span data-stu-id="dcfdb-152">Accessible Procedures</span></span><br />
<span data-ttu-id="dcfdb-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-154">Indica se o usuário tem acesso a procedimentos armazenados.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-155">Tabelas acessíveis</span><span class="sxs-lookup"><span data-stu-id="dcfdb-155">Accessible Tables</span></span><br />
<span data-ttu-id="dcfdb-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-157">Indica se o usuário tem permissão para executar instruções SELECT nas tabelas do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-158">Instruções de ativas</span><span class="sxs-lookup"><span data-stu-id="dcfdb-158">Active Statements</span></span><br />
<span data-ttu-id="dcfdb-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-160">Indica o número de identificadores aos quais um driver ODBC pode oferecer suporte em uma conexão.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-161">Nome do driver</span><span class="sxs-lookup"><span data-stu-id="dcfdb-161">Driver Name</span></span><br />
<span data-ttu-id="dcfdb-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-163">Indica o nome do arquivo do driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-164">Versão do driver ODBC</span><span class="sxs-lookup"><span data-stu-id="dcfdb-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="dcfdb-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-166">Indica a versão do ODBC à qual o driver oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-167">Uso de arquivos</span><span class="sxs-lookup"><span data-stu-id="dcfdb-167">File Usage</span></span><br />
<span data-ttu-id="dcfdb-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-169">Indica como o driver trata um arquivo em uma fonte de dados; como uma tabela ou como um catálogo.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-170">Escape cláusula LIKE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-170">Like Escape Clause</span></span><br />
<span data-ttu-id="dcfdb-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-172">Indica se o driver oferece suporte à definição e utilização de um caractere de escape no lugar do caractere de porcentagem (%) e do caractere de sublinhado (_) no predicado LIKE de uma cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-173">Máximo de colunas no grupo por</span><span class="sxs-lookup"><span data-stu-id="dcfdb-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="dcfdb-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-175">Indica o número máximo de colunas que podem ser listadas na cláusula GROUP BY de uma instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-176">Máximo de colunas no índice</span><span class="sxs-lookup"><span data-stu-id="dcfdb-176">Max Columns in Index</span></span><br />
<span data-ttu-id="dcfdb-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-178">Indica o número máximo de colunas que podem ser incluídas em um índice.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-179">Máximo de colunas por ordem</span><span class="sxs-lookup"><span data-stu-id="dcfdb-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="dcfdb-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-181">Indica o número máximo de colunas que podem ser listadas na cláusula ORDER BY de uma instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-182">Máximo de colunas em Select</span><span class="sxs-lookup"><span data-stu-id="dcfdb-182">Max Columns in Select</span></span><br />
<span data-ttu-id="dcfdb-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-184">Indica o número máximo de colunas que podem ser listadas na parte SELECT de uma instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-185">Máximo de colunas na tabela</span><span class="sxs-lookup"><span data-stu-id="dcfdb-185">Max Columns in Table</span></span><br />
<span data-ttu-id="dcfdb-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-187">Indica o número máximo de colunas permitidas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-188">Funções numéricas</span><span class="sxs-lookup"><span data-stu-id="dcfdb-188">Numeric Functions</span></span><br />
<span data-ttu-id="dcfdb-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-p109">Indica as funções numéricas às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-192">Recursos de associação externa</span><span class="sxs-lookup"><span data-stu-id="dcfdb-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="dcfdb-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-194">Indica os tipos de junções externas (OUTER JOINs) aos quais o provedor oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-195">Junções externas</span><span class="sxs-lookup"><span data-stu-id="dcfdb-195">Outer Joins</span></span><br />
<span data-ttu-id="dcfdb-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-197">Indica se o provedor oferece suporte a junções externas (OUTER JOINs).</span><span class="sxs-lookup"><span data-stu-id="dcfdb-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-198">Caracteres especiais</span><span class="sxs-lookup"><span data-stu-id="dcfdb-198">Special Characters</span></span><br />
<span data-ttu-id="dcfdb-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-200">Indica quais caracteres têm um significado especial para o driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-201">Procedimentos armazenados</span><span class="sxs-lookup"><span data-stu-id="dcfdb-201">Stored Procedures</span></span><br />
<span data-ttu-id="dcfdb-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-203">Indica se há procedimentos armazenados disponíveis para utilização com esse driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-204">Funções de sequência</span><span class="sxs-lookup"><span data-stu-id="dcfdb-204">String Functions</span></span><br />
<span data-ttu-id="dcfdb-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-p110">Indica as funções de cadeia de caracteres às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-208">Funções do sistema</span><span class="sxs-lookup"><span data-stu-id="dcfdb-208">System Functions</span></span><br />
<span data-ttu-id="dcfdb-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-p111">Indica as funções do sistema às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-212">Funções de data/hora</span><span class="sxs-lookup"><span data-stu-id="dcfdb-212">Time/Date Functions</span></span><br />
<span data-ttu-id="dcfdb-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-p112">Indica as funções de hora e data às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-216">Suporte a gramática SQL</span><span class="sxs-lookup"><span data-stu-id="dcfdb-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="dcfdb-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-218">Indica a gramática SQL à qual o driver ODBC oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="dcfdb-219">Propriedades de Recordset e Command específicas para provedor</span><span class="sxs-lookup"><span data-stu-id="dcfdb-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="dcfdb-p113">O provedor OLE DB para ODBC adiciona várias propriedades à coleção **Properties** dos objetos **Recordset** e **Command**. A tabela abaixo lista essas propriedades com o nome da propriedade do OLE DB correspondente entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dcfdb-222">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="dcfdb-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="dcfdb-223">Descrição</span><span class="sxs-lookup"><span data-stu-id="dcfdb-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-224">Consultas com base em exclui/atualizações/inserirá</span><span class="sxs-lookup"><span data-stu-id="dcfdb-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="dcfdb-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-226">Indica se atualizações, exclusões e inserções podem ser realizadas utilizando consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-227">Tipo de simultaneidade ODBC</span><span class="sxs-lookup"><span data-stu-id="dcfdb-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="dcfdb-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-229">Indica o método utilizado para reduzir problemas potenciais que surgem quando dois usuários tentam acessar simultaneamente os mesmos dados na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-230">Acessibilidade do BLOB no cursor somente de encaminhamento</span><span class="sxs-lookup"><span data-stu-id="dcfdb-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="dcfdb-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-232">Indica se <strong>Fields</strong> BLOB podem ser acessados quando um cursor somente de encaminhamento estiver sendo utilizado.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-233">Incluem valores SQL_FLOAT, SQL_DOUBLE e SQL_REAL em QBU WHERE cláusulas</span><span class="sxs-lookup"><span data-stu-id="dcfdb-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="dcfdb-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-235">Indica se valores SQL_FLOAT, SQL_DOUBLE e SQL_REAL podem ser incluídos em uma cláusula QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-236">Posição na última linha, após inserir</span><span class="sxs-lookup"><span data-stu-id="dcfdb-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="dcfdb-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-238">Indica que, após a inserção de um novo registro em uma tabela, a última linha da tabela passará a ser a linha atual.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="dcfdb-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="dcfdb-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-241">Indica se a interface <strong>IRowsetChange</strong> oferece suporte a informações estendidas.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-242">Tipo de Cursor ODBC</span><span class="sxs-lookup"><span data-stu-id="dcfdb-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="dcfdb-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-244">Indica o tipo de cursor utilizado pelo <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-245">Gerar um conjunto de linhas que pode ser empacotado.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="dcfdb-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="dcfdb-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-247">Indica que o driver ODBC gera um conjunto de registros que pode ser empacotado.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="dcfdb-248">Texto de comando</span><span class="sxs-lookup"><span data-stu-id="dcfdb-248">Command Text</span></span>

<span data-ttu-id="dcfdb-249">A forma de utilização do objeto [Command](command-object-ado.md) depende em grande parte da fonte de dados e dos tipos de consultas e instruções de comando que ela aceita.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="dcfdb-250">O ODBC fornece uma sintaxe específica para chamar procedimentos armazenados.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-250">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="dcfdb-251">Para a propriedade [CommandText](commandtext-property-ado.md) do argumento *origem* para o método **Open** em um [Recordset](recordset-object-ado.md) , o argumento *CommandText* para o método **Execute** em um objeto de [Conexão](connection-object-ado.md) ou um objeto **Command** objeto, passa em uma cadeia de caracteres com esta sintaxe:</span><span class="sxs-lookup"><span data-stu-id="dcfdb-251">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="dcfdb-p115">Cada **?** faz referência a um objeto na coleção [Parameters](parameters-collection-ado.md). O primeiro **?** faz referência a **Parameters**(0), o segundo **?** a **Parameters**(1), e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p115">Each **?** references an object in the [Parameters](parameters-collection-ado.md) collection. The first **?** references **Parameters**(0), the next **?** references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="dcfdb-p116">As referências a parâmetros são opcionais e dependem da estrutura do procedimento armazenado. Se você quiser chamar um procedimento armazenado que não define qualquer parâmetro, sua cadeia de caracteres será semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="dcfdb-259">Se você tiver dois parâmetros de consulta, sua cadeia de caracteres será semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="dcfdb-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="dcfdb-p117">Se o procedimento armazenado retornar um valor, esse valor de retorno será tratado como outro parâmetro. Se você não tiver parâmetros de consulta, mas tiver um valor de retorno, sua cadeia de caracteres será semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="dcfdb-262">Finalmente, se você tiver um valor de retorno e dois parâmetros de consulta, sua cadeia de caracteres será semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="dcfdb-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="dcfdb-263">Comportamento do Recordset</span><span class="sxs-lookup"><span data-stu-id="dcfdb-263">Recordset Behavior</span></span>

<span data-ttu-id="dcfdb-264">As tabelas abaixo listam os métodos e propriedades do ADO disponíveis em um objeto **Recordset** aberto com esse provedor.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="dcfdb-265">Para obter informações mais detalhadas sobre o comportamento do **Recordset** na sua configuração de provedor, execute o método [Supports](supports-method-ado.md) e enumere a coleção **Properties** de **Recordset** para identificar se propriedades dinâmicas específicas para provedor estão presentes.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="dcfdb-266">Disponibilidade das propriedades padrão do **Recordset** do ADO:</span><span class="sxs-lookup"><span data-stu-id="dcfdb-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="dcfdb-267">Propriedade</span><span class="sxs-lookup"><span data-stu-id="dcfdb-267">Property</span></span></p></th>
<th><p><span data-ttu-id="dcfdb-268">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="dcfdb-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="dcfdb-269">Dinâmico</span><span class="sxs-lookup"><span data-stu-id="dcfdb-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="dcfdb-270">Conjunto de chaves</span><span class="sxs-lookup"><span data-stu-id="dcfdb-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="dcfdb-271">Estático</span><span class="sxs-lookup"><span data-stu-id="dcfdb-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-273">não disponível</span><span class="sxs-lookup"><span data-stu-id="dcfdb-273">not available</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-274">não disponível</span><span class="sxs-lookup"><span data-stu-id="dcfdb-274">not available</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-275">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-276">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-278">não disponível</span><span class="sxs-lookup"><span data-stu-id="dcfdb-278">not available</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-279">não disponível</span><span class="sxs-lookup"><span data-stu-id="dcfdb-279">not available</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-280">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-281">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-283">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-284">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-285">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-286">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-288">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-289">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-290">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-291">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-293">não disponível</span><span class="sxs-lookup"><span data-stu-id="dcfdb-293">not available</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-294">não disponível</span><span class="sxs-lookup"><span data-stu-id="dcfdb-294">not available</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-295">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-296">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-298">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-299">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-300">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-301">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-303">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-304">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-305">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-306">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-308">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-309">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-310">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-311">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-313">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-314">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-315">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-316">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-317"><a href="filter-property-ado.md">Filtrar</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-318">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-319">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-320">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-321">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-322"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-323">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-324">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-325">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-326">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-328">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-329">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-330">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-331">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-333">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-334">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-335">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-336">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-338">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-339">não disponível</span><span class="sxs-lookup"><span data-stu-id="dcfdb-339">not available</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-340">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-341">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-343">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-344">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-345">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-346">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-348">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-349">não disponível</span><span class="sxs-lookup"><span data-stu-id="dcfdb-349">not available</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-350">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-351">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-352"><a href="source-property-ado-recordset.md">Origem</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-353">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-354">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-355">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-356">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dcfdb-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-358">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-359">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-360">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-361">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-362"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-363">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-364">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-365">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-366">somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcfdb-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dcfdb-367">As propriedades [AbsolutePosition](absoluteposition-property-ado.md) e [AbsolutePage](absolutepage-property-ado.md) são somente leitura quando o ADO é utilizado com a versão 1.0 do Microsoft OLE DB Provider for ODBC.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="dcfdb-368">Disponibilidade dos métodos padrão do **Recordset** do ADO:</span><span class="sxs-lookup"><span data-stu-id="dcfdb-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="dcfdb-369">Método</span><span class="sxs-lookup"><span data-stu-id="dcfdb-369">Method</span></span></p></th>
<th><p><span data-ttu-id="dcfdb-370">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="dcfdb-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="dcfdb-371">Dinâmico</span><span class="sxs-lookup"><span data-stu-id="dcfdb-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="dcfdb-372">Conjunto de chaves</span><span class="sxs-lookup"><span data-stu-id="dcfdb-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="dcfdb-373">Estático</span><span class="sxs-lookup"><span data-stu-id="dcfdb-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-375">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-376">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-377">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-378">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-379"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-380">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-381">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-382">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-383">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-385">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-386">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-387">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-388">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-390">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-391">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-392">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-393">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-395">Não</span><span class="sxs-lookup"><span data-stu-id="dcfdb-395">No</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-396">Não</span><span class="sxs-lookup"><span data-stu-id="dcfdb-396">No</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-397">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-398">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-400">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-401">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-402">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-403">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-404"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-405">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-406">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-407">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-408">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-410">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-411">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-412">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-413">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-414"><a href="move-method-ado.md">Mover</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-415">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-416">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-417">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-418">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Métodos MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-420">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-421">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-422">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-423">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-425">Não</span><span class="sxs-lookup"><span data-stu-id="dcfdb-425">No</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-426">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-427">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-428">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-430">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-431">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-432">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-433">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-435">Não</span><span class="sxs-lookup"><span data-stu-id="dcfdb-435">No</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-436">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-437">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-438">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="dcfdb-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-440">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-441">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-442">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-443">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-445">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-446">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-447">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-448">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-450">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-451">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-452">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-453">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-454"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-455">Não</span><span class="sxs-lookup"><span data-stu-id="dcfdb-455">No</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-456">Não</span><span class="sxs-lookup"><span data-stu-id="dcfdb-456">No</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-457">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-458">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-459"><a href="supports-method-ado.md">Suporta</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-460">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-461">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-462">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-463">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-464"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-465">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-466">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-467">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-468">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="dcfdb-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="dcfdb-470">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-471">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-472">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-473">Sim</span><span class="sxs-lookup"><span data-stu-id="dcfdb-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dcfdb-474">\*Sem suporte em bancos de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="dcfdb-475">Propriedades dinâmicas</span><span class="sxs-lookup"><span data-stu-id="dcfdb-475">Dynamic Properties</span></span>

<span data-ttu-id="dcfdb-476">O Microsoft OLE DB Provider for ODBC insere várias propriedades dinâmicas na coleção **Properties** dos objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) e [Command](command-object-ado.md) não abertos.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="dcfdb-p118">As tabelas abaixo são um índice cruzado dos nomes do ADO e do OLE DB de cada propriedade dinâmica. A Referência do programador do OLE DB diz respeito a um nome de propriedade do ADO de acordo com o termo, "Descrição." Você encontrará mais informações sobre essas propriedades na Referência do programador do OLE DB. Localize o nome da propriedade do OLE DB no Índice ou consulte o Apêndice C: propriedades do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="dcfdb-481">Propriedades dinâmicas de Connection</span><span class="sxs-lookup"><span data-stu-id="dcfdb-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="dcfdb-482">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dcfdb-483">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="dcfdb-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="dcfdb-484">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="dcfdb-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-485">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="dcfdb-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-487">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="dcfdb-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-489">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="dcfdb-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-491">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="dcfdb-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-493">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="dcfdb-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="dcfdb-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-495">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="dcfdb-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="dcfdb-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-497">Column Definition</span><span class="sxs-lookup"><span data-stu-id="dcfdb-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="dcfdb-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-499">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="dcfdb-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-501">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="dcfdb-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="dcfdb-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-503">Data Source</span><span class="sxs-lookup"><span data-stu-id="dcfdb-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-505">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="dcfdb-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="dcfdb-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-507">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="dcfdb-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="dcfdb-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-509">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="dcfdb-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="dcfdb-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-511">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="dcfdb-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="dcfdb-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-513">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="dcfdb-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="dcfdb-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-515">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="dcfdb-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="dcfdb-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-517">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="dcfdb-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="dcfdb-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-519">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="dcfdb-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-521">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="dcfdb-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dcfdb-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-523">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="dcfdb-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-525">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="dcfdb-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="dcfdb-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-527">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="dcfdb-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="dcfdb-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-529">Location</span><span class="sxs-lookup"><span data-stu-id="dcfdb-529">Location</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="dcfdb-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-531">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="dcfdb-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-533">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="dcfdb-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-535">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="dcfdb-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="dcfdb-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-537">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-539">Mode</span><span class="sxs-lookup"><span data-stu-id="dcfdb-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-541">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="dcfdb-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-543">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="dcfdb-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-545">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="dcfdb-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-547">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="dcfdb-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-549">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="dcfdb-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="dcfdb-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-551">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="dcfdb-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="dcfdb-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-553">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="dcfdb-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="dcfdb-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-555">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="dcfdb-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="dcfdb-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-557">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="dcfdb-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-559">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="dcfdb-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-561">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="dcfdb-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-563">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="dcfdb-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="dcfdb-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-565">Password</span><span class="sxs-lookup"><span data-stu-id="dcfdb-565">Password</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="dcfdb-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-567">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="dcfdb-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-569">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="dcfdb-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="dcfdb-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-571">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="dcfdb-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-573">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="dcfdb-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="dcfdb-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-575">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="dcfdb-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="dcfdb-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-577">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="dcfdb-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="dcfdb-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="dcfdb-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-581">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="dcfdb-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="dcfdb-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-583">Provider Name</span><span class="sxs-lookup"><span data-stu-id="dcfdb-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="dcfdb-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-585">Provider Version</span><span class="sxs-lookup"><span data-stu-id="dcfdb-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="dcfdb-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-587">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="dcfdb-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="dcfdb-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-589">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="dcfdb-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="dcfdb-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-591">Schema Term</span><span class="sxs-lookup"><span data-stu-id="dcfdb-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="dcfdb-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-593">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="dcfdb-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-595">SQL Support</span><span class="sxs-lookup"><span data-stu-id="dcfdb-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-597">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="dcfdb-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-599">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="dcfdb-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="dcfdb-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-601">Table Term</span><span class="sxs-lookup"><span data-stu-id="dcfdb-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="dcfdb-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-603">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="dcfdb-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="dcfdb-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-605">User ID</span><span class="sxs-lookup"><span data-stu-id="dcfdb-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="dcfdb-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-607">User Name</span><span class="sxs-lookup"><span data-stu-id="dcfdb-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="dcfdb-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-609">Window Handle</span><span class="sxs-lookup"><span data-stu-id="dcfdb-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="dcfdb-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="dcfdb-611">Propriedades dinâmicas do Recordset</span><span class="sxs-lookup"><span data-stu-id="dcfdb-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="dcfdb-612">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dcfdb-613">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="dcfdb-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="dcfdb-614">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="dcfdb-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-615">Access Order</span><span class="sxs-lookup"><span data-stu-id="dcfdb-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="dcfdb-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-617">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="dcfdb-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-619">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="dcfdb-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="dcfdb-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-623">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="dcfdb-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-625">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="dcfdb-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-627">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="dcfdb-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-629">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="dcfdb-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-631">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="dcfdb-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-633">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="dcfdb-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="dcfdb-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="dcfdb-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="dcfdb-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="dcfdb-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="dcfdb-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="dcfdb-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="dcfdb-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="dcfdb-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="dcfdb-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="dcfdb-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-645">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="dcfdb-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="dcfdb-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="dcfdb-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="dcfdb-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="dcfdb-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="dcfdb-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="dcfdb-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="dcfdb-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="dcfdb-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="dcfdb-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="dcfdb-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="dcfdb-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="dcfdb-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="dcfdb-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="dcfdb-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="dcfdb-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="dcfdb-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="dcfdb-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-664">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="dcfdb-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-666">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="dcfdb-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="dcfdb-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-668">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="dcfdb-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-670">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="dcfdb-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-672">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="dcfdb-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-674">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="dcfdb-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="dcfdb-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-676">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="dcfdb-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="dcfdb-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-678">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="dcfdb-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-680">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="dcfdb-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-682">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="dcfdb-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-684">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="dcfdb-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-686">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="dcfdb-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-688">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="dcfdb-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="dcfdb-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-690">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="dcfdb-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-692">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="dcfdb-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="dcfdb-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-694">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="dcfdb-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="dcfdb-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-696">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="dcfdb-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-698">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-700">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-702">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-704">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="dcfdb-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-706">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="dcfdb-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-708">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="dcfdb-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="dcfdb-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-710">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-712">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-714">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-716">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-718">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-720">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-722">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="dcfdb-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-724">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="dcfdb-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="dcfdb-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-726">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="dcfdb-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="dcfdb-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-728">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="dcfdb-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-730">Updatability</span><span class="sxs-lookup"><span data-stu-id="dcfdb-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="dcfdb-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-732">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="dcfdb-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="dcfdb-734">Propriedades dinâmicas do Command</span><span class="sxs-lookup"><span data-stu-id="dcfdb-734">Command Dynamic Properties</span></span>

<span data-ttu-id="dcfdb-735">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="dcfdb-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dcfdb-736">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="dcfdb-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="dcfdb-737">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="dcfdb-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-738">Access Order</span><span class="sxs-lookup"><span data-stu-id="dcfdb-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="dcfdb-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-740">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="dcfdb-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-742">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="dcfdb-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="dcfdb-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-746">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="dcfdb-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-748">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="dcfdb-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-750">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="dcfdb-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-752">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="dcfdb-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-754">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="dcfdb-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-756">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="dcfdb-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="dcfdb-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="dcfdb-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="dcfdb-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="dcfdb-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="dcfdb-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="dcfdb-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="dcfdb-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="dcfdb-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="dcfdb-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="dcfdb-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-768">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="dcfdb-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="dcfdb-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="dcfdb-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="dcfdb-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="dcfdb-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="dcfdb-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="dcfdb-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="dcfdb-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="dcfdb-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="dcfdb-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="dcfdb-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="dcfdb-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="dcfdb-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="dcfdb-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="dcfdb-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="dcfdb-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="dcfdb-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="dcfdb-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-787">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="dcfdb-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-789">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="dcfdb-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="dcfdb-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-791">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="dcfdb-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-793">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="dcfdb-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-795">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="dcfdb-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-797">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="dcfdb-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="dcfdb-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-799">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="dcfdb-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="dcfdb-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-801">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="dcfdb-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-803">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="dcfdb-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-805">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="dcfdb-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-807">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="dcfdb-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-809">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="dcfdb-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-811">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="dcfdb-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="dcfdb-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-813">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="dcfdb-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-815">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="dcfdb-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="dcfdb-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-817">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="dcfdb-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="dcfdb-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-819">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="dcfdb-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-821">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-823">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-825">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-827">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="dcfdb-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-829">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="dcfdb-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-831">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="dcfdb-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="dcfdb-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-833">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-835">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-837">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="dcfdb-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-839">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-841">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-843">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="dcfdb-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="dcfdb-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-845">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="dcfdb-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-847">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="dcfdb-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="dcfdb-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-849">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="dcfdb-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="dcfdb-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfdb-851">Updatability</span><span class="sxs-lookup"><span data-stu-id="dcfdb-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="dcfdb-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfdb-853">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="dcfdb-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="dcfdb-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="dcfdb-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="dcfdb-855">Confira também</span><span class="sxs-lookup"><span data-stu-id="dcfdb-855">See also</span></span>

<span data-ttu-id="dcfdb-856">Para obter detalhes sobre a implementação específica e informações funcionais sobre o Microsoft OLE DB Provider for ODBC, consulte o [Guia do programador do OLE DB do](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) ou visite a [Central de desenvolvedores de plataforma de dados](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="dcfdb-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

