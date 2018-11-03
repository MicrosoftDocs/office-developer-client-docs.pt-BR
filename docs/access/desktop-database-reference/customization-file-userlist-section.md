---
title: Seção UserList do arquivo de personalização
TOCTitle: Customization File UserList section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62aaba79fa010de62fb1ac35939673b2056be3f7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944092"
---
# <a name="customization-file-userlist-section"></a><span data-ttu-id="95df3-102">Seção UserList do arquivo de personalização</span><span class="sxs-lookup"><span data-stu-id="95df3-102">Customization File UserList section</span></span>


<span data-ttu-id="95df3-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="95df3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95df3-104">A seção **userlist** refere-se à seção **se conectar** com o mesmo parâmetro *identifier* de seção.</span><span class="sxs-lookup"><span data-stu-id="95df3-104">The **userlist** section pertains to the **connect** section with the same section *identifier* parameter.</span></span>

<span data-ttu-id="95df3-105">Esta seção pode conter uma *entrada de acesso de usuário*, que especifica os direitos de acesso do usuário especificado e substitui a *entrada de acesso* do *padrão* na seção **Conectar** correspondentes.</span><span class="sxs-lookup"><span data-stu-id="95df3-105">This section can contain a *user access entry*, which specifies access rights for the specified user and overrides the *default* *access entry* in the matching **connect** section.</span></span>

## <a name="syntax"></a><span data-ttu-id="95df3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95df3-106">Syntax</span></span>

<span data-ttu-id="95df3-107">Uma entrada de acesso de usuário tem este formato:</span><span class="sxs-lookup"><span data-stu-id="95df3-107">A user access entry is of the form:</span></span>

<span data-ttu-id="95df3-108">*userName \* \* \* =* accessRights \* \* \*</span><span class="sxs-lookup"><span data-stu-id="95df3-108">*userName\*\*\*=* accessRights\*\*\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95df3-109">Parte</span><span class="sxs-lookup"><span data-stu-id="95df3-109">Part</span></span></p></th>
<th><p><span data-ttu-id="95df3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="95df3-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95df3-111"><em>userName</em></span><span class="sxs-lookup"><span data-stu-id="95df3-111"><em>userName</em></span></span></p></td>
<td><p><span data-ttu-id="95df3-p101">O <em>nome de usuário</em> da pessoa que utiliza a conexão. Os nomes válidos de usuário são estabelecidos através da caixa de diálogo <strong>Gerenciador de Serviços</strong> do IIS.</span><span class="sxs-lookup"><span data-stu-id="95df3-p101">The <em>user name</em> of the person employing this connection. Valid user names are established with the IIS <strong>Service Manager</strong> dialog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95df3-114"><strong><em>accessRights</em></strong></span><span class="sxs-lookup"><span data-stu-id="95df3-114"><strong><em>accessRights</em></strong></span></span></p></td>
<td><p><span data-ttu-id="95df3-115">Um dos seguintes direitos de acesso:
</span><span class="sxs-lookup"><span data-stu-id="95df3-115">One of the following access rights:</span></span><br />
</p>
<ul>
<li><p><span data-ttu-id="95df3-116"><strong>NoAccess</strong> — o usuário não pode acessar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="95df3-116"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="95df3-117"><strong>ReadOnly</strong> — o usuário pode ler a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="95df3-117"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="95df3-118"><strong>ReadWrite</strong> — o usuário pode ler a fonte de dados ou gravar nela.</span><span class="sxs-lookup"><span data-stu-id="95df3-118"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

