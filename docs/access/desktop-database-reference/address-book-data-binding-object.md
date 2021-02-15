---
title: Objeto de vinculação de dados do Catálogo de Endereços
TOCTitle: Address Book Data-Binding object
ms:assetid: cf43f645-1ee1-8655-eb70-86d601e9f3f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250030(v=office.15)
ms:contentKeyID: 48547807
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fb5302d1c2b8e4eebb6dbe1a5906459834b8e41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281864"
---
# <a name="address-book-data-binding-object"></a>Objeto de vinculação de dados do Catálogo de Endereços


**Aplica-se ao:** Access 2013, Office 2013

O aplicativo do catálogo de endereços usa o objeto [RDS.DataControl](datacontrol-object-rds.md) para vincular os dados do banco de dados SQL Server para um objeto visual (nesse caso, uma tabela DHTML) na página HTML do cliente de aplicativos. A lógica do programa VBScript controlada por eventos usa o [RDS.DataControl](datacontrol-object-rds.md) para:

  - Consultar o banco de dados, enviar atualizações ao banco de dados e atualizar a grade de dados.

  - Permite que os usuários se movimentem para o primeiro, próximo, anterior ou último registro na grade de dados.

O seguinte código define o componente **RDS.DataControl**:

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

A marca OBJECT define o componente **RDS.DataControl** no programa. A marca inclui dois tipos de parâmetros:

  - Os associados à marca OBJECT genérica.

  - Os específicos ao objeto **RDS.DataControl**.

## <a name="generic-object-tag-parameters"></a>Parâmetros da marca OBJECT genérica

A tabela a seguir descreve os parâmetros associados à marca OBJECT.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parâmetro</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><em>CLASSID</em></strong></p></td>
<td><p>Um número exclusivo de 128 bits que identifica o tipo de objeto incorporado ao sistema. Esse identificador é mantido no registro de sistema do computador local. (Para os IDs de classe do objeto <strong>RDS.DataControl</strong>, consulte o <a href="datacontrol-object-rds.md">Objeto RDS.DataControl</a>.)</p></td>
</tr>
<tr class="even">
<td><p><strong><em>ID</em></strong></p></td>
<td><p>Define um identificador que abrange o documento para o objeto incorporado que é usado para identificá-lo no código.</p></td>
</tr>
</tbody>
</table>


## <a name="rdsdatacontrol-tag-parameters"></a>Parâmetros da marca RDS.DataControl

A tabela a seguir descreve os parâmetros específicos ao objeto **RDS.DataControl**. (Para obter uma lista completa de parâmetros de objetos **RDS.DataControl** e ao implementá-los, consulte o [objeto RDS.DataControl](datacontrol-object-rds.md).)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parâmetro</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="server-property-rds.md">SERVIDOR</a></p></td>
<td><p>Se você estiver usando HTTP, o valor será o nome do computador servidor precedido por https:// .</p></td>
</tr>
<tr class="even">
<td><p><a href="connect-property-rds.md">CONNECT</a></p></td>
<td><p>Fornece informações de conexão necessárias para que o <strong>RDS.DataControl</strong> se conecte ao SQL Server.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado">SQL</a></p></td>
<td><p>Define ou retorna a cadeia de consulta usada para recuperar o <a href="recordset-object-ado.md">Recordset</a>.</p></td>
</tr>
</tbody>
</table>

