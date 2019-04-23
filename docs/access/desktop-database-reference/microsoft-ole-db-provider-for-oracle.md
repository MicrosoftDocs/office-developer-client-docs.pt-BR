---
title: Microsoft OLE DB Provider for Oracle
TOCTitle: Microsoft OLE DB Provider for Oracle
ms:assetid: 97508e3f-077f-9b85-f4dd-8dd01a201aba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249674(v=office.15)
ms:contentKeyID: 48546465
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b9b506f40039ff91a6b1985606322fd86a9e7c0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288929"
---
# <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="b106d-102">Provedor Microsoft OLE DB para Oracle</span><span class="sxs-lookup"><span data-stu-id="b106d-102">Microsoft OLE DB Provider for Oracle</span></span>

<span data-ttu-id="b106d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b106d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b106d-104">O Microsoft OLE DB Provider for Oracle permite que o ADO acesse bancos de dados Oracle.</span><span class="sxs-lookup"><span data-stu-id="b106d-104">The Microsoft OLE DB Provider for Oracle allows ADO to access Oracle databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="b106d-105">Parâmetros da sequência de conexão</span><span class="sxs-lookup"><span data-stu-id="b106d-105">Connection String Parameters</span></span>

<span data-ttu-id="b106d-106">Para conectar-se a esse provedor, defina o argumento *Provider* da propriedade [ConnectionString](connectionstring-property-ado.md) como:</span><span class="sxs-lookup"><span data-stu-id="b106d-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAORA 
```

<span data-ttu-id="b106d-107">A leitura da propriedade [Provider](provider-property-ado.md) também retornará essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b106d-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

<span data-ttu-id="b106d-p101">Se uma consulta de junção com um cursor de conjunto de chaves ou dinâmico for executada em um banco de dados Oracle, ocorrerá um erro. O Oracle oferece suporte apenas a cursores estáticos somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b106d-p101">If a join query with a keyset or dynamic cursor is executed in an Oracle database, an error occurs. Oracle only supports a static read-only cursor.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="b106d-110">Sequência de conexão típica</span><span class="sxs-lookup"><span data-stu-id="b106d-110">Typical Connection String</span></span>

<span data-ttu-id="b106d-111">Esta é uma sequência de conexão típica para esse provedor:</span><span class="sxs-lookup"><span data-stu-id="b106d-111">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
```

<span data-ttu-id="b106d-112">A cadeia de caracteres consiste nas seguintes palavras-chave:</span><span class="sxs-lookup"><span data-stu-id="b106d-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b106d-113">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="b106d-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="b106d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b106d-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b106d-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="b106d-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="b106d-116">Especifica o Microsoft OLE DB Provider for Oracle.</span><span class="sxs-lookup"><span data-stu-id="b106d-116">Specifies the OLE DB Provider for Oracle.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b106d-117"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="b106d-117"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="b106d-118">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="b106d-118">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b106d-119"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="b106d-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="b106d-120">Especifica o nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="b106d-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b106d-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="b106d-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="b106d-122">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="b106d-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="b106d-123">Parâmetros de conexão específicos para provedor</span><span class="sxs-lookup"><span data-stu-id="b106d-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="b106d-p102">O provedor oferece suporte a vários parâmetros de conexão específicos para provedor, além daqueles definidos pelo ADO. Assim como as propriedades de conexão do ADO, essas propriedades específicas para provedor também podem ser definidas por meio da coleção [Properties](properties-collection-ado.md) de um objeto [Connection](connection-object-ado.md) ou como parte da **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="b106d-p102">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or as part of the **ConnectionString**.</span></span>

<span data-ttu-id="b106d-p103">Esses parâmetros são descritos integralmente na Referência do programador do OLE DB. (O [Índice da propriedade dinâmica do ADO](ado-dynamic-property-index.md) fornece uma referência cruzada entre esses nomes de parâmetros e as propriedades do OLE DB correspondentes.)</span><span class="sxs-lookup"><span data-stu-id="b106d-p103">These parameters are fully described in the OLE DB Programmer's Reference. (The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between these parameter names and the corresponding OLE DB properties.)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b106d-128">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="b106d-128">Parameter</span></span></p></th>
<th><p><span data-ttu-id="b106d-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="b106d-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b106d-130"><strong>Window Handle</strong></span><span class="sxs-lookup"><span data-stu-id="b106d-130"><strong>Window Handle</strong></span></span></p></td>
<td><p><span data-ttu-id="b106d-131">Indica o identificador da janela que deverá ser usado para solicitar informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="b106d-131">Indicates the window handle to use to prompt for additional information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b106d-132"><strong>Locale Identifier</strong></span><span class="sxs-lookup"><span data-stu-id="b106d-132"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="b106d-p104">Indica um número único de 32 bits (por exemplo, 1033) que especifica preferências relacionadas ao idioma do usuário. Essas preferências indicam como as datas e os horários serão formatados, se os itens serão classificados em ordem alfabética, como as cadeias de caracteres serão comparadas, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b106d-p104">Indicates a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language. These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b106d-135"><strong>OLE DB Services</strong></span><span class="sxs-lookup"><span data-stu-id="b106d-135"><strong>OLE DB Services</strong></span></span></p></td>
<td><p><span data-ttu-id="b106d-136">Indica uma máscara de bits especificando os serviços do OLE DB que deverão ser habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="b106d-136">Indicates a bitmask that specifies OLE DB services to enable or disable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b106d-137"><strong>Prompt</strong></span><span class="sxs-lookup"><span data-stu-id="b106d-137"><strong>Prompt</strong></span></span></p></td>
<td><p><span data-ttu-id="b106d-138">Indica se o usuário deverá ser avisado enquanto uma conexão estiver sendo estabelecida.</span><span class="sxs-lookup"><span data-stu-id="b106d-138">Indicates whether to prompt the user while a connection is being established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b106d-139"><strong>Extended Properties</strong></span><span class="sxs-lookup"><span data-stu-id="b106d-139"><strong>Extended Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="b106d-140">Uma cadeia de caracteres contendo informações de conexão estendidas específicas para provedor.</span><span class="sxs-lookup"><span data-stu-id="b106d-140">A string containing provider-specific, extended connection information.</span></span> <span data-ttu-id="b106d-141">Use esta propriedade somente para informações de conexão específicas para provedor que não possam ser descritas pelo mecanismo de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b106d-141">Use this property only for provider-specific connection information that cannot be described through the property mechanism.</span></span></p></td>
</tr>
</tbody>
</table>

