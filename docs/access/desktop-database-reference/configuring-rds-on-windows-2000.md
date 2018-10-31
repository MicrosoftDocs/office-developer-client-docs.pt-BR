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
# <a name="configuring-rds-on-windows-2000"></a>Configurando o RDS no Windows 2000


**Aplica-se a**: Access 2013 | Office 2013

Se tiver dificuldades para fazer com que o RDS funcione corretamente depois de fazer a atualização para o Windows 2000, siga as etapas a seguir para solucionar o problema.

1.  Certifique-se de que o serviço de publicação na World Wide Web é executado primeiro navegando até https://*server* usando o Internet Explorer. Se você não puder acessar o servidor Web dessa forma, vá para um prompt de comando e digite o seguinte comando, "NET START W3SVC".

2.  No menu Iniciar, selecione Executar. Digite msdfmap.ini e clique em OK para abrir o arquivo msdfmap.ini no Bloco de Notas. Verifique o \[conectar padrão\] seção e se o parâmetro de acesso é definido como NOACCESS, altere-o para somente leitura.

3.  Usando o utilitário RegEdit, navegue até "HKEY\_LOCAL\_máquina\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" e verifique se **HandlerRequired** está definido como 0 e **DefaultHandler** é "" (nulo cadeia de caracteres).
    
    > [!NOTE]
    > [!OBSERVAçãO] Se você fizer quaisquer alterações nesta seção do Registro, deverá parar e reiniciar o Serviço de Publicação na World Wide Web, inserindo os seguintes comandos em um prompt de comando: "NET STOP W3SVC" e "NET START W3SVC".

4.  Usando o utilitário RegEdit, navegue no registro para "HKEY\_LOCAL\_máquina\\sistema\\CurrentControlSet\\serviços\\W3SVC\\parâmetros\\ADCLaunch" e verifique se há uma chave **chamado Rdsserver**. Se não houver, crie-a.

<<<<<<< HEAD
5.  Usando o Gerenciador de Serviços de Internet, vá para o Site Padrão e visualize as propriedades da raiz virtual MSADC. Inspecione a Segurança do Diretório/Endereço IP e as Restrições de Nome de Domínio. Se "Acesso Negado" estiver marcado, selecione "Concedido".
=======
5.  Usando o Gerenciador de serviços de Internet, vá para o site padrão e exibir as propriedades da raiz virtual MSADC. Inspecione a Segurança do Diretório/Endereço IP e as Restrições de Nome de Domínio. Se "Acesso Negado" estiver marcado, selecione "Concedido".
>>>>>>> mestre

Certifique-se de tentar reiniciar o servidor se as alterações não parecerem solucionar o problema em um primeiro momento.

