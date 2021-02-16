---
title: Perfis e serviços de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df0db1e4-69c8-44ec-bb2a-d31fc8a564b9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 78a13bacf13b019bbf9436830ad66db7fdfaf425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415464"
---
# <a name="message-services-and-profiles"></a>Perfis e serviços de mensagens
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Alguns usuários exigem os serviços de vários sistemas de mensagens, cada um com um ou mais provedores de serviços. Como é complicado instalar e configurar cada um desses provedores de serviços individualmente e como um servidor de mensagens geralmente exige um grupo de provedores relacionados para expor toda a sua funcionalidade, o MAPI inclui o conceito de um serviço de mensagens. Os serviços de mensagens ajudam os usuários a instalar e configurar seus provedores de serviços.
  
Para criar um serviço de mensagens, um desenvolvedor grava um programa de ponto de entrada de serviço de mensagem para lidar com a configuração de cada provedor no serviço e um programa de instalação para fazer o seguinte:
  
- Instale cada provedor no serviço.
    
- Crie entradas de arquivo de registro e inicialização.
    
- Crie entradas no arquivo de configuração MAPI, Mapisvc.inf.
    
O arquivo Mapisvc.inf contém informações relacionadas à configuração de todos os serviços de mensagem e provedores de serviços instalados no computador. Ele é organizado em seções hierárquicas, com cada nível vinculado ao próximo. Na parte superior, há três seções que contêm o seguinte: 
  
- Uma lista de arquivos de Ajuda do serviço de mensagens.
    
- Uma lista dos serviços de mensagem mais importantes ou padrão.
    
- Uma lista de todos os serviços no computador.
    
O próximo nível contém seções para cada serviço de mensagens e o último nível contém seções para cada provedor de serviços em um serviço. MAPI requires that developers of service providers and message services add certain entries to Mapisvc.inf; os desenvolvedores podem adicionar outras entradas a seu próprio critério. A maioria das informações em Mapisvc.inf termina em um ou mais perfis, um conjunto de informações de configuração para o conjunto preferencial de serviços de mensagens de um usuário. Como um computador pode ter vários usuários e um único usuário pode ter vários conjuntos de preferências, muitos perfis podem existir em um computador. Cada perfil descreve um conjunto diferente de serviços de mensagens. Ter vários perfis permite que um usuário trabalhe, por exemplo, em casa com um conjunto de serviços de mensagens e no escritório com um conjunto diferente.
  
Os perfis são criados no momento da instalação ou no horário de logon do serviço de mensagens por um aplicativo cliente que fornece suporte à configuração. MAPI provides two such client applications: a Control Panel item and the Profile Wizard. O item painel de controle é um aplicativo de configuração de serviço completo com o qual os usuários podem criar, excluir, editar e copiar perfis, bem como fazer modificações nas entradas em um perfil. O Assistente de Perfil é um aplicativo simples projetado para facilitar ao máximo a adição de um serviço de mensagens a um perfil. O Assistente de Perfil consiste em uma série de caixas de diálogo, chamadas de páginas de propriedades, que solicitam ao usuário o processo de instalação e configuração de um serviço. O usuário é solicitado apenas pelos valores das configurações mais críticas; todas as outras configurações herdam valores padrão. Depois que o perfil tiver sido criado, os usuários não poderão fazer alterações. 
  
Enquanto o item do Painel de Controle é sempre invocado por meio do Painel de Controle, há uma variedade de cenários que podem fazer com que o Assistente de Perfil seja chamado. Os aplicativos cliente podem chamar o Assistente de Perfil para criar um perfil padrão no momento do logon quando um ainda não foi criado. Em vez de reimplante o código para adicionar um perfil, o item do Painel de Controle ou outro aplicativo cliente pode depender da funcionalidade que já está no Assistente de Perfil. Um serviço de mensagens, em sua função de ponto de entrada, pode chamar o Assistente de Perfil quando o serviço precisar ser adicionado ao perfil padrão. Os serviços de mensagem que usam o Assistente de Perfil devem escrever uma função de ponto de entrada extra e um procedimento de caixa de diálogo padrão do Windows. O Assistente de Perfil chama a função de ponto de entrada para recuperar a caixa de diálogo de configuração do serviço enquanto o procedimento da caixa de diálogo trata as mensagens geradas quando essa caixa de diálogo está em uso. 
  
Os perfis são organizados de maneira semelhante ao arquivo Mapisvc.inf. Perfis têm seções hierárquicas vinculadas; os provedores de serviços têm seções no nível mais baixo, os serviços de mensagens têm seções no nível intermediário e o MAPI possui seções no nível mais alto. Cada seção é identificada com um identificador exclusivo conhecido como [MAPIUID.](mapiuid.md) As seções MAPI contêm informações internas para MAPI, como os identificadores de todas as seções de perfil de serviço de mensagens e links para cada uma das outras seções. Cada seção de serviço de mensagens armazena links para suas seções de provedor, e cada seção do provedor armazena um link para sua seção de serviço. 
  
A ilustração a seguir mostra o conteúdo de dois perfis típicos. Sam tem dois perfis em seu computador, um para uso em casa e outro para uso no escritório. O perfil home contém três serviços de mensagem. O Serviço de Mensagens X é um serviço de provedor único para gerenciamento de livro de endereços. Os Serviços de Mensagens Y e Z têm três provedores: um provedor de agendas, um provedor de armazenamento de mensagens e um provedor de transporte. O Perfil de Trabalho do Sam contém dois serviços de mensagem diferentes, cada um deles tem um provedor de agenda, um provedor de armazenamento de mensagens e um provedor de transporte. 
  
**Profile example**
  
![Exemplo de perfil de](media/amapi_56.gif "exemplo de perfil")
  
A ilustração a seguir mostra um perfil que inclui dois serviços de mensagem. O código para instalar e configurar os provedores de serviços que pertencem ao serviço de mensagens reside na mesma DLL que o código para os provedores. Este código lê informações do perfil no momento do logon para configurar os provedores de serviços e solicita ao usuário, se possível e necessário, informações ausentes. As solicitações de um cliente para exibir ou alterar as definições de configuração de qualquer um dos provedores também são tratadas por esse código comum.
  
**Installing and configuring service providers**
  
![Instalando e configurando provedores de serviços](media/amapi_55.gif "instalando e configurando provedores de serviços")
  
## <a name="see-also"></a>Confira também

- [MAPIUID](mapiuid.md)
- [Visão geral da programação MAPI](mapi-programming-overview.md)

