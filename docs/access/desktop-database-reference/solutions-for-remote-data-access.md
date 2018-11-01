---
title: Soluções para o acesso remoto a dados
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 59a7a43e6e3f19bae687eb181bc290883c4915e6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887758"
---
# <a name="solutions-for-remote-data-access"></a>Soluções para o acesso remoto a dados


**Aplica-se a**: Access 2013, o Office 2013

## <a name="the-issue"></a>O problema

O ADO permite que seu aplicativo obtenha acesso direto às fontes de dados (algumas vezes, chamado de sistema de duas camadas) e modifique-as. Por exemplo, se sua conexão for estabelecida com a fonte de dados que contém seus dados, ela será uma conexão direta em um sistema de duas camadas.

Entretanto, é possível que você deseje acessar as fontes de dados indiretamente, através de um intermediário, como o Microsoft® Internet Information Services (IIS). Essa organização algumas vezes é chamada de sistema de três camadas. O IIS é um sistema cliente/servidor que oferece uma forma eficiente de um aplicativo local, ou cliente, chamar um programa remoto, ou de servidor, pela Internet ou por uma intranet. O programa de servidor obtém acesso à fonte de dados e, opcionalmente, processa os dados adquiridos.

Por exemplo, sua página da Web de intranet contém um aplicativo escrito no Microsoft® Visual Basic Scripting Edition (VBScript), que se conecta ao IIS. O IIS, por sua vez, conecta-se à fonte de dados real, recupera os dados, processa-os de alguma maneira e retorna as informações processadas ao aplicativo.

Neste exemplo, seu aplicativo nunca esteve diretamente conectado à fonte de dados, ao contrário do IIS. Além disso, o IIS acessou os dados através do ADO.


> [!NOTE]
> <P>[!OBSERVAçãO] O aplicativo cliente/servidor não precisa se basear na Internet ou em uma intranet (ou seja, basear-se na Web)  ele pode conter apenas programas compilados em uma rede local. Entretanto, o caso típico é um aplicativo baseado na Web.</P>



Como alguns controles visuais, como grade, caixa de seleção ou lista, podem usar as informações retornadas, essas informações devem ser facilmente usadas por esses controles.

Você deseja uma interface de programação de aplicativo simples e eficiente que ofereça suporte a sistemas de três camadas e retorne informações com a mesma facilidade que ocorre com a recuperação em um sistema de duas camadas. O RDS (Remote Data Service) é essa interface.

## <a name="the-solution"></a>A solução

O RDS define um modelo de programação  a sequência de atividades necessárias para obter acesso a uma fonte de dados e atualizá-la  para obter acesso aos dados por meio de um intermediário, por exemplo, o Internet Information Services (IIS). O modelo de programação resume toda a funcionalidade do RDS.

