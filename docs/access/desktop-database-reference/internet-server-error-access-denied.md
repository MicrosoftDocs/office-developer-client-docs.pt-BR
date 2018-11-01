---
title: 'Erro no servidor da Internet: acesso negado'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 132ecc75c01cdc54eb2d7664227b7abb1578cc2f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876537"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="203fa-102">Erro no servidor da Internet: acesso negado</span><span class="sxs-lookup"><span data-stu-id="203fa-102">Internet Server Error: Access Denied</span></span>


<span data-ttu-id="203fa-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="203fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="203fa-104">Se você receber este erro, geralmente significa que o Microsoft Internet Information Services (IIS) retornou o seguinte status:</span><span class="sxs-lookup"><span data-stu-id="203fa-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="203fa-105">HTTP\_STATUS\_NEGADOS 401</span><span class="sxs-lookup"><span data-stu-id="203fa-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="203fa-106">Certifique-se de que os diretórios acessados pelo IIS têm as permissões adequadas.</span><span class="sxs-lookup"><span data-stu-id="203fa-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="203fa-107">RDS podem se comunicar com um servidor de web IIS executando em qualquer um dos três modos de autenticação de senha: anônima, básica ou o desafio/resposta do NT (chamado de autenticação integrada do Windows no Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="203fa-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="203fa-108">Além disso, o servidor web deve ter permissões para o computador de origem de dados, caso se trate de um computador Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="203fa-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

