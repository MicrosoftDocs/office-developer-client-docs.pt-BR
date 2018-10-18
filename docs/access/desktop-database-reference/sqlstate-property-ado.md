---
<span data-ttu-id="5cc5c-101"><<<<<<< Título cabeça: propriedade SQLState (ADO) TOCTitle: propriedade SQLState (ADO) === título: propriedade SQLState (ADO) TOCTitle: propriedade SQLState (ADO)</span><span class="sxs-lookup"><span data-stu-id="5cc5c-101"><<<<<<< HEAD title: SQLState Property (ADO) TOCTitle: SQLState Property (ADO) ======= title: SQLState property (ADO) TOCTitle: SQLState property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5cc5c-102">ms:assetid de mestre: cf3b078a-849e-1ad2-cba4-a26160080868 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15) ms:contentKeyID: ms.date 48547806: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="5cc5c-102">master ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15) ms:contentKeyID: 48547806 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="5cc5c-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="5cc5c-103"><<<<<<< HEAD</span></span>
# <a name="sqlstate-property-ado"></a><span data-ttu-id="5cc5c-104">Propriedade SQLState (ADO)</span><span class="sxs-lookup"><span data-stu-id="5cc5c-104">SQLState Property (ADO)</span></span>
=======
# <a name="sqlstate-property-ado"></a><span data-ttu-id="5cc5c-105">Propriedade SQLState (ADO)</span><span class="sxs-lookup"><span data-stu-id="5cc5c-105">SQLState property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5cc5c-106">mestre</span><span class="sxs-lookup"><span data-stu-id="5cc5c-106">master</span></span>


<span data-ttu-id="5cc5c-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5cc5c-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5cc5c-108">Indica o estado do SQL de um determinado objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5cc5c-108">Indicates the SQL state for a given [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="5cc5c-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="5cc5c-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="5cc5c-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5cc5c-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="5cc5c-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5cc5c-111">Return value</span></span>
>>>>>>> <span data-ttu-id="5cc5c-112">mestre</span><span class="sxs-lookup"><span data-stu-id="5cc5c-112">master</span></span>

<span data-ttu-id="5cc5c-113">Retorna um valor **String** de cinco caracteres que segue o padrão ANSI SQL e indica o código de erro.</span><span class="sxs-lookup"><span data-stu-id="5cc5c-113">Returns a five-character **String** value that follows the ANSI SQL standard and indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cc5c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cc5c-114">Remarks</span></span>

<span data-ttu-id="5cc5c-p101">Utilize a propriedade **SQLState** para ler o código de erro de cinco caracteres que o provedor retornar quando ocorrer um erro durante o processamento de uma instrução SQL. Por exemplo, ao utillizar o Microsoft OLE DB Provider for ODBC com um banco de dados Microsoft SQL Server, os códigos de erro do estado do SQL serão originados do ODBC, com base nos erros específicos para o ODBC, ou em erros que se originaram do Microsoft SQL Server e, em seguida, serão mapeados para os erros do ODBC. Esses códigos de erro são documentados no padrão ANSI SQL, mas poderão ser implementados de formas diferentes por diversas fontes de dados.</span><span class="sxs-lookup"><span data-stu-id="5cc5c-p101">Use the **SQLState** property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement. For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors. These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</span></span>

