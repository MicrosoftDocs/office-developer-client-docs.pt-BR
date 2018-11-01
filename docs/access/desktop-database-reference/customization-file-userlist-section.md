---
title: Seção userlist do arquivo de personalização
TOCTitle: Customization File UserList Section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a4aa7604edc887e97cbdfbea9b75e6f46ad55f35
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880765"
---
# <a name="customization-file-userlist-section"></a><span data-ttu-id="e56ca-102">Seção userlist do arquivo de personalização</span><span class="sxs-lookup"><span data-stu-id="e56ca-102">Customization File UserList Section</span></span>


<span data-ttu-id="e56ca-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e56ca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e56ca-104">A seção **userlist** refere-se à seção **se conectar** com o mesmo parâmetro *identifier* de seção.</span><span class="sxs-lookup"><span data-stu-id="e56ca-104">The **userlist** section pertains to the **connect** section with the same section *identifier* parameter.</span></span>

<span data-ttu-id="e56ca-105">Esta seção pode conter uma *entrada de acesso de usuário*, que especifica os direitos de acesso do usuário especificado e substitui a *entrada de acesso* do *padrão* na seção **Conectar** correspondentes.</span><span class="sxs-lookup"><span data-stu-id="e56ca-105">This section can contain a *user access entry*, which specifies access rights for the specified user and overrides the *default* *access entry* in the matching **connect** section.</span></span>

## <a name="syntax"></a><span data-ttu-id="e56ca-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e56ca-106">Syntax</span></span>

<span data-ttu-id="e56ca-107">Uma entrada de acesso de usuário tem este formato:</span><span class="sxs-lookup"><span data-stu-id="e56ca-107">A user access entry is of the form:</span></span>

<span data-ttu-id="e56ca-108">*userName \* \* \* =* accessRights \* \* \*</span><span class="sxs-lookup"><span data-stu-id="e56ca-108">*userName\*\*\*=* accessRights\*\*\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e56ca-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e56ca-109">Part</span></span></p></th>
<th><p><span data-ttu-id="e56ca-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e56ca-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e56ca-111"><em>userName</em></span><span class="sxs-lookup"><span data-stu-id="e56ca-111"><em>userName</em></span></span></p></td>
<td><p><span data-ttu-id="e56ca-p101">O <em>nome de usuário</em> da pessoa que utiliza a conexão. Os nomes válidos de usuário são estabelecidos através da caixa de diálogo <strong>Gerenciador de Serviços</strong> do IIS.</span><span class="sxs-lookup"><span data-stu-id="e56ca-p101">The <em>user name</em> of the person employing this connection. Valid user names are established with the IIS <strong>Service Manager</strong> dialog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e56ca-114"><strong><em>accessRights</em></strong></span><span class="sxs-lookup"><span data-stu-id="e56ca-114"><strong><em>accessRights</em></strong></span></span></p></td>
<td><p><span data-ttu-id="e56ca-115">Um dos seguintes direitos de acesso:
</span><span class="sxs-lookup"><span data-stu-id="e56ca-115">One of the following access rights:</span></span><br />
</p>
<ul>
<li><p><span data-ttu-id="e56ca-116"><strong>NoAccess</strong> — o usuário não pode acessar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="e56ca-116"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="e56ca-117"><strong>ReadOnly</strong> — o usuário pode ler a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="e56ca-117"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="e56ca-118"><strong>ReadWrite</strong> — o usuário pode ler a fonte de dados ou gravar nela.</span><span class="sxs-lookup"><span data-stu-id="e56ca-118"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

