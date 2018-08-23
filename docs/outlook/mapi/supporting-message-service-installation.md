---
title: Suporte à instalação do serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1f82741e3c44c589a18a1428fd68cebe6a501d5c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581990"
---
# <a name="supporting-message-service-installation"></a>Suporte à instalação do serviço de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O programa de instalação para instalar o serviço de mensagem deve fazer o seguinte:
  
1. Copie os arquivos do serviço de mensagens, como o serviço de mensagem e o provedor de serviços de DLLs, de um CD ou disco, para uma unidade local na estação de trabalho. Os arquivos que precisam ser copiados dependem de seu serviço de mensagem. Normalmente, você irá copiar DLL pelo menos um.
    
2. Adicione entradas para o arquivo de configuração Mapisvc. Para obter mais informações sobre como modificar esse arquivo para os provedores de serviços de suporte no seu serviço de mensagem, consulte o [Formato de arquivo do Mapisvc](file-format-of-mapisvc-inf.md).
    
3. Adicione entradas, conforme apropriado para o registro do sistema para serviços de mensagem. Para obter mais informações sobre como as entradas devem aparecer no registro do sistema, consulte [Instalando o subsistema de MAPI](installing-the-mapi-subsystem.md).
    
4. Crie um perfil padrão, caso ainda não exista usando um dos seguintes itens:
    
  - O Assistente de perfil para criar um perfil usando a interação do usuário através de uma série de caixas de diálogo. Para obter mais informações sobre como usar o Assistente de perfil, consulte o [tópico Criando um perfil usando o Assistente de perfil](creating-a-profile-by-using-the-profile-wizard.md).
    
  - O painel de controle para criar um perfil usando a interação do usuário. O painel de controle oferece ao usuário mais flexibilidade do que o Assistente de perfil para configurar os serviços de mensagem e definir propriedades de perfil. 
    
Coloque o programa de instalação em uma pasta pública designada. Isso é importante porque a maioria dos clientes de configuração, como o painel de controle, exigem que os usuários insiram o nome do diretório. O painel de controle invoca um programa de instalação quando um usuário clica no botão **Adicionar** , invoca a caixa de diálogo **Com disco** e especifica o caminho para o programa. O painel de controle executa o programa e chama a função de ponto de entrada do seu serviço de mensagem com o parâmetro _ulContext_ definido como MSG_SERVICE_INSTALL. 
  
> [!CAUTION]
> Como os perfis são uma parte descartáveis da arquitetura do MAPI, certifique-se de que seu programa de instalação não armazene nada no perfil padrão que seria difícil de recriar. Não há nenhuma utilitários para recuperação de perfil, para mover os perfis de um computador para outro, para backup off-line ou para restauração individual ou global de cópias de backup. 
  
## <a name="see-also"></a>Confira também



[Implementação do serviço de mensagens](message-service-implementation.md)

