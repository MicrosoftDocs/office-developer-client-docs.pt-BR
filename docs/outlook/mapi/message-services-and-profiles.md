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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356951"
---
# <a name="message-services-and-profiles"></a>Perfis e serviços de mensagens
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Alguns usuários exigem os serviços de vários sistemas de mensagens, cada um com um ou mais provedores de serviços. Como é complicado instalar e configurar cada um desses provedores de serviços individualmente, e como um servidor de mensagens geralmente requer um grupo de provedores relacionados para expor toda sua funcionalidade, o MAPI inclui o conceito de um serviço de mensagens. Os serviços de mensagens ajudam os usuários a instalar e configurar seus provedores de serviços.
  
Para criar um serviço de mensagens, um desenvolvedor grava um programa de ponto de entrada de serviço de mensagem para lidar com a configuração de cada provedor no serviço e um programa de configuração para fazer o seguinte:
  
- Instale cada provedor no serviço.
    
- Criar entradas de registro e arquivo de inicialização.
    
- Crie entradas no arquivo de configuração MAPI, MAPISVC. inf.
    
O arquivo MAPISVC. inf contém informações relacionadas à configuração de todos os serviços de mensagens e provedores de serviços instalados no computador. Ele é organizado em seções hierárquicas, com cada nível vinculado ao próximo. Na parte superior há três seções que contêm o seguinte: 
  
- Uma lista de arquivos de ajuda do serviço de mensagens.
    
- Uma lista dos serviços de mensagens mais importantes, ou padrão.
    
- Uma lista de todos os serviços no computador.
    
O próximo nível contém seções para cada serviço de mensagens e o último nível contém seções para cada provedor de serviços em um serviço. MAPI requer que os desenvolvedores de provedores de serviços e serviços de mensagens adicionem determinadas entradas a MAPISVC. inf; os desenvolvedores podem adicionar outras entradas por conta própria. A maioria das informações no MAPISVC. inf acaba em um ou mais perfis, uma coleção de informações de configuração para o conjunto de serviços de mensagem preferencial de um usuário. Como um computador pode ter vários usuários e um único usuário pode ter vários conjuntos de preferências, muitos perfis podem existir em um computador. Cada perfil descreve um conjunto diferente de serviços de mensagens. Ter vários perfis permite que um usuário trabalhe, por exemplo, em casa com um conjunto de serviços de mensagem e no escritório com um conjunto diferente.
  
Os perfis são criados na instalação do serviço de mensagens ou no tempo de logon por um aplicativo cliente que fornece suporte à configuração. MAPI fornece dois aplicativos cliente: um item do painel de controle e o assistente de perfil. O item do painel de controle é um aplicativo de configuração de serviço completo com o qual os usuários podem criar, excluir, editar e copiar perfis, bem como fazer modificações nas entradas de um perfil. O assistente de perfil é um aplicativo simples projetado para tornar a adição de um serviço de mensagens a um perfil o mais fácil possível. O assistente de perfil consiste em uma série de caixas de diálogo, chamadas páginas de propriedades, que solicitam ao usuário o processo de instalação e configuração de um serviço. O usuário é solicitado apenas por valores para as configurações mais críticas; todas as outras configurações herdam valores padrão. Depois que o perfil tiver sido criado, os usuários não poderão fazer alterações. 
  
Enquanto o item do painel de controle é sempre chamado pelo painel de controle, há uma variedade de cenários que podem fazer com que o assistente de perfil seja chamado. Os aplicativos cliente podem chamar o assistente de perfil para criar um perfil padrão em tempo de logon quando ainda não tiver sido criado. Em vez de reimplementar o código para adicionar um perfil, o item do painel de controle ou outro aplicativo cliente pode depender da funcionalidade já existente no assistente de perfil. Um serviço de mensagens, em sua função de ponto de entrada, pode chamar o assistente de perfil quando o serviço precisa ser adicionado ao perfil padrão. Os serviços de mensagens que usam o assistente de perfil devem escrever uma função de ponto de entrada extra e um procedimento de caixa de diálogo padrão do Windows. O assistente de perfil chama a função de ponto de entrada para recuperar a caixa de diálogo de configuração do serviço enquanto o procedimento da caixa de diálogo manipula as mensagens que são geradas quando essa caixa de diálogo está em uso. 
  
Os perfis são organizados de forma semelhante ao arquivo MAPISVC. inf. Os perfis têm seções hierárquicas vinculadas; os provedores de serviços possuem seções no nível mais baixo, as seções de serviços de mensagens no nível intermediário e o MAPI possui seções no nível mais alto. Cada seção é identificada com um identificador exclusivo conhecido como [MAPIUID](mapiuid.md). As seções MAPI contêm informações internas para MAPI, como os identificadores de todas as seções de perfil de serviço de mensagens e links para cada uma das outras seções. Cada seção de serviço de mensagens armazena links para suas seções de provedor e cada seção de provedor armazena um link para sua seção de serviço. 
  
A ilustração a seguir mostra o conteúdo de dois perfis típicos. O Sam tem dois perfis no computador, um para uso doméstico e um para uso do Office. O perfil inicial contém três serviços de mensagens. Message Service X é um serviço de provedor único para gerenciamento de catálogo de endereços. Os serviços de mensagem Y e Z têm três provedores — um provedor de catálogo de endereços, um provedor de repositório de mensagens e um provedor de transporte. O perfil de trabalho do Sam contém dois serviços de mensagens diferentes, cada um com um provedor de catálogo de endereços, um provedor de repositório de mensagens e um provedor de transporte. 
  
**Profile example**
  
![Exemplo de perfil] (media/amapi_56.gif "Exemplo de perfil")
  
A ilustração a seguir mostra um perfil que inclui dois serviços de mensagens. O código para instalar e configurar os provedores de serviço que pertencem ao serviço de mensagens residem na mesma DLL que o código para os provedores. Este código lê as informações do perfil no momento do logon para configurar os provedores de serviço e solicita ao usuário, se possível e necessário, para obter informações ausentes. As solicitações de um cliente para exibir ou alterar as definições de configuração de qualquer um dos provedores também são tratadas por esse código comum.
  
**Installing and configuring service providers**
  
![Instalando e configurando provedores de serviços] (media/amapi_55.gif "Instalando e configurando provedores de serviços")
  
## <a name="see-also"></a>Confira também

- [MAPIUID](mapiuid.md)
- [Vis�o geral da programa��o MAPI](mapi-programming-overview.md)

