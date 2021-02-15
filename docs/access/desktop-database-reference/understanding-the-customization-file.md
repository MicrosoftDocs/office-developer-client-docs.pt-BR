---
title: Noções básicas sobre o arquivo de personalização
TOCTitle: Understanding the Customization File
ms:assetid: 98fd5ec1-d5bd-cdd2-5eb5-9a1682fbed79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249686(v=office.15)
ms:contentKeyID: 48546507
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b977fc4273068ac52efe8960761a9e28a6234e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314067"
---
# <a name="understanding-the-customization-file"></a><span data-ttu-id="24e9d-102">Noções básicas sobre o arquivo de personalização</span><span class="sxs-lookup"><span data-stu-id="24e9d-102">Understanding the Customization File</span></span>


<span data-ttu-id="24e9d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="24e9d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="24e9d-104">Cada título de seção no arquivo de personalização consiste em colchetes ( **\[\]** ) contendo um tipo e um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="24e9d-104">Each section header in the customization file consists of square brackets (**\[\]**) containing a type and parameter.</span></span> <span data-ttu-id="24e9d-105">Os quatro tipos de seção são indicados pela sequência de caracteres literal **connect**, **sql**, **userlist** ou **logs**.</span><span class="sxs-lookup"><span data-stu-id="24e9d-105">The four section types are indicated by the literal strings **connect**, **sql**, **userlist**, or **logs**.</span></span> <span data-ttu-id="24e9d-106">O parâmetro pode ser a sequência de caracteres literal, o padrão, um identificador especificado pelo usuário ou nada.</span><span class="sxs-lookup"><span data-stu-id="24e9d-106">The parameter is the literal string, the default, a user-specified identifier, or nothing.</span></span>

<span data-ttu-id="24e9d-107">Portanto, cada seção é marcada com um destes cabeçalhos de seção:</span><span class="sxs-lookup"><span data-stu-id="24e9d-107">Therefore, each section is marked with one of the following section headers:</span></span>

```text 
 
[ connect   default     ]
[ connect   identifier  ]
[ sql       default     ]
[ sql       identifier  ]
[ userlist  identifier  ]
[ logs                  ]
```

<span data-ttu-id="24e9d-108">Os cabeçalhos de seção possuem as seguintes partes.</span><span class="sxs-lookup"><span data-stu-id="24e9d-108">The section headers have the following parts.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="24e9d-109">Sair</span><span class="sxs-lookup"><span data-stu-id="24e9d-109">Part</span></span></p></th>
<th><p><span data-ttu-id="24e9d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="24e9d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24e9d-111"><strong>connect</strong></span><span class="sxs-lookup"><span data-stu-id="24e9d-111"><strong>connect</strong></span></span></p></td>
<td><p><span data-ttu-id="24e9d-112">Uma sequência de caracteres literal que modifica uma sequência de conexão.</span><span class="sxs-lookup"><span data-stu-id="24e9d-112">A literal string that modifies a connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24e9d-113"><strong>sql</strong></span><span class="sxs-lookup"><span data-stu-id="24e9d-113"><strong>sql</strong></span></span></p></td>
<td><p><span data-ttu-id="24e9d-114">Uma sequência de caracteres literal que modifica uma sequência de comando.</span><span class="sxs-lookup"><span data-stu-id="24e9d-114">A literal string that modifies a command string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24e9d-115"><strong>userlist</strong></span><span class="sxs-lookup"><span data-stu-id="24e9d-115"><strong>userlist</strong></span></span></p></td>
<td><p><span data-ttu-id="24e9d-116">Uma sequência de caracteres literal que modifica os direitos de acesso de um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="24e9d-116">A literal string that modifies the access rights of a specific user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24e9d-117"><strong>logs</strong></span><span class="sxs-lookup"><span data-stu-id="24e9d-117"><strong>logs</strong></span></span></p></td>
<td><p><span data-ttu-id="24e9d-118">Uma sequência de caracteres literal que especifica um arquivo de log que registra erros operacionais.</span><span class="sxs-lookup"><span data-stu-id="24e9d-118">A literal string that specifies a log file recording operational errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24e9d-119"><strong>default</strong></span><span class="sxs-lookup"><span data-stu-id="24e9d-119"><strong>default</strong></span></span></p></td>
<td><p><span data-ttu-id="24e9d-120">Uma sequência de caracteres literal usada quando nenhum identificador é especificado ou localizado.</span><span class="sxs-lookup"><span data-stu-id="24e9d-120">A literal string that is used if no identifier is specified or found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24e9d-121"><em>identificador</em></span><span class="sxs-lookup"><span data-stu-id="24e9d-121"><em>identifier</em></span></span></p></td>
<td><p><span data-ttu-id="24e9d-122">Uma sequência de caracteres que corresponde a uma sequência de caracteres na sequência de <strong>conexão</strong> ou de <strong>comando</strong>.</span><span class="sxs-lookup"><span data-stu-id="24e9d-122">A string that matches a string in the <strong>connect</strong> or <strong>command</strong> string.</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="24e9d-123">Use esta seção se o cabeçalho de seção contiver <strong>connect</strong> e a sequência identifier for localizada na sequência de conexão.</span><span class="sxs-lookup"><span data-stu-id="24e9d-123">Use this section if the section header contains <strong>connect</strong> and the identifier string is found in the connection string.</span></span></p></li>
<li><p><span data-ttu-id="24e9d-124">Use esta seção se o cabeçalho de seção contiver <strong>sql</strong> e a sequência identifier for localizada na sequência de comando.</span><span class="sxs-lookup"><span data-stu-id="24e9d-124">Use this section if the section header contains <strong>sql</strong> and the identifier string is found in the command string.</span></span></p></li>
<li><p><span data-ttu-id="24e9d-125">Use esta seção se o cabeçalho de seção contiver <strong>userlist</strong> e a sequência identifier corresponder a um identificador de seção <strong>connect</strong>.</span><span class="sxs-lookup"><span data-stu-id="24e9d-125">Use this section if the section header contains <strong>userlist</strong> and the identifier string matches a <strong>connect</strong> section identifier.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="24e9d-p102">O **DataFactory** chama o manipulador, passando parâmetros cliente. O manipulador procura sequências de caracteres completas nesses parâmetros que correspondam aos identificadores nos cabeçalhos de seção apropriados. Se for encontrada uma correspondência, o conteúdo dessa seção será aplicado ao parâmetro cliente.</span><span class="sxs-lookup"><span data-stu-id="24e9d-p102">The **DataFactory** calls the handler, passing client parameters. The handler searches for whole strings in the client parameters that match identifiers in the appropriate section headers. If a match is found, the contents of that section are applied to the client parameter.</span></span>

