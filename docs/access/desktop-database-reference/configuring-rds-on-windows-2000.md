---
title: Configurando o RDS no Windows 2000
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 80ce29ed129035dcb6799844a4b78509b976f0ee
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862937"
---
# <a name="configuring-rds-on-windows-2000"></a><span data-ttu-id="373bd-102">Configurando o RDS no Windows 2000</span><span class="sxs-lookup"><span data-stu-id="373bd-102">Configuring RDS on Windows 2000</span></span>


<span data-ttu-id="373bd-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="373bd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="373bd-104">Se tiver dificuldades para fazer com que o RDS funcione corretamente depois de fazer a atualização para o Windows 2000, siga as etapas a seguir para solucionar o problema.</span><span class="sxs-lookup"><span data-stu-id="373bd-104">If you experience difficulties getting RDS to function properly after upgrading to Windows 2000, follow the steps below to troubleshoot the issue.</span></span>

1.  <span data-ttu-id="373bd-105">Certifique-se de que o serviço de publicação na World Wide Web é executado primeiro navegando até https://*server* usando o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="373bd-105">Make sure that the World Wide Web Publishing Service is running first by navigating to https://*server* using Internet Explorer.</span></span> <span data-ttu-id="373bd-106">Se você não puder acessar o servidor Web dessa forma, vá para um prompt de comando e digite o seguinte comando, "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="373bd-106">If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".</span></span>

2.  <span data-ttu-id="373bd-107">No menu Iniciar, selecione Executar.</span><span class="sxs-lookup"><span data-stu-id="373bd-107">From the Start menu, select Run.</span></span> <span data-ttu-id="373bd-108">Digite msdfmap.ini e clique em OK para abrir o arquivo msdfmap.ini no Bloco de Notas.</span><span class="sxs-lookup"><span data-stu-id="373bd-108">Type msdfmap.ini and click OK to open the msdfmap.ini file in Notepad.</span></span> <span data-ttu-id="373bd-109">Verifique o \[conectar padrão\] seção e se o parâmetro de acesso é definido como NOACCESS, altere-o para somente leitura.</span><span class="sxs-lookup"><span data-stu-id="373bd-109">Check the \[CONNECT DEFAULT\] section, and if the ACCESS parameter is set to NOACCESS, change it to READONLY.</span></span>

3.  <span data-ttu-id="373bd-110">Usando o utilitário RegEdit, navegue até "HKEY\_LOCAL\_máquina\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" e verifique se **HandlerRequired** está definido como 0 e **DefaultHandler** é "" (nulo cadeia de caracteres).</span><span class="sxs-lookup"><span data-stu-id="373bd-110">Using the RegEdit utility, navigate to "HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" and make sure **HandlerRequired** is set to 0 and **DefaultHandler** is "" (Null string).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="373bd-111">[!OBSERVAçãO] Se você fizer quaisquer alterações nesta seção do Registro, deverá parar e reiniciar o Serviço de Publicação na World Wide Web, inserindo os seguintes comandos em um prompt de comando: "NET STOP W3SVC" e "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="373bd-111">If you make any changes to this section of the registry, you must stop and restart the World Wide Web Publishing Service by entering the following commands at a command prompt: "NET STOP W3SVC" and "NET START W3SVC".</span></span>

4.  <span data-ttu-id="373bd-112">Usando o utilitário RegEdit, navegue no registro para "HKEY\_LOCAL\_máquina\\sistema\\CurrentControlSet\\serviços\\W3SVC\\parâmetros\\ADCLaunch" e verifique se há uma chave **chamado Rdsserver**.</span><span class="sxs-lookup"><span data-stu-id="373bd-112">Using the RegEdit utility, navigate in the registry to "HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\W3SVC\\Parameters\\ADCLaunch" and verify that there is a key called **RDSServer.Datafactory**.</span></span> <span data-ttu-id="373bd-113">Se não houver, crie-a.</span><span class="sxs-lookup"><span data-stu-id="373bd-113">If not, create it.</span></span>

<span data-ttu-id="373bd-114"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="373bd-114"><<<<<<< HEAD</span></span>
5.  <span data-ttu-id="373bd-115">Usando o Gerenciador de Serviços de Internet, vá para o Site Padrão e visualize as propriedades da raiz virtual MSADC.</span><span class="sxs-lookup"><span data-stu-id="373bd-115">Using Internet Services Manager, go to the Default Web Site and view the properties of the MSADC virtual root.</span></span> <span data-ttu-id="373bd-116">Inspecione a Segurança do Diretório/Endereço IP e as Restrições de Nome de Domínio.</span><span class="sxs-lookup"><span data-stu-id="373bd-116">Inspect the Directory Security/IP Address and Domain Name Restrictions.</span></span> <span data-ttu-id="373bd-117">Se "Acesso Negado" estiver marcado, selecione "Concedido".</span><span class="sxs-lookup"><span data-stu-id="373bd-117">If the "Access is Denied" is checked then select "Granted".</span></span>
=======
5.  <span data-ttu-id="373bd-118">Usando o Gerenciador de serviços de Internet, vá para o site padrão e exibir as propriedades da raiz virtual MSADC.</span><span class="sxs-lookup"><span data-stu-id="373bd-118">Using Internet Services Manager, go to the default website and view the properties of the MSADC virtual root.</span></span> <span data-ttu-id="373bd-119">Inspecione a Segurança do Diretório/Endereço IP e as Restrições de Nome de Domínio.</span><span class="sxs-lookup"><span data-stu-id="373bd-119">Inspect the Directory Security/IP Address and Domain Name Restrictions.</span></span> <span data-ttu-id="373bd-120">Se "Acesso Negado" estiver marcado, selecione "Concedido".</span><span class="sxs-lookup"><span data-stu-id="373bd-120">If the "Access is Denied" is checked then select "Granted".</span></span>
>>>>>>> <span data-ttu-id="373bd-121">mestre</span><span class="sxs-lookup"><span data-stu-id="373bd-121">master</span></span>

<span data-ttu-id="373bd-122">Certifique-se de tentar reiniciar o servidor se as alterações não parecerem solucionar o problema em um primeiro momento.</span><span class="sxs-lookup"><span data-stu-id="373bd-122">Be sure to try rebooting the server if the changes to do not appear to solve the problem at first.</span></span>

