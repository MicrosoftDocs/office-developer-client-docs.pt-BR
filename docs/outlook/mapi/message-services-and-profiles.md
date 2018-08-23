---
title: Perfis e serviços de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df0db1e4-69c8-44ec-bb2a-d31fc8a564b9
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 60a102a68ee11cd6002be9edf47d0cee93ed2e15
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581430"
---
# <a name="message-services-and-profiles"></a>Perfis e serviços de mensagem
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Alguns usuários necessitam dos serviços de diversos sistemas de mensagens, cada um com um ou mais provedores de serviço. Porque ele é complicado para instalar e configurar cada um desses provedores de serviço individualmente e como um servidor de mensagens normalmente exige um grupo de provedores relacionados expor toda sua funcionalidade, MAPI inclui o conceito de um serviço de mensagem. Serviços de mensagens ajudam os usuários a instalar e configurar seus provedores de serviço.
  
Para criar um serviço de mensagem, um desenvolvedor grava um programa de ponto de entrada de serviço de mensagem para lidar com a configuração de cada provedor de serviço e um programa de instalação para fazer o seguinte:
  
- Instale cada provedor no serviço.
    
- Crie registro e inicialização entradas do arquivo.
    
- Crie entradas no arquivo de configuração MAPI Mapisvc.
    
O arquivo Mapisvc contém informações relacionadas à configuração de todos os serviços de mensagem e provedores de serviços instalados no computador. Ele é organizado nas seções hierárquicas, com cada nível vinculada para a próxima. Na parte superior são três seções que contêm o seguinte: 
  
- Uma lista de arquivos de Ajuda do serviço de mensagem.
    
- Uma lista dos mais importantes ou padrão, serviços de mensagem.
    
- Uma lista de todos os serviços no computador.
    
O próximo nível contém seções para cada serviço de mensagem e o último nível contém seções para cada provedor de serviços em um serviço. MAPI exige que o desenvolvedores de provedores de serviço e serviços de mensagem adicionem certas entradas para Mapisvc; os desenvolvedores podem adicionar outras entradas suas próprias critério. Maioria das informações em MAPISVC termina em um ou mais perfis, uma coleção de informações de configuração de um usuário preferencial conjunto de serviços de mensagem. Porque um computador pode ter vários usuários e um único usuário pode ter vários conjuntos de preferências, muitos perfis podem existir em um computador. Cada perfil descreve um conjunto diferente de serviços de mensagem. Ter vários perfis permite que um usuário trabalhe, por exemplo, em casa, com um conjunto de serviços de mensagem e no escritório com um conjunto diferente.
  
Perfis são criados no tempo de logon ou de instalação do serviço de mensagem por um aplicativo cliente que oferece suporte a configuração. MAPI fornece dois tal cliente aplicativos: um item do painel de controle e o Assistente de perfil. O item do painel de controle é um aplicativo de serviço completo de configuração com a qual os usuários podem criar, excluir, editar e copiar perfis, bem como fazer modificações as entradas em um perfil. O Assistente de perfil é um aplicativo simples projetado para facilitar a adição de um serviço de mensagem a um perfil tão fácil quanto possível. O Assistente de perfil consiste em uma série de caixas de diálogo, chamado páginas de propriedades, que solicita ao usuário durante o processo de instalação e configuração de um serviço. O usuário será solicitado apenas para os valores para as configurações mais importantes; todas as outras configurações herdarem valores padrão. Depois que o perfil tiver sido criado, os usuários não poderão fazer alterações. 
  
Enquanto o item do painel de controle sempre é invocado por meio do painel de controle, há uma variedade de cenários que podem causar o Assistente de perfil a ser chamado. Aplicativos cliente podem chamar o Assistente de perfil para criar um perfil padrão no momento do logon quando um ainda não tiver sido criado. Em vez de reimplementação código para adicionar um perfil, o item do painel de controle ou outro aplicativo cliente pode depender a funcionalidade já no Assistente de perfil. Um serviço de mensagem, na sua função de ponto de entrada, é possível chamar o Assistente de perfil quando o serviço precisa ser adicionada ao perfil padrão. Serviços de mensagem que usam o Assistente de perfil devem escrever uma função de ponto de entrada extra e um procedimento de caixa de diálogo padrão do Windows. O Assistente de perfil chama a função do ponto de entrada para recuperar a caixa de diálogo de configuração do serviço enquanto o procedimento da caixa de diálogo trata as mensagens que são geradas quando esta caixa de diálogo está em uso. 
  
Os perfis são organizados de forma semelhante ao arquivo Mapisvc. Perfis vinculou seções hierárquicas; seções próprio de provedores de serviço no nível mais baixo, serviços de mensagem proprietário seções do nível intermediário e MAPI possui seções o nível mais alto. Cada seção é identificada com um identificador exclusivo, conhecido como um [MAPIUID](mapiuid.md). As seções MAPI contêm informações internas para MAPI, como os identificadores de todas as seções de perfil de serviço de mensagem e links para cada uma das outras seções. Cada seção do serviço de mensagem armazena links para seu provedor de seções e cada seção de provedor armazena um link para a seção seu serviço. 
  
A ilustração a seguir mostra o conteúdo de dois perfis típicos. SAM tem dois perfis no seu computador, um para uso doméstico e outro para uso do office. O perfil residencial contém três serviços de mensagem. X do serviço de mensagem é um serviço único provedor para gerenciamento de catálogo de endereços. Mensagem serviços Y e Z tem três provedores — um fornecedor de catálogo de endereços, um provedor de armazenamento de mensagens e um provedor de transporte. Perfil de trabalho de SAM contém dois serviços de mensagens diferentes, cada um deles tem um fornecedor de catálogo de endereços, um provedor de armazenamento de mensagens e um provedor de transporte. 
  
**Profile example**
  
![Exemplo de perfil] (media/amapi_56.gif "Exemplo de perfil")
  
A ilustração a seguir mostra um perfil que inclui dois serviços de mensagem. O código para instalar e configurar os provedores de serviços que pertencem ao serviço de mensagem reside na mesma DLL como o código para os provedores. Este código lê as informações do perfil na hora do logon para configurar os provedores de serviço e solicita que o necessário, para obter informações ausentes e usuário, se possível. Solicitações de um cliente para visualizar ou alterar as definições de configuração de qualquer um dos provedores também são manipuladas por este código comuns.
  
**Installing and configuring service providers**
  
![Instalando e configurando provedores de serviço] (media/amapi_55.gif "Instalando e configurando provedores de serviço")
  
## <a name="see-also"></a>Confira também

- [MAPIUID](mapiuid.md)
- [Vis�o geral da programa��o MAPI](mapi-programming-overview.md)

