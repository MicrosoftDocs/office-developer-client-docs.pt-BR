---
title: Membros do espaço de trabalho (DAO)
TOCTitle: Workspace Members
ms:assetid: 13ac7d41-1b25-20d2-5c85-0f21bfd38328
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845437(v=office.15)
ms:contentKeyID: 48543374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec5e11a8bdc33923ca92f96833605338e9f19566
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889991"
---
# <a name="workspace-members-dao"></a>Membros do espaço de trabalho (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Um objeto Workspace define uma sessão nomeada por um usuário. Ele contém bancos de dados abertos e fornece mecanismos para transações simultâneas e, nos espaços de trabalho do Microsoft Access, suporte a grupos de trabalho seguros.

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
<td><p><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></p></td>
<td><p>Inicia uma nova transação. <strong>Database</strong> de leitura/gravação.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-close-method-dao.md">Fechar</a></strong></p></td>
<td><p>Fecha um <strong>Workspace</strong> aberto.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></p></td>
<td><p>Encerra a transação atual e salva as alterações.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-createdatabase-method-dao.md">Método CreateDatabase</a></strong></p></td>
<td><p>Cria um novo objeto <strong><a href="database-object-dao.md">Database</a></strong>, salva o banco de dados no disco e retorna um objeto <strong>Database</strong> aberto (apenas espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</P>


<p>Abre um objeto <strong><a href="connection-object-dao.md">Connection</a></strong> em uma fonte de dados ODBC (apenas espaços de trabalho ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></p></td>
<td><p>Abre um banco de dados especificado em um objeto <strong><a href="workspace-object-dao.md">Workspace</a></strong> e retorna uma referência ao objeto <strong><a href="database-object-dao.md">Database</a></strong> que o representa.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></p></td>
<td><p>Encerra a transação atual e restaura os bancos de dados no objeto <strong>Workspace</strong> para o estado em que estavam quando a transação atual começou.</p></td>
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
<td><p><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></p></td>
<td><p>Retorna uma coleção <strong>Connections</strong> que representa as conexões atuais do <strong>Workspace</strong> especificado. Somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></p></td>
<td><p>Retorna uma coleção <strong>Databases</strong> que representa os banco de dados abertos em um <strong>Workspace</strong> especificado. Somente leitura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</P>


<p>Define ou retorna o tipo de driver de cursor utilizado na conexão criada pelos métodos <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> ou <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> (apenas espaços de trabalho ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></p></td>
<td><p>Define ou retorna um valor que indica se vários transactiond, que envolvem o mesmo mecanismo do banco de dados do Microsoft Access conectado à fonte de dados ODBC, estão isolados (somente em espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></p></td>
<td><p>Define ou retorna o número de segundos antes de ocorrer um erro durante a tentativa de fazer logon em um banco de dados ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-name-property-dao.md">Nome</a></strong></p></td>
<td><p>Retorna ou define o nome do objeto especificado. <strong>String</strong> de leitura/gravação se o objeto não foi acrescentado a uma coleção. <strong>String</strong> somente leitura se o objeto foi acrescentado a uma coleção.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-properties-property-dao.md">Propriedades</a></strong></p></td>
<td><p>Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-type-property-dao.md">Tipo</a></strong></p></td>
<td><p>Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. <strong>Integer</strong> somente leitura.</p></td>
</tr>
</tbody>
</table>

