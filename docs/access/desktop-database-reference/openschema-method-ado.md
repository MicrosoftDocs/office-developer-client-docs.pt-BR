---
title: Método OpenSchema (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ca69b9d761629d42138780517f8de806ed7e8c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701008"
---
# <a name="openschema-method-ado"></a><span data-ttu-id="246a5-102">Método OpenSchema (ADO)</span><span class="sxs-lookup"><span data-stu-id="246a5-102">OpenSchema method (ADO)</span></span>

<span data-ttu-id="246a5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="246a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="246a5-104">Obtém informações do esquema do banco de dados a partir doprovedor .</span><span class="sxs-lookup"><span data-stu-id="246a5-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="246a5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="246a5-105">Syntax</span></span>

<span data-ttu-id="246a5-106">**Definir \* \* \* recordset* = *conexão*. OpenSchema (* QueryType \* *critérios*, *SchemaID*)</span><span class="sxs-lookup"><span data-stu-id="246a5-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="246a5-107">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="246a5-107">Return values</span></span>

<span data-ttu-id="246a5-108">Retorna um objeto [Recordset](recordset-object-ado.md) que contém informações de esquema.</span><span class="sxs-lookup"><span data-stu-id="246a5-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="246a5-109">O **Recordset** será aberto como um cursorestático somente de leitura.</span><span class="sxs-lookup"><span data-stu-id="246a5-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="246a5-110">O *QueryType* determina quais colunas aparecem no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="246a5-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="246a5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="246a5-111">Parameters</span></span>

|<span data-ttu-id="246a5-112">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="246a5-112">Parameter</span></span>|<span data-ttu-id="246a5-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="246a5-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="246a5-114">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="246a5-114">*QueryType*</span></span> |<span data-ttu-id="246a5-115">Qualquer valor [SchemaEnum](schemaenum.md) que represente o tipo de consulta de esquema a ser executado.</span><span class="sxs-lookup"><span data-stu-id="246a5-115">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>|
|<span data-ttu-id="246a5-116">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="246a5-116">*Criteria*</span></span> |<span data-ttu-id="246a5-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="246a5-117">Optional.</span></span> <span data-ttu-id="246a5-118">Uma matriz de restrições de consulta para cada opção *QueryType* , conforme listado em **SchemaEnum**.</span><span class="sxs-lookup"><span data-stu-id="246a5-118">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>|
|<span data-ttu-id="246a5-119">*SchemaID*</span><span class="sxs-lookup"><span data-stu-id="246a5-119">*SchemaID*</span></span> |<span data-ttu-id="246a5-120">O GUID de uma consulta de esquema do provedor não definida pela especificação de banco de dados OLE.</span><span class="sxs-lookup"><span data-stu-id="246a5-120">The GUID for a provider-schema query not defined by the OLE DB specification.</span></span> <span data-ttu-id="246a5-121">Este parâmetro é obrigatório se *QueryType* estiver definida como **adSchemaProviderSpecific**; Caso contrário, ele não é usado.</span><span class="sxs-lookup"><span data-stu-id="246a5-121">This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="246a5-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="246a5-122">Remarks</span></span>

<span data-ttu-id="246a5-123">O método **OpenSchema** retorna informações auto-descritivas sobre a fonte de dados, tais como quais tabelas estão na fonte de dados, as colunas nas tabelas e os tipos de dados suportados.</span><span class="sxs-lookup"><span data-stu-id="246a5-123">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="246a5-124">O argumento *QueryType* é um GUID que indica as colunas (esquemas) é retornado.</span><span class="sxs-lookup"><span data-stu-id="246a5-124">The *QueryType* argument is a GUID that indicates the columns (schemas) returned.</span></span> <span data-ttu-id="246a5-125">A especificação de banco de dados OLE tem uma lista completa de esquemas.</span><span class="sxs-lookup"><span data-stu-id="246a5-125">The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="246a5-p105">O argumento *Criteria* limita os resultados de uma consulta de esquema. *Criteria* especifica uma matriz de valores que devem ocorrer em um subconjunto de colunas correspondentes, denominadas *colunas de restrição*, no **Recordset** resultante.</span><span class="sxs-lookup"><span data-stu-id="246a5-p105">The *Criteria* argument limits the results of a schema query. *Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="246a5-128">A constante **adSchemaProviderSpecific** é usado para o argumento *QueryType* se o provedor define suas próprias consultas de esquema não padrão fora dos listados acima.</span><span class="sxs-lookup"><span data-stu-id="246a5-128">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above.</span></span> <span data-ttu-id="246a5-129">Quando esta constante é usado, o argumento *SchemaID* é necessária para passar o GUID do esquema de consulta para executar.</span><span class="sxs-lookup"><span data-stu-id="246a5-129">When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute.</span></span> <span data-ttu-id="246a5-130">Se *QueryType* estiver definido como **adSchemaProviderSpecific** , mas *SchemaID* não for fornecido, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="246a5-130">If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="246a5-131">Os provedores não precisam suportar todas as consultas de esquema padrão do banco de dados OLE.</span><span class="sxs-lookup"><span data-stu-id="246a5-131">Providers are not required to support all of the OLE DB standard schema queries.</span></span> <span data-ttu-id="246a5-132">Especificamente, apenas **adSchemaTables**, **adSchemaColumns** e **adSchemaProviderTypes** são necessárias pela especificação do banco de dados OLE.</span><span class="sxs-lookup"><span data-stu-id="246a5-132">Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification.</span></span> <span data-ttu-id="246a5-133">No entanto, o provedor não é necessário para suportar as restrições de *critérios* listadas acima para essas consultas de esquema.</span><span class="sxs-lookup"><span data-stu-id="246a5-133">However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="246a5-134">**Uso de serviço de dados remotos** O método **OpenSchema** não está disponível em um objeto de [Conexão](connection-object-ado.md) do cliente.</span><span class="sxs-lookup"><span data-stu-id="246a5-134">**Remote Data Service Usage**The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>

> [!NOTE]
> <span data-ttu-id="246a5-p108">No Visual Basic, as colunas que têm um inteiro sem sinal de quatro bytes (DBTYPE UI4) no **Recordset** retornado do método **OpenSchema** no objeto **Connection** não podem ser comparadas a outras variáveis. Para obter mais informações sobre os tipos de dados de banco de dados OLE, consulte o Capítulo 13 e o Apêndice A do *Microsoft OLE DB Programmer's Reference*.</span><span class="sxs-lookup"><span data-stu-id="246a5-p108">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the **Recordset** returned from the **OpenSchema** method on the **Connection** object cannot be compared to other variables. For more information about OLE DB data types, see Chapter 13 and Appendix A of the *Microsoft OLE DB Programmer's Reference*.</span></span>


