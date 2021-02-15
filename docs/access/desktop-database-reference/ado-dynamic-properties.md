---
title: Propriedades dinâmicas do ADO
TOCTitle: ADO dynamic properties
ms:assetid: a908bc52-2cb0-89c7-a997-2cde93477e4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249782(v=office.15)
ms:contentKeyID: 48546915
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fae0df2a4cc5c9de585d2b101e9fa31cb6a0a545
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281712"
---
# <a name="ado-dynamic-properties"></a><span data-ttu-id="13d9b-102">Propriedades dinâmicas do ADO</span><span class="sxs-lookup"><span data-stu-id="13d9b-102">ADO dynamic properties</span></span>

<span data-ttu-id="13d9b-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="13d9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="13d9b-p101">As propriedades dinâmicas podem ser adicionadas às coleções [Properties](properties-collection-ado.md) dos objetos [Connection](connection-object-ado.md), [Command](command-object-ado.md) ou [Recordset](recordset-object-ado.md). A fonte dessas propriedades é um provedor de dados, como o [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), ou um provedor de serviços, como o [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Consulte a documentação apropriada do provedor de dados ou do provedor de serviços para obter mais informações sobre uma propriedade dinâmica específica.</span><span class="sxs-lookup"><span data-stu-id="13d9b-p101">Dynamic properties can be added to the [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), or [Recordset](recordset-object-ado.md) objects. The source for these properties is either a data provider, such as the [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), or a service provider, such as the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Refer to the appropriate data provider or service provider documentation for more information about a specific dynamic property.</span></span>

<span data-ttu-id="13d9b-107">O [Índice de propriedade dinâmica do ADO](ado-dynamic-property-index.md) fornece uma referência cruzada entre os nomes do ADO e do OLE DB para cada propriedade dinâmica padrão do provedor de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="13d9b-107">The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span>

<span data-ttu-id="13d9b-p102">As seguintes propriedades dinâmicas são importantes e estão documentadas nas fontes mencionadas acima. A funcionalidade especial com ADO está documentada nos tópicos de ajuda do ADO listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="13d9b-p102">The following dynamic properties are of special interest, and are also documented in the sources mentioned above. Special functionality with ADO is documented in the ADO help topics listed below.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="13d9b-110">Propriedade dinâmica</span><span class="sxs-lookup"><span data-stu-id="13d9b-110">Dynamic property</span></span></th>
<th><span data-ttu-id="13d9b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="13d9b-111">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13d9b-112"><a href="optimize-property-dynamic-ado.md">Otimização</a></span><span class="sxs-lookup"><span data-stu-id="13d9b-112"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="13d9b-113">Especifica se um índice deve ser criado nesse campo.</span><span class="sxs-lookup"><span data-stu-id="13d9b-113">Specifies whether an index should be created on this field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13d9b-114"><a href="prompt-property-dynamic-ado.md">Prompt</a></span><span class="sxs-lookup"><span data-stu-id="13d9b-114"><a href="prompt-property-dynamic-ado.md">Prompt</a></span></span></p></td>
<td><p><span data-ttu-id="13d9b-115">Especifica se o provedor de OLE DB deve solicitar ao usuário informações de inicialização.</span><span class="sxs-lookup"><span data-stu-id="13d9b-115">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13d9b-116"><a href="reshape-name-property-dynamic-ado.md">Nome</a></span><span class="sxs-lookup"><span data-stu-id="13d9b-116"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="13d9b-117">Especifica um nome para o objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="13d9b-117">Specifies a name for the <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13d9b-118"><a href="resync-command-property-dynamic-ado.md">Comando</a></span><span class="sxs-lookup"><span data-stu-id="13d9b-118"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="13d9b-119">Especifica uma cadeia de caracteres de comando, fornecida pelo usuário, que o método <strong>Resync</strong> emite para atualizar os dados na tabela chamada na propriedade dinâmica <strong>Tabela exclusiva</strong>.</span><span class="sxs-lookup"><span data-stu-id="13d9b-119">Specifies a user-supplied command string that the <strong>Resync</strong> method issues to refresh the data in the table named in the <strong>Unique Table</strong> dynamic property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13d9b-120"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Tabela exclusiva, Esquema exclusivo, Catálogo exclusivo</a></span><span class="sxs-lookup"><span data-stu-id="13d9b-120"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="13d9b-121"><strong>Unique Table</strong> — especifica o nome da tabela base na qual atualizações, inserções e exclusões são permitidas.</span><span class="sxs-lookup"><span data-stu-id="13d9b-121"><strong>Unique Table</strong> — specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span><br/><br/><span data-ttu-id="13d9b-122"><strong>Esquema exclusivo</strong> — especifica o esquema ou o nome do proprietário da tabela.</span><span class="sxs-lookup"><span data-stu-id="13d9b-122"><strong>Unique Schema</strong> — specifies the schema, or name of the owner of the table.</span></span><br/><br/><span data-ttu-id="13d9b-123"><strong>Unique Catalog</strong> — especifica o catálogo ou o nome do banco de dados que contém a tabela.</span><span class="sxs-lookup"><span data-stu-id="13d9b-123"><strong>Unique Catalog</strong> — specifies the catalog, or name of the database containing the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13d9b-124"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span><span class="sxs-lookup"><span data-stu-id="13d9b-124"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span></span></p></td>
<td><p><span data-ttu-id="13d9b-125">Especifica se o método <strong>UpdateBatch</strong> é seguido por uma operação de método <strong>Resync</strong> implícita e, em caso positivo, o escopo dessa operação.</span><span class="sxs-lookup"><span data-stu-id="13d9b-125">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation, and if so, the scope of that operation.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

