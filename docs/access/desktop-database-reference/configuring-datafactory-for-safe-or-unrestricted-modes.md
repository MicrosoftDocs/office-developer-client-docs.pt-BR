---
title: Configurando o DataFactory para modos Safe ou Unrestricted
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4313d48359499eaf249a68eb97408c8ed4ecb88
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702730"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a>Configurando o DataFactory para modos Safe ou Unrestricted


**Aplica-se a**: Access 2013, o Office 2013

Por padrão, o ADO é instalado com uma configuração [RDSServer.DataFactory](datafactory-object-rdsserver.md) "segura". O modo seguro para os componentes do Servidor RDS indica que o seguinte seja verdadeiro:

1.  O manipulador é requerido com RDSServer.DataFactory (isso é comandado por uma configuração de chave de registro).

2.  O manipulador padrão, msdfmap.handler, é registrado, presente na lista do manipulador seguro e marcado como manipulador padrão.

3.  O arquivo msdfmap.ini está instalado no diretório Windows. Você deve configurar esse arquivo de acordo com suas necessidades antes de utilizar o RDS no modo de três camadas.

Opcionalmente, você pode configurar uma instalação **DataFactory** não restrita. O **DataFactory** pode ser usado diretamente sem o manipulador personalizado. Os usuários ainda podem utilizar um manipulador personalizado modificando as sequências de conexão, mas isso não é requerido. Para obter mais informações sobre as implicações do uso do objeto **rdsserver. DataFactory** , consulte [Protegendo aplicativos do RDS](securing-rds-applications.md).

O arquivo de registro handsafe.reg foi fornecido para configurar as entradas de registro do manipulador para configuração segura. Para executar no modo seguro, execute o handsafe.reg. O arquivo de registro handunsf.reg foi fornecido para configurar as entradas de registro do manipulador para a configuração irrestrita. Para executar no modo irrestrito, execute handunsf.reg.

Após a execução Handsafe ou handunsf.reg, você deve parar e reiniciar o serviço de publicação na World Wide Web no servidor web, digitando os seguintes comandos em uma janela de comando: "NET STOP W3SVC" e "NET iniciar W3SVC".

Para obter mais informações sobre o uso do recurso do manipulador de personalização do RDS, consulte o artigo técnico Usando o recurso do manipulador de personalização no RDS 2.1.

