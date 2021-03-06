---
title: Membros index (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 895f29a5dd3e7ed267b96d6a46dc2c8710b4998e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291793"
---
# <a name="index-members-dao"></a>Membros index (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Os objetos Index especificam a ordem dos registros acessados a partir de tabelas de banco de dados e se registros duplicados são aceitos, fornecendo acesso eficiente aos dados. Para bancos de dados externos, os objetos Index descrevem os índices estabelecidos para tabelas externas (apenas espaços de trabalho do Microsoft Access ).

## <a name="methods"></a>Métodos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></p></td>
<td><p>Cria um novo objeto <strong><a href="field-object-dao.md">Field</a></strong> (apenas espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Cria um novo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido pelo usuário (apenas espaços de trabalho do Microsoft Access).</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Propriedades

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></p></td>
<td><p>Define ou retorna um valor que indica se um objeto <strong>Index</strong> representa um índice agrupado para uma tabela (apenas espaços de trabalho do Microsoft Access). <strong>Boolean</strong> de leitura/gravação.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></p></td>
<td><p>Retorna um valor que indica o número de valores exclusivos para o objeto <strong><a href="index-object-dao.md">Index</a></strong> que estão incluídos na tabela associada (apenas espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Retorna uma coleção <strong>Fields</strong> que representa todos os objetos <strong>Field</strong> armazenados para o objeto especificado. Leitura/gravação.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-foreign-property-dao.md">Externo</a></strong></p></td>
<td><p>Retorna um valor que indica se um objeto <strong><a href="index-object-dao.md">Index</a></strong> representa uma chave estrangeira em uma tabela (apenas espaços de trabalho Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></p></td>
<td><p>Define ou retorna um valor que indica se os registros com valores Null nos campos de índice têm entradas de índice (somente nos espaços de trabalho do Microsoft Access ).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-name-property-dao.md">Name</a></strong></p></td>
<td><p>Retorna ou define o nome do objeto especificado. <strong>String</strong> de leitura/gravação se o objeto não foi acrescentado a uma coleção. <strong>String</strong> somente leitura se o objeto foi acrescentado a uma coleção.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-primary-property-dao.md">Primário</a></strong></p></td>
<td><p>Define ou retorna um valor que indica se um objeto <strong><a href="index-object-dao.md">Index</a></strong> representa um índice de chave primária de uma tabela (somente em espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-required-property-dao.md">Obrigatório</a></strong></p></td>
<td><p>Define ou retorna um valor que indica se um objeto <strong><a href="field-object-dao.md">Field</a></strong> requer um valor não Null.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-unique-property-dao.md">Exclusivo</a></strong></p></td>
<td><p>Define ou retorna um valor que indica se objeto <strong><a href="index-object-dao.md">Index</a></strong> representa um índice (chave) exclusivo para uma tabela (somente em espaços de trabalho do Microsoft Access).</p></td>
</tr>
</tbody>
</table>

