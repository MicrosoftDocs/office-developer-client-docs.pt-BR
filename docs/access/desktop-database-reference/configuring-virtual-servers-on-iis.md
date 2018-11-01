---
title: Configurando os servidores virtuais no IIS
TOCTitle: Configuring Virtual Servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7408e2dc10a5e47b298b77a9244477b16bca3ff1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879239"
---
# <a name="configuring-virtual-servers-on-iis"></a>Configurando os servidores virtuais no IIS


**Aplica-se a**: Access 2013, o Office 2013

Ao criar os servidores virtuais no Internet Information Services 4.0, as próximas duas etapas adicionais serão necessárias para configurar o servidor virtual para trabalhar com o RDS:

1.  Ao configurar o servidor, marque "Permitir Acesso de Execução".

2.  Mova a Msadcs *vroot*\\msadc, em que *vroot* é um diretório base do servidor virtual.

