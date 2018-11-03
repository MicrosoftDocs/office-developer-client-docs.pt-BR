---
title: Criando a cadeia de caracteres de conexão
TOCTitle: Creating the connection string
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2db1ae3266df3a84cbcac70a86cf5fca302b16d0
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944939"
---
# <a name="creating-the-connection-string"></a>Criando a cadeia de caracteres de conexão

**Aplica-se a**: Access 2013, o Office 2013

O ADO oferece suporte direto a cinco argumentos em uma sequência de conexão. Outros argumentos são passados ao provedor cujo nome é atribuído no argumento *Provider*, sem processamento pelo ADO.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Provider</em></p></td>
<td><p>Especifica o nome de um provedor a ser usado para a conexão.</p></td>
</tr>
<tr class="even">
<td><p><em>Nome do Arquivo</em></p></td>
<td><p>Especifica o nome de um arquivo específico do provedor (por exemplo, um objeto de fonte de dados persistente) contendo informações de conexão predefinidas.</p></td>
</tr>
<tr class="odd">
<td><p><em>URL</em></p></td>
<td><p>Especifica a cadeia de caracteres de conexão como uma URL absoluta que identifica um recurso, como um arquivo ou diretório.</p></td>
</tr>
<tr class="even">
<td><p><em>Remote Provider</em></p></td>
<td><p>Especifica o nome do provedor a ser usado ao abrir uma conexão no cliente (somente Remote Data Service).</p></td>
</tr>
<tr class="odd">
<td><p><em>Remote Server</em></p></td>
<td><p>Especifica o nome do caminho do servidor a ser usado ao abrir uma conexão do lado do cliente. (Apenas para o Remote Data Service.)</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Nos exemplos a seguir e em todo o guia do programador do ADO, a id de usuário "MyId" com uma senha de "123aBc" é usada para autenticar com base no servidor. Você deve substituir esses valores pelas credenciais de logon válidas no seu servidor. Além disso, substitua "MySqlServer" pelo nome do seu servidor.

O aplicativo HelloData no Capítulo 1 usava a seguinte sequência de conexão:

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

O único parâmetro do ADO fornecido nessa sequência de conexão foi "Provider=SQLOLEDB", que indicava o Microsoft OLE DB Provider for SQL Server. Outros parâmetros válidos a serem passados na sequência de conexão podem ser determinados por meio da referência à documentação de provedores individuais. De acordo com o OLE DB Provider for documentação do SQL Server, você pode substituir "Server" para o parâmetro de *Fonte de dados* e "Database" para o parâmetro *Initial Catalog* . Assim, a seguinte sequência de conexão produziria resultados idênticos à primeira:

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Server='MySqlServer';" & _ 
 "Database='Northwind';Integrated Security='SSPI';" 
```

Para abrir a conexão, basta passar a sequência de conexão como o primeiro argumento no método **Open** do objeto **Connection**:

```vb 
 
objConn.Open m_sConnStr 
```

Também é possível fornecer boa parte dessas informações definindo propriedades do objeto **Connection** antes de abrir a conexão. Por exemplo, você pode obter o mesmo efeito que o da sequência de conexão acima usando o seguinte código:

```vb 
 
With objConn 
 .Provider = "SQLOLEDB" 
 .DefaultDatabase = "Northwind" 
 .Properties("Data Source") = "MySqlServer" 
 .Properties("Integrated Security") = "SSPI" 
 .Open 
End With 
```

