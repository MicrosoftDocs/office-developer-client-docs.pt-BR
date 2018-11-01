---
title: Método OpenSchema (ADO)
TOCTitle: OpenSchema Method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36f82510c4dd0004aa89b3f79ac0049cc2193ed3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877664"
---
# <a name="openschema-method-ado"></a><span data-ttu-id="45753-102">Método OpenSchema (ADO)</span><span class="sxs-lookup"><span data-stu-id="45753-102">OpenSchema Method (ADO)</span></span>


<span data-ttu-id="45753-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="45753-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="45753-104">Obtém informações do esquema do banco de dados a partir doprovedor .</span><span class="sxs-lookup"><span data-stu-id="45753-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="45753-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45753-105">Syntax</span></span>

<span data-ttu-id="45753-106">**Definir \* \* \* recordset* = *conexão*. OpenSchema (* QueryType \* *critérios*, *SchemaID*)</span><span class="sxs-lookup"><span data-stu-id="45753-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="45753-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="45753-107">Return values</span></span>

<span data-ttu-id="45753-108">Retorna um objeto [Recordset](recordset-object-ado.md) que contém informações de esquema.</span><span class="sxs-lookup"><span data-stu-id="45753-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="45753-109">O **Recordset** será aberto como um cursorestático somente de leitura.</span><span class="sxs-lookup"><span data-stu-id="45753-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="45753-110">O *QueryType* determina quais colunas aparecem no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="45753-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="45753-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45753-111">Parameters</span></span>

  - <span data-ttu-id="45753-112">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="45753-112">*QueryType*</span></span>

  - <span data-ttu-id="45753-113">Qualquer valor [SchemaEnum](schemaenum.md) que represente o tipo de consulta de esquema a ser executado.</span><span class="sxs-lookup"><span data-stu-id="45753-113">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>

  - <span data-ttu-id="45753-114">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="45753-114">*Criteria*</span></span>

  - <span data-ttu-id="45753-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="45753-115">Optional.</span></span> <span data-ttu-id="45753-116">Uma matriz de restrições de consulta para cada opção *QueryType* , conforme listado em **SchemaEnum**.</span><span class="sxs-lookup"><span data-stu-id="45753-116">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>

  - <span data-ttu-id="45753-117">*SchemaID*</span><span class="sxs-lookup"><span data-stu-id="45753-117">*SchemaID*</span></span>

  - <span data-ttu-id="45753-118">O GUID de uma consulta de esquema do provedor não definida pela especificação de banco de dados OLE.</span><span class="sxs-lookup"><span data-stu-id="45753-118">The GUID for a provider-schema query not defined by the OLE DB specification.</span></span> <span data-ttu-id="45753-119">Este parâmetro é obrigatório se *QueryType* estiver definida como **adSchemaProviderSpecific**; Caso contrário, ele não é usado.</span><span class="sxs-lookup"><span data-stu-id="45753-119">This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="45753-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="45753-120">Remarks</span></span>

<span data-ttu-id="45753-121">O método **OpenSchema** retorna informações auto-descritivas sobre a fonte de dados, tais como quais tabelas estão na fonte de dados, as colunas nas tabelas e os tipos de dados suportados.</span><span class="sxs-lookup"><span data-stu-id="45753-121">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="45753-122">O argumento *QueryType* é um GUID que indica as colunas (esquemas) é retornado.</span><span class="sxs-lookup"><span data-stu-id="45753-122">The *QueryType* argument is a GUID that indicates the columns (schemas) returned.</span></span> <span data-ttu-id="45753-123">A especificação de banco de dados OLE tem uma lista completa de esquemas.</span><span class="sxs-lookup"><span data-stu-id="45753-123">The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="45753-p105">O argumento *Criteria* limita os resultados de uma consulta de esquema. *Criteria* especifica uma matriz de valores que devem ocorrer em um subconjunto de colunas correspondentes, denominadas *colunas de restrição*, no **Recordset** resultante.</span><span class="sxs-lookup"><span data-stu-id="45753-p105">The *Criteria* argument limits the results of a schema query. *Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="45753-126">A constante **adSchemaProviderSpecific** é usado para o argumento *QueryType* se o provedor define suas próprias consultas de esquema não padrão fora dos listados acima.</span><span class="sxs-lookup"><span data-stu-id="45753-126">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above.</span></span> <span data-ttu-id="45753-127">Quando esta constante é usado, o argumento *SchemaID* é necessária para passar o GUID do esquema de consulta para executar.</span><span class="sxs-lookup"><span data-stu-id="45753-127">When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute.</span></span> <span data-ttu-id="45753-128">Se *QueryType* estiver definido como **adSchemaProviderSpecific** , mas *SchemaID* não for fornecido, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="45753-128">If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="45753-129">Os provedores não precisam suportar todas as consultas de esquema padrão do banco de dados OLE.</span><span class="sxs-lookup"><span data-stu-id="45753-129">Providers are not required to support all of the OLE DB standard schema queries.</span></span> <span data-ttu-id="45753-130">Especificamente, apenas **adSchemaTables**, **adSchemaColumns** e **adSchemaProviderTypes** são necessárias pela especificação do banco de dados OLE.</span><span class="sxs-lookup"><span data-stu-id="45753-130">Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification.</span></span> <span data-ttu-id="45753-131">No entanto, o provedor não é necessário para suportar as restrições de *critérios* listadas acima para essas consultas de esquema.</span><span class="sxs-lookup"><span data-stu-id="45753-131">However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="45753-132">**Uso de serviço de dados remotos** O método **OpenSchema** não está disponível em um objeto de [Conexão](connection-object-ado.md) do cliente.</span><span class="sxs-lookup"><span data-stu-id="45753-132">**Remote Data Service Usage**The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="45753-p108">No Visual Basic, as colunas que têm um inteiro sem sinal de quatro bytes (DBTYPE UI4) no <STRONG>Recordset</STRONG> retornado do método <STRONG>OpenSchema</STRONG> no objeto <STRONG>Connection</STRONG> não podem ser comparadas a outras variáveis. Para obter mais informações sobre os tipos de dados de banco de dados OLE, consulte o Capítulo 13 e o Apêndice A do <EM>Microsoft OLE DB Programmer's Reference</EM>.</span><span class="sxs-lookup"><span data-stu-id="45753-p108">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the <STRONG>Recordset</STRONG> returned from the <STRONG>OpenSchema</STRONG> method on the <STRONG>Connection</STRONG> object cannot be compared to other variables. For more information about OLE DB data types, see Chapter 13 and Appendix A of the <EM>Microsoft OLE DB Programmer's Reference</EM>.</span></span></P>


