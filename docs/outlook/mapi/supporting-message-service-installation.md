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
  
O programa de instalação do serviço de mensagens deve fazer o seguinte:
  
1. Copie arquivos de serviço de mensagens, como DLLs do serviço de mensagens e do provedor de serviços, de um CD ou disco para uma unidade local na estação de trabalho. Os arquivos que precisam ser copiados dependem do serviço de mensagens. Normalmente, você copiará pelo menos uma DLL.
    
2. Adicione entradas ao arquivo de configuração Mapisvc.inf. Para obter mais informações sobre como modificar esse arquivo para dar suporte aos provedores de serviço em seu serviço de mensagens, consulte o formato de arquivo [de MapiSvc.inf](file-format-of-mapisvc-inf.md).
    
3. Adicione entradas, conforme apropriado, ao registro do sistema para serviços de mensagens. For more information about how the entries should appear in the system registry, see [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).
    
4. Crie um perfil padrão se ainda não existir um usando um dos seguintes itens:
    
  - O Assistente de Perfil para criar um perfil usando a interação do usuário por meio de uma série de caixas de diálogo. Para obter mais informações sobre como usar o Assistente de Perfil, consulte [Criando um Perfil usando o Assistente de Perfil.](creating-a-profile-by-using-the-profile-wizard.md)
    
  - O Painel de Controle para criar um perfil usando a interação do usuário. O Painel de Controle oferece ao usuário mais flexibilidade do que o Assistente de Perfil para configurar os serviços de mensagens e definir as propriedades de perfil. 
    
Coloque o programa de instalação em um diretório público designado. Isso é importante porque a maioria dos clientes de configuração, como o Painel de Controle, exige que os usuários insiram o nome do diretório. O Painel de Controle invoca um programa  de instalação quando  um usuário clica no botão Adicionar, invoca a caixa de diálogo Ter Disco e especifica o caminho para o programa. O Painel de Controle executa o programa e chama a função de ponto de entrada do serviço de mensagens com o  _parâmetro ulContext_ definido como MSG_SERVICE_INSTALL. 
  
> [!CAUTION]
> Como os perfis são uma parte expendável da arquitetura MAPI, certifique-se de que seu programa de instalação não armazene nada no perfil padrão que seria difícil de recriar. Não há utilitários para recuperação de perfil, para mover perfis de um computador para outro, para backup off-line ou para restauração individual ou global a partir de cópias de backup. 
  
## <a name="see-also"></a>Confira também



[Implementação do serviço de mensagens](message-service-implementation.md)

