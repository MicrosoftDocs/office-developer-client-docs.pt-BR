---
title: Suporte à instalação do serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 328884e8758e679eb1c9d968547cba02c01d4d47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404698"
---
# <a name="supporting-message-service-installation"></a>Suporte à instalação do serviço de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O programa de instalação para instalar o serviço de mensagens deve fazer o seguinte:
  
1. Copie arquivos de serviço de mensagens, como o serviço de mensagens e DLLs do provedor de serviços, de um CD ou disco para uma unidade local na estação de trabalho. Os arquivos que precisam ser copiados dependem do serviço de mensagens. Normalmente, você copiará pelo menos uma DLL.
    
2. Adicione entradas ao arquivo de configuração MAPISVC. inf. Para obter mais informações sobre como modificar esse arquivo para oferecer suporte aos provedores de serviço em seu serviço de mensagens, confira o [formato de arquivo MapiSvc. inf](file-format-of-mapisvc-inf.md).
    
3. Adicione entradas, conforme apropriado, ao registro do sistema para serviços de mensagens. Para obter mais informações sobre como as entradas devem aparecer no registro do sistema, consulte [instalando o subsistema MAPI](installing-the-mapi-subsystem.md).
    
4. Crie um perfil padrão se ainda não existir um usando um dos seguintes itens:
    
  - O assistente de perfil para criar um perfil usando a interação do usuário por meio de uma série de caixas de diálogo. Para obter mais informações sobre como usar o assistente de perfil, consulte [criando um perfil usando o assistente de perfil](creating-a-profile-by-using-the-profile-wizard.md).
    
  - O painel de controle para criar um perfil usando a interação do usuário. O painel de controle oferece ao usuário mais flexibilidade do que o assistente de perfil para configurar os serviços de mensagens e as propriedades de perfil de configuração. 
    
Coloque o programa de instalação em um diretório público designado. Isso é importante porque a maioria dos clientes de configuração, como o painel de controle, exige que os usuários insiram o nome do diretório. O painel de controle invoca um programa de instalação quando um usuário clica no botão **Adicionar** , invoca a caixa de diálogo **ter disco** e especifica o caminho para o programa. O painel de controle executa o programa e chama a função de ponto de entrada do serviço de mensagens com o parâmetro _ulContext_ definido como MSG_SERVICE_INSTALL. 
  
> [!CAUTION]
> Como os perfis são uma parte inutilizável da arquitetura MAPI, certifique-se de que o programa de instalação não armazene nada no perfil padrão que seria difícil de recriá-lo. Não há utilitários para recuperação de perfil, para mover perfis de um computador para outro, para backup off-line ou para restauração individual ou global de cópias de backup. 
  
## <a name="see-also"></a>Confira também



[Implementação do serviço de mensagens](message-service-implementation.md)

