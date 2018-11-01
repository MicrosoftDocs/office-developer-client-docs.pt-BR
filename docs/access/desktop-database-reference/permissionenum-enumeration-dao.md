---
title: Enumeração PermissionEnum (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3583737eebc881ed5462fe76b6e4a37ad25a8f3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875221"
---
# <a name="permissionenum-enumeration-dao"></a>Enumeração PermissionEnum (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Usada com a propriedade **Permissions** para especificar o tipo das permissões.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbSecCreate</p></td>
<td><p>1</p></td>
<td><p>O usuário pode criar novos documentos (não é válido para objetos Document).</p></td>
</tr>
<tr class="even">
<td><p>dbSecDBAdmin</p></td>
<td><p>8</p></td>
<td><p>O usuário pode replicar um banco de dados e alterar a senha do banco de dados (não é válido para objetos Document).</p></td>
</tr>
<tr class="odd">
<td><p>dbSecDBCreate</p></td>
<td><p>1</p></td>
<td><p>O usuário pode criar novos bancos de dados. Esta opção é válida somente no contêiner Bancos de Dados do arquivo de informações do grupo de trabalho (Systen.mdw). Esta constante não é válida para objetos Document.</p></td>
</tr>
<tr class="even">
<td><p>dbSecDBExclusive</p></td>
<td><p>4</p></td>
<td><p>O usuário tem acesso exclusivo ao banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecDBOpen</p></td>
<td><p>2</p></td>
<td><p>O usuário pode abrir o banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>dbSecDelete</p></td>
<td><p>65536</p></td>
<td><p>O usuário pode excluir o objeto.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecDeleteData</p></td>
<td><p>128</p></td>
<td><p>O usuário pode excluir registros.</p></td>
</tr>
<tr class="even">
<td><p>dbSecFullAccess</p></td>
<td><p>1048575</p></td>
<td><p>O usuário tem acesso completo ao objeto.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecInsertData</p></td>
<td><p>32</p></td>
<td><p>O usuário pode adicionar registros.</p></td>
</tr>
<tr class="even">
<td><p>dbSecNoAccess</p></td>
<td><p>0</p></td>
<td><p>O usuário não tem acesso ao objeto (não é válido para objetos Document).</p></td>
</tr>
<tr class="odd">
<td><p>dbSecReadDef</p></td>
<td><p>4</p></td>
<td><p>O usuário pode ler a definição da tabela, inclusive informações de coluna e índice.</p></td>
</tr>
<tr class="even">
<td><p>dbSecReadSec</p></td>
<td><p>131072</p></td>
<td><p>O usuário pode ler as informações relativas à segurança do objeto.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecReplaceData</p></td>
<td><p>64</p></td>
<td><p>O usuário pode modificar registros.</p></td>
</tr>
<tr class="even">
<td><p>dbSecRetrieveData</p></td>
<td><p>20</p></td>
<td><p>O usuário pode recuperar dados do objeto Document.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecWriteDef</p></td>
<td><p>65548</p></td>
<td><p>O usuário pode modificar ou excluir a definição da tabela, inclusive as informações de coluna e índice.</p></td>
</tr>
<tr class="even">
<td><p>dbSecWriteOwner</p></td>
<td><p>524288</p></td>
<td><p>O usuário pode alterar a configuração da propriedade Proprietário.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecWriteSec</p></td>
<td><p>262144</p></td>
<td><p>O usuário pode alterar permissões de acesso.</p></td>
</tr>
</tbody>
</table>

