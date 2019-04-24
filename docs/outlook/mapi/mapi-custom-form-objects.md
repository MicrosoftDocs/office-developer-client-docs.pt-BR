---
title: Objetos de formulário personalizados MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 306d62b1-d541-4039-9759-3903f62e0f26
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4c1c04e5b04be9bb67b050f5cf498be89d380410
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318240"
---
# <a name="mapi-custom-form-objects"></a>Objetos de formulário personalizados MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os objetos de formulários personalizados são implementados por três componentes diferentes:
  
- Um servidor de formulários.
    
- Um provedor de biblioteca de formulários.
    
- Um visualizador de formulários.
    
Um servidor de formulário é semelhante em funcionalidade a um aplicativo de objeto de documento composto OLE. É um componente executável que implementa o formulário; Ele controla sua exibição e as operações que um usuário pode executar. MAPI inicia um servidor de formulário quando um usuário deseja exibir uma mensagem junto com uma classe de mensagem exibida usando um formulário suportado pelo servidor de formulário. Os servidores de formulário implementam três objetos: um objeto de fábrica de formulários que se assemelha à fábrica de classe OLE padrão, um coletor de aviso de formulário para lidar com eventos específicos do formulário e o próprio formulário. 
  
Um provedor de biblioteca de formulários fornece acesso para clientes para o conjunto de propriedades de um formulário, para seu contêiner e para o objeto que vincula mensagens de uma classe específica ao servidor que pode abrir o formulário para essa classe. Os provedores de biblioteca de formulários implementam três objetos: um objeto de informações de formulário, um contêiner de formulários e um gerente de formulário para vincular uma mensagem ao servidor de formulário apropriado com base na classe da mensagem.
  
Um visualizador de formulários é um componente incluído em clientes que dão suporte à exibição de formulários personalizados em seus visualizadores de pastas. Os visualizadores de formulários não são componentes MAPI independentes, como os provedores de biblioteca de formulários e os servidores de formulário. Os visualizadores de formulários iniciam os servidores de formulário e fornecem contexto para eles. Os visualizadores de formulários implementam três objetos: um site de mensagens, um contexto de exibição e um coletor de aviso para lidar com eventos específicos de exibição.
  
A tabela a seguir descreve todos os objetos de formulário personalizados. 
  
|**Objeto Form**|**Descrição**|
|:-----|:-----|
|Formulário  <br/> |Controla a exibição e a operação de um formulário personalizado para exibir mensagens de uma classe específica.  <br/> |
|Coletor de aviso de formulário  <br/> |Lida com notificações do Visualizador de formulários.  <br/> |
|Fábrica de formulários  <br/> |Cria uma instância de um formulário e permite que o servidor permaneça na memória.  <br/> |
|Contêiner de formulários  <br/> |Contém informações de formulário.  <br/> |
|Informações do formulário  <br/> |Contém mensagens e outros contêineres de mensagem.  <br/> |
|Gerente de formulário  <br/> |Fornece acesso a uma visão integrada de informações de formulários personalizados relacionadas a todos os formulários instalados. Também corresponde a classes de mensagem com identificadores de classe de formulário correspondentes.  <br/> |
|Site de mensagens  <br/> |Manipula a manipulação de objetos Form de dentro do cliente e fornece acesso a um objeto Gerenciador de formulários.  <br/> |
|Contexto de exibição  <br/> |Dá suporte a comandos de formulário para a ativação de mensagens próximas e anteriores e para salvar ou imprimir.  <br/> |
|Exibir coletor de avisos  <br/> |Lida com notificações do servidor de formulários.  <br/> |
   
A ilustração a seguir mostra a relação entre os componentes de formulário personalizados, os objetos e as interfaces que eles implementam e os componentes que são usuários dos objetos. Observe que, diferentemente da maioria dos outros objetos MAPI, o objeto Form implementa duas interfaces que não estão relacionadas pela herança direta. Quando um objeto expõe várias interfaces independentes, um usuário do objeto que tem um ponteiro para uma das interfaces pode recuperar um ponteiro para qualquer uma das outras interfaces. Essa capacidade de navegar entre implementações de interface de um objeto é um recurso do método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) . 
  
**Custom form components**
  
![Componentes de formulário personalizados] (media/amapi_67.gif "Componentes de formulário personalizados")
  
## <a name="see-also"></a>Confira também

- [Visão geral de interface e objeto MAPI](mapi-object-and-interface-overview.md)

