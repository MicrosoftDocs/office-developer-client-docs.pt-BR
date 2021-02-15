---
title: 'Erro no servidor da Internet: acesso negado'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: af823f46653b3ec83950c2e2cfe639b514196b08
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291252"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="1d55c-102">Erro no servidor da Internet: acesso negado</span><span class="sxs-lookup"><span data-stu-id="1d55c-102">Internet Server error: Access Denied</span></span>


<span data-ttu-id="1d55c-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d55c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d55c-104">Se você receber este erro, geralmente significa que o Microsoft Internet Information Services (IIS) retornou o seguinte status:</span><span class="sxs-lookup"><span data-stu-id="1d55c-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="1d55c-105">HTTP \_ STATUS \_ NEGADO 401</span><span class="sxs-lookup"><span data-stu-id="1d55c-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="1d55c-106">Certifique-se de que os diretórios acessados pelo IIS têm as permissões adequadas.</span><span class="sxs-lookup"><span data-stu-id="1d55c-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="1d55c-107">O RDS pode se comunicar com um servidor Web do IIS em execução em qualquer um dos três modos de Autenticação de Senha: Anônimo, Básico ou Desafio/Resposta NT (chamado de autenticação integrada do Windows no Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="1d55c-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="1d55c-108">Além disso, o servidor Web deve ter permissões para o computador de fonte de dados se for um computador Com Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1d55c-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