<span data-ttu-id="24e9d-129">Uma seção específica é usada nas seguintes circunstâncias:</span><span class="sxs-lookup"><span data-stu-id="24e9d-129">A particular section is used under the following circumstances:</span></span>

  - <span data-ttu-id="24e9d-130">Uma **seção connect** é usada se a parte de valor da palavra-chave de cadeia  de caracteres de conexão do cliente, "\**Data Source=\*\*\*value*", corresponde a um identificador de seção de conexão *.*</span><span class="sxs-lookup"><span data-stu-id="24e9d-130">A **connect** section is used if the value part of the client connect string keyword, "\**Data Source=\*\*\*value*", matches a **connect** section identifier *.*</span></span>

  - <span data-ttu-id="24e9d-131">Uma seção **sql** será usada se a sequência de comando do cliente contiver uma sequência de caracteres que corresponda a um identificador de seção **sql**.</span><span class="sxs-lookup"><span data-stu-id="24e9d-131">An **sql** section is used if the client command string contains a string that matches an **sql** section identifier.</span></span>

  - <span data-ttu-id="24e9d-132">Uma seção **connect** ou **sql** com um parâmetro padrão será usada se não houver nenhum identificador correspondente.</span><span class="sxs-lookup"><span data-stu-id="24e9d-132">A **connect** or **sql** section with a default parameter is used if there is no matching identifier.</span></span>

  - <span data-ttu-id="24e9d-p103">Uma seção **userlist** será usada se o identificador da seção **userlist** corresponder a um identificador da seção **connect**. Em caso de correspondência, o conteúdo da seção **userlist** será aplicado à conexão administrada pela seção **connect**.</span><span class="sxs-lookup"><span data-stu-id="24e9d-p103">A **userlist** section is used if the **userlist** section identifier matches a **connect** section identifier. If there is a match, the contents of the **userlist** section are applied to the connection governed by the **connect** section.</span></span>

  - <span data-ttu-id="24e9d-135">Se a sequência de caracteres em uma sequência de conexão ou de comando não corresponder ao identificador de nenhum cabeçalho da seção **connect** ou **sql** e se não houver cabeçalho da seção **connect** ou **sql** com um parâmetro padrão, a sequência de caracteres do cliente será usada sem modificação.</span><span class="sxs-lookup"><span data-stu-id="24e9d-135">If the string in a connection or command string does not match the identifier in any **connect** or **sql** section header, and there is no **connect** or **sql** section header with a default parameter, then the client string is used without modification.</span></span>

  - <span data-ttu-id="24e9d-136">A seção **logs** será usada sempre que **DataFactory** estiver em operação.</span><span class="sxs-lookup"><span data-stu-id="24e9d-136">The **logs** section is used whenever the **DataFactory** is in operation.</span></span>

