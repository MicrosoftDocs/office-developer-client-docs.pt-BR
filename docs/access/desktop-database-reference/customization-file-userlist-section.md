---
title: Seção UserList do arquivo de personalização
TOCTitle: Customization File UserList section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ecaf77765051a202925449d0221f0a68a2a06622
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295153"
---
# <a name="customization-file-userlist-section"></a><span data-ttu-id="f293f-102">Seção UserList do arquivo de personalização</span><span class="sxs-lookup"><span data-stu-id="f293f-102">Customization File UserList section</span></span>


<span data-ttu-id="f293f-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f293f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f293f-104">A seção **userlist** refere-se à seção **connect** com o mesmo parâmetro *identifier* de seção.</span><span class="sxs-lookup"><span data-stu-id="f293f-104">The **userlist** section pertains to the **connect** section with the same section *identifier* parameter.</span></span>

<span data-ttu-id="f293f-105">Esta seção pode conter *uma* entrada de acesso de usuário , que   especifica os direitos de acesso para o usuário especificado e substitui a entrada de acesso padrão na seção **de conexão correspondente.**</span><span class="sxs-lookup"><span data-stu-id="f293f-105">This section can contain a *user access entry*, which specifies access rights for the specified user and overrides the *default* *access entry* in the matching **connect** section.</span></span>

## <a name="syntax"></a><span data-ttu-id="f293f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f293f-106">Syntax</span></span>

<span data-ttu-id="f293f-107">Uma entrada de acesso de usuário tem este formato:</span><span class="sxs-lookup"><span data-stu-id="f293f-107">A user access entry is of the form:</span></span>

<span data-ttu-id="f293f-108">*userName\*\*\*=* accessRights\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f293f-108">*userName\*\*\*=* accessRights\*\*\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f293f-109">Sair</span><span class="sxs-lookup"><span data-stu-id="f293f-109">Part</span></span></p></th>
<th><p><span data-ttu-id="f293f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f293f-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f293f-111"><em>userName</em></span><span class="sxs-lookup"><span data-stu-id="f293f-111"><em>userName</em></span></span></p></td>
<td><p><span data-ttu-id="f293f-112">O <em>nome de usuário</em> da pessoa que utiliza a conexão.</span><span class="sxs-lookup"><span data-stu-id="f293f-112">The <em>user name</em> of the person employing this connection.</span></span> <span data-ttu-id="f293f-113">Os nomes válidos de usuário são estabelecidos através da caixa de diálogo <strong>Gerenciador de Serviços</strong> do IIS.</span><span class="sxs-lookup"><span data-stu-id="f293f-113">Valid user names are established with the IIS <strong>Service Manager</strong> dialog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f293f-114"><strong><em>accessRights</em></strong></span><span class="sxs-lookup"><span data-stu-id="f293f-114"><strong><em>accessRights</em></strong></span></span></p></td>
<td><p><span data-ttu-id="f293f-115">Um dos seguintes direitos de acesso:</span><span class="sxs-lookup"><span data-stu-id="f293f-115">One of the following access rights:</span></span><br />
</p>
<ul>
<li><p><span data-ttu-id="f293f-116"><strong>NoAccess</strong> — o usuário não pode acessar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="f293f-116"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="f293f-117"><strong>ReadOnly</strong> — o usuário pode ler a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="f293f-117"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="f293f-118"><strong>ReadWrite</strong> — o usuário pode ler a fonte de dados ou gravar nela.</span><span class="sxs-lookup"><span data-stu-id="f293f-118"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

