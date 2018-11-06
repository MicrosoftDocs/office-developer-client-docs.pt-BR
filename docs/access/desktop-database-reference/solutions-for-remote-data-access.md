---
title: Soluções para o acesso remoto a dados
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef617f91aa6f36969932a4d8f2914df2de935787
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998158"
---
# <a name="solutions-for-remote-data-access"></a>Soluções para o acesso remoto a dados

**Aplica-se a**: Access 2013, o Office 2013

## <a name="the-issue"></a>O problema

O ADO permite que seu aplicativo obtenha acesso direto às fontes de dados (algumas vezes, chamado de sistema de duas camadas) e modifique-as. Por exemplo, se sua conexão for estabelecida com a fonte de dados que contém seus dados, ela será uma conexão direta em um sistema de duas camadas.

No entanto, convém acessar fontes de dados indiretamente por meio de um intermediário, como o Microsoft Internet Information Services (IIS). Essa organização algumas vezes é chamada de sistema de três camadas. O IIS é um sistema cliente/servidor que oferece uma forma eficiente de um aplicativo local, ou cliente, chamar um programa remoto, ou de servidor, pela Internet ou por uma intranet. O programa de servidor obtém acesso à fonte de dados e, opcionalmente, processa os dados adquiridos.

Por exemplo, sua página da Web de intranet contém um aplicativo escrito em Microsoft Visual Basic Scripting Edition (VBScript), que se conecta ao IIS. O IIS, por sua vez, conecta-se à fonte de dados real, recupera os dados, processa-os de alguma maneira e retorna as informações processadas ao aplicativo.

Neste exemplo, seu aplicativo nunca esteve diretamente conectado à fonte de dados, ao contrário do IIS. Além disso, o IIS acessou os dados através do ADO.

> [!NOTE]
> O aplicativo cliente/servidor não precisa ser baseado em Internet ou intranet (ou seja, baseado na web) — ele pode consistir somente compilados programas em uma rede local. No entanto, o caso típico é um aplicativo baseado na web.

Como alguns controles visuais, como grade, caixa de seleção ou lista, podem usar as informações retornadas, essas informações devem ser facilmente usadas por esses controles.

Você deseja uma interface de programação de aplicativo simples e eficiente que ofereça suporte a sistemas de três camadas e retorne informações com a mesma facilidade que ocorre com a recuperação em um sistema de duas camadas. O RDS (Remote Data Service) é essa interface.

## <a name="the-solution"></a>A solução

RDS define um modelo de programação — a sequência de atividades necessárias para acessar e atualizar uma fonte de dados — para obter acesso a dados por meio de um intermediário, como serviços de informações da Internet (IIS). O modelo de programação resume toda a funcionalidade do RDS.

