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
# <a name="ado-dynamic-properties"></a>Propriedades dinâmicas do ADO

**Aplica-se ao:** Access 2013, Office 2013

As propriedades dinâmicas podem ser adicionadas às coleções [Properties](properties-collection-ado.md) dos objetos [Connection](connection-object-ado.md), [Command](command-object-ado.md) ou [Recordset](recordset-object-ado.md). A fonte dessas propriedades é um provedor de dados, como o [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), ou um provedor de serviços, como o [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Consulte a documentação apropriada do provedor de dados ou do provedor de serviços para obter mais informações sobre uma propriedade dinâmica específica.

O [Índice de propriedade dinâmica do ADO](ado-dynamic-property-index.md) fornece uma referência cruzada entre os nomes do ADO e do OLE DB para cada propriedade dinâmica padrão do provedor de OLE DB.

As seguintes propriedades dinâmicas são importantes e estão documentadas nas fontes mencionadas acima. A funcionalidade especial com ADO está documentada nos tópicos de ajuda do ADO listados abaixo.

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Propriedade Dynamic</th>
<th>Descrição</th>
</tr>
<tr class="odd">
<td><p><a href="optimize-property-dynamic-ado.md">Otimização</a></p></td>
<td><p>Especifica se um índice deve ser criado nesse campo.</p></td>
</tr>
<tr class="even">
<td><p><a href="prompt-property-dynamic-ado.md">Prompt</a></p></td>
<td><p>Especifica se o provedor de OLE DB deve solicitar ao usuário informações de inicialização.</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Nome</a></p></td>
<td><p>Especifica um nome para o objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Comando</a></p></td>
<td><p>Especifica uma cadeia de caracteres de comando, fornecida pelo usuário, que o método <strong>Resync</strong> emite para atualizar os dados na tabela chamada na propriedade dinâmica <strong>Tabela exclusiva</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Tabela exclusiva, Esquema exclusivo, Catálogo exclusivo</a></p></td>
<td><p><strong>Tabela exclusiva</strong> — especifica o nome da tabela base na qual atualizações, inserções e exclusões são permitidas.<br/><br/><strong>Esquema exclusivo</strong> — especifica o esquema ou o nome do proprietário da tabela.<br/><br/><strong>Catálogo exclusivo</strong> — especifica o catálogo ou o nome do banco de dados que contém a tabela.</p></td>
</tr>
<tr class="even">
<td><p><a href="update-resync-property-dynamic-ado.md">Update Resync</a></p></td>
<td><p>Especifica se o método <strong>UpdateBatch</strong> é seguido por uma operação de método <strong>Resync</strong> implícita e, em caso positivo, o escopo dessa operação.</p></td>
</tr>
</tbody>
</table>

<br/>

