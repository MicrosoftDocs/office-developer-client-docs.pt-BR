---
title: Configuração de servidores virtuais no IIS
TOCTitle: Configuring virtual servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9c7f5782885aafd43e365ddc4f08dedd0975234
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719307"
---
# <a name="configuring-virtual-servers-on-iis"></a><span data-ttu-id="5f06b-102">Configuração de servidores virtuais no IIS</span><span class="sxs-lookup"><span data-stu-id="5f06b-102">Configuring virtual servers on IIS</span></span>

<span data-ttu-id="5f06b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f06b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5f06b-104">Ao criar os servidores virtuais no Internet Information Services 4.0, as próximas duas etapas adicionais serão necessárias para configurar o servidor virtual para trabalhar com o RDS:</span><span class="sxs-lookup"><span data-stu-id="5f06b-104">When creating virtual servers in Internet Information Services 4.0, the following two extra steps are needed in order to configure the virtual server to work with RDS:</span></span>

1.  <span data-ttu-id="5f06b-105">Ao configurar o servidor, marque "Permitir Acesso de Execução".</span><span class="sxs-lookup"><span data-stu-id="5f06b-105">When setting up the server, check "Allow Execute Access."</span></span>

2.  <span data-ttu-id="5f06b-106">Mova a Msadcs *vroot*\\msadc, em que *vroot* é um diretório base do servidor virtual.</span><span class="sxs-lookup"><span data-stu-id="5f06b-106">Move msadcs.dll to *vroot*\\msadc, where *vroot* is the home directory of your virtual server.</span></span>

