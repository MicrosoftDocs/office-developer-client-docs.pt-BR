---
title: Seção Connect do arquivo de personalização
TOCTitle: Customization File Connect section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8652aa2c028350aab79cdf101cba189026b9a5ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295139"
---
# <a name="customization-file-connect-section"></a><span data-ttu-id="04444-102">Seção Connect do arquivo de personalização</span><span class="sxs-lookup"><span data-stu-id="04444-102">Customization File Connect section</span></span>

<span data-ttu-id="04444-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04444-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04444-p101">O comportamento padrão do manipulador é negar todas as conexões. A seção **connect** especifica exceções a esse comportamento. Por exemplo, se todas as seções **connect** estivessem ausentes ou vazias, nenhuma conexão seria estabelecida por padrão.</span><span class="sxs-lookup"><span data-stu-id="04444-p101">The default behavior of the handler is to deny all connections. The **connect** section specifies exceptions to that behavior. For example, if all the **connect** sections were absent or empty, then by default no connections could be made.</span></span>

<span data-ttu-id="04444-107">A seção **connect** pode conter:</span><span class="sxs-lookup"><span data-stu-id="04444-107">The **connect** section can contain:</span></span>

- <span data-ttu-id="04444-p102">Uma entrada de acesso padrão que especifica as operações de leitura e gravação padrão permitidas na conexão. Se a seção não tiver entrada de acesso padrão, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="04444-p102">A default access entry that specifies the default read and write operations allowed on this connection. If there is no default access entry in the section, the section will be ignored.</span></span>

- <span data-ttu-id="04444-110">Uma nova sequência de conexão que substitui a sequência de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="04444-110">A new connection string that replaces the client connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="04444-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04444-111">Syntax</span></span>

<span data-ttu-id="04444-112">Uma entrada de acesso padrão tem este formato:</span><span class="sxs-lookup"><span data-stu-id="04444-112">A default access entry is of the form:</span></span>

`Access=accessRight`

<span data-ttu-id="04444-113">Uma entrada de sequência de substituição de conexão tem este formato:</span><span class="sxs-lookup"><span data-stu-id="04444-113">A replacement connection string entry is of the form:</span></span>

`Connect=connectionString`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="04444-114">Parte</span><span class="sxs-lookup"><span data-stu-id="04444-114">Part</span></span></p></th>
<th><p><span data-ttu-id="04444-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="04444-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04444-116"><strong>Connect</strong></span><span class="sxs-lookup"><span data-stu-id="04444-116"><strong>Connect</strong></span></span></p></td>
<td><p><span data-ttu-id="04444-117">Uma sequência literal que indica uma entrada de sequência de conexão.</span><span class="sxs-lookup"><span data-stu-id="04444-117">A literal string that indicates this is a connection string entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04444-118"><strong><em>connectionString</em></strong></span><span class="sxs-lookup"><span data-stu-id="04444-118"><strong><em>connectionString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="04444-119">Uma sequência de caracteres que substitui toda a sequência de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="04444-119">A string that replaces the whole client connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04444-120"><strong>Access</strong></span><span class="sxs-lookup"><span data-stu-id="04444-120"><strong>Access</strong></span></span></p></td>
<td><p><span data-ttu-id="04444-121">Uma sequência literal que indica uma entrada de acesso.</span><span class="sxs-lookup"><span data-stu-id="04444-121">A literal string that indicates this is an access entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04444-122"><strong><em>accessRight</em></strong></span><span class="sxs-lookup"><span data-stu-id="04444-122"><strong><em>accessRight</em></strong></span></span></p></td>
<td><p><span data-ttu-id="04444-123">Um dos seguintes direitos de acesso:</span><span class="sxs-lookup"><span data-stu-id="04444-123">One of the following access rights:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="04444-124"><strong>NoAccess</strong> — o usuário não pode acessar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="04444-124"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="04444-125"><strong>ReadOnly</strong> — o usuário pode ler a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="04444-125"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="04444-126"><strong>ReadWrite</strong> — o usuário pode ler a fonte de dados ou gravar nela.</span><span class="sxs-lookup"><span data-stu-id="04444-126"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="04444-127">Se você quiser permitir qualquer conexão (em vigor, desabilitando o comportamento padrão do manipulador), defina a entrada de acesso na seção **Connect default** como e exclua ou comente qualquer outra seção \*\*\*\* *identificador* de conexão.</span><span class="sxs-lookup"><span data-stu-id="04444-127">If you want to allow any connection (in effect, disabling the default handler behavior), set the access entry in the **connect default** section to , and delete or comment out any other **connect** *identifier* section.</span></span>

