---
title: Seção connect do arquivo de personalização
TOCTitle: Customization File Connect Section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd4b7eed3cb5d8192866127322c00e7ecd5a15b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463819"
---
# <a name="customization-file-connect-section"></a><span data-ttu-id="92254-102">Seção connect do arquivo de personalização</span><span class="sxs-lookup"><span data-stu-id="92254-102">Customization File Connect Section</span></span>

<span data-ttu-id="92254-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="92254-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="92254-p101">O comportamento padrão do manipulador é negar todas as conexões. A seção **connect** especifica exceções a esse comportamento. Por exemplo, se todas as seções **connect** estivessem ausentes ou vazias, nenhuma conexão seria estabelecida por padrão.</span><span class="sxs-lookup"><span data-stu-id="92254-p101">The default behavior of the handler is to deny all connections. The **connect** section specifies exceptions to that behavior. For example, if all the **connect** sections were absent or empty, then by default no connections could be made.</span></span>

<span data-ttu-id="92254-107">A seção **connect** pode conter:</span><span class="sxs-lookup"><span data-stu-id="92254-107">The **connect** section can contain:</span></span>

- <span data-ttu-id="92254-p102">Uma entrada de acesso padrão que especifica as operações de leitura e gravação padrão permitidas na conexão. Se a seção não tiver entrada de acesso padrão, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="92254-p102">A default access entry that specifies the default read and write operations allowed on this connection. If there is no default access entry in the section, the section will be ignored.</span></span>

- <span data-ttu-id="92254-110">Uma nova sequência de conexão que substitui a sequência de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="92254-110">A new connection string that replaces the client connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="92254-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92254-111">Syntax</span></span>

<span data-ttu-id="92254-112">Uma entrada de acesso padrão tem este formato:</span><span class="sxs-lookup"><span data-stu-id="92254-112">A default access entry is of the form:</span></span>

`Access=accessRight`

<span data-ttu-id="92254-113">Uma entrada de sequência de substituição de conexão tem este formato:</span><span class="sxs-lookup"><span data-stu-id="92254-113">A replacement connection string entry is of the form:</span></span>

`Connect=connectionString`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="92254-114">Parte</span><span class="sxs-lookup"><span data-stu-id="92254-114">Part</span></span></p></th>
<th><p><span data-ttu-id="92254-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="92254-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92254-116"><strong>Connect</strong></span><span class="sxs-lookup"><span data-stu-id="92254-116"><strong>Connect</strong></span></span></p></td>
<td><p><span data-ttu-id="92254-117">Uma sequência literal que indica uma entrada de sequência de conexão.</span><span class="sxs-lookup"><span data-stu-id="92254-117">A literal string that indicates this is a connection string entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92254-118"><strong><em>connectionString</em></strong></span><span class="sxs-lookup"><span data-stu-id="92254-118"><strong><em>connectionString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="92254-119">Uma sequência de caracteres que substitui toda a sequência de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="92254-119">A string that replaces the whole client connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92254-120"><strong>Access</strong></span><span class="sxs-lookup"><span data-stu-id="92254-120"><strong>Access</strong></span></span></p></td>
<td><p><span data-ttu-id="92254-121">Uma sequência literal que indica uma entrada de acesso.</span><span class="sxs-lookup"><span data-stu-id="92254-121">A literal string that indicates this is an access entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92254-122"><strong><em>accessRight</em></strong></span><span class="sxs-lookup"><span data-stu-id="92254-122"><strong><em>accessRight</em></strong></span></span></p></td>
<td><p><span data-ttu-id="92254-123">Um dos seguintes direitos de acesso:
</span><span class="sxs-lookup"><span data-stu-id="92254-123">One of the following access rights:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="92254-124"><strong>NoAccess</strong> — o usuário não pode acessar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="92254-124"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="92254-125"><strong>ReadOnly</strong> — o usuário pode ler a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="92254-125"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="92254-126"><strong>ReadWrite</strong> — o usuário pode ler a fonte de dados ou gravar nela.</span><span class="sxs-lookup"><span data-stu-id="92254-126"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="92254-127">Se você quiser permitir que qualquer conexão (desabilitando o comportamento padrão do manipulador), defina a entrada de acesso na seção **Conectar padrão** e exclua ou comente qualquer outra **Conectar** *identificador de* seção.</span><span class="sxs-lookup"><span data-stu-id="92254-127">If you want to allow any connection (in effect, disabling the default handler behavior), set the access entry in the **connect default** section to , and delete or comment out any other **connect** *identifier* section.</span></span>

