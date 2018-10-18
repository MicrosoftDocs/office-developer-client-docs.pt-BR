---
title: Configurando o DataFactory para modos Safe ou Unrestricted
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a3f551e4c377a0c24a0b733ff094e19d1b75d725
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606399"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a>Configurando o DataFactory para modos Safe ou Unrestricted


**Aplica-se a**: Access 2013 | Office 2013

Por padrão, o ADO é instalado com uma configuração [RDSServer.DataFactory](datafactory-object-rdsserver.md) "segura". O modo seguro para os componentes do Servidor RDS indica que o seguinte seja verdadeiro:

1.  O manipulador é requerido com RDSServer.DataFactory (isso é comandado por uma configuração de chave de registro).

2.  O manipulador padrão, msdfmap.handler, é registrado, presente na lista do manipulador seguro e marcado como manipulador padrão.

3.  O arquivo msdfmap.ini está instalado no diretório Windows. Você deve configurar esse arquivo de acordo com suas necessidades antes de utilizar o RDS no modo de três camadas.

Opcionalmente, você pode configurar uma instalação **DataFactory** não restrita. O **DataFactory** pode ser usado diretamente sem o manipulador personalizado. Os usuários ainda podem utilizar um manipulador personalizado modificando as sequências de conexão, mas isso não é requerido. Para obter mais informações sobre as implicações do uso do objeto **RDSServer.DataFactory**, consulte [Protegendo aplicativos RDS](securing-rds-applications.md).

O arquivo de registro handsafe.reg foi fornecido para configurar as entradas de registro do manipulador para configuração segura. Para executar no modo seguro, execute o handsafe.reg. O arquivo de registro handunsf.reg foi fornecido para configurar as entradas de registro do manipulador para a configuração irrestrita. Para executar no modo irrestrito, execute handunsf.reg.

<<<<<<< Cabeça após a execução Handsafe ou handunsf.reg, você deve parar e reiniciar o serviço de publicação na World Wide Web no servidor Web, digitando os seguintes comandos em uma janela de comando: "NET STOP W3SVC" e "NET iniciar W3SVC".
=== Após a execução Handsafe ou handunsf.reg, você deve parar e reiniciar o serviço de publicação na World Wide Web no servidor web, digitando os seguintes comandos em uma janela de comando: "NET STOP W3SVC" e "NET iniciar W3SVC".
>>>>>>> mestre

Para obter mais informações sobre o uso do recurso do manipulador de personalização do RDS, consulte o artigo técnico Usando o recurso do manipulador de personalização no RDS 2.1.

