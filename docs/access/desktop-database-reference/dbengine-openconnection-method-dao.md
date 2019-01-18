---
title: Método DBEngine.OpenConnection (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 778a581f-be42-94ee-e5c6-4cbc1843450d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196074(v=office.15)
ms:contentKeyID: 48545729
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053574
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 845c710954d83003f49a6cd9db21ae3f3bfab383
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704599"
---
# <a name="dbengineopenconnection-method-dao"></a>Método DBEngine.OpenConnection (DAO)

**Aplica-se a**: Access 2013, o Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . OpenConnection (***nome***, ***Opções***, ***ReadOnly***, ***Conecte-se***)

*expressão* Uma variável que representa um objeto **DBEngine** .

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Uma expressão em sequência. Consulte a discussão em Comentários.</p></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Define as várias opções para a conexão, como especificado em Comentários. Com base nessa valor, o gerenciador do driver ODBC solicita ao usuário informações de conexão, como o DSN (Nome da fonte de dados), o nome do usuário e a senha.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>True</strong> se a conexão tiver que ser aberta para acesso somente leitura, e <strong>False</strong> se a conexão tiver que ser aberta para acesso de leitura/gravação (padrão).</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma cadeia de caracteres de conexão ODBC. Consulte a propriedade <strong><a href="connection-connect-property-dao.md">Connect</a></strong> para os elementos específicos e a sintaxe dessa cadeia de caracteres. Um antecedendo &quot;ODBC; &quot; é necessário.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor de retorno

Connection

## <a name="remarks"></a>Comentários

Use o método **OpenConnection** para estabelecer uma conexão com uma fonte de dados ODBC a partir de um espaço de trabalho ODBCDirect. O método **OpenConnection** é semelhante mas não igual a **OpenDatabase**. A principal diferença é que **OpenConnection** está disponível em um espaço de trabalho ODBCDirect.

Se você especificar um nome registrado de fonte de dados do ODBC (DSN) no argumento conectar, em seguida, o argumento nome pode ser qualquer cadeia de caracteres válida e também fornecerá a propriedade **Name** para o objeto de **Conexão** . Se um DSN válido não está incluído no argumento conectar, em seguida, nome deve se referir a um DSN ODBC válido, que também será a propriedade **Name** . Se nem nome nem conectar contém um DSN válido, o Gerenciador de driver ODBC pode ser definido (via o argumento options) para solicitar ao usuário as informações de conexão necessárias. O DSN é fornecido pela solicitação e depois fornece a propriedade **Name**.

O argumento options determina se e quando solicitar que o usuário estabeleça a conexão e se a conexão será aberta de forma assíncrona ou não. Você pode usar uma das constantes a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDriverNoPrompt</strong></p></td>
<td><p>O Gerenciador de Driver ODBC usa a cadeia de caracteres de conexão fornecida em <em>dbname</em> e <em>connect</em>. Se você não fornecer informações suficientes, ocorrerá um erro em tempo de execução.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverPrompt</strong></p></td>
<td><p>O Gerenciador de driver ODBC exibe a caixa de diálogo <strong>Fontes de Dados ODBC</strong>, que mostra quaisquer informações relevantes fornecidas em <em>dbname</em> ou <em>connect</em>. A sequência de conexão é composta pelo DSN que o usuário seleciona via caixas de diálogo ou, se o usuário não especificar um DSN, pelo DSN padrão.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDriverComplete</strong></p></td>
<td><p>Padrão. Se o argumento <em>connect</em> incluir todas as informações necessárias para estabelecer a conexão,  o Gerenciador de driver ODBC utilizará a sequência em <em>connect</em>. Caso contrário, ele se comportará da mesma forma como quando você especifica <strong>dbDriverPrompt</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverCompleteRequired</strong></p></td>
<td><p>Essa opção se comporta como <strong>dbDriverComplete</strong> exceto pelo fato de que o driver ODBC desabilita as solicitações para qualquer informação não exigida para estabelecer a conexão.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Execute o método de modo assíncrono. Essa constante pode ser usada com quaisquer outras constantes <em>options</em>.</p></td>
</tr>
</tbody>
</table>


**OpenConnection** retorna um objeto **Connection** que contém informações sobre a conexão. O objeto **Connection** é semelhante a um objeto **[Database](database-object-dao.md)**. A principal diferença é que um objeto **Database** geralmente representa um banco de dados, embora ele possa ser usado para representar uma conexão a uma fonte de dados ODBC a partir de um espaço de trabalho do Microsoft Access.

