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
# <a name="configuring-virtual-servers-on-iis"></a>Configuração de servidores virtuais no IIS

**Aplica-se a**: Access 2013, o Office 2013

Ao criar os servidores virtuais no Internet Information Services 4.0, as próximas duas etapas adicionais serão necessárias para configurar o servidor virtual para trabalhar com o RDS:

1.  Ao configurar o servidor, marque "Permitir Acesso de Execução".

2.  Mova a Msadcs *vroot*\\msadc, em que *vroot* é um diretório base do servidor virtual.

