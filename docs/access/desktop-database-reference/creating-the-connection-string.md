---
title: Criando a sequência de conexão
TOCTitle: Creating the Connection String
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8420beb2c6136123c334a55b68bd6601f214faa5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465209"
---
# <a name="creating-the-connection-string"></a><span data-ttu-id="d891a-102">Criando a sequência de conexão</span><span class="sxs-lookup"><span data-stu-id="d891a-102">Creating the Connection String</span></span>


<span data-ttu-id="d891a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d891a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d891a-p101">O ADO oferece suporte direto a cinco argumentos em uma sequência de conexão. Outros argumentos são passados ao provedor cujo nome é atribuído no argumento *Provider*, sem processamento pelo ADO.</span><span class="sxs-lookup"><span data-stu-id="d891a-p101">ADO directly supports five arguments in a connection string. Other arguments are passed to the provider that is named in the *Provider* argument without any processing by ADO.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d891a-106">Argumento</span><span class="sxs-lookup"><span data-stu-id="d891a-106">Argument</span></span></p></th>
<th><p><span data-ttu-id="d891a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d891a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d891a-108"><em>Provider</em></span><span class="sxs-lookup"><span data-stu-id="d891a-108"><em>Provider</em></span></span></p></td>
<td><p><span data-ttu-id="d891a-109">Especifica o nome de um provedor a ser usado para a conexão.</span><span class="sxs-lookup"><span data-stu-id="d891a-109">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d891a-110"><em>Nome do Arquivo</em></span><span class="sxs-lookup"><span data-stu-id="d891a-110"><em>File Name</em></span></span></p></td>
<td><p><span data-ttu-id="d891a-111">Especifica o nome de um arquivo específico do provedor (por exemplo, um objeto de fonte de dados persistente) contendo informações de conexão predefinidas.</span><span class="sxs-lookup"><span data-stu-id="d891a-111">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d891a-112"><em>URL</em></span><span class="sxs-lookup"><span data-stu-id="d891a-112"><em>URL</em></span></span></p></td>
<td><p><span data-ttu-id="d891a-113">Especifica a cadeia de caracteres de conexão como uma URL absoluta que identifica um recurso, como um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="d891a-113">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d891a-114"><em>Remote Provider</em></span><span class="sxs-lookup"><span data-stu-id="d891a-114"><em>Remote Provider</em></span></span></p></td>
<td><p><span data-ttu-id="d891a-p102">Especifica o nome do provedor a ser usado ao abrir uma conexão no cliente (somente Remote Data Service).</span><span class="sxs-lookup"><span data-stu-id="d891a-p102">Specifies the name of a provider to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d891a-117"><em>Remote Server</em></span><span class="sxs-lookup"><span data-stu-id="d891a-117"><em>Remote Server</em></span></span></p></td>
<td><p><span data-ttu-id="d891a-p103">Especifica o nome do caminho do servidor a ser usado durante a abertura de uma conexão no cliente. (somente Remote Data Service.)</span><span class="sxs-lookup"><span data-stu-id="d891a-p103">Specifies the path name of the server to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="d891a-p104">Nos exemplos a seguir e em todo o Guia do programador do ADO, a identificação de usuário "MyId" com a senha "123aBc" é usada para realizar a autenticação no servidor. Você deve substituir esses valores pelas credenciais de logon válidas no seu servidor. Além disso, substitua "MySqlServer" pelo nome do seu servidor.</span><span class="sxs-lookup"><span data-stu-id="d891a-p104">In the following examples and throughout the ADO Programmer's Guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server. You should substitute these values with valid login credentials for your server. Also, substitute the name of your server for "MySqlServer".</span></span></P>



<span data-ttu-id="d891a-123">O aplicativo HelloData no Capítulo 1 usava a seguinte sequência de conexão:</span><span class="sxs-lookup"><span data-stu-id="d891a-123">The HelloData application in Chapter 1 used the following connection string:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="d891a-124">O único parâmetro do ADO fornecido nessa sequência de conexão foi "Provider=SQLOLEDB", que indicava o Microsoft OLE DB Provider for SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d891a-124">The only ADO parameter supplied in this connection string was "Provider=SQLOLEDB", which indicated the Microsoft OLE DB Provider for SQL Server.</span></span> <span data-ttu-id="d891a-125">Outros parâmetros válidos a serem passados na sequência de conexão podem ser determinados por meio da referência à documentação de provedores individuais.</span><span class="sxs-lookup"><span data-stu-id="d891a-125">Other valid parameters that can be passed in the connection string can be determined by referring to individual providers' documentation.</span></span> <span data-ttu-id="d891a-126">De acordo com o OLE DB Provider for documentação do SQL Server, você pode substituir "Server" para o parâmetro de *Fonte de dados* e "Database" para o parâmetro *Initial Catalog* .</span><span class="sxs-lookup"><span data-stu-id="d891a-126">According to the OLE DB Provider for SQL Server documentation, you can substitute "Server" for the *Data Source* parameter and "Database" for the *Initial Catalog* parameter.</span></span> <span data-ttu-id="d891a-127">Assim, a seguinte sequência de conexão produziria resultados idênticos à primeira:</span><span class="sxs-lookup"><span data-stu-id="d891a-127">Thus, the following connection string would produce results identical to the first:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Server='MySqlServer';" & _ 
 "Database='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="d891a-128">Para abrir a conexão, basta passar a sequência de conexão como o primeiro argumento no método **Open** do objeto **Connection**:</span><span class="sxs-lookup"><span data-stu-id="d891a-128">To open the connection, simply pass the connection string as the first argument in the **Connection** object **Open** method:</span></span>

```vb 
 
objConn.Open m_sConnStr 
```

<span data-ttu-id="d891a-p106">Também é possível fornecer boa parte dessas informações definindo propriedades do objeto **Connection** antes de abrir a conexão. Por exemplo, você pode obter o mesmo efeito que o da sequência de conexão acima usando o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="d891a-p106">It is also possible to supply much of this information by setting properties of the **Connection** object before opening the connection. For example, you could achieve the same effect as the connection string above by using the following code:</span></span>

```vb 
 
With objConn 
 .Provider = "SQLOLEDB" 
 .DefaultDatabase = "Northwind" 
 .Properties("Data Source") = "MySqlServer" 
 .Properties("Integrated Security") = "SSPI" 
 .Open 
End With 
```

