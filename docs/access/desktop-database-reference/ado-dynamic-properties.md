---
title: Propriedades dinâmicas do ADO
TOCTitle: ADO Dynamic Properties
ms:assetid: a908bc52-2cb0-89c7-a997-2cde93477e4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249782(v=office.15)
ms:contentKeyID: 48546915
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a35bf0cd62db8f635540bfd1ccd65995b198b46
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877545"
---
# <a name="ado-dynamic-properties"></a><span data-ttu-id="51940-102">Propriedades dinâmicas do ADO</span><span class="sxs-lookup"><span data-stu-id="51940-102">ADO Dynamic Properties</span></span>


<span data-ttu-id="51940-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="51940-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51940-p101">As propriedades dinâmicas podem ser adicionadas às coleções [Properties](properties-collection-ado.md) dos objetos [Connection](connection-object-ado.md), [Command](command-object-ado.md) ou [Recordset](recordset-object-ado.md). A fonte dessas propriedades é um provedor de dados, como o [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), ou um provedor de serviços, como o [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Consulte a documentação apropriada do provedor de dados ou do provedor de serviços para obter mais informações sobre uma propriedade dinâmica específica.</span><span class="sxs-lookup"><span data-stu-id="51940-p101">Dynamic properties can be added to the [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), or [Recordset](recordset-object-ado.md) objects. The source for these properties is either a data provider, such as the [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), or a service provider, such as the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Refer to the appropriate data provider or service provider documentation for more information about a specific dynamic property.</span></span>

<span data-ttu-id="51940-107">O [Índice de propriedade dinâmica do ADO](ado-dynamic-property-index.md) fornece uma referência cruzada entre os nomes do ADO e do OLE DB para cada propriedade dinâmica padrão do provedor de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="51940-107">The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span>

<span data-ttu-id="51940-p102">As seguintes propriedades dinâmicas são importantes e estão documentadas nas fontes mencionadas acima. A funcionalidade especial com ADO está documentada nos tópicos de ajuda do ADO listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="51940-p102">The following dynamic properties are of special interest, and are also documented in the sources mentioned above. Special functionality with ADO is documented in the ADO help topics listed below.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51940-110"><a href="optimize-property-dynamic-ado.md">Otimizar</a></span><span class="sxs-lookup"><span data-stu-id="51940-110"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="51940-111">Especifica se um índice deve ser criado nesse campo.</span><span class="sxs-lookup"><span data-stu-id="51940-111">Specifies whether an index should be created on this field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51940-112"><a href="prompt-property-dynamic-ado.md">Prompt</a></span><span class="sxs-lookup"><span data-stu-id="51940-112"><a href="prompt-property-dynamic-ado.md">Prompt</a></span></span></p></td>
<td><p><span data-ttu-id="51940-113">Especifica se o provedor OLE DB deveria solicitar ao usuário as informações de inicialização.</span><span class="sxs-lookup"><span data-stu-id="51940-113">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51940-114"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span><span class="sxs-lookup"><span data-stu-id="51940-114"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="51940-115">Especifica um nome para o objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="51940-115">Specifies a name for the <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51940-116"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span><span class="sxs-lookup"><span data-stu-id="51940-116"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="51940-117">Especifica uma cadeia de caracteres de comando, fornecida pelo usuário, que o método <strong>Resync</strong> emite para atualizar os dados na tabela chamada na propriedade dinâmica <strong>Tabela exclusiva</strong>.</span><span class="sxs-lookup"><span data-stu-id="51940-117">Specifies a user-supplied command string that the <strong>Resync</strong> method issues to refresh the data in the table named in the <strong>Unique Table</strong> dynamic property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51940-118"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span><span class="sxs-lookup"><span data-stu-id="51940-118"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="51940-119"><strong>Tabela exclusiva</strong> — Especifica o nome da tabela base sobre a qual atualizações, inserções e exclusões são permitidas.</span><span class="sxs-lookup"><span data-stu-id="51940-119"><strong>Unique Table</strong> — specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span> <span data-ttu-id="51940-120"><strong>Esquema exclusivo</strong> — Especifica o esquema ou o nome do proprietário da tabela.</span><span class="sxs-lookup"><span data-stu-id="51940-120"><strong>Unique Schema</strong> — specifies the schema, or name of the owner of the table.</span></span> <span data-ttu-id="51940-121"><strong>Catálogo exclusivo</strong> — Especifica o catálogo ou o nome do banco de dados que contém a tabela.</span><span class="sxs-lookup"><span data-stu-id="51940-121"><strong>Unique Catalog</strong> — specifies the catalog, or name of the database containing the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51940-122"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span><span class="sxs-lookup"><span data-stu-id="51940-122"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span></span></p></td>
<td><p><span data-ttu-id="51940-123">Especifica se o método <strong>UpdateBatch</strong> é seguido por uma operação de método <strong>Resync</strong> implícita e, em caso positivo, o escopo dessa operação.</span><span class="sxs-lookup"><span data-stu-id="51940-123">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation, and if so, the scope of that operation.</span></span></p></td>
</tr>
</tbody>
</table>

