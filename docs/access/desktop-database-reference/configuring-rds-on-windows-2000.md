---
title: Configurando o RDS no Windows 2000
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8482df5ca2fab110e5b1a77fe227c5f0c583d893
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296014"
---
# <a name="configuring-rds-on-windows-2000"></a>Configuração do RDS no Windows 2000


**Aplica-se ao:** Access 2013, Office 2013

Se tiver dificuldades para fazer com que o RDS funcione corretamente depois de fazer a atualização para o Windows 2000, siga as etapas a seguir para solucionar o problema.

1.  Certifique-se de que o serviço de publicação na World Wide Web esteja sendo executado primeiro navegando até o*servidor* https://usando o Internet Explorer. Se você não puder acessar o servidor Web dessa forma, vá para um prompt de comando e digite o seguinte comando, "NET START W3SVC".

2.  No menu Iniciar, selecione Executar. Digite msdfmap.ini e clique em OK para abrir o arquivo msdfmap.ini no Bloco de Notas. Verifique a \[seção Connect\] default e, se o parâmetro Access estiver definido como NoAccess, altere-o para ReadOnly.

3.  Usando o utilitário RegEdit, navegue até "software\_\\da\_máquina\\local da\\Microsoft datafactory\\HandlerInfo" e certifique-se de que **HandlerRequired** esteja definido como 0 e defaulthandler seja "" (nulo **** Cadeia de caracteres).
    
    > [!NOTE]
    > [!OBSERVAçãO] Se você fizer quaisquer alterações nesta seção do Registro, deverá parar e reiniciar o Serviço de Publicação na World Wide Web, inserindo os seguintes comandos em um prompt de comando: "NET STOP W3SVC" e "NET START W3SVC".

4.  Usando o utilitário RegEdit, navegue no registro para "HKEY\_local\_Machine\\System\\CurrentControlSet\\Services\\W3SVC\\Parameters\\ADCLaunch" e verifique se há uma chave chamada ** RDSServer.** datafactory. Se não houver, crie-a.

5.  Usando o Gerenciador de serviços de Internet, vá para o site padrão e exiba as propriedades da raiz virtual do MSADC. Inspecione a Segurança do Diretório/Endereço IP e as Restrições de Nome de Domínio. Se "Acesso Negado" estiver marcado, selecione "Concedido".

Certifique-se de tentar reiniciar o servidor se as alterações não parecerem solucionar o problema em um primeiro momento.

