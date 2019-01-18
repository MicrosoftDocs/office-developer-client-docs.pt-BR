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
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a><span data-ttu-id="fc393-102">Configurando o DataFactory para modos Safe ou Unrestricted</span><span class="sxs-lookup"><span data-stu-id="fc393-102">Configuring DataFactory for Safe or Unrestricted Modes</span></span>


<span data-ttu-id="fc393-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc393-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc393-p101">Por padrão, o ADO é instalado com uma configuração [RDSServer.DataFactory](datafactory-object-rdsserver.md) "segura". O modo seguro para os componentes do Servidor RDS indica que o seguinte seja verdadeiro:</span><span class="sxs-lookup"><span data-stu-id="fc393-p101">By default, ADO is installed with a "safe" [RDSServer.DataFactory](datafactory-object-rdsserver.md) configuration. Safe mode for RDS Server components means that the following are true:</span></span>

1.  <span data-ttu-id="fc393-106">O manipulador é requerido com RDSServer.DataFactory (isso é comandado por uma configuração de chave de registro).</span><span class="sxs-lookup"><span data-stu-id="fc393-106">Handler is required with the RDSServer.DataFactory (this is mandated by a registry key setting).</span></span>

2.  <span data-ttu-id="fc393-107">O manipulador padrão, msdfmap.handler, é registrado, presente na lista do manipulador seguro e marcado como manipulador padrão.</span><span class="sxs-lookup"><span data-stu-id="fc393-107">The default handler, msdfmap.handler, is registered, present in the safe-handler list, and marked as the default handler.</span></span>

3.  <span data-ttu-id="fc393-p102">O arquivo msdfmap.ini está instalado no diretório Windows. Você deve configurar esse arquivo de acordo com suas necessidades antes de utilizar o RDS no modo de três camadas.</span><span class="sxs-lookup"><span data-stu-id="fc393-p102">Msdfmap.ini file is installed in the Windows directory. You must configure this file according to your needs, before using RDS in three-tier mode.</span></span>

<span data-ttu-id="fc393-110">Opcionalmente, você pode configurar uma instalação **DataFactory** não restrita.</span><span class="sxs-lookup"><span data-stu-id="fc393-110">Optionally, you can configure an unrestricted **DataFactory** installation.</span></span> <span data-ttu-id="fc393-111">O **DataFactory** pode ser usado diretamente sem o manipulador personalizado.</span><span class="sxs-lookup"><span data-stu-id="fc393-111">**DataFactory** can be used directly without the custom handler.</span></span> <span data-ttu-id="fc393-112">Os usuários ainda podem utilizar um manipulador personalizado modificando as sequências de conexão, mas isso não é requerido.</span><span class="sxs-lookup"><span data-stu-id="fc393-112">Users can still use a custom handler by modifying the connection strings, but it is not required.</span></span> <span data-ttu-id="fc393-113">Para obter mais informações sobre as implicações do uso do objeto **rdsserver. DataFactory** , consulte [Protegendo aplicativos do RDS](securing-rds-applications.md).</span><span class="sxs-lookup"><span data-stu-id="fc393-113">For more information about the implications of using the **RDSServer.DataFactory** object, see [Securing RDS Applications](securing-rds-applications.md).</span></span>

<span data-ttu-id="fc393-p104">O arquivo de registro handsafe.reg foi fornecido para configurar as entradas de registro do manipulador para configuração segura. Para executar no modo seguro, execute o handsafe.reg. O arquivo de registro handunsf.reg foi fornecido para configurar as entradas de registro do manipulador para a configuração irrestrita. Para executar no modo irrestrito, execute handunsf.reg.</span><span class="sxs-lookup"><span data-stu-id="fc393-p104">The registry file handsafe.reg has been provided to set up the handler registry entries for a safe configuration. To run in safe mode, run handsafe.reg. The registry file handunsf.reg has been provided to set up the handler registry entries for an unrestricted configuration. To run in unrestricted mode, run handunsf.reg.</span></span>

<span data-ttu-id="fc393-117">Após a execução Handsafe ou handunsf.reg, você deve parar e reiniciar o serviço de publicação na World Wide Web no servidor web, digitando os seguintes comandos em uma janela de comando: "NET STOP W3SVC" e "NET iniciar W3SVC".</span><span class="sxs-lookup"><span data-stu-id="fc393-117">After running either handsafe.reg or handunsf.reg, you must stop and restart the World Wide Web Publishing Service on the web server by typing the following commands in a command window: "NET STOP W3SVC" and "NET START W3SVC".</span></span>

<span data-ttu-id="fc393-118">Para obter mais informações sobre o uso do recurso do manipulador de personalização do RDS, consulte o artigo técnico Usando o recurso do manipulador de personalização no RDS 2.1.</span><span class="sxs-lookup"><span data-stu-id="fc393-118">For more information about using the customization handler feature of RDS, see the technical article Using the Customization Handler Feature in RDS 2.1.</span></span>

