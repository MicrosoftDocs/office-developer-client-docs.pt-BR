---
title: Membros do documento (DAO)
TOCTitle: Document Members
ms:assetid: 8de770e6-e4d1-372a-3ef8-8539c921b41f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197365(v=office.15)
ms:contentKeyID: 48546270
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd50ec72113b0615849ff6b8b2e8d73c0e61c3ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293788"
---
# <a name="document-members-dao"></a>Membros do documento (DAO)


**Aplica-se ao:** Access 2013, Office 2013

O objeto Document inclui informações sobre uma instância de um objeto. O objeto pode ser um banco de dados, uma tabela, uma consulta ou uma relação salva (apenas bancos de dados do mecanismo de banco de dados do Microsoft Access).

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
<td><p><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
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
<td><p><strong><a href="document-container-property-dao.md">Caixa</a></strong></p></td>
<td><p>Retorna o nome do objeto <strong><a href="container-object-dao.md">Container</a></strong> ao qual um objeto <strong>Document</strong> pertence (apenas espaços de trabalho do Microsoft Access). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Retorna a data e a hora que um objeto foi criado. Somente leitura <strong>Variant</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Retorna a data e a hora da alteração mais recente feita em um objeto. <strong>Variant</strong> somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="document-name-property-dao.md">Nome</a></strong></p></td>
<td><p>Retorna o nome do objeto especificado. Somente leitura <strong>cadeia de caracteres</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="document-properties-property-dao.md">Propriedades</a></strong></p></td>
<td><p>Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</p></td>
</tr>
</tbody>
</table>

