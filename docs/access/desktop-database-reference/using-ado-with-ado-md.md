---
title: Usando o ADO com o ADO MD
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 469480b0735c6cfbc6bf43e54c529f3e40f6818d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880541"
---
# <a name="using-ado-with-ado-md"></a><span data-ttu-id="9b0e3-102">Usando o ADO com o ADO MD</span><span class="sxs-lookup"><span data-stu-id="9b0e3-102">Using ADO with ADO MD</span></span>


<span data-ttu-id="9b0e3-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b0e3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b0e3-p101">O ADO e o ADO MD são modelos de objeto relacionados, porém, separados. O ADO oferece objetos para conexão a fontes de dados, execução de comandos, recuperação de dados tabulares e metadados de esquema em um formato tabular e exibição de informações de erro do provedor. O ADO MD fornece objetos para recuperação de dados multidimensionais e exibição de metadados de esquemas multidimensionais.</span><span class="sxs-lookup"><span data-stu-id="9b0e3-p101">ADO and ADO MD are related but separate object models. ADO provides objects for connecting to data sources, executing commands, retrieving tabular data and schema metadata in a tabular format, and viewing provider error information. ADO MD provides objects for retrieving multidimensional data and viewing multidimensional schema metadata.</span></span>

<span data-ttu-id="9b0e3-p102">Ao trabalhar com um MDP, você pode usar o ADO, o ADO MD ou ambos com seu aplicativo. Fazendo referência às duas bibliotecas do projeto, você terá acesso total à funcionalidade fornecida pelo MDP.</span><span class="sxs-lookup"><span data-stu-id="9b0e3-p102">When working with an MDP you may choose to use ADO, ADO MD, or both with your application. By referencing both libraries within your project, you will have full access to the functionality provided by your MDP.</span></span>

<span data-ttu-id="9b0e3-109">É sempre útil que os consumidores obtenham uma exibição plana e tabular de um conjunto de dados multidimensional.</span><span class="sxs-lookup"><span data-stu-id="9b0e3-109">It is often useful for consumers to get a flattened, tabular view of a multidimensional dataset.</span></span> <span data-ttu-id="9b0e3-110">Para isso, basta usar o objeto [Recordset](recordset-object-ado.md) do ADO.</span><span class="sxs-lookup"><span data-stu-id="9b0e3-110">You can do this by using the ADO [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="9b0e3-111">Especifica a fonte para seu [conjunto de células](cellset-object-ado-md.md) , como o parâmetro ***Source*** do método [Open](open-method-ado-recordset.md) de um **Recordset**, e não como a origem para um **conjunto de células**do ADO MD.</span><span class="sxs-lookup"><span data-stu-id="9b0e3-111">Specify the source for your [Cellset](cellset-object-ado-md.md) as the ***Source*** parameter for the [Open](open-method-ado-recordset.md) method of a **Recordset**, rather than as the source for an ADO MD **Cellset**.</span></span>

<span data-ttu-id="9b0e3-112">Também pode ser útil exibir o metadados do esquema em um modo de exibição tabular, e não como uma hierarquia de objetos.</span><span class="sxs-lookup"><span data-stu-id="9b0e3-112">It may also be useful to view the schema metadata in a tabular view rather than as a hierarchy of objects.</span></span> <span data-ttu-id="9b0e3-113">O método [OpenSchema](openschema-method-ado.md) do ADO no objeto [Connection](connection-object-ado.md) permite que o usuário abra um **Recordset** que contém informações de esquema.</span><span class="sxs-lookup"><span data-stu-id="9b0e3-113">The ADO [OpenSchema](openschema-method-ado.md) method on the [Connection](connection-object-ado.md) object allows the user to open a **Recordset** containing schema information.</span></span> <span data-ttu-id="9b0e3-114">O parâmetro ***QueryType*** do método **OpenSchema** tem vários valores de [SchemaEnum](schemaenum.md) relacionados especificamente ao MDPs.</span><span class="sxs-lookup"><span data-stu-id="9b0e3-114">The ***QueryType*** parameter of the **OpenSchema** method has several [SchemaEnum](schemaenum.md) values that relate specifically to MDPs.</span></span> <span data-ttu-id="9b0e3-115">Estes são os valores:</span><span class="sxs-lookup"><span data-stu-id="9b0e3-115">These values are:</span></span>

  - <span data-ttu-id="9b0e3-116">**adSchemaCubes**</span><span class="sxs-lookup"><span data-stu-id="9b0e3-116">**adSchemaCubes**</span></span>

  - <span data-ttu-id="9b0e3-117">**adSchemaDimensions**</span><span class="sxs-lookup"><span data-stu-id="9b0e3-117">**adSchemaDimensions**</span></span>

  - <span data-ttu-id="9b0e3-118">**adSchemaHierarchies**</span><span class="sxs-lookup"><span data-stu-id="9b0e3-118">**adSchemaHierarchies**</span></span>

  - <span data-ttu-id="9b0e3-119">**adSchemaLevels**</span><span class="sxs-lookup"><span data-stu-id="9b0e3-119">**adSchemaLevels**</span></span>

  - <span data-ttu-id="9b0e3-120">**adSchemaMeasures**</span><span class="sxs-lookup"><span data-stu-id="9b0e3-120">**adSchemaMeasures**</span></span>

  - <span data-ttu-id="9b0e3-121">**adSchemaMembers**</span><span class="sxs-lookup"><span data-stu-id="9b0e3-121">**adSchemaMembers**</span></span>

<span data-ttu-id="9b0e3-p105">Para usar os valores enumerados do ADO com as propriedades ou os métodos do ADO MD, seu projeto deve fazer referência às bibliotecas do ADO e do ADO MD. Por exemplo, você pode usar os valores enumerados **adState** do ADO com a propriedade [State](state-property-ado-md.md) do ADO MD. Para obter mais informações sobre como estabelecer referências a bibliotecas, consulte a documentação da ferramenta de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="9b0e3-p105">To use ADO enum values with ADO MD properties or methods, your project must reference both the ADO and ADO MD libraries. For example, you can use the ADO **adState** enum values with the ADO MD [State](state-property-ado-md.md) property. For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="9b0e3-125">Para obter mais informações sobre os objetos e os métodos do ADO, consulte [Referência da API do ADO](ado-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9b0e3-125">For more information about the ADO objects and methods, see the [ADO API Reference](ado-api-reference.md).</span></span>

