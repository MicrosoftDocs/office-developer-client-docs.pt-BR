---
title: Microsoft OLE DB Provider for Oracle
TOCTitle: Microsoft OLE DB Provider for Oracle
ms:assetid: 97508e3f-077f-9b85-f4dd-8dd01a201aba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249674(v=office.15)
ms:contentKeyID: 48546465
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b4a8847dd7c96813cec6bd8a9868bc9a92b0d2a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463713"
---
# <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="76e76-102">Microsoft OLE DB Provider for Oracle</span><span class="sxs-lookup"><span data-stu-id="76e76-102">Microsoft OLE DB Provider for Oracle</span></span>

<span data-ttu-id="76e76-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="76e76-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="76e76-104">O Microsoft OLE DB Provider for Oracle permite que o ADO acesse bancos de dados Oracle.</span><span class="sxs-lookup"><span data-stu-id="76e76-104">The Microsoft OLE DB Provider for Oracle allows ADO to access Oracle databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="76e76-105">Parâmetros da sequência de conexão</span><span class="sxs-lookup"><span data-stu-id="76e76-105">Connection String Parameters</span></span>

<span data-ttu-id="76e76-106">Para conectar-se a esse provedor, defina o argumento *Provider* da propriedade [ConnectionString](connectionstring-property-ado.md) como:</span><span class="sxs-lookup"><span data-stu-id="76e76-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAORA 
```

<span data-ttu-id="76e76-107">A leitura da propriedade [Provider](provider-property-ado.md) também retornará essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="76e76-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

<span data-ttu-id="76e76-p101">Se uma consulta de junção com um cursor de conjunto de chaves ou dinâmico for executada em um banco de dados Oracle, ocorrerá um erro. O Oracle oferece suporte apenas a cursores estáticos somente leitura.</span><span class="sxs-lookup"><span data-stu-id="76e76-p101">If a join query with a keyset or dynamic cursor is executed in an Oracle database, an error occurs. Oracle only supports a static read-only cursor.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="76e76-110">Sequência de conexão típica</span><span class="sxs-lookup"><span data-stu-id="76e76-110">Typical Connection String</span></span>

<span data-ttu-id="76e76-111">Esta é uma sequência de conexão típica para esse provedor:</span><span class="sxs-lookup"><span data-stu-id="76e76-111">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
```

<span data-ttu-id="76e76-112">A cadeia de caracteres consiste nas seguintes palavras-chave:</span><span class="sxs-lookup"><span data-stu-id="76e76-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76e76-113">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="76e76-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="76e76-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="76e76-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76e76-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="76e76-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="76e76-116">Especifica o Microsoft OLE DB Provider for Oracle.</span><span class="sxs-lookup"><span data-stu-id="76e76-116">Specifies the OLE DB Provider for Oracle.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76e76-117"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="76e76-117"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="76e76-118">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="76e76-118">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76e76-119"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="76e76-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="76e76-120">Especifica o nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="76e76-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76e76-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="76e76-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="76e76-122">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="76e76-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="76e76-123">Parâmetros de conexão específicos para provedor</span><span class="sxs-lookup"><span data-stu-id="76e76-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="76e76-p102">O provedor oferece suporte a vários parâmetros de conexão específicos para provedor, além daqueles definidos pelo ADO. Assim como as propriedades de conexão do ADO, essas propriedades específicas para provedor também podem ser definidas por meio da coleção [Properties](properties-collection-ado.md) de um objeto [Connection](connection-object-ado.md) ou como parte da **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="76e76-p102">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or as part of the **ConnectionString**.</span></span>

<span data-ttu-id="76e76-p103">Esses parâmetros são descritos integralmente na Referência do programador do OLE DB. (O [Índice da propriedade dinâmica do ADO](ado-dynamic-property-index.md) fornece uma referência cruzada entre esses nomes de parâmetros e as propriedades do OLE DB correspondentes.)</span><span class="sxs-lookup"><span data-stu-id="76e76-p103">These parameters are fully described in the OLE DB Programmer's Reference. (The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between these parameter names and the corresponding OLE DB properties.)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76e76-128">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="76e76-128">Parameter</span></span></p></th>
<th><p><span data-ttu-id="76e76-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="76e76-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76e76-130"><strong>Window Handle</strong></span><span class="sxs-lookup"><span data-stu-id="76e76-130"><strong>Window Handle</strong></span></span></p></td>
<td><p><span data-ttu-id="76e76-131">Indica o identificador da janela que deverá ser usado para solicitar informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="76e76-131">Indicates the window handle to use to prompt for additional information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76e76-132"><strong>Locale Identifier</strong></span><span class="sxs-lookup"><span data-stu-id="76e76-132"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="76e76-p104">Indica um número único de 32 bits (por exemplo, 1033) que especifica preferências relacionadas ao idioma do usuário. Essas preferências indicam como as datas e os horários serão formatados, se os itens serão classificados em ordem alfabética, como as cadeias de caracteres serão comparadas, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="76e76-p104">Indicates a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language. These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76e76-135"><strong>OLE DB Services</strong></span><span class="sxs-lookup"><span data-stu-id="76e76-135"><strong>OLE DB Services</strong></span></span></p></td>
<td><p><span data-ttu-id="76e76-136">Indica uma máscara de bits especificando os serviços do OLE DB que deverão ser habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="76e76-136">Indicates a bitmask that specifies OLE DB services to enable or disable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76e76-137"><strong>Prompt</strong></span><span class="sxs-lookup"><span data-stu-id="76e76-137"><strong>Prompt</strong></span></span></p></td>
<td><p><span data-ttu-id="76e76-138">Indica se o usuário deverá ser avisado enquanto uma conexão estiver sendo estabelecida.</span><span class="sxs-lookup"><span data-stu-id="76e76-138">Indicates whether to prompt the user while a connection is being established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76e76-139"><strong>Extended Properties</strong></span><span class="sxs-lookup"><span data-stu-id="76e76-139"><strong>Extended Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="76e76-p105">Uma cadeia de caracteres contendo informações de conexão estendidas específicas para provedor. Use esta propriedade somente para informações de conexão específicas para provedor que não possam ser descritas pelo mecanismo de propriedades.</span><span class="sxs-lookup"><span data-stu-id="76e76-p105">A string containing provider-specific, extended connection information. Use this property only for provider-specific connection information that cannot be described through the property mechanism.</span></span></p></td>
</tr>
</tbody>
</table>

